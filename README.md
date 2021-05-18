# Project Scope

The Sparkify start up needs the best way to compare users experiences data with their goals. Primarily, all data are in logs (json files) that it is not the best format to extract business information. This project reads data from data logs and metadata to insert then in an postgres Database; 


# Instructions on how to run the files 

* The first step is open a python terminal;
* The second step is execute the sql_queries.py to create all project tables;
* The third step is execute etl.py to read all data logs and load on postgres tables;

# Data Model Schema

The data model schema is a star schema and it has one fact table (songplays) and four dimension tables (songs, users, artists and time);

* Fact table songplays: columns (songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent); 
* Dimension table songs: columns (song_id, title, artist_id, year, duration);
* Dimension table users: columns (user_id, first_name, last_name, gender, level);
* Dimension table artists: columns (artist_id, name, location, latitude, longitude);
* Dimension table time: columns (hour, day, week, month, year, weekday);

# ETL Pipeline that led to the Data Model Schema

The ETL Pipeline has two functions to read data from json files: process_song_file and process_log_file. In the both functions is used Pandas dataframe to handle and transform data and insert into Postgres database. 

# Files in the repository

* CREATE_TABLES.ipynp: notebook file to create all database tables;
* create_tables.py: code file to create all database tables;
* etl.py: code file to read json log files and ingest then into Postgres database; 
* sql_queries.py: code file has all SQL codes;
* test.ipynb: notebook file to execute tables query and view tables content.

  



