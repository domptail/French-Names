# French Names
## Introduction:
This is a short analysis of French first names between 1900 and 2015 using Python 3.6.

The analysis is solely based on one database. It is not a sociological study of names. 

The database can be downloaded from INSEE's website at: https://www.insee.fr/fr/statistiques/2540004#consulter

It contains four features:
- gender,
- first name,
- year of birth, between 1900 and 2015,
- number of people born with given name, gender, and year of birth. 

There are 589,411 entries, corresponding to almost 83 million people, and over 31,000 unique names.

## Content:

1. Import and prepare the dataset
2. Most common names in 2015 and overall between 1900 and 2015
3. Trend of some specific names throughout the years
4. Evolution of the number of different names
5. Name trends
6. Evolution of the length of names

A short article summarizing the main results is also available on my GitHub page.

## Potential future analysis:
- Gender of names: Some names can be both male and female (e.g., Camille, Dominique). Study the evolution over time of the gender of some names (percentage of males vs. females).
- Impact of movies: Some correlations with movies/books (characters/actors) were shown anecdotally with some names (e.g., M, Arya, Daenerys). A more thorough analysis could be conducted using for example IMDb database.
- Regional specificities: A more detailed analysis could show differences/similarities between France's regions. A file with regional information is available on INSEE's website. See for example the analysis done by Le Monde: http://www.lemonde.fr/les-decodeurs/article/2014/04/29/la-carte-des-prenoms-les-plus-donnes-en-france_4408677_4355770.html
- Classification of curves: Classifying trend curves may enable us to predict lifetime and periodicity of names.
- Soundex: The Soundex phonetic algorithm could be used to identify homophone names and further the analysis based on ngrams. For example, new spellings of the same names may also explain the increasing name diversity. 

