## Before you start the experiment
Although lexical decision tasks are typically low-risk and low-cost experiments, one must know if they have the available resources. You need to consider several practical aspects before starting data collection, which are mostly the same as for other low-risk psychological experiments:

- Lab-based study: a quiet lab room with a computer
- Online study: Web server or funding for a hosting service. 
- Potentially funding for the research software, but be aware that there are multiple open source software solutions without costs. 
- Participant reimbursement: How much can I or am I expected to pay participants?
- Ethics permission: At present, ethics permission is not required by law but may be subject to university, funder, and journal policies. It is highly advised to obtain an ethical vote. In case your university does not have an ethics committee, one can consult the ethics committee of the DGPS (German Society of Psychology)
- Data safety and storage: In the European Union, data storage needs to comply with the GDPR (as of 2025). It is the researcher's responsibility to ensure that their experiment complies with the local and current standards. 

## Programming the experiment
The first step is to program the experiment: We want the experimental software to show each trial and to record the participant’s response to the trial and the reaction time. A lexical decision task can be programmed with medium-low programming skills. Templates are available for beginners on many of the existing experimental platforms (see examples below).

### Possible platforms to run the experiment
Here is a nonexhaustive list of programs used by the group in recent years. Typically, all solutions have a forum for customer support and examples available. Find more information at the webpages linked below. 

| Program                                                                       | Cost     | Programming skill | Online hosting | 
|-------------------------------------------------------------------------------|----------|-------------------|----------------|
| [Psytoolkit](https://www.psytoolkit.org)                                      | Free     | Intermediate      | Platform       | 
| [PsychoPy](https://www.psychopy.org/)                                         | Free     | No                | Self           |
| [Pavlovia](https://pavlovia.org/)                                             | Yes      | No                | Platform       |
| [PsychJS](https://www.jspsych.org/v7/)                                        | Free     | Yes               | Self           |
| [Open Sesame](https://osdoc.cogsci.nl/)                                       | Free     | No                | Self           |
| [Open Sesame Online (OSWeb)](https://osdoc.cogsci.nl/3.3/manual/osweb/osweb/) | Free     | No                | Platform       |
| [EyeLink Experiment Builder](https://www.sr-research.com/experiment-builder/) | Licenced | No                | No             |

<!--| Gorilla                            |        |                |                |  |                    |
| Inquisit                           |        |                |                |  |                    |-->

The performance of the systems/platforms should be checked regarding the timing of the stimulus presentation and the latency of the key press. Information on this can be found [here](https://doi.org/10.7717/peerj.9414) and [here](https://doi.org/10.3758/s13428-020-01501-5).

## Participants
The number of participants should be determined by a power calculation based on the size of the effect of interest (e.g., see [Brysbaert & Stevens, 2018](https://doi.org/10.5334/joc.10)). Note there are differences in power considerations when investigating individual differences (e.g., see [Hedge et al. (2018)](https://doi.org/10.3758/s13428-017-0935-1))

There are no fixed rules about inclusion criteria. If the aim is to minimise inter-individual differences and examine differences on the word (or non-word) level, criteria can maximise similarity between participants (e.g., age, level of education). Possible recruitment strategies could be a convenience sample (e.g., undergraduate students), online platforms, or snowball sampling.

Unless it is relevant to the research question, we strongly recommend minimizing the number of additional questions. Every new bit of information reduces the anonymity, as identification based on the data should not be possible by law (i.e., GDPR rules). For example, if location, gender, and highest education are collected, identification in a rural region could be possible already. In addition, fewer questions reduce the testing time for participation. Such a questionnaire should be embedded at the beginning of the experiment. 

We recommend asking for:

- Language history
- Age
- Highest education
- Although gender is often reported and even requested by reviewers, we consider it irrelevant, as there is no evidence of moderation of the cognitive processes underlying reading in German adult readers.

## Design options

### Controlled experiment
With a small number of available participants and strong theoretical motivation, a controlled experiment is feasible. Here, participants respond to several items selected to vary on a specific characteristic, while not co-varying on other characteristics that may also affect reading processes (see relevant the section on How to determine the effect of a specific variable based on lexical decision data in [“Materials”](https://trust-network-guidelines.readthedocs.io/en/latest/materials/)). The design of a lexical decision task relies on the trade-off between available time and data quality. On the one hand, as the length of the experiment increases, the likelihood of participant drop-out increases. On the other hand, a short study with only a couple of items is less likely to provide high data quality. Considering time, assuming that a typical reading adult can finish a 30-minute task is reasonable. Such a task length may be suitable for 500 decisions (i.e., 250 words and 250 non-words), including pre-stimulus and post-response delays and pauses between blocks. 

### Lexicon Projects
Lexicon projects are, in principle, infrastructure projects that allow the exploration of new phenomena in extensive datasets with a broad stimulus and participant base. This format is particularly suitable when one wants to provide resources relevant to investigating reading and psycholinguistic processing, for example, in the context of a language or across many languages (i.e., as there are now many different lexicon projects; Chinese: [Tse et al., 2017](https://doi.org/10.3758/s13428-016-0810-5); Dutch: [Keuleers et al., 2010](https://doi.org/10.3389/fpsyg.2010.00174); English: [Keuleers et al., 2012](https://doi.org/10.3758/s13428-011-0118-4); French [Ferrand et al., 2010](https://doi.org/10.3758/brm.42.2.488); German [Schreuter & Schroeder, 2017](https://doi.org/10.3758/s13428-016-0851-9); Hebrew: [Stein et al., 2024](https://doi.org/10.3758/s13428-024-02502-4); Malay [Yap et al., 2010](https://doi.org/10.3758/brm.42.4.992); Persian: [Nemati et al., 2022](https://doi.org/10.1007/s10936-022-09863-x); Portuguese [Soares et al., 2019](https://doi.org/10.1080/23273798.2019.1578395); Spanish: [Aguasvivas et al., 2018](https://doi.org/10.3389/fpsyg.2018.02156)). The aim is to provide reaction time and accuracy estimates for single words. For such studies, it is recommended to maximise the number of experimental items, with several tens of thousands of words, and at least 30 datapoints per item. Due to time constraints, generally each participant responds to only a subset of items. Note that one can use the datasets from lexicon projects to create *virtual* controlled experiments (see [Kuperman 2015](https://doi.org/10.1080/17470218.2014.989865))

### Crowd-sourcing lexical decision projects
If the researcher aims to collect large amounts of data, they may consider crowd-sourcing a project. Here, one would use a gamified lexical decision task, where each participant provides limited data in a very short experiment duration (e.g., 3 minutes). As this approach is more prone to noise, a much larger amount of data needs to be collected, with the recommendation to cover at least 100,000 words and 40 observations per item ([Amenta et al., 2025](https://doi.org/10.3758/s13428-024-02548-4)). 
The study can estimate the participants’ vocabulary knowledge at the end of the study to provide an incentive for participation. For the items, one may choose a selection of higher-frequency words that are known to participants and words that are not generally known to all participants. This will allow for more informative vocabulary scores for the participants. In this case, the recommendation is to minimise the number of non-words, such that one has a ratio of 3 non-words to 7 words. 

## Programming the experiment
Several decisions have to be made when programming experiments. These relate to the task structure, the use of the response device, and data quality assurance. Typically, an experimental session consists of blocks of items, with each block consisting of trials, which refers to the sequence of events that the participant engages with. In the classical lexical decision task, a single word or non-word is presented in each trial.

### Text encoding
In principle, the text presentation is simple, but there can be nerve-wracking pitfalls. A special case for German is how text is encoded (i.e., the internal code for storing letter strings in the memory of the presenting computer). Some encodings do not allow the proper presentation of German-specific letters (e.g., umlauts *äöü* or the sharp s *ß*). We highly recommend checking the presentation setup specifically for words containing such letters. 

We recommend *UTF-8* encoding, which can be defined on the file level or in the presentation software. This encoding usually works well. 

### Trial structure
A trial generally has the following structure:

- Fixation cross
    - Fixation-cross presentation is implemented to prepare the participant for the upcoming trial. This presentation prevents eye movements or attentional blinks that could increase response times.
    - Typically used signs are “+”, “*” or “x”. These fixation crosses serve as a forward mask to the reading material, potentially influencing behavior. 
    - Our suggested alternative is to use vertical and horizontal lines indicating the location of the stimulus, but without an overlap between bars and the word. 
    - Suggested duration of fixation cross presentation: 500 ms

- Letter string presentation
    - Reaction time, a main measure of the task, is measured from when the item appears on the screen until the response occurs. 
    - Letter strings are recommended to stay on screen until a response. Alternatively, one can have a specific hypothesis that would make a shorter presentation time reasonable. Also, one could show the stimulus for a fixed amount of time to incentivize participants to focus on the task, respond quickly, and avoid taking long breaks in the middle of a block. Here, presentation duration could range from 1500 ms to 5000 ms. For this case, pilot testing is advised to determine the typical range of response times for one’s specific stimulus set.
    - The letter strings should be presented in a different random order for each participant.

- Particiant response 
    - Typically, participants are instructed to respond by pressing on a keyboard, e.g., Left key: “d”, right key: “k”
    - Suppose the aim is to directly compare words and non-words (i.e., the so-called lexicality effect). In that case, it is recommended to counterbalance the response key between participants, such that half of them will press the left key for words and the right key for pseudowords, and the other half the other way around.
    - If the number of words and non-words is counterbalanced, it is typical to instruct participants to press the Right key for words and the Left key for non-words.
    - Alternatives to keyboard responses exist, such as keypads, touchscreens, or mouse clicks. For more information see [Pronk et al., 2020](https://doi.org/10.3758/s13428-019-01321-2), [Bridges et al., 2020](https://doi.org/10.7717/peerj.9414) or [Rodd, 2024](https://doi.org/10.1016/j.jml.2023.104472) for more information. 
    - Inter-stimulus interval: A break before the next stimulus will reduce interference effects. We recommend a blank screen inter-trial interval of 500 ms between the response and the next fixation cross.

After 100 trials, we recommend a short, self-paced break (“Press the space bar when you’re ready to continue”). 