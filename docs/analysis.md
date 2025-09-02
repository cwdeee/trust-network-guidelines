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