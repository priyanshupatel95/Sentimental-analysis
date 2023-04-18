# Text Analysis
This project is designed to perform text analysis on financial texts to drive sentimental opinions, sentiment scores, readability, passive words, personal pronouns, and more.
```
Sentimental Analysis
Sentimental analysis is a process of determining the sentiment of a piece of writing, whether it's positive, negative, or neutral. To perform this analysis, the following steps are taken:

```

Cleaning using Stop Words Lists
The Stop Words Lists, located in the folder StopWords, are used to clean the text by excluding the words found in the list.

Creating a dictionary of Positive and Negative words
The Master Dictionary, located in the folder MasterDictionary, is used to create a dictionary of Positive and Negative words. Only those words that are not found in the Stop Words Lists are added to the dictionary.

Extracting Derived variables
The text is converted into a list of tokens using the nltk tokenize module. We then calculate the four variables described below:

Positive Score: This score is calculated by assigning the value of +1 for each word if found in the Positive Dictionary and then adding up all the values.
Negative Score: This score is calculated by assigning the value of -1 for each word if found in the Negative Dictionary and then adding up all the values. We multiply the score with -1 so that the score is a positive number.
Polarity Score: This score determines whether the given text is positive or negative in nature. It is calculated using the formula:
Polarity Score = (Positive Score – Negative Score)/ ((Positive Score + Negative Score) + 0.000001)
The range is from -1 to +1.
Subjectivity Score: This score determines whether the given text is objective or subjective. It is calculated using the formula:
Subjectivity Score = (Positive Score + Negative Score)/ ((Total Words after cleaning) + 0.000001)
The range is from 0 to +1.
Analysis of Readability
Analysis of Readability is calculated using the Gunning Fox index formula, which takes into account the following factors:

Average Sentence Length = the number of words / the number of sentences
Percentage of Complex words = the number of complex words / the number of words
Fog Index = 0.4 * (Average Sentence Length + Percentage of Complex words)
Average Number of Words Per Sentence
The formula for calculating the average number of words per sentence is:

Average Number of Words Per Sentence = the total number of words / the total number of sentences

Complex Word Count
Complex words are words in the text that contain more than two syllables.

Word Count
The total number of cleaned words present in the text is counted by removing the stop words using the stopwords class of the nltk package and removing any punctuations like ? ! , . from the word before counting.

Syllable Count Per Word
The number of syllables in each word of the text is counted by counting the vowels present in each word. Exceptions like words ending with "es","ed" are handled by not counting them as a syllable.

Personal Pronouns
To calculate Personal Pronouns mentioned in the text, regex is used to find the counts of the words - “I,” “we,” “my,” “ours,” and “us”. Special care is taken so that the country name US is not included in the list.

Average Word Length
The average word length is calculated by the formula:

Sum of the total number of characters in each word/Total number of words
