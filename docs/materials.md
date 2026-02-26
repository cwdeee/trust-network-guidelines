
This section is concerned with the stimulus Selection for German lexicon decision tasks. In lexical decision experiments, participants see a single word or non-word (e.g., a pseudoword) on the screen and respond with a keypress to indicate whether the item is a word or a pseudoword. Items are generally selected to fit specific criteria that depend on the research question. The after finding a research question one of the first steps is to select the items – to identify suitable words and find or generate pseudowords. 

## Where to find words  ![Importance Rating 2](images/rating5.png)
One should select words from Corpora. The field of corpus linguistics provides text resources that offer representative collections of texts, including words from a given language. These resources allow us to determine the word status of a letter string and word characteristics that are important as selection criteria. For example, word frequency is one of the essential variables for lexical decision studies, that describes how often a word occurs in a corpus which depending on the corpus quality (i.e., size and register), which more or less reflects the frequency in natural language ([Brysbaert et al., 2017](https://doi.org/10.1177/0963721417727521)). 


### Corpora to Consider  ![Importance Rating 2](images/rating5.png)
Conducting a lexical decision experiment in German requires relying on existing resources. Many resources are freely available, and others require a university account. Generally, corpora differ in size and register. A small corpus may provide inaccurate frequency estimates, especially for low-frequency words ([Gernsbacher 1984](https://doi.org/10.1037/0096-3445.113.2.256)). Register refers to the population sampled in the corpus. For example, the words in a child-book corpus differ from those in an adult newspaper corpus. Further, we can distinguish between written, spoken, subtitle and internet corpora as well as ways to generate specific corpora. Below, we present a non-exhaustive list of German resources that the members of the group recommend. To ensure word status, we highly recommended checking multiple corpora to account for potential misspellings that happen regularly. 


We provide links in the following.

Register Legend:

| Symbol | Register |
| --- | --- |
| 👧 | Children |

Note that no symbol reflects that the register are typical adults.

#### Written Corpora  ![Importance Rating 2](images/rating5.png)
Texts collected from newspapers and books. 

- [dlexDB corpus](https://doi.org/10.5281/zenodo.15097663)
    - Syllable frequency, letter n-gram frequencies, and orthographic similarity
- [DWDS corpus](https://www.dwds.de/r/lexdb#kern)
    - Provides annotated data, Representative for 20th century
- [WebCELEX corpus](https://webcelex.ivdnt.org/) (University-Login needed)
    - Easy to use, contains frequency values, lemmatisation, and phonological transcription and syllable-level statistics, Based only on newspapers, so not representative 
- 👧[ChildLex corpus](https://www.dwds.de/d/korpora/childlex)
    - Separate frequency counts for different ages (between 6 and 12), Contains annotation about word class, lemma, orthographic neighbourhood, bigram frequencies, etc.


#### Spoken Corpora  ![Importance Rating 2](images/rating4.png)
[Here](https://dgd.ids-mannheim.de/dgd/pragdb.dgd_extern.sys_inv?v_session_id=) one can find a list of German corpora of spoken language with diverse Registers and Sizes (Sign up necessary) constantly updated by the Institute of the German Language in Manheim. 

#### Subtitle Corpora  ![Importance Rating 2](images/rating4.png)
Texts that have been used as movie/TV series subtitles. They represent spoken language after a script but provide written word forms. 

- [SUBTLEX-DE](https://osf.io/py9ba/)
- [FILMS corpus](https://osf.io/rd7p6/)

#### Internet Corpora  ![Importance Rating 2](images/rating5.png) 
This type of resource collects texts available on the Internet. The advantage is that a large amount of text is available. However, data quality is typically lower (e.g., there is a higher rate of misspellings).

- [Leipzig corpus](https://corpora.uni-leipzig.de/en?corpusId=deu_news_2021) 
- [deWaC corpus](https://wacky.sslmit.unibo.it/doku.php?id=frequency_lists)

#### Ways to generate Corpora 
Here are new ideas for creating corpora with generative language models ([Schepens et al., 2025](https://doi.org/10.1162/OPMI.a.30)). 

- 👧[LLM created ChildLex corpora](https://doi.org/10.17605/OSF.IO/WMUVJ)

### Variables to consider  ![Importance Rating 2](images/rating5.png)  

Words vary in terms of orthographic features (e.g., number of letters, written word form frequency), phonological features (e.g., number of syllables, number of phonemes), morphological features (e.g., morphological complexity, number of morphemes), syntactical features (e.g., Part of Speech) and semantic features (e.g., word class, valence). There are no strict rules for which items to exclude when selecting words/non-words for a study. Manual filtering is not recommended because it’s time-consuming, not reproducible, and error-prone. The filtering process depends on the research question.

#### Exclusion of Taboo Words  ![Importance Rating 2](images/rating4.png)
Excluding taboo words can prevent participant traumatization. Thus, such words should only be used if necessary, and experiments involving them should account for measures that prevent adverse outcomes for participants. In general, it is advised to consult with an ethics committee. It is recommended to exclude slurs that some participants may perceive to be personally offensive and to include a trigger warning if such words are under investigation. [Sulpizio et al. (2024)](https://doi.org/10.3758/s13428-024-02376-6) provide a full list of German taboo words [HERE](https://osf.io/ecr32/overview). Please note that the list of taboo words for German is quite inclusive, thus also including terms that may not necessarily be considered offensive or taboo when presented as an isolated word, e.g. Esel/donkey (sometimes used as an insult).

#### Inflections  ![Importance Rating 2](images/rating4.png)
German is an especially inflection-rich language and has more inflected words than English (see [Clahsen, 1999](https://doi.org/10.1017/S0140525X99002228 )). Inflected word forms are adjustments to base word forms (i.e., Lemmas) that indicate grammatical aspects such as time or gender. The experimenter needs to decide how to treat inflected word forms. For example, the verb "gehen" has 17 different forms, including "ging" (past form).

- There are many more inflected word forms than lemmas, including very similar words that are almost identical in both form and meaning  (e.g., "Katze" – cat, and "Katzen"; [Chilson et al., 2024](https://doi.org/10.31219/osf.io/zy5qf)). If inflected word forms are included, one may want to ensure that there are not too many similar words in the chosen word set.
- Gender-Forms: Some nouns have gendered forms (Lehrer vs. Lehrerin; [Abbasova, 2024](https://doi.org/10.69760/gsrh.0101202404)). Traditionally, the male form is considered the default in most cases. It is possible to include only the more frequent form of each word. However, this may provide a biased picture, especially across multiple studies or in a large-scale study. In attempts to make language more gender-neutral, non-gendered plural forms are also increasingly common. These may be typographically unusual, such as the intrusion of non-letter characters "Lehrer*innen", "Lehrer:innen", or "Lehrer_innen". Other forms can be camel-back letters ("LehrerInnen") or intermediate slashes ("Lehrer/innen"). If such words are included, there must be foil non-words with similar structures to avoid providing a non-lexical cue to the word's lexicality. Another option could be using 50% of the relevant words in female form and the other 50% in male form. This will result in an equal representation of male and female versions, but not considering non-binary individuals. Accounting for the non-binary version, one could use gender neutral forms like "Lehrperson" (e.g., [Bruns & Leiting, 2024](https://books.google.at/books?hl=en&lr=&id=2oUaEQAAQBAJ&oi=fnd&pg=PA97&dq=Using+gender-inclusive+language+in+German%3F+It%27s.+Public+attitudes+towards+gender-inclusive+language:+A+multilingual+perspective,+31,+97.&ots=PJO-r9B597&sig=MWLKm8CY7eLRdjzD6kXuXyzfi2E&redir_esc=y#v=onepage&q&f=false).
- Using inflected words is closer to the actual use of language.

####  Inclusion of compounds  ![Importance Rating 2](images/rating4.png)
A distinctive feature of German is the use of compound words (e.g., “Kühlschrank”, which means fridge, is a cooling cupboard when translated literally). The creation of compound words is productive, such that speakers can create novel word forms on the fly (e.g., [Beyersmann et al., 2020](https://doi.org/10.1080/10888438.2020.1730847)). This poses some questions when selecting items. 

- Including compounds allows us to examine a feature for which the German language is famous, and it stays closer to the actual use of language.  
- If compounds are included, one might need a much larger number of items to have a broad coverage of representative words. At the same time, a larger number of words becomes available. 
- The frequency counts for compound words may not be comparable cross-linguistically. At the extreme end, we may have perfectly legal and understandable neologisms with a frequency of 0 (e.g., [Hasenäcker & Schroeder, 2019](10.1037/xlm0000623)). This is also to be considered when applying a word frequency threshold. A potential solution here is to consider a combined version of the single-word frequency within the individual compounds.

#### Part of Speech  ![Importance Rating 2](images/rating4.png)
Excluding certain parts of speech (e.g., function words) can simplify the selection process (e.g., [Brysbaert et al., 2012](https://doi.org/10.3758/s13428-012-0190-4)). However, it may reduce the items' representativeness.

#### Lemmatization  ![Importance Rating 2](images/rating4.png)
Lemmatization involves using lemmas (i.e., base forms of words; typically found in dictionaries) instead of individual word forms (e.g., [Levelt et al., 1999](https://doi.org/10.1017/S0140525X99001776)). 

Pros:

- Shorter list of words
- Lemmas have more overlap with other corpora
- If participant behavior (e.g., response times, accuracies) are not collected for a specific type, then one option may be to infer responses from corresponding lemmas
- Many more practical applications of behavioral response data with lemmas (e.g., evaluating text difficulty, predicting item difficulty)

Cons:

- Lemmas may be unrepresentative of natural language use

####  Filtering by other word characteristics  ![Importance Rating 2](images/rating5.png) 
It is common to filter experimental items by other word characteristics. Find a list of the most important word characteristics below. This has the advantage of removing “weird” items, which reduces variance not associated with the effect of interest, but at the same time runs the risk of creating a word set that is not representative of the actual language.

Pro

- Reduces the number of untypical words (i.e., too long, too infrequent, too untypical letter combinations)

Cons

- May not be representative of the language
- The cut-off points will be somewhat arbitrary 

##### Word frequency  ![Importance Rating 2](images/rating5.png)
There is an argument for excluding words with particularly low frequency, as these will be unknown to many participants.  

- The experimenter can base the cut-off on word frequency based on the chosen corpus (see [HERE](https://trust-network-guidelines.readthedocs.io/en/latest/materials/#corpora-to-consider-tcr)). 
- One should expect higher error rates if many low-frequency words are included. Rarely used words will likely be categorised as "not-a-word". 
- To effectively measure the word frequency effect, select words with a wide range of frequency values. Including both high- and low-frequency words increases the likelihood of observing frequency modulation. Restricting the analysis to low-frequency words decreases the probability of detecting the effect (see [Brysbaert et al., 2017](https://doi.org/10.1177/0963721417727521) for more information).

##### Word length (letters, phonemes, syllables)  ![Importance Rating 2](images/rating5.png)

- There may be pragmatic reasons for excluding very long words (i.e., making sure they fit on the screen)
- There may be physiological reasons for excluding very long words (i.e., ensuring the word fits within the foveal region of the retina, thus reducing the need for eye movements). An empirical length restriction estimate is 7 or fewer letters (see [Kliegl et al., 2004](https://doi.org/10.1080/09541440340000213)), as longer words may require additional fixations to perceive all letters in the fovea. This may be especially relevant when considering [compound words](https://trust-network-guidelines.readthedocs.io/en/latest/materials/#inclusion-of-compounds). 
- One should be mindful that this may lead to a non-representative sample of words, such as a disproportionate exclusion of compound words and low-frequency words. 
- Furthermore, there is no agreed-upon cut-off at which one would exclude words. 
- Length covaries with many other variables, such as orthographic neighbourhood (long words have very few orthographic neighbours, if any). In selecting the length range, one should consider the extent to which length covaries with variables one is interested in.
- Some previous studies (e.g., [Andrews, 1989](https://doi.org/10.1037/0278-7393.15.5.802); [Fu & Gagl, 2025](https://doi.org/10.1162/jocn_a_02301)) have adopted a restriction to one-word items, e.g., using only four-letter words within an experiment. If one is interested in word-length effects, one can use blocks with a specified word length. The argument for such a procedure is that word length can be perceived in parafoveal vision in natural reading contexts and thus should be known to the participant in advance (e.g., see [Rayner et al.,2011](https://doi.org/10.1037/a0020990)). For the [German Lexicon Project](https://gewonn.github.io/trust/glp/), we accounted for this issue by implementing fixation bars that indicated word length before stimulus presentation. 
- In German letter length is highly correlated with phoneme or syllable length but not exactly the same. For example the grapheme "sch" has one phoneme (/ʃ/; see [Gagl et al., 2015](https://doi.org/10.1080/10888438.2015.1026969)). 

##### Orthographic similarity/familiarity/typicality  ![Importance Rating 2](images/rating5.png)

- There are many ways to measure orthographic similarity/familiarity/typicality of a word and non-words
- Letter string similarity include the orthographic Levenshtein distance ([Yarkoni et al., 2008](https://doi.org/10.3758/PBR.15.5.971)) 
- Letter string familiarity measures refer to bi-, tri-, or quadri-gram frequency metrics that reflect the familiarity of substrings within a given letter sequence (e.g., [Vinckier et al., 2007](https://doi.org/10.1016/j.neuron.2007.05.031)). Information about n-gram frequency can be obtained from WordGen ([Duyck et al., 2004](https://doi.org/10.3758/BF03195595)). 
- Letter string typicality measures include orthographic neighborhood size ([Coltheart et al., 1977](https://www.taylorfrancis.com/chapters/edit/10.4324/9781003309734-29/access-internal-lexicon-max-coltheart-eileen-davelaar-jon-torfi-jonasson-derek-besner)).
- Note that these measures can also be implemented at the phoneme level, generating phonological metrics.
- Mathematically motivated measures include orthographic uncerntainty/entropy (e.g., see [Westbury & Yang, 2024](https://doi.org/10.1075/ml.24006.wes); [Gagl et al., 2022](https://doi.org/10.1371/journal.pcbi.1009995))
- Neuro-cognitively motivated measures of orthographic similarity include orthographic prediction error representations, which avoid the confound with word frequency that is typically present in other measures ([Gagl et al., 2020](https://doi.org/10.1016/j.neuroimage.2020.116727)). 
- Overall, when selecting one of these measures, theoretical assumptions must be considered, as each makes different assumptions about how orthographic information is processed. 

## Non-word creation and selection  ![Importance Rating 2](images/rating5.png)
A lexical decision task requires using non-word stimuli, most prominently pronounceable non-words, so-called pseudowords, or unpronounceable non-words, such as consonant strings. While they are often used simply as foils, interesting research questions can be addressed by manipulating non-word characteristics. In addition, non-word characteristics will influence task difficulty (e.g., see Fig. 1 in [Balota & Chumbley, 1984](https://doi.org/10.1037/0096-1523.10.3.340)). Besides the ratio of words and non-words, other variables can influence processing depth and task difficulty. For example, the task difficulty is higher when pseudowords are used as foils only. In contrast, when using consonant strings as foils, participants can rely solely on a vowel-detection strategy to solve the task, so task difficulty will be low. To this end, one should consider how difficult the task should be, given the study's central hypothesis, as the selection of the non-words will influence word processing. Typically, non-words are word-like and comparable to the words used in the actual study on the level of orthographic similarity, typicality, and familiarity. Furthermore, with differences in processing difficulty, one would also assume differences in the type of processing involved. Contrasting consonant strings with pseudowords or pseudohomophones (letterstrings that sound like words), one could expect that different processing levels are involved (e.g., phonological for pseudowords but not for consonant strings).

### Variables to consider for non-words  ![Importance Rating 2](images/rating5.png)
There are numerous variables for which words and non-words in an experiment can be used to consider wordlikeness. If non-words are very non-word-like (e.g., "XQRPT"), the task will be easy for the participants to make correct lexical decisions without lexically processing the word. There are different ways to quantify word-likeness, and they are likely to be correlated. When available, it is advisable to check for all of the measures. 

- Consonant-vowel structure: Pseudowords that contain unusual consonant or vowel clusters should be avoided. One way to do this is to ensure that the CV structure is identical to the words used in the experiment.
- Morphological complexity: The morphological structure of words should match that of the words in the experiment.
- Orthographic metrics described [HERE](https://trust-network-guidelines.readthedocs.io/en/latest/materials/#orthographic-similarityfamiliaritytypicality)
- Visual characteristics like Optimal Transport measures ([Taylor et al., 2025](https://doi.org/10.1162/NOL.a.19)), acenders and decenders or similar. 

### How to create non-words  ![Importance Rating 2](images/rating5.png)
We recommend automating the process of non-word creation, especially if a large number of items are involved. There are numerous ways of doing this:

- Pseudoword creators for German are available, such as [Wuggy](https://doi.org/10.3758/BRM.42.3.627) or [UniPseudo](https://doi.org/10.1177/17470218231164373). 
- Python is good for working with letter strings, and with medium-low programming skills, you can use it to create pseudowords:
    - Change one vowel or exchange all vowels with consonants to a set of non-words that match the words in your experimental task. 
    - From your basewords, exchange consonants for consonants and vowels for vowels with a certain probability
    - From your basewords, exchanging bigrams or trigrams
    - Instead of relying on basewords, you can depend on language statistics: Combine common bigrams from the language (e.g., based on a [corpus](https://trust-network-guidelines.readthedocs.io/en/latest/materials/#corpora-to-consider)). Specify the length of your desired pseudowords. Select a random letter and then add letters with probabilities matching the structure of the German language. 

### What to avoid  ![Importance Rating 2](images/rating4.png)
- Avoid using pseudowords that resemble slurs, as they may cause offense, unless necessary to address the research question.  
- Eliminate illegal letter clusters when constructing pronounceable non-words (i.e., pseudowords). 
- Consult a representative of your target population (e.g., teenagers, undergraduate students) to check for potential slang words.
- Check that nonword items are not real words in other languages likely spoken by the participants (e.g., English, French, Spanish, Turkish, Arabic or Italian). One can do this by filtering out words from corpora of other languages.

## How to determine the effect of a specific variable based on lexical decision data  ![Importance Rating 2](images/rating5.png)
If we are interested in the effect of a given variable, we have several different paradigms available:

- Orthogonal design: Select words and non-words so they vary maximally on the variable of interest while keeping the conditions comparable to all other variables listed above. Although it’s sometimes unavoidable to use such a design, there are some disadvantages:
    - It often constrains the number of possible items, leading to small numbers.
    - The selection of items that are not representative of the language or orthography. 
    - Lack of methods to test if conditions are comparable (i.e., “matched”): Often, people use a t-test to show that, e.g., the two conditions don’t differ in word frequency, but this method has many problems. So we would advise against (i.e., t-tests cannot be used for equivalence testing, see [Lakens et al., 2018](https://doi.org/10.1177/2515245918770963); also infering the population mean is not what we want here; see [Sassenhagen & Alday, 2016](https://doi.org/10.1016/j.bandl.2016.08.001)). There is a fundamental research gap, and more work is needed. One solution here could be to combine an orthogonal design with regression analyses.  
    - Possible tools to help in designing a study could be [LexOPS](https://doi.org/10.3758/s13428-020-01389-1) or [MILP](https://doi.org/10.1016/j.neuron.2021.02.019) 

- Dichotomising of naturally continuous variables: If our variable of interest is continuous, we must make arbitrary decisions about what constitutes a “low” versus “high” value for assigning words to different conditions. This also prevents us from investigating non-linearity.
- Decorrelated item sets: You can select a number of items that vary on your variable of interest but have a small correlation with other variables ([Protopapas & Kapnoula, 2013](https://escholarship.org/uc/item/1f2883gp)). The advantages/disandvantages are the same as above. 
- Large-scale study & bootstrapping ([Perry, 2022](https://doi.org/10.1177/17470218221086533)). 	
- Regression analysis: This involves using confounding variables as regressors of no interest. Here, statistical methods like linear mixed effect models are advised as they can account for variance components on the level of the stimuli and participants simultaneously. 

## Dialectic-specific considerations  ![Importance Rating 2](images/rating4.png)
The German language has a wide range of dialects (see the [German Language Map](https://dsa.info/europe/institution/dsa)). However, as most people (predominantly undergraduate students) are regularly exposed to Standard German (e.g., at school, through movies and TV), and given the high mobility within the German-speaking realm (especially among undergraduate students), we are not aware of research that provides clear recommendations. This is a research gap. 
