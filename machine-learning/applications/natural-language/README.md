# Natural language

### Introduction

 **Natural Language Processing**, usually shortened as NLP, is a branch of artificial intelligence that deals with the interaction between computers and humans using the **natural language**. The ultimate objective of NLP is to read, decipher, understand, and make sense of the human languages in a manner that is valuable

### Concepts and steps



**Identify and mark sentence, phrase, and paragraph boundaries** – these markers are important when doing entity extraction and NLP since they serve as useful breaks within which analysis occurs.

**Acronym normalization and tagging** – acronyms can be specified as “I.B.M.” or “IBM” so these should be tagged and normalized.

**Tokenization:** Tokenization refers to dividing a sentence into chunks of words. Usually tokenization is the first task performed in the natural language processing pipeline. Tokenization can be performed at two levels: word-level and sentence-level.

**Decompounding** – for some languages \(typically Germanic, Scandinavian, and Cyrillic languages\), compound words will need to be split into smaller parts to allow for accurate NLP. For example: “samstagmorgen” is “Saturday Morning” in German.

**Stop Word Removal:** Stop words in natural language are words that do not provide any useful information in a given context. For instance if you are developing an emotion detection engine, words such as "is", "am", and "the" do not convey any information related to emotions.

**Stemming and Lemmatization:** Stemming refers to the process of stripping suffixes from words in attempt to normalize them and reduce them to their non-changing portion. For example, stemming the words "computational", "computed", "computing" would all result in "comput" since this is the non-changing part of the word. Stemming operates on single words and do not take context of the word into account. However, "comput" has no semantic information.

**Entity extraction** – identifying and extracting entities \(people, places, companies, etc.\) is a necessary step to simplify downstream processing. 

**Parts of Speech \(POS\):** Another important NLP task is to assign parts of speech tags to the words. To construct a meaningful and grammatically correct sentence, parts of speech play an important role. The arrangement and co-occurrence of different parts of speech in a word make it grammatically and semantically understandable. Furthermore, parts of speech are also integral to context identification. POS tagging helps achieve these tasks.

### Implementations and libraries

* [Python NLTK](https://www.nltk.org/): A simple yet powerful and fast NLP library
* Amazon has an [out-of-the-box tool](https://aws.amazon.com/comprehend/?trk=ps_a131L0000083KwIQAU&trkCampaign=2020_PAITW_Comprehend_PDP&sc_channel=ps&sc_campaign=Comprehend_GS_WP_nlp&sc_outcome=AIML_Digital_Marketing&sc_geo=mult&sc_country=mult&sc_publisher=Google&sc_detail=natural%20language%20processing&ef_id=Cj0KCQjwz4z3BRCgARIsAES_OVcXtxaskUc6-t3GOr5VAVD6UBtsP-NcKEza9dI3LNEXrXbE3bdhWJ0aAgWyEALw_wcB:G:s&s_kwcid=AL!4422!3!411177164393!e!!), for people with no machine learning background

### Further read

{% embed url="https://stackabuse.com/what-is-natural-language-processing/" %}

See the following for all the steps and libraries, and what is possible in NLP:

{% embed url="https://www.searchtechnologies.com/blog/natural-language-processing-techniques" %}







