# BootCamp_Project1
## Executive Producers
Travis Cook, Matthew Groh, Marshal Rittenger, Julia Olson

## Proposal:  
We are a production company (Don't Panic Productions) that will be pitching a Netflix original. Before that, we need to analyze the Netflix catalog and determine what 
types of productions would be most likely to succeed. Would Netflix be more likely to buy a TV show versus a movie? What genres have been popular recently, and what 
elements are common in those genres? What combinations of leading actors would be successful? And finally, what other countries should we partner with and why? All of 
this will go into formulating our ideal project to pitch to Netflix

## Process:
Our initial analysis aimed to determine Netflix's preference between films and TV series. It revealed that 64% of their catalog consists of movies, suggesting a higher 
likelihood of them acquiring a film project.  However, we discovered that TV series tend to receive higher ratings on IMDb through histogram and t-test comparisons, 
indicating a significant statistical difference in ratings. Despite TV series receiving higher ratings, we favored producing a movie due to its 
one-time production nature. We further analyzed the ideal movie length, finding that films between 90-104 minutes tend to dominate Netflix's catalog.  
We also wanted to see whether varying movie lengths received different ratings. Our line chart analysis hinted that longer films tend to receive better ratings.  To 
determine if there is more to this, we created a scatterplot analysis of runtime against IMDb ratings to investigate any correlation. The resulting r-value of 0.13 
signifies a very weak correlation, suggesting that movie length is unlikely to reflect rating and should not be used to influence our decision-making.

Cleaning our IMDB Scores:
In our dataset, the number of IMDb votes for each title is visible. Obscure titles with only a few votes can disproportionately influence the IMDb score, impacting the 
overall average. To address this, we applied quartiles to remove the lowest 25% of vote counts, while still retaining the top 25%. This approach helps mitigate the 
impact of lower outliers on the IMDb scores, ensuring a more accurate representation of each movie

For our actor analysis, we had to merge the two CSV files to get the full cast list for each film entry. Then from that we created another dataframe that grouped
the relevant data by actor. In this case, what was most important was the mean IMDB score for each actor and the sum total of votes on IMDB that their films and
movies received. We also only considered actors in more than one production on Netflix, to improve our sample size. We grouped and sorted first by actors 
in the dataset with the most IMDB votes, i.e. the actors with the most popular projects on IMDB. It was clear that Leonardo DiCaprio was the most popular actor on 
Netflix with over 8 million votes and Cillian Murphy was in a distant, but clear second with slightly over 5 million votes. To analyze which of these Top 15 
actors had the highest quality projects (on average) we then sorted that data by mean IMDB rating  and found that Murphy ranked higher than DiCaprio. We also 
discovered that Russ Fega, upon some Googling, is an actor who has appeared in Christopher Nolan's movies, but only in bit parts, so not someone we would seriously 
consider for our movie. So from this data, we've discovered that we should aim to cast DiCaprio and Murphy.

We also wanted to see which actors had the highest average rating on Netflix. We made a data frame that only considered the top 50% of vote-getters since, as we've 
seen, the top actors are getting millions of votes, but the majority of actors even in multiple things on Netflix have less than 50 thousand votes in total. Upon 
producing those charts we found that the top actors were still in small parts in very big movies (Emily Carey and Russ Fega) or voice actors (Akari Kito). However,
from this data we were still happy to find Shanola Hampton (Shameless) and Emily Hampshire (Schitt's Creek) as great additions to Leo and Cillian. They obviously 
have fewer total ratings than someone like Robin Wright with over 3 million, but we'd prefer some less famous actors to pair with our leading men.

We also created a function to easily find the best actor options by genre. This function sorts the data and creates a bar graph showing the actors with the most IMDB votes
on movies or TV shows that include the input genres. Upon doing this for crime and thriller, we discover that DiCaprio and Murphy are once again at or near 
the top of both lists. We also did analyses of average IMDB and TMDB ratings and found there was a significant difference between them, with TMDB ratings being
higher on average. Because we knew our presentation time would be limited and we didn't quite have the time for further analysis, we didn't let this finding affect 
our final decisions. 

## Conclusion:
We learned quite a bit about what should make a successful production for Netflix. Based on our analysis, we decided to pitch a film that is about 100 minutes and encompasses
the genres crime/thriller and comedy/romance. We'd ideally cast Leonardo DiCaprio, Cillian Murphy, Shinola Hampton and Emily Hampshire and partner with production companies 
in India and Japan. Based on the data that we had, we came up with an excellent option for the executives at Netflix that has a high probability of getting made. We learned 
that you often have to make do with the data that you have and even then it might not always be clear what decisions you should make. At the end of the day, your goals have 
to guide you as much as the data does. 
