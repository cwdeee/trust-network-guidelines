Before addressing the research question of interest, pre-processing may be needed to exclude responses that may not reflect the cognitive processes and thus decrease the signal-to-noise ratio. 

## Preprocessing  ![Importance Rating 2](images/rating5.png)
We recommend keeping the pre-processing to a minimum, to avoid systematic bias in excluding potentially meaningful datapoints and maximise the number of observations. As there are many different rules of thumb, we suggest either minimising the amount of pre-processing (e.g., when the amount of data is limited) or conducting a robustness analysis, where the results are verified with a set of different pre-processing methods (e.g., when there is a large amount of data available; see [Short et al. 2025](https://doi.org/10.31222/osf.io/4yzeh_v1)). 

Below are some recommended pre-processing options. Please note that they should be specified in a pre-registration.

- Excluding long responses
    - When a time-out criterion was used (e.g., the word disappeared after 5000 ms and the response times were therefore set to 5000 ms), it needs to be set to *Not Available* (e.g., *NA* in R).
    - When no time-out was used, find evidence-based criteria to remove unusually long reaction times.
    - Note that for different groups (e.g., children), these criteria can differ considerably. 

-  Excluding short responses
    - Button presses within the first 200 ms are generally considered accidental responses, as this short amount doesn’t allow for the relevant cognitive processes to unfold, as premature responses can be made. They, also, should be set to *Not Available*.

- Participants with chance-level performance should be excluded.
    - The chance level is 50% when there are 50% words and 50% pseudowords.
    - If the percentage of words deviates from 50% (e.g., if it’s 70%), then participants who always provide a “word” response may have above-chance accuracy but still need to be removed.

- Individual participant data quality check
    - For each participant, we can assess whether the response times for each trial correlate with the average response times for the same items across all other participants. The participant can be excluded if the correlation is low (e.g., below *r < 0.5*). 
    - Item-level removal: While some studies remove items with particularly low accuracy, this may create a systematic bias. We thus recommend against it.

An important decision is whether one is interested in analysing response times or accuracy. In studies with adults, accuracy is generally high. For response time analyses, one excludes all trials with incorrect responses. However, if accuracy is low, this systematically excludes data for the more difficult items. If accuracy is high, one needs to be aware of ceiling effects when investigating accuracy.

<!--- As a rule of thumb: 

- If accuracy is above 90%, it is advisable to analyse reaction times only, as there will be ceiling effects in accuracy. 
- If accuracy is below 70%, one analyzes accuracy only. 
- If accuracy is between 70% and 90%, one analyzes both accuracy and response times and seeks to obtain converging evidence; if the results are discrepant, this needs to be addressed in the discussion section. --->

Note that there are model based analysis that allow the simultanous analysis of response times and accuracy at the same time (e.g., drift-diffusion modelling; [Ratcliff, & McKoon, 2008](https://doi.org/10.1162/neco.2008.12-06-420))

##  Data transformation  ![Importance Rating 2](images/rating5.png)
Reaction time data generally has an exponentially modified Gaussian (Ex-Gaussian) or shifted log-normal distribution, which looks like a bell-shaped curve with a right skew. As most frequentist analysis methods assume a normal distribution, one can choose between transforming the data or using a model that assumes an Ex-Gaussian or shifted log-normal distribution (see [HERE](https://lindeloev.shinyapps.io/shiny-rt/) for illustrations and more details).

Possible transformations include:

- Log-RT: In R-code logRT <- log(RT)
- Inverse RT: invRT <- 1/RT. Note that this gives you a reading rate in Hertz (Hz; assuming that the RT is seconds, not smaller or larger units) rather than speed, such that small numbers correspond to larger RTs (i.e., 1 Hz would transform to one word per second; i.e., a 1-second RT; see [Gagl et al., 2022](https://doi.org/10.1038/s41562-021-01215-4). Note that sometimes the RT values are multiplied by -1, so smaller values correspond to faster response times. 
- Z-transformations: For each participant, subtract the mean from the trial RT and divide by the participant's standard deviation. This transformation will remove any between-participant variability, which is an issue when it is a matter of investigation, but is advantageous if one wants to avoid the problems with over-additivity ([Faust et al., 1999](https://doi.org/10.1037/0033-2909.125.6.777)). Here, it is worth noting that after this transformation, explicitly modelling participant variance (e.g., as in linear mixed modelling) is no longer necessary.

If one wants to model the Ex-Gaussian or shifted log-normal distribution explicitly, it is possible with Bayesian methods (e.g., as implemented in the [brms package in R](https://github.com/paul-buerkner/brms)). One could also use gamma generalized linear mixed models (GLMM), an alternative way that allows statistical inference without data transformation on non-normal distributions (see [Lo & Andrews, 2015](https://doi.org/10.3389/fpsyg.2015.01171)). 


## Statistics 
### Sanity check analysis  ![Importance Rating 2](images/rating4.png)
Some effects are well-established and can serve as a sanity check to ensure good data quality. We expect long items to be responded to more slowly than short items, and pseudowords more slowly than words; there should also be an interaction between these, with a more substantial length effect for pseudowords than words (e.g., [Weekes, 1997](https://doi.org/10.1080/713755710)). Alternatively, one can investigate the word frequency effect. 
If the main effects and interaction are not present, one should troubleshoot the following: 

- The data export process (e.g., is it possible that some columns in a spreadsheet were sorted while the others were not) 
- The design of the experiment (are the reaction times recorded as the number of seconds/milliseconds between stimulus onset and response?) 
<!--- - The participant responses (do they provide atypically short or long responses, potentially suggesting low engagement with the task; e.g., if a participants wants that the experiment ends fast the best strategy would be to do a reaction time task where one presses a button irrespective of stimulus quality as fast as possible, ignoring that the instruction would be also to do the task correctly).  --->

### Assessing the effect of interest
- We recommend Linear Mixed Effect modelling on trial-level data, with crossed random effects for item and participant (see the [lme4 package](https://github.com/lme4/lme4) for a frequentist and [brm package](https://github.com/paul-buerkner/brms)) for a Bayesian approach). 
- Center all continuous variables (i.e., subtract the mean of all values of each given variable from the value itself, so that the average is 0) - this means that the estimates of the model will represent the grand mean. We strongly advise against dichotomising continuous variables as several potential problems can arise (e.g., equal distribution of cases, etc.)
- Contrast code dichotomous variables (e.g., see [Schad et al., 2020](https://doi.org/10.1016/j.jml.2019.104038) for a tutorial).
- Fit the fixed effect specification in accordance with the hypothesis (e.g., if interested in the frequency-by-lexicality interaction: rt ~ freq * lex; R formula syntax)
- Then, add covariates of no interest as fixed effects (frequency, trial order, previous trial RT, orthographic/phonological Levenshtein distance, Age of Acquisition, etc.).
- For a tutorial regarding the random effect specification, see [Bates et al. (2018)](https://doi.org/10.48550/arXiv.1506.04967)
- Use theoretical knowledge about the different predictors to decide whether the effect of continuous variables should be linear or not (e.g., see [Kliegl et al., 2006](https://doi.org/10.1037/0096-3445.135.1.12)
 

### Inference and reporting
Depending on your research question and preferences, you can either assess the significance of effects of interests or quantify the size of these effects (including whether the estimate is likely zero). 

- Frequentist significance testing: This is the most common approach. 

    - If you fit the model with the R packages lme4 to estimate effect sizes and model fits. If needed, one can use a package like lmerTest to provide p-values for each fixed effect and interaction in the model. 
    - We recommend reporting the unstandardised model effect size estimate (slope), standard error of the estimate, and t- and p-values. 
    - For pre-registered a priori hypotheses, we recommend an alpha-level of 0.05 to determine significance. In the case of exploratory or post-hoc analyses, one should apply a Bonferroni correction (see [von der Malsburg & Angele, 2017](https://doi.org/10.1016/j.jml.2016.10.003)).
    - Frequentist effect size estimation: To interpret the effect size and its estimated accuracy, one can report the effect size estimate and its 95% confidence interval (see [Cumming, 2013](https://doi.org/10.1177/095679761350496)). The package nlme provides 95% confidence intervals for main effects and interactions in mixed-effect models.

- Bayesian statistical tests: Instead of frequentist p-values, one can rely on Bayes Factors for inference (e.g., [Schmalz et al., 2023](https://doi.org/10.1037/met0000421)).

    - In R, you can use the package BayesFactor to calculate Bayes Factors for specific effects in linear mixed-effect models.
    - Here, one compares a model with an effect or interaction of interest to one that excludes this particular effect or interaction. The Bayes Factor is a ratio that quantifies the extent to which the data is more compatible with the model in the numerator than the denominator.
    - Large values support the model in the numerator and small values support the model in the denominator.
    - Unless one has theoretical reasons for doing otherwise, we recommend using the default prior to the BayesFactor package. If a different prior is chosen, it should be clearly reported and justified.
    - For more straightforward interpretability, we recommend placing the more complex model in the numerator, so that increasingly small values (< 1) correspond to evidence for the null model and increasingly large values (>1) correspond to evidence for the alternative model.
    - We recommend a continuous interpretation of the Bayes Factor rather than a "trichotomisation".
    - Bayesian effect size estimation: Unlike the Frequentist approach, which relies on the observed data only, Bayesian effect size estimation considers prior knowledge, which can take the form of existing data. See Bürkner, 2017 (10.18637/jss.v080.i01) for a tutorial.

### Additional possibilities for analysis
Monte-carlo simulated experiments for a priori or post hoc measurements.
Existing large-scale datasets (i.e., lexicon projects like the [British Lexicon Project](https://doi.org/10.3758/s13428-011-0118-4)) allow subsampling experiments that enable running experiments with specific sample sizes and stimulus material to investigate effects (see [Kupermann, 2015](https://doi.org/10.1080/17470218.2014.989865), [Perry, 2024](https://doi.org/10.1371/journal.pone.0296874) for examples)

Beyond measuring an effect or phenomenon typically means implementing completely different inference methods. Commonly, one would like to predict future events based on current data (i.e., the prediction approach) or explain the causal structure of a phenomenon/effect to understand reading better (see [Hofman et al. 2021](https://doi.org/10.1038/s41586-021-03659-0) for a perspective). 

- Explanation focused (neuro)-cognitive models, one would use model simulations a priori to specify hypotheses potentially leading to model comparison leading to inference over models (e.g., [Perry et al., 2007](https://doi.org/10.1037/0033-295X.114.2.273) or [Gagl et al., 2025](https://doi.org/10.1101/2024.06.25.600635); see [Norris, 2013](https://doi.org/10.1016/j.tics.2013.08.003) for a review)
    
    - Another interesting case here is the drift diffusion model ([Ratcliff et al., 2004](https://doi.org/10.1037/0033-295X.111.1.159)) that allows for modeling both reaction times and accuracy data at the same time. Also, the model's output can be interpreted as the effect estimated on assumed processes like the drift rate (i.e., reflecting evidence accumulation before a decision is implemented). Note that the model can cope with exponential Gaussian response time distributions. 


- Prediction-focused learning models (e.g., Machine learning methods) can be used for many things:

    - Explainations based on archetectual constraints (i.e., compare [Linke et al., 2017](https://doi.org/10.1371/journal.pone.0183876) vs. [Hannagan et al., 2014](https://doi.org/10.1371/journal.pone.0084843)) or through implementation of different training regimes ([Hannagan et al., 2022](https://doi.org/10.1073/pnas.2104779118)) or the investigation of neuro-cognitive processes related to reading ([Rajalingham et al., 2020](https://doi.org/10.1038/s41467-020-17714-3); but see model comparisons can be applied to infer over-prediction and explanation focused models [Pauli et al., 2025](https://doi.org/10.1101/2025.05.16.654419)).
    - Investigating memory structure (e.g., [Trautwein et al., 2018](https://doi.org/10.3389/fpsyg.2018.02252) or [Gatti et al., 2023](https://doi.org/10.1037/xge0001304))
    - Diagnostics (e.g., [Gregorova et al., 2024](https://doi.org/10.1038/s41539-024-00237-7); but see [Ziegler et al., 2020](https://doi.org/10.1177/0956797618823540) for an approach using a explaination focused model)