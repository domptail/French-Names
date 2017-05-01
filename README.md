# AN ANALYSIS OF FIRST NAMES IN FRANCE IN 1900-2015
## Introduction:
This is an analysis of first names in France between 1900 and 2015 using Python 3.6.

This is not a sociological study of names as there is no information on education, income, religion, etc. 

The database can be downloaded from INSEE's [website](https://www.insee.fr/fr/statistiques/2540004#consulter).

It contains four features:
- gender,
- first name,
- year of birth, between 1900 and 2015,
- number of people born with given name, gender, and year of birth. 

There are 589,411 entries, corresponding to almost 83 million people, and over 31,000 unique names.

## Methodology:
The purpose of this project was to learn a toolset to manipulate and visualize data, not necessarily to do in-depth analysis on said data.

This is a personal project to practice programming so all the data manipulation and most of the visualization was done in Python 3.6. The treemaps were prepared using Microsoft visualization software Power BI. 

There are still many possible improvements to the code (e.g., factoring). However, since the code is only used for a ‘one-time’ analysis, and not to be used repeatedly, full optimization might not be necessary. 

The code and graphs are available on my GitHub page (Jupyter [notebook](https://github.com/domptail/French-Names/blob/master/French%20Names%20-%20Python%20Code.ipynb)).

## Content:

1. Import and prepare the dataset
2. Most common names in 2015 and overall between 1900 and 2015
3. Trend of some specific names throughout the years
4. Evolution of the number of different names
5. Name trends
6. Evolution of the length of names

An article summarizing the main results is available on my GitHub page [md file](https://github.com/domptail/French-Names/blob/master/French%20Names%20-%20Results%20Summary.md).

## Potential future analysis:
- Gender of names: Some names can be both male and female (e.g., Camille, Dominique). It would be interesting to study the evolution over time of the gender of some names (percentage of males vs. females).
- Impact of movies: Some correlations with movies/books (characters/actors) were shown anecdotally with some names (e.g., M, Arya, Daenerys). A more thorough analysis could be conducted using for example IMDb database.
- Regional specificities: A more detailed analysis could show differences/similarities between France's regions. A file with regional information is available on INSEE's website. See for example the [analysis](http://www.lemonde.fr/les-decodeurs/article/2014/04/29/la-carte-des-prenoms-les-plus-donnes-en-france_4408677_4355770.html) done by Le Monde.
- Soundex: The Soundex phonetic algorithm could be used to identify homophone names and further the analysis based on ngrams. For example, new spellings of the same names may also explain the increasing name diversity.
- Name periodicity: Clustering shapes of trend curves may enable us to predict lifetime and periodicity of names.


