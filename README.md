# Phase 1 IMDB Exploratory Data Analysis for Microsoft


## Project Overview

### Business Problem

Microsoft decided to create a new movie studio, but they don’t know anything about creating movies. They want to know what types of films are currently doing the best at the box office.  What characteristic  makes the film more likely to be box office hit.
My resposibility is to explor what types of films are currently doing the best at the box office, and make recomendations based on the finding to help them decide what direction should they take to enter the market.

### The Data

In the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

During the analysis I will use the following data sources:
![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)


#### DataBase tables
 - movie_basics
 - movie_ratings
 
#### CSV file
 - zippedData/tn.movie_budgets.csv.gz
 
### Data overview
I worked with the following following columns from the dataset:
Genre, Realease time, Movie title, Runtime, 
In addition to these information I also created Foreign Gross, Profit, Profitable, and ROI columns.

### Data Cleaning
During the data cleaning process I removed the rows which were missing the genre information.
ALso removed the outliers in the runtime coumn, wich were less than 10 minutes and anything over 300 minutes. After that I filtered the data to only show the movies from 2010 to 2019.

### Analysis

After cleaning the dataset, the analysis should yield information on what genres are the most profitable, what is the average length of a movie in each genre. When is the best time to release a movie and what initial investment amount is requred if Microsoft decide to creat movies in a specific genre.


#### Distribution of Profit Over Rating

![Distribution of Profit and Movie Rating](./img/top10.png)

After plotting the profit and rating together, it shows that they have no correlation, increasing profit not necessarily lead to higher profit.

![Distribution of Number of Votes and Average Rating](./img/top10.png)

Similarly to the previous distribution, the number of votes and average rating also not shows any correlation.  

#### Top 10 movies

![Top 10 grossing movies](./img/top10.png)

The above diagram shows the top 10 movies by worldwide grossing.
Avangers: Infinity War came out as the top grossing movie with worldwide revenue a little over 2 billion $. Then followed by Jurassic World as second with around 1.6 billion $, and finally on the third place The Avangers with the total grossing of 1.5 billion.
It worth to mention that there are two animation movies in the top 10 list, Frozen and the Incredibles 2, with a total gross of 1.25 billion $. This need to be taken into consideration when selecting the target audience, as movies targeted for kids make significant amount of revenue.

![Genre Ditribution of Top Grossing Movies](./img/genres_for_top_10.png)

These top 10 grossing movies distributed over 3 genres. Action, Animation and Fantasy.


#### Most profitable genres

![Top 10 grossing movies](./img/profitability.png)

From all the movies between 2010 and 2019, 63 % of them were profitable, and almost 37% of them cost more money to make than the gross revenue the film earned.
Most profitable genres to make movies are the following: Action, Animation, Fantasy, Adventure and Romance. 

Important to note that my chart shows the History had 100% profitability, however the dataset I used only had two History movies and they both turned out to be profitable.
Besides this there are significant amount of movies in each genre, they represent the profitability for the rest of the genres correctly.


#### Runtime

![Average Runtime per Genre](./img/runtime.png)

Optimal length for Action movies is 133 mins, Animation is around 95 mins, for Fantasy - 119, Adventure - 139 mins and  Romance is 110 minutes.


#### Best time to release a movie

![Number of Movie Releases by Month](./img/numofrelease.png)


Best time to release a movie are falling into the following months: March, September, October and December. This shows some seasonality. From my pesonal experience in each month there are several holidays or school breaks when more people have time to go to the moves, this could explain that increased number of movie releases.

On the graph there are noticable drops in the number of film releases in certain month. I would recomment to avid releaseing movies in these month to maximise the gross revenue.
The month should be avoided are January, February, May, June and July


### Next Steps


If I had more time I would expand the analysis to see how successful are the original movies or those which are based on book adaptation.
Besids the box office revenue, lot of movies make extra revenue through merchandising and licencing. Looking at that information would might change the top 10 movies or their genre distribution. 
In addition to these it would also worth to check the actors / actresses in movies where the initial investment is on the lower side but the Return of Investment is high, might show some patterns for some A listers who attract more people to the movies.


### Recommendations


Based on the analysis the following should be taken into consideration before entering the movie market:

Most profitable genres to make movies are : 
     Action
     Animation
     Fantasy
     Adventure
     Romance

Optimal length for top genres:
    Action movies is 133 mins 
    Animation is around 95 mins
    Fantasy - 119 mins 
    Adventure - 139 mins
    Romance - 110 mins

Best time to release a movie: 
    March
    September 
    October 
    December

Month to avoid release: 
    January 
    February 
    May 
    June
    July

In average for each genres the following initial investments are required if the company decides to make a movie in these catergories.
The amount is in million $.

![Average Initial Investment per Genres](./img/budget.png)

This concludes my exploratory data analysis of IMDB data.

### Thank you.




5. `.gitignore`
   * A file called `.gitignore` at the root of the repository directory instructs Git to ignore large, unnecessary, or private files
     * Because it starts with a `.`, you will need to type `ls -a` in the terminal in order to see that it is there
   * GitHub maintains a [Python .gitignore](https://github.com/github/gitignore/blob/master/Python.gitignore) that may be a useful starting point for your version of this file
   * To tell Git to ignore more files, just add a new line to `.gitignore` for each new file name
     * Consider adding `.DS_Store` if you are using a Mac computer, as well as project-specific file names
     * If you are running into an error message because you forgot to add something to `.gitignore` and it is too large to be pushed to GitHub [this blog post](https://medium.com/analytics-vidhya/tutorial-removing-large-files-from-git-78dbf4cf83a?sk=c3763d466c7f2528008c3777192dfb95)(friend link) should help you address this

You wil submit a link to the GitHub repository on Canvas.

See the [Grading](#grading) section for further explanation of how the GitHub repository will be graded.

For further reading on creating professional notebooks and `README`s, check out [this reading](https://github.com/learn-co-curriculum/dsc-repo-readability-v2-2).
