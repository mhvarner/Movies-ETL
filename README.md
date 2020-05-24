# Movies-ETL
## Challenge
The ETL module was extremely difficult. I had to rewrite my code over and over for each function to run an tried to automate where I saw fit. I believe the pseudocode for my ETL notebook best explains what I want the user of the notebook to do: Pseudocode for challenge:

For user of this code, you will need to use exact columns from the original csv files, and  add in the new
data of the ratings.csv, movies_metadata.csv, and json file (which was merged with the movies_metadata).
Then, you will need to delete the "rating_empty = ratings[0:0]" and "movies_df_empty = movies_df[0:0]" in order for the datasets to render, instead of being blank. If errors appear, make sure the data has the same number of columns
as errors occur when the columns are not matching from different csv files. Also make sure name of the new csv files
are the same as the csv files presented here; if not change the name of the new csv files. I created a
few try-except blocks as well to deal with possible errors. At the bottom, that code imports the rating file rows into PGAdmin, as I am sure the new datasets applied will be just as large as the original dataset. The code left over from the module I deemed necessary for the new data to render like the old data did, as the code will come back with different
results and variables. I created a new database for the challenge for the datasets to be loaded into called
movie_data_challenge and named the two tables "Movies" (which includes both the movies_metadata.csv
and the wikipedia.movies.json data) and "Ratings" which includes the four original columns of the massive ratings.csv
The rating_counts transforms the data into columns of ratings and indexes the movie title to show the movies at the
far left of the table. If the user wanted to use that table setup, all that would be needed is to change the 
"rating_empty = ratings[0:0]" to rating_counts_empty = ratings[0:0] and change "rating_empty.to_sql(name='Ratings', con=engine)" to rating_counts_empty.to_sql(name='Ratings', con=engine). This would render a more succinct and readable table. Once you run this code in this notebook, you will want to refresh the new database created and the data will follow.

This code analyzes what I have done and gives the user the exact steps necessary to be able to use it. I had to create a new database which separated my module data from my challenge data.
All in all, this was the most difficult challenge to date.
