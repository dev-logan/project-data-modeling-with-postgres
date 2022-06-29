## Introduction
Sparkify is a music streaming app that wants to analyze the data it collects about songs and user activity.
The ETL pipeline defines fact and dimension tables, and uses Python and SQL to transfer data from files in two local directories to Postgres tables.

## Database Schema
### Fact Table
1. songplays - records in log data associated with song plays i.e. records with page NextSong
    * songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
    
### Dimension Tables
1. users - users in the app
    * user_id, first_name, last_name, gender, level
2. songs - songs in music database
    * song_id, title, artist_id, year, duration
3. artists - artists in music database
    * artist_id, name, location, latitude, longitude
4. time - timestamps of records in songplays broken down into specific units
    * start_time, hour, day, week, month, year, weekday

## How to run
Executable codes for other files are included in **etl.ipynb**, so you can do the necessary work by running the entire code.

## File Description
**create_tables.py** creates a database, creates tables, and drops them.

**etl.py** contains the core codes for ETL work. It collects data of all files in each path and organizes them into a database.

**sql_queries.py** contains all SQL queries necessary for the above operation.