# AN ANALYSIS OF FIRST NAMES IN FRANCE BETWEEN 1900 AND 2015

## Introduction

This is an analysis of first names in France between 1900 and 2015. This is not a sociological study of names as there is no information on education, income, religion, etc. Still, I was pleasantly surprised by how many insights could be derived from a simple database with only 4 columns!

The data can be downloaded from the French National Institute of Statistics and Economic Studies (INSEE)'s website. 

It contains four features:
- Gender
- First name
- Year of birth, between 1900 and 2015
- Number of people born with given name, gender, and year of birth

INSEE has managed the database since 1946 and used the following criteria to include a name or not:
1.	Between 1900-1945 and/or 1946-2015, the name has been given at least 20 times to either males or females.
2.	For a given year, the name has been given at least 3 times to males or females.

Names that do not comply with condition 1 are grouped by sex and year of birth under one entry with the value 'PRENOMS_RARES' (rare first names) in the ‘name’ column.

Names that comply with condition 1 but not condition 2 are grouped by sex and name under one entry with the value 'XXXX' in the ‘year’ column.

There are 589,411 entries, corresponding to almost 83 million people, and over 31,000 unique names.

## Methodology

The purpose of this project was to learn a toolset to manipulate and visualize data, not necessarily to do in-depth analysis on said data.

This is a personal project to practice programming so all the data manipulation and most of the visualization was done in Python 3.6. The treemaps were prepared using Microsoft visualization software Power BI. Throughout the project, I practiced data manipulation (pandas dataframe), data visualization (pyplot), and some natural language processing (nltk, ngrams).
There are still many possible improvements to the code (e.g., factoring). However, since the code is only used for a ‘one-time’ analysis, and not to be used repeatedly, full optimization might not be necessary. 

The code and graphs are available on my GitHub [page](https://github.com/domptail) (Jupyter [notebook](https://github.com/domptail/French-Names/blob/master/French%20Names%20from%201900%20to%202015.ipynb)).

## Results

Below is a summary of some of the most interesting results.

### Dips in births during WWI, WWII and the Baby Boom

We can use the data to estimate the annual number of births in France between 1900 and 2015. The graph clearly shows:
- a dip in the number of births during WWI, from 548,000 in 1913 down to 283,000 in 1916 (-48% in 3 years)!
- a dip in the number of births during WWII
- the Baby Boom after WWII, from 592,000 births in 1945 up to 893,000 in 1947 (+51% in 2 years)!

The diminution in birth rate is indeed another consequence of wars which dramatically affects demography. Note that WWI was far more devastating to France than WWII both in terms of number of births and deaths. The country lost about 600k soldiers and civilians in WWII but 1.7 million in WWI. In the overall conflicts however, there were 3-4 times more losses in WWII (60-80M) than in WWI (19M). 

<p align="center">
  <b>Number of births per year</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573861/f5803ffe-2dfd-11e7-95a8-1f417d7102ec.PNG">
</p>

The repercussions of the two wars can be seen on the number of people named Marie and Jean, the two most given names overall throughout the century by far (2.2 million Maries and 1.9 million Jeans). We can control for the effects of the wars by calculating instead the percentage of births of the same gender these names represent each year. It is interesting to see that Marie and Jean have had very different popularity trends.

<p align="center">
  <b>Trend of the two most popular names overall Marie and Jean - In number of people</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573856/f57a85e6-2dfd-11e7-8fbe-72d1b29af3d2.PNG">
</p>

<p align="center">
  <b>Trend of the two most popular names overall Marie and Jean - In percentage of male and female births respectively</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573860/f57bf480-2dfd-11e7-9d9f-d5199a98a6a2.PNG">
</p>

   
### Correlations between name trends and world events 

#### My first name, Kim

I grew up in France and had only ever met one other person named Kim before moving to the US. Indeed, there were only 79 people named Kim the year I was born (1986) and there have been less than 6000 people named Kim born in France in total between 1900 and 2015. We can also notice that:
- There were almost no Kims at all in France before 1952 (males) and 1954 (females).
- The number of Kims increased around 1978, and reached a local maximum (231 Kims) in 1993.

The trend of the name Kim is probably correlated to the following events: 
- Immigration from Vietnam following the First Indochina War (1946-1954). Kim is a Sino-Vietnamese name (金) meaning gold (metal).
- The American actress, Kim Basinger, started her acting career around 1978, and gained mainstream exposure in 1989 (Batman).
- There are other famous Kims, such as the American actress Kim Novak, who began her career in 1954, the English singer Kim Wilde, popular in France since 1981, and Kim Kardashian, popular since the 2007 reality show. Even though we cannot easily see direct correlations, they might have contributed to the popularity of the name Kim.
                
<p align="center">
  <b>Trend of the name Kim</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573855/f56543a2-2dfd-11e7-9c9a-3ef87147785a.PNG">
</p>
 
#### Names appearing after movies

Some names are particular (e.g., M, Arya, Daenerys and Khaleesi) and can be assumed to have been popularized by movies. 
- The name 'M' was first given in the early 1960s. This seems to correlate with the first James Bond movie (Dr. No, 1962), where M is the Head of the Secret Intelligence Service and Bond's superior. It is difficult to identify correlations in later years with specific James Bond movies since there have been new releases almost every 2 years on average (24 movies in 53 years).
- Similarly, the uptake in 'Arya', 'Daenerys' and 'Khaleesi' in France seems to correlate with the 'Game of Thrones' TV series. Even though 'A Game of Thrones', the first novel in 'A Song of Ice and Fire' series, was first published in 1996, the story became most popular with the TV series, which premiered in 2011.

<p align="center">
  <b>Genesis of the name M</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573853/f563a88a-2dfd-11e7-9448-a57e35a44216.PNG">
</p>

<p align="center">
  <b>Genesis of the names Arya, Daenerys and Khaleesi</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573850/f563268a-2dfd-11e7-9429-b914516bb717.PNG">
</p>
      

### There is increasing diversity in names

The number of different names increased from 1,600 in 1900 to 12,400 in 2015! The ratio of names to births also quadrupled between 1900 (0.004) and 2015 (0.016). Another indicator of name diversity is the number of people with rare names, which jumped from 2,980 people in 1900 (0.7% of births) to 56,107 in 2015 (7.2% of births). 

The increasing name diversity can be correlated to the different French ‘Naming Laws’. The Law of 1803, established under Napoléon Bonaparte, limited names to those found in calendars of saints and 'historic names'. The Law of 1966 extended the list of authorized names (e.g., mythology, regional, and foreign names). Finally, the Law of 1993 authorized almost any name, as long as it is not contrary to the interests of the child.

Other factors might be correlated to increasing name diversity such as new means of communication and cultural exchanges (television, Internet), immigrations, and new spellings of the same names (homophones). However, these are out of the scope of this article.

<p align="center">
  <b>Number of different names per birth</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573851/f563581c-2dfd-11e7-8b5d-51c4b55871cd.PNG">
</p>

<p align="center">
  <b>Percentage of births with ‘rare names’ per gender</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573858/f57b73b6-2dfd-11e7-9ff6-abeb17c6928f.PNG">
</p>
                      
Treemaps are yet another clear way to picture the increasing name diversity. Half of the people born in 1900 had one of 28 names, vs. 297 in 2015. Similarly, the top 20 names represented 43% of total births in 1900 but only 11% in 2015.

<p align="center">
  <b>Treemaps of names representing 50% of births in 1900</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573862/f59153a2-2dfd-11e7-98c3-68864dce05e2.PNG">
</p>

<p align="center">
  <b>Treemaps of names representing 50% of births in 2015</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573863/f592af4a-2dfd-11e7-9292-4502b741469c.PNG">
</p>


### Similar types of names are popular at the same time
In general, both male and female compound names were most popular between 1940 and 1965. Note that most compound names were composed of the names Jean and Marie respectively! 

In the following graphs each line represent at least 10,000 births overall.

<p align="center">
  <b>Trend of compound names - Males</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573852/f5634642-2dfd-11e7-955e-12f577941775.PNG">
</p>

<p align="center">
  <b>Trend of compound names - Females</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573854/f563a6aa-2dfd-11e7-97a8-fb3c27d702ba.PNG">
</p>

  
Interestingly, we can observe common trends for other types of names (data not included, see Jupyter notebook):
- Names ending in -ETTE (e.g., Paulette, Yvette, Odette, Colette) were most popular in 1920-1940.
- Names ending in -IANE (e.g., Christiane, Josiane, Liliane) were most popular in 1940-1960.
- Names containing 'CLAUD' (e.g., Claude, Jean-Claude, Claudine) were most popular in 1930-1960.
- Names ending in '-INE' (e.g., Catherine, Martine, Christine, Sandrine) were most popular between 1950 and 1980.

### Male/female name pairs are popular at the same time
Five-grams can help us find pairs of male/female names (e.g., Joël/Joëlle, Jacques/Jacqueline, Louis/Louise, Laurent/Laurence, Julien/Julie, Christian/Christiane, Patrice/Patricia, André/Andrée). In general, both names follow the same trend.

<p align="center">
  <b>Examples of parallel trends for male/female name pairs</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573857/f57b4d0a-2dfd-11e7-84d3-ced646b6fb6b.PNG">
</p>
 
### The Top 15 names include both old and recent names 
The top 15 names in 2015 comprised both ‘old’ names becoming popular again (e.g., Louis, Paul, Jules for males and Louise, Alice, Lucie for females), and ‘recent’ names (e.g., Lucas, Adam, Hugo for males, and Jade, Lina, Lola for female).

<p align="center">
  <b>Top 15 female names in 2015 - Old names becoming popular again</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573548/5346a888-2dfb-11e7-82b5-dc94f73128f8.PNG">
</p>

<p align="center">
  <b>Top 15 female names in 2015 - 'Recent' names</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573857/f57b4d0a-2dfd-11e7-84d3-ced646b6fb6b.PNG">
</p>
 
### Popular names are on average shorter than in the past
The mean name length went from 6.3 letters in 1910 to 7.1 in 1970 and 5.5 in 2010. Throughout the century, names ranged from one letter (A, L, N, M) to 19 letters (Guillaume-Alexandre, François-Christophe)!

<p align="center">
  <b>Evolution of mean name length (weighted average by number of births)</b><br>
  <img src="https://cloud.githubusercontent.com/assets/25837658/25573859/f57bb9fc-2dfd-11e7-847d-fda19f3ade66.PNG">
</p>
 
## Additional Questions
Below is a non-exhaustive list of other interesting topics to look into:
- Impact of movies: Some correlations with movies/books (characters/actors) were shown anecdotally with certain names (e.g., M, Arya, Daenerys), a more thorough analysis could be conducted using for example IMDb database.
- Regional specificities: A more detailed analysis could show differences/similarities between France's regions. A file with regional information is available on INSEE's website. See for example the [analysis](http://www.lemonde.fr/les-decodeurs/article/2014/04/29/la-carte-des-prenoms-les-plus-donnes-en-france_4408677_4355770.html) done by Le Monde.
- Soundex: The Soundex phonetic algorithm could be used to identify homophone names and further the analysis based on ngrams. For example, new spellings of the same names may also explain the increasing name diversity.
- Name periodicity: Clustering shapes of trend curves may enable us to predict lifetime and periodicity of names.
