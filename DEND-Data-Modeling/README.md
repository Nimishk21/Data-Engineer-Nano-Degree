#### Context:
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

#### Project Goal: 
We want to create a Postgres Database Schema and ETL pipeline to optimize queries for song play analysis.

#### Project Description:
We have to model data using Postgres and build an ETL pipeline using Python.We will need to define fact and dimension tables for a star schema for a particular analytic focus and write an ETL pipeline that transfers data from files in two local directories into tables using python and SQL

#### Data:
Song dataset: all json files are nested in subdirectories under /data/song_data
Log dataset: all json files are nested in subdirectories under /data/log_data

#### Database Schema:
We will be using star schema for this project.There will be one fact table containing all the measures associated to each event and 4 dimension tables,each with primary key referencing from fact table.

## Fact table: songplays records in log data associated with song plays

## Dimension table:
users in the app
songs in music database
artists in music database
time: timestamps of records in songplays broken down into specific units

## Why to use relational database:
1.we know before-hand the sctructure of the data(json) we need to analyze, and where and how to extract and transform each field
2.Data we need to analyze is not big enough


#### Project Structure:
## Following are the files that are used:
1.sql_queries.py contains all your sql queries, and is imported into the files bellow.
2.create_tables.py drops and creates tables. You run this file to reset your tables before each time you run your ETL scripts.
3.test.ipynb displays the first few rows of each table to let you check your database.
4.etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables.
5.etl.py reads and processes files from song_data and log_data and loads them into your tables

## following are the steps that needs to be followed:
-Wrote DROP, CREATE and INSERT query statements in sql_queries.py
-Run create_tables.py in console
-Used test.ipynb Jupyter Notebook to interactively verify that all tables were created correctly
-Followed the instructions and completed etl.ipynb Notebook to create the blueprint of the pipeline to process and insert all data into the tables
-Once verified that base steps were correct by checking with test.ipynb, complete etl.py program.
-Run etl in console, and verify results

