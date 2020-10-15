# Aspect-based-opinion-mining-NLP-with-Python-
Aspect-Based Opinion Mining involves extracting aspects or features of an entity and figuring out opinions about those aspects. It's a method of text classification that has evolved from sentiment analysis and named entity extraction (NER). ABOM is thus a combination of aspect extraction and opinion mining. While opinions about entities are useful, opinions about aspects of those entities are more granular and insightful.

In this project, we are basically finding opinion words, these are the words which express opinion towards aspects. The opinion words are mostly adjectives, verbs, adverb adjective, and adverb verb combinations. For finding this opinion words Tagging is used.  Tagging is the process of assigning a part of speech marker to each word in an input text. Because tags are generally also applied to punctuation, tokenization is usually performed before, or as part of, the tagging process. For each opinion word, we need to identify its semantic orientation that tells us how it supports, positively or negatively to the overall aspect, which we used to predict the sentiment of each opinion sentence. Following are the course of actions performed:

## Steps:
##1)Selecting the texts to examine:
          
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

