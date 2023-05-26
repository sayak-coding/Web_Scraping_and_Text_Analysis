# Web_Scraping_and_Text_Analysis

1. Objective

The objective of this assignment is to extract textual data articles from the given URL and perform text analysis to compute variables that are explained below. 

2. Data Extraction

Input.xlsx

For each of the articles, given in the input.xlsx file, extract the article text and save the extracted article in a text file with URL_ID as its file name, please make sure your program extracts only the article title and the article text. It should not extract the website header, footer, or anything other than the article text. 

3. Data Analysis

For each of the extracted texts from the article, perform textual analysis and compute variables, given in the output structure excel file. 

4. Variables

a. POSITIVE SCORE

This score is calculated by assigning the value of +1 for each word if found in the Positive Dictionary and then adding up all the values.

b. NEGATIVE SCORE

This score is calculated by assigning the value of -1 for each word if found in the Negative Dictionary and then adding up all the values. We multiply the score with -1 so that the score is a positive number.

c. POLARITY SCORE

This is the score that determines if a given text is positive or negative in nature. It is calculated by using the formula: 
Polarity Score = (Positive Score – Negative Score)/ ((Positive Score + Negative Score) + 0.000001)
Range is from -1 to +1

d. SUBJECTIVITY SCORE

This is the score that determines if a given text is objective or subjective. It is calculated by using the formula: 
Subjectivity Score = (Positive Score + Negative Score)/ ((Total Words after cleaning) + 0.000001)
Range is from 0 to +1

e. AVG SENTENCE LENGTH

 the number of words / the number of sentences
 
f. PERCENTAGE OF COMPLEX WORDS

the number of complex words / the number of words 

g. FOG INDEX

 0.4 * (Average Sentence Length + Percentage of Complex words)

h. AVG NUMBER OF WORDS PER SENTENCE

the total number of words / the total number of sentences

i. COMPLEX WORD COUNT

Complex words are words in the text that contain more than two syllables.

j. WORD COUNT

We count the total cleaned words present in the text by 
1. removing the stop words (using stopwords class of nltk package).
2. removing any punctuations like ? ! , . from the word before counting

k. SYLLABLE PER WORD

We count the number of Syllables in each word of the text by counting the vowels present in each word. We also handle some exceptions like words ending with "es","ed" by not counting them as a syllable.

l. PERSONAL PRONOUNS

To calculate Personal Pronouns mentioned in the text, we use regex to find the counts of the words - “I,” “we,” “my,” “ours,” and “us”. Special care is taken so that the country name US is not included in the list.

m. AVG WORD LENGTH

Sum of the total number of characters in each word/Total number of words


