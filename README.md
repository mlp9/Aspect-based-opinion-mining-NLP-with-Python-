# Aspect-based-opinion-mining-NLP-with-Python
Aspect-Based Opinion Mining involves extracting aspects or features of an entity and figuring out opinions about those aspects. It's a method of text classification that has evolved from sentiment analysis and named entity extraction (NER). ABOM is thus a combination of aspect extraction and opinion mining. While opinions about entities are useful, opinions about aspects of those entities are more granular and insightful.

In this project, we are basically finding opinion words, these are the words which express opinion towards aspects. The opinion words are mostly adjectives, verbs, adverb adjective, and adverb verb combinations. For finding this opinion words Tagging is used.  Tagging is the process of assigning a part of speech marker to each word in an input text. Because tags are generally also applied to punctuation, tokenization is usually performed before, or as part of, the tagging process. For each opinion word, we need to identify its semantic orientation that tells us how it supports, positively or negatively to the overall aspect, which we used to predict the sentiment of each opinion sentence. Following are the course of actions performed:

## Steps:
## 1)Selecting the texts to examine:
          
a) Load data: 

Loading data into the memory and storing it in a dataframe or appropriate data type.

b) Split by whitespace:

Clean text often means a list of words or tokens that we can work with in our machine learning models. This means converting the raw text into a list of words and               saving it again. A very simple way we used to do this is split the document by white space, including” “, new lines, tabs and more.

c) Remove punctuation:

We wanted the words, but without the punctuation like commas and quotes. We also wanted to keep contractions together.
So then we split the document into words by white space (as in “2. Split by Whitespace“), then use string translation to replace all punctuation with nothing. 

d) Normalizing case:

It is common to convert all words to one case for efficient processing.

This means that the vocabulary will shrink in size, but some distinctions are lost (e.g. “Apple” the company vs “apple” the fruit is a commonly used example).

e) Remove stop words: 

Stop words are those words that do not contribute to the deeper meaning of the phrase. They are the most common words such as: “the“, “a“, and “is“.

## 2) Deciding the unit of analysis:
Once the texts have been carefully selected the next thing we did is, determine what the features of our unit of analysis would be.

Features to consider:

o	Tagging:  

With this extraction method, a batch of unstructured data is scanned to identify names of people, products, organizations, locations or dates. Such an approach might be useful to determine the relationship and pattern of interactions between the named entities. It is implemented using POS (Part-of-speech) Tagger.

o	Part-of-speech tagging:

In corpus linguistics, part-of-speech tagging (POS tagging), also called grammatical tagging or word-category disambiguation, is the process of marking up a word in a text (corpus) as corresponding to a particular part of speech, based on both its definition and its context—i.e., its relationship with adjacent and related words in a phrase, sentence, or paragraph. A simplified form of this is the identification of words as nouns, verbs, adjectives, adverbs, etc.


It’s probably easiest to understand the process through an example. Let’s take a look at a simple review for an employee named john.

## Example review:

“Overall Appreciation for performance in last 12 months: John has filled big role in my team as Sr Manager RF Planning and have shown Good progress. John has managed to meet and often exceed target for AOP sites month on month. He has shown true leadership and demonstrated outstanding performance by pitching in and tracking U900swap, capacity addition and making sure sites goes on Air without a hitch. John has lived up the true Vodafone way.”

Steps:

o	We first replace the pronouns in the sentence using a pre-trained neural coreference model; in this particular review, it is not really relevant. 

o	We then segment the chunk of text into sentences, and analyze sentence by sentence. The first step for a given sentence is to tag it with an aspect using POS Tagger.

“Overall Appreciation for performance in last 12 months: John has filled big role in my team as Sr Manager RF Planning and have shown Good progress. - John has managed to meet and often exceed target for AOP sites month on month. He has shown true leadership and demonstrated outstanding performance by pitching in and tracking U900swap, capacity addition and making sure sites goes on Air without a hitch. John has lived up the true Vodafone way.”

o	The next step is to identify opinion words by cross referencing the opinion lexicon for negative and positive words. Once found, the spaCy’s dependency parser is able to identify other dependency words linked to that particular opinion word. This allows you to extract the aspect term, which are shown above. Then, we find the sentiment score based on the opinion words that support the aspect in a positive or negative way and then we assign that sentiment score to the aspect term that it’s referring to.

This application was a part of my internship project that I worked on during my time as a Data Science Intern at Catalyst Executive Education Institute(CEEI).
