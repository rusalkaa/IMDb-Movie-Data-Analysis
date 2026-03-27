# IMDb-Movie-Data-Analysis
This is my very first Power BI project. I used an IMDb dataset to explore how movie ratings change based on their genres and release years. My goal was to practice data cleaning and basic visualization.

## What I Did?
The raw dataset was a bit messy. Before making any charts, I used Power Query to clean the data:
- **Simplified Genres & Directors:** Movies often had multiple genres (like "Action, Adventure, Sci-Fi"). To avoid messing up the data model and calculations, I split these columns by the comma delimiter and kept only the Primary Genre and Primary Director.
- **Cleaned Text:** Removed weird characters (like `*`) from movie titles using the "Replace Values" feature without deleting the actual rows.
- **Created Categories:** I wrote a custom rule to group movies into "Short", "Normal", and "Very Long" categories based on their runtime minutes.

## What I Found?
- **Ratings are dropping over time:** My line chart shows a clear downward trend in average movie ratings from the 1920s to today. Why? Back then, there were fewer movies, making each release feel special and impactful. Today, the market is flooded with endless movies. Audiences have much higher expectations, endless options to compare, and are simply harder to impress.
- **Top Genres:** Westerns and Documentaries actually have the highest average ratings in this dataset, scoring much higher than popular genres like Action or Thriller.

## The Dashboard
Here is a screenshot of my final Power BI dashboard:
![Power BI Dashboard](imdb_movies_v1.png)

## Update v2.0: From Static to Interactive Dashboard
For the second version of this project, my goal was to turn the static charts into an interactive "Executive Dashboard." I wanted the user to explore the data themselves, rather than just looking at a fixed report. 

## What I did? 
- **Slicers:** I added filters for Release Year, Genre, and Runtime Categories. Now, if you select "Action," the whole dashboard instantly updates to show only Action movie trends.
- **Matrix:** I created a matrix to see which directors are actually the best. Why? Because looking only at "Average Rating" is a trap. A director with only one movie that scored 10/10 shouldn't rank higher than a master who directed 30 great movies. So, I put "Avg. Rating" and "Total Movies" side by side, and filtered out anyone with fewer than 10 movies.

## v2.0 Dashboard
![Power BI Dashboard](imdb_movies_v2.png)


