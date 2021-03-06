# Project Name:

Microsoft Movie Analysis

# Project Description:

An analysis of movie and video game data to generate a few recommendations for Microsoft's new interest in movie making.

# Data Used:

Data comes from 4 different files:
* IMDb (x2)
* Box Office Mojo
* The Numbers

And Wikipedia:
* https://en.wikipedia.org/wiki/List_of_best-selling_Xbox_One_video

**Data can be found in the zippedData folder.**

### When is the best time to release a movie?

For this analysis I used data from The Numbers. There were no missing values, but I did have to convert the $ amounts to integers and change the dates to datetime. After that analysis was fairly straight-forward. 

I looked at the month that has the most new releases. I wondered if that was just a popular month to release a movie, or if the movies were released then because they would make more money.
I analyzed the release month against it's gross product (domestic and worldwide). I also checked the average worldwide gross by the month the movie was released in. After not being able to see, I eliminated about 400 of the highest grossing movies to look carefully at the analysis.


**Key Findings:**

More movies are released in December than any other month.
Movies released it December can make a lot of money.
However, the average movie released in May and June make more money than ones released in other months once the outliers are taken into account.

Interestingly, the more outliers (~600 instead of 400) that are removed, the less successful May gets. June, July and November really begin to shine with December not far behind. May shrinks to be on par with most other months.

The image below shows May and June having the largest span when measuring a movie's worldwide gross by it's release month.

![most profitable_films](images/Month-average.png)

### What are the top 15 highest grossing films and which studios made them?

To accomplish this analysis, I needed to merge three different files together.
While merging, I was doing some data cleaning. The data types were correct, but there were quite a few missing values and duplicates. 

After cleaning those out, I was able to graph the 15 highest grossing movies (based on domestic gross) and see what their average review. Then I looked at the studios that made the movies in that top 15.

The image below shows the average reviews for the top 15 highest domestic grossing movies.

![average_ratings_top_15](images/avg_ratings.png)

**Key Findings:**

Three of the movies had average reviews of 8 or higher. Most of the movies were between 7 and 8. The lowest rated film went to Jurassic World: Fallen Kingdom at 6.2.

Of the 15 highest grossing movies, BV (AKA Buena Vista AKA Disney) made 10 of them. If Microsoft is looking for some guidance on how to make a hit, it could take a lesson from Disney.

### Which genre could generate the most profit?

In this analysis, I used a file that I had already cleaned up (from the first analysis). I calculated the return on investment (or ROI) to see where the profits were. Some movies were on this list that had been released, but did not have any data. I wasn't interested in that so I removed any entries that had "0" in the "worldwide gross" column. I also filtered out movies that were made more than 10 years ago. I wanted to be looking at more recent data that wouldn't skew any results.

I merged the file that had the genre information and again cleaned the data by removing the duplicates. From here I had to split the genres into separate columns.

**It is important to note here that if there were multiple genres, the genres were listed in alphabetical order and not by their primary category. Therefore, the analysis was done on all three columns to see the whole picture.**

An analysis was done to see if the genres at the end of the alphabet would increase because they were not listed first. Then trends over the 3 visualizations were noted.

Taking it a step further, I then looked at the total ROI for each genre and the average ROI for each genre.

**Key Findings:**

Mystery and Horror are great genres if you are looking to make the biggest profit. Animation also ranks high on all of the graphs. Showing that whether animation is the only genre listed, or if it fits in with multiple genres, it tends to make a decent profit.

The image below shows the genres, and their respective ROI's.

(Some movies had one or more than one listed genre. Thus, three separate charts.)

![genres_and_roi](images/genre--roi.png)

### How do Movies and Microsoft Go Together?

I wanted to think about how Microsoft's successful video games could be leveraged to create a film. I used data from Wikipedia and looked specifically at the top selling Xbox One games.

The data was fairly clean, but I still had to adjust column names and change the data types for the columns release date and copies sold. 

Once the columns were in order, I looked at how many of the top selling games were made my Microsoft. I added a column to show if the game was or was not made by Microsoft Studios. With that I was able to graph the copies sold based on the year it was released while also showing if it was made by Microsoft or not. I also ranked Microsoft Studios games by their highest sales and the year they were released. 

**Key Findings:**

Of the 32 games, Microsoft has made 12 of them. Microsoft had some okay sales that have been big hits, and you can see that the trend of games made by Microsoft is going up. 

Another graph shows the game that sold the most copies was also newest. This game, or other top selling games could be inspiration for Microsoft to create an instant hit and generate more revenue back into their video game market.

The graphic below shows the 32 top selling Xbox One games ranked by their year of release and the copies sold. The color difference shows if the game was or was not made by Microsoft Studios.

![Microsoft_sales_img](images/Microsoft-top-selling.png)

# Summary:

After an analysis of data files about previous movie sales and video game sales, I came to the following conclusions:

* June is a good month to release a film
* Disney made two-thirds of the top 15 grossing movies
* Mystery / Horror / Thriller movies generate the most return on investment
* Microsoft can look at their top selling Xbox games for film inspiration and increase revenue in multiple markets
