### Stimulus Selection for German lexicon decision tasks
In lexical decision experiments, participants see a single word or pseudoword on the screen and respond with a keypress to indicate whether the item is a word or a pseudoword. Items are generally selected to fit specific criteria that depend on the research question. The first step is to select the items – to identify suitable words and find or generate pseudowords. One should select Words from Corpora: these resources contain many words from a given language and allow us to determine specific word characteristics, which are, in turn, important as selection criteria. Word frequency is one of the essential variables for lexical decision studies: How often a word occurs per million words in natural language ([more details](https://doi.org/10.1177/0963721417727521)). 



#### Corpora to Consider
Conducting a lexical decision experiment in German requires relying on existing resources. Many resources are freely available, and others require a university account. Generally, corpora differ in size and register. A small corpus may provide inaccurate frequency estimates, especially for low-frequency words ([more details](https://doi.org/10.1037/0096-3445.113.2.256)). Register refers to the population sampled in the corpus. For example, the words in a child-book corpus differ from those in an adult newspaper corpus. Further, we can distinguish between written, spoken, subtitle and internet corpora as well as ways to generate specific corpora. Below, we present a non-exhaustive list of German resources that the members of the group recommend. To ensure word status, we highly recommended checking multiple corpora to account for potential miss spellings that happen regularly. 


We provide links in the following.

Register Legend:

| Symbol | Register |
| --- | --- |
| 👧 | Children |

Note that no symbol reflects that the register are typical adults.

##### Written Corpora 
Texts collected from newspapers and books. 

- [dlexDB corpus](https://doi.org/10.5281/zenodo.15097663)
- [DWDS corpus](https://www.dwds.de/r/lexdb#kern)
- [WebCELEX corpus](https://webcelex.ivdnt.org/)
- 👧[ChildLex corpus](https://www.dwds.de/d/korpora/childlex)

##### Spoken Corpora 
[Here](https://dgd.ids-mannheim.de/dgd/pragdb.dgd_extern.sys_inv?v_session_id=) one can find a list of updated German corpora of spoken language with diverse Registers and Sizes (sign up necessary)

##### Subtitle Corpora 
Texts that have been used as movie/TV series subtitles. They represent spoken language after a script but provide written word forms. 

- [SubtLex corpus](https://osf.io/py9ba/)
- [FILMS corpus](https://osf.io/rd7p6/)

##### Internet Corpora 
This type of resource collects texts available on the Internet. The advantage is that a large amount of text is available. However, data quality is typically lower (i.e., there is a higher rate of misspellings).

- [Leipzig corpus](https://corpora.uni-leipzig.de/en?corpusId=deu_news_2021) 
- [deWaC corpus](https://wacky.sslmit.unibo.it/doku.php?id=frequency_lists)

##### Ways to generate Corpora 
Here are ideas of creating corpora  with geneartive language models ([more details](https://doi.org/10.31234/osf.io/gm9b6_v5)). 

- 👧[LLM created ChildLex corpora](https://doi.org/h10.17605/OSF.IO/WMUVJ)



#### Variables to Consider
Here is a list of variables to be considered when selecting words for word recognition tasks like a lexical decision task in German. 

##### Exclusion of Taboo Words ![Importance Rating 2](images/rating2.png)
Excluding taboo words can prevent participant traumatization.

#### Word frequency ![Importance Rating 4](images/rating4.png)
A frequency cut-off can be used to exclude low-frequency words. 

Pro:

- Reduces the number of low-frequency words

Con:

- May not be representative of the language
- Requires additional work to determine the cut-off point

#### Word Length
Word length can be measured in letters or syllables. The pros of not excluding words based on length are:
- Simple in selection
- Most representative
However, the cons are:
- May not be representative of the language
- Requires additional work to determine the cut-off point

#### Part of Speech
Excluding certain parts of speech (e.g., function words) can simplify the selection process. However, it may also reduce the language's representativeness.

#### Inclusion of Compounds
Including compounds is relatively unique to German. The pros are:
- More representative of the language
However, the cons are:
- Many very low-frequency words
- A large number of words

#### Gender Forms
German words have gendered forms (e.g., "Lehrer" vs. "Lehrerin"). The pros of using gender forms are:
- Simpler selection rules
However, the cons are:
- Some words will only appear in one gendered form
- Male and female parts need to be matched

#### Inflections
German is an inflection-rich language, with different projects dealing with inflections in various ways. Including inflections can massively increase the possible number of words. For example, the verb "gehen" has 17 different forms, including "ging" (past form). The pros of including inflections are:
- Specialty of German
- Does not require an annotated corpus
- Closer to the actual use of language
However, the cons are:
- The experiment will be much longer
- More words included means more participants are needed

#### Lemmatization
Lemmatization involves using lemmas (base forms of words) instead of individual word forms. The pros of lemmatization are:
- Shorter list of words
- Lemmas have more overlap with other corpora
- Making inferences about a type based on the lemma RT is better than not having an RT of the type
- Many more practical applications of RT data with lemmas (e.g., evaluating text difficulty, predicting item difficulty)
However, the cons are:
- Lemmas are often not identical to what is seen or heard in natural language
