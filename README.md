# BootCamp_Project1
## Executive Producers
Travis Cook, Matthew Groh, Marshal Rittenger, Julia Olson

## Proposal:  
We are a production company (Don't Panic Productions) that will be pitching a Netflix original. Before that, we need to analyze the Netflix catalog and determine what 
types of productions would be most likely to succeed. Would Netflix be more likely to buy a TV show versus a movie? What genres have been popular recently, and what 
elements are common in those genres? What combinations of leading actors would be successful? And finally, what other countries should we partner with and why? All of 
this will go into formulating our ideal project to pitch to Netflix

## Data Source:
https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies

## Process:
### Media Type Analysis:
Our initial analysis aimed to determine Netflix's preference between films and TV series. It revealed that 64% of their catalog consists of movies, suggesting a higher 
likelihood of them acquiring a film project.  However, we discovered that TV series tend to receive higher ratings on IMDb through histogram and t-test comparisons, 
indicating a significant statistical difference in ratings. Despite TV series receiving higher ratings, we favored producing a movie due to its 
one-time production nature. We further analyzed the ideal movie length, finding that films between 90-104 minutes tend to dominate Netflix's catalog.  

We also wanted to see whether varying movie lengths received different ratings. Our line chart analysis hinted that longer films tend to receive better ratings.  To 
determine if there is more to this, we created a scatterplot analysis of runtime against IMDb ratings to investigate any correlation. The resulting r-value of 0.13 
signifies a very weak correlation, suggesting that movie length is unlikely to reflect rating and should not be used to influence our decision-making.

### Cleaning our IMDB Scores:
In our dataset, the number of IMDb votes for each title is visible. Obscure titles with only a few votes can disproportionately influence the IMDb score, impacting the 
overall average. To address this, when looping into movies vs. tv shows, we applied quartiles to remove the lowest 25% of vote counts, while still retaining the top 25%. 
This approach helps mitigate the impact of lower outliers on the IMDb scores, ensuring a more accurate representation of each movie.

### Genre Analysis:
After deciding that movies are more dominant on Netflix, our next analysis aimed to determine
which genres are most common and popular in these movies. When looking at individual genres,
we found that about 65% of Netflix movies contain the genre "drama" and almost 40% contain
"comedy". Some difficulties with this analysis were that several of the genres listed in the data
are rather vague or all-encompassing, such as "drama", or are more akin to mediums,
such as "animation". Therefore, for our purposes, we used the top genres we deemed
most fitting of the term.

We followed up the single genre analysis with analyzing which genre-pairs between our previously-decided
top genres were most common on Netflix. This analysis showed that "crime/thriller" and "comedy/romance"
were easily the most popular genre-pairs, present in about 35% and 30% of Netflix movies respectively.
Therefore, we decided to combine these top results to make our movie a crime/thriller/comedy/romance.

### Keyword Analysis:
After determining the genres for our movie, our next analysis aimed to determine what elements and themes
we should include in our movie based on common keywords in Netflix movies of those genres.
When looking at crime/thriller movies, "police" was the most common keyword, appearing in about 17.5% of
movies. Other common words included "crime", "young", "case", and "murder", rather unsurprisingly for
crime/thrillers. For comedy/romance movies, "love" was overwhelmingly the most common keyword, appearing
in about 45% of movie descriptions. Other common words included "different", "college", "journey", and "school",
again unsurprising for the genres. We concluded from this that the most popular Netflix crime/thrillers contain
largely the basic elements of a murder case and investigation and the most popular comedy/romances contain
young love forming primarily in a school setting. Since we're combining these genre-pairs, our movie will contain
young love forming in the midst of a murder investigation.

### Actor Analysis:
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

### Country Partnerships Analysis:
We began our country partnerships analysis by determining which countries had the most productions. We broke this down by the total number of productions, the total number of movies, and the total number of shows. We determined that the US had the most productions, with a grand total of 1822, making up 60.2% of all productions on Netflix. Followed by the US was India, which had 568 productions, which was about 18.8% of all productions. The final 21% consisted of Japan with 242 productions, the UK with 204 productions, and Korea with 192 productions. We also narrowed our analysis to the last ten years and found similar results. Looking at just movies, we found that the US made the most movies, with a total of 1081 movies produced (or 57.8%), then India with 530 movies produced (or 28.4%), then Japan with 89 movies produced (or 4.8%), then Spain with 87 movies produced (or 4.7%), and lastly, the UK with 82 movies produced (or 4.4%). Looking at just shows, we found that the US remained on top with 741 shows produced (or 60.1%), followed by Japan with 153 shows (or 12.4%), Korea with 150 shows (or 12.2%), the UK with 122 shows (or 9.9%), and Spain with 66 shows (or 5.4%). While India was second to the US in the total number of productions and total number of movies produced, it did not make the list of countries with the most shows produced. However, given that we decided we would be making a movie, and not a show, our analysis points to  India as a country we would want to partner with, since it seems like they are able to bump out productions at a rapid rate. 

We then examined which countries with the most productions had the highest IMDb scores on average. While the US and India made the most productions, they did not rank the highest when it came to IMDb scores. Instead, Korea, with an IMDb score of 7.25, came out on top. Following Korea was Japan with an IMDb score of 7.05, then the UK with an IMDb score of 7.01, and finally the US with an IMDb score of 6.55 and India with and IMDb score of 6.41. However, when we examined the highest IMDb scores on average for just movies we found that Japan ranked the highest at 6.76, then the UK at 6.67, then India at 6.38, then the US at 6.3, and lastly, Korea, at 6.28. As for shows, Korea also had the highest score, that being 7.52, followed by the UK at 7.24, Japan at 7.22, the US at 6.99, and India at 6.77. Given these results, especially in regards to the average IMDb score for movies, we determined that Japan would also be a good partner, since they seem to produce higher quality movies.

## Conclusion:
We learned quite a bit about what should make a successful production for Netflix. Based on our analysis, we decided to pitch a film that is about 100 minutes and encompasses
the genres crime/thriller and comedy/romance. We'd ideally cast Leonardo DiCaprio, Cillian Murphy, Shinola Hampton and Emily Hampshire and partner with production companies 
in India and Japan. Based on the data that we had, we came up with an excellent option for the executives at Netflix that has a high probability of getting made. We learned 
that you often have to make do with the data that you have and even then it might not always be clear what decisions you should make. At the end of the day, your goals have 
to guide you as much as the data does. 
