Reporting the research process transparently will allow others to reproduce the study and build on your work. We recommend maximising transparency of the whole research process. For a lexical decision study, the following are the most relevant aspects:

## Rationale for the study:

- Research questions can evolve around novel exploration, phenomena, or existing theories of reading. Relevant German theories and computational models are the Dual Route Cascaded model (German version: [Ziegler et al., 2000](https://doi.org/10.1080/09541440050114570)), CDP+ ([Perry et al., 2010](https://doi.org/10.1080/09541440902978365)), or, more recently, the speechless reader model investigating orthographic processing with a neuro-cognitively plausible implementation ([Gagl et al., 2024](https://doi.org/10.1101/2024.06.25.600635)). 
- Hypothesis: A pre-registration is highly recommended if the study is confirmatory and involves testing a specific hypothesis. Here, one should include the power calculation (to obtain the number of words and number of participants) and the statistical model, including the covariates and random effects structure. If highlighted as an exploration model, modifications can be conducted post-hoc but must be transparently reported.
- Exploratory analyses: If one cannot determine a hypothesis a priori, one should transparently report that the analyses are exploratory

## Documentation of contributions and sources

- Keep track of contributions to the study, relevant papers and discussions with collaborators.
- We recommend specifying author contributions using the CRedIT system to keep track and determine whether a contribution warrants co-authorship ([Holcombe, 2019](https://doi.org/10.3390/publications7030048)).

## Methodology

- Keep track of the relevant choices and the rationale for the selection (e.g., "We used an inter-stimulus interval of 500 ms, as recommended by the TRUST guidelines"). 
- For the reproducibility of a lexical decision study, you need to specify:

    - Variable(s) of interest, along with rationale (if applicable)
    - The corpus used for word selection
    - Non-word generation process (with code as a supplement, if applicable)
    - Selection criteria for words and non-words(with code as a supplement, if applicable)
    - Specification of how word- and non-word-level characteristics were determined (with code as a supplement) 
    - A table with all item characteristics as part of the appendix or supplementary materials. 
    - A table with the mean values for each characteristic for words and non-words

    - Participant recruitment procedure, including procedure and justification for determining sample size 
    - Participant inclusion & exclusion criteria, including justification and definition (e.g., if participants with dyslexia are excluded: Why, and how was this determined?)
    - Number of participants, including an a priori power analysis, when hypotheses are tested, confirmatory
    - Pilot studies that were used to inform decisions, along with justifications (as appendix or supplementary materials)
    - Experimental setup: e.g., online, Lab, field, or similar

## Experimental procedure

- Equipment:

    - In-lab hardware: display size, display refresh rate, distance from display [approximate or controlled with chinrest], chinrest if used, anything else you controlled
    - In-lab tech specs: include in shared data information like OS, CPU, GPU, RAM
    - Online study hardware: which devices were allowed and the proportions of responses from each device, as well as the internet browser used, including this as a variable in the trial-level data

- Software:

    - Report the program used to run, and version(s)
    - Share the code used to run the experiment, whether developed internally or using existing tools.
    - It is highly recommended that any shared code can be run independently without requiring additional software. The best-case scenario would be the code availability in a repository, including a list of all the dependencies (i.e., programming languages,  libraries, environments, etc). For more complex solutions, it can make sense to implement a connection to a cloud computing device, such that one can run code without installing anything (e.g., see this [speechless reader implementation]()).

- Trial sequence:

    - What fixation indicator is used (e.g., +)
    - Durations of everything shown to the participants (inter-stimulus intervals, inter-trial intervals if relevant)
    - Stimulus onset asynchrony (i.e., mean, range, standard deviation, distribution type, etc.)
    - Whether participant responses terminate stimulus presentation
    - Pacing: Is the task self-paced, or is there a fixed pace
    - Timeouts are used for the response
    - Other relevant information: Have there been breaks, the randomisation method/trial order (potentially including transition probabilities), the number of trials, if stimulus and stimulus type repetitions were implemented, and if attention checks were implemented.

- Instructions

    - Information given about the purpose and the procedure of the study.
    - Overall duration of testing sessions, including when to expect breaks

- Stimulus parameters:

    - Font (including font file if possible)
    - If the font is relevant to your experiment, use an open-source font.
    - Size (degrees of visual angle if controlled, give approximate visual angle if possible, see [here for tool to calculate stimulus size in visual angle](https://elvers.us/perception/visualAngle/))
    - Luminance
    - Background colour
    - Text colour
    - Kerning if not default
    - Graphic card setting like Anti-aliasing, etc.

- “Macro” procedure

    - Order of events: entering the lab, information about the study, experiment, debrief, payment, etc.

## Results & Analysis

- Data & code

    - Share the raw trial-level data and code with necessary information: Item, anonymised participant ID, accuracy, reaction time, trial order, and central metadata: Relevant item and participant characteristics. Here, one can review the dataset description provided in the [BIDS specifications for guidance](https://bids-specification--1128.org.readthedocs.build/en/1128/modality-agnostic-files/dataset-description.html).
    - Analysis script, including libraries used & versions as supplementary materials
    - Report in the manuscript what software and libraries were used, if possible - for example, share a containerized environment (e.g., Docker or better Podman files) for reproducing the computing environment, in case libraries differ between operating systems and computer architectures.
    - Record who wrote what code (e.g., standardised file headers, a separate document containing this metadata; specify in CRedIT)
    - Comment code well to increase readability and understanding.
    - Use relative rather than absolute paths.
    - Report and provide implemented data cleaning/preprocessing pipelines.
    - Give summary statistics of lost trials, items, participants, etc., from each criterion applied.
    - Justify whatever decisions are made in data cleaning
    - If one implements a multiverse/robustness analysis to decide on rules for data cleaning, one should report this and share the code to reproduce it.

- Data analysis

    - Give descriptives that make sense for the data, in terms of central tendency and dispersion/spread.
    - Visualise only if this helps communicate (e.g., complex interactive effects)
    - Explicate the criteria on which a decision for one modelling approach or another was made
    - Describe the model structure (e.g., fixed, random effects, distributional parameters, etc.) and the software used to fit it
    - If a model takes a long time to fit, share the output (e.g., share a .rds file for a Bayesian model if it takes more than a couple of hours to fit)
    - Describe & justify model diagnostics. For example, report model comparisons used to determine which variables were included in the model (both fixed & random effects). If there is a justification for a certain model diagnostic, then report it.	
