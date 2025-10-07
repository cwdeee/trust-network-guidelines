Before addressing the research question of interest, pre-processing is needed to exclude responses that may not reflect the cognitive processes and thus decrease the signal-to-noise ratio. 

## Preprocessing
We recommend keeping the pre-processing to a minimum, to avoid systematic bias in excluding potentially meaningful datapoints and maximise the number of observations. As there are many different rules of thumb, we suggest either minimising the amount of pre-processing (e.g., when the amount of data is limited) or conducting a robustness analysis, where the results are verified with a set of different pre-processing methods (e.g., when there is a large amount of data available; see [Short et al. 2025](https://doi.org/10.31222/osf.io/4yzeh_v1)). 

Below are some recommended pre-processing options. Please note that they should be specified in a pre-registration.

- Excluding long responses
    - When a time-out criterion was used (e.g., the word disappeared after 5000 ms and the response times were therefore set to 5000 ms), it needs to be set to *Not Available* (e.g., *NA* in R).
    - When no time-out was used, find evidence-based criteria to remove unusually long reaction times, for example, by visually inspecting [qq-plots](https://en.wikipedia.org/wiki/Q%E2%80%93Q_plot).

-  Excluding short responses
    - Button presses within the first 200 ms are generally considered accidental responses, as this short amount doesn’t allow for the relevant cognitive processes to unfold, as premature responses can be made. They, also, should be set to *Not Available*.

- Participants with chance-level performance should be excluded.
    - The chance level is 50% when there are 50% words and 50% pseudowords.
    - If the percentage of words deviates from 50% (e.g., if it’s 70%), then participants who always provide a “word” response may have above-chance accuracy but still need to be removed.

- Individual participant data quality check
    - For each participant, we can assess whether the response times for each trial correlate with the average response times for the same items across all other participants. The participant can be excluded if the correlation is low (e.g., below *r < 0.5*). 
    - Item-level removal: While some studies remove items with particularly low accuracy, this may create a systematic bias. We thus recommend against it.

An important decision is whether one is interested in analysing response times or accuracy. In studies with adults, accuracy is generally high. For response time analyses, one excludes all trials with incorrect responses. However, if accuracy is low, this systematically excludes data for the more difficult items. 

As a rule of thumb: 

- If accuracy is above 90%, it is advisable to analyse reaction times only, as there will be ceiling effects in accuracy. 
- If accuracy is below 70%, one analyzes accuracy only. 
- If accuracy is between 70% and 90%, one analyzes both accuracy and response times and seeks to obtain converging evidence; if the results are discrepant, this needs to be addressed in the discussion section. 

Note that there are model based analysis that allow the simultanous analysis of response times and accuracy at the same time (e.g., drift-diffusion modelling; [Ratcliff, & McKoon, 2008](https://doi.org/10.1162/neco.2008.12-06-420))

##  Data transformation
Reaction time data generally has an exponentially modified Gaussian (Ex-Gaussian) distribution, which looks like a bell-shaped curve with a right skew. As most frequentist analysis methods assume a normal distribution, one can choose between transforming the data or using a model that assumes an Ex-Gaussian distribution.

Possible transformations include:

- Log-RT: In R-code logRT <- log(RT)
- Inverse RT: invRT <- 1/RT. Note that this gives you a reading rate in Herz (assuming that the RT is seconds, not smaller or larger units) rather than speed, such that small numbers correspond to larger RTs (i.e., 1 Herz would transform to one word per second; i.e., a 1-second RT; see [Gagl et al., 2022](https://doi.org/10.1038/s41562-021-01215-4). Note that sometimes the RT values are multiplied by -1, so smaller values correspond to faster response times. 
- Z-transformations: For each participant, subtract the mean from the trial RT and divide by the participant's standard deviation. This transformation  will remove any between-participant variability, which is an issue when it is a matter of investigation, but is advantageous if one wants to avoid the problems with over-additivity ([Faust et al., 1999](https://doi.org/10.1037/0033-2909.125.6.777))

If one wants to model the Ex-Gaussian explicitly, it is possible with Bayesian methods (e.g., as implemented in the [brm package in R](https://github.com/paul-buerkner/brms)). 


## Statistics 
### Sanity check analysis
Some effects are well-established and can serve as a sanity check to ensure good data quality. We expect long items to be responded to more slowly than short items, and pseudowords more slowly than words; there should also be an interaction between these, with a more substantial length effect for pseudowords than words (e.g., [Weekes, 1997](https://doi.org/10.1080/713755710)). 
If the main effects and interaction are not present, one should troubleshoot the following: 

- The data export process (e.g., is it possible that some columns in a spreadsheet were sorted while the others were not) 
- The design of the experiment (are the reaction times recorded as the number of seconds/milliseconds between stimulus onset and response?) 
- The participant responses (do they provide atypically short or long responses, potentially suggesting low engagement with the task; e.g., if a participants wants that the experiment ends fast the best strategy would be to do a reaction time task where one presses a button irrespective of stimulus quality as fast as possible, ignoring that the instruction would be also to do the task correctly).  

### Assessing the effect of interest
- We recommend Linear Mixed Effect modelling on trial-level data, with crossed random effects for item and participant (see the [lmer package]() for a frequentist and [brm package]() for a Bayesian approach). 
- Center all continuous variables (i.e., subtract the mean of all values of each given variable from the value itself, so that the average is 0) - this means that the estimates of the model will represent the grand mean. We strongly advise against dichotomising continuous variables as several potential problems can arise (e.g., equal distribution of cases, etc.)
- Contrast code dichotomous variables (e.g., see [Schad et al., 2020](https://doi.org/10.1016/j.jml.2019.104038) for a tutorial).
- Fit the fixed effect specification in accordance with the hypothesis (e.g., if interested in the frequency-by-lexicality interaction: rt ~ freq * lex; R formula syntax)
- Then, add covariates of no interest as fixed effects (frequency, trial order, previous trial RT, orthographic/phonological Levenshtein distance, Age of Acquisition, etc.).
- For a tutorial regarding the random effect specification, see [Bates et al. (2018)](https://doi.org/10.48550/arXiv.1506.04967)
- Use theoretical knowledge about the different predictors to decide whether the effect of continuous variables should be linear or not (e.g., see [Kliegl et al., 2006](https://doi.org/10.1037/0096-3445.135.1.12)
 