# French Names
This is a short analysis of French first names between 1900 and 2015 using Python 3.

The database can be downloaded from INSEE's website at: https://www.insee.fr/fr/statistiques/2540004#consulter

It contains four features:
- gender,
- first name,
- year of birth, between 1900 and 2015,
- number of people born with given name, gender, and year of birth. 

There are 589,411 entries, corresponding to almost 83 million people, and over 31,000 unique names.

## Part 1:

0. Import and prepare the dataset
1. Most common names in 2015 and overall between 1900 and 2015
2. Evolution of some specific names throughout the years
3. Evolution of the number of different names
4. Evolution of the length of names

## Potential future analysis:
- Gender of names: Some names can be both male and female (e.g., Camille, Dominique, Valérie). Study the evolution over time of the gender of some names (percentage of males vs. females).
- Impact of movies: Some correlations with movies/books (characters/actors) were shown anecdotically with some names (e.g., M, Arya, Daenerys). A more thorough analysis could be conducted using for example IMDb database.
- Regional specificities: Study the differences between France's regions. A file with regional information is available on INSEE's website. See for example the analysis done by Le Monde: http://www.lemonde.fr/les-decodeurs/article/2014/04/29/la-carte-des-prenoms-les-plus-donnes-en-france_4408677_4355770.html
- Evolution curves: Classify the different types of evolution curves.
