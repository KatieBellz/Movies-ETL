## Module 8 Challenge ETL
The project task is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables.

## Summary of Tasks
Deliverable 1: Write an ETL Function to Read Three Data Files

* Filename: ETL_function_test.ipynb

* Created extract_transform_load() function

* Extracts data from three files: kaggle metadata and MovieLens ratings CSV (included in ignore file) files and raw wiki movie data json file

* Returns dataframe of each datasource


## Deliverable 2: Extract and Transform the Wikipedia Data

* Filename: ETL_clean_wiki_movies.ipynb
* Reuse extract_transform_load() function from Deliverable 2
* Created clean_movie() function to fix columns or data designating language, and change column names
* Created parse_dollars function within clean_movie() function
* Extract only movies
* Extract and create IMDB_ID
* Clean Box Office, Budget, Release Date, Running Time columns
* Dropped old columns
* Returns dataframe of each datasource


## Deliverable 3: Extract and Transform the Kaggle data

* Filename: ETL_clean_kaggle_data.ipynb
* Repurpose all functions from Deliverable 2
*Added functionality to clean Kaggle data
* Added merging of wiki and Kaggle dataframes
* Dropped unnecessary columns
* Filling in missing Kaggle data
* Filter and rename columns
* Transformed and merged ratings dataframe

## Deliverable 4: Create the Movie Database

* Filename: ETL_create_database.ipynb and config.py (included in ignore file)
* Reuse deliverable 3 code
* Added filepath parameters to the extract_transform_load() function and removed returning any dataframes
* Updated extract_transform_load() function to make a connection to the database and insert/update the "movies" and "ratings" tables in the "movie_data" database

## Resources

* Data Source: movies_metadata.csv, ratings.csv, wikipedia-movies.json
* Software: Python 3.9.12, Jupyterlab 3.3.2, Pandas 1.4.2, numpy 1.21.5, sqlalchemy 1.4.32, psycopg2-binary 2.9.3
