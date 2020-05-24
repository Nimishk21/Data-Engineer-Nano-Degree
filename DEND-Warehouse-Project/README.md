#### Context:
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

#### Project Goal: 
We want to create a Postgres Database Schema and ETL pipeline to optimize queries for song play analysis.

#### Project Description:
Application of Data warehouse and AWS to build an ETL Pipeline for a database hosted on Redshift Will need to load data from S3 to staging tables on Redshift and execute SQL Statements that create fact and dimension tables from these staging tables to create analytics

#### Data:
Song dataset: s3://udacity-dend/song_data Log Data Path 
Log dataset:  s3://udacity-dend/log_data 
Log Data JSON Path  s3://udacity-dend/log_json_path.json

## Fact table: songplays records in log data associated with song plays
## Staging tables:1.Staging_events 2.staging_songs
## Dimension table:
users in the app
songs in music database
artists in music database
time: timestamps of records in songplays broken down into specific units

#### Project Structure:
## Following are the files that are used:
1.sql_queries.py contains all your sql queries, and is imported into the files below.
2.create_tables.py is where you'll create your fact and dimension tables for the star schema in Redshift.
3.etl.py is where you'll load data from S3 into staging tables on Redshift and then process that data into your analytics tables on Redshift.

## Create Table Schema

1.Write a SQL CREATE statement for each of these tables in sql_queries.py
2.Complete the logic in create_tables.py to connect to the database and create these tables
3.Write SQL DROP statements to drop tables in the beginning of create_tables.py if the tables already exist. This way, you can run create_tables.py whenever you want to reset your database and test your ETL pipeline.
4.Launch a redshift cluster and create an IAM role that has read access to S3.
5.Add redshift database and IAM role info to dwh.cfg.
6.Test by running create_tables.py and checking the table schemas in your redshift database.

## Build ETL Pipeline
1.Implement the logic in etl.py to load data from S3 to staging tables on Redshift.
2.Implement the logic in etl.py to load data from staging tables to analytics tables on Redshift.
3.Test by running etl.py after running create_tables.py and running the analytic queries on your Redshift database to compare your results with the expected results.
4.Delete your redshift cluster when finished.

## following are the steps that needs to be followed:
1.We will need to fill parameters of cluster in dwh.cfg(I am using the same clusters parameters created from the previous excerise)
2.We need to design tables and schemas in sql_queries script and run it.
3.Run the etl script to extract data from the files in S3,stage it in redshift and finally store it in dimensional tables.
4.Verify the tables and data in it by quering in query editor.