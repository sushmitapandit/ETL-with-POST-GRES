# Data Modeling with Postgres & ETL Pipeline for Sparkify

Sparkify is a music streaming app Company. They have been collecting data on songs and user activity. Now they want to analyze using this data particularly to find out

  - Which songs users are listening to

## Data
Currently, the company do not have an easy way to query their data, their data resides in

  - directory of JSON **logs** on user activity on the app
  - directory with JSON metadata on the **songs** in their app

## Database creation and ETL data pipeline creation
We are creating database schema on postgres servers and creating a pipeline to load data on the database.

### We will do these things
  - Create Fact Table (songplays) and Dimension Tables (users, songs, artists and time) 
  - extract the data from all the json log files and json song files and load them on Pandas Data frame. Further, extracting these datas on data frames songplays,users, songs, artists and time
  - utilising sql queries and inserting data from the dataframes into the respective tables

### Files used 
- sql_queries - Contains drop, create and insert into tables queries
- create_tables - creates sparkify DB and then utilises queries from sql_queries.py file to drop and create tables.
- etl.ipynb  - connects to JSON file and loads data into data frame and then test insertions on to the respective db tables
- etl.py contains the complete etl script along with all the scripts from etl.ipynb
- test.ipynb uses magic commands to help test the etl pipelines if its working.

### Observations
- While we processed data, we found 72 files in data/song_data and 30 files in data/log_data




