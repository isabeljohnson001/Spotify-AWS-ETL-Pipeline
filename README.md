# Spotify Data Engineering Project with AWS

This project demonstrates the development of an ETL (Extract, Transform, Load) pipeline using Python and AWS services to extract  extracts artist, album, and song information from Spotify's "Discover Weekly" playlist,which updates every Monday with 30 personalized songs for each user. he process includes pulling data from the Spotify API, modifying it to make it ready for analysis, uploading the adjusted data to Amazon S3, and then accessing this data for queries through Amazon Athena, with the use of AWS Glue for managing catalogs and metadata.

Objective
The main goal is to leverage the Spotify API and AWS services to build an ETL pipeline that processes data from the "Discover Weekly" playlist, which updates every Monday with 30 personalized songs for each user.

Architecture Overview

Tools and Services Used
Python: For scripting the ETL process.
AWS S3: To store raw and processed data.
AWS Lambda: To run Python code for data extraction and transformation.
AWS CloudWatch: For monitoring and logging.
AWS EventBridge: To schedule data extraction.
AWS Glue: For data cataloging and running crawlers to infer schema.
Amazon Athena: To query transformed data.
Pre-requisites
Spotify API credentials (Client ID and Client Secret).
AWS account setup with permissions for Lambda, S3, Glue, and Athena.
Python environment for initial script development.
ETL Process
Extract
Data is extracted from the Spotify API using the Spotipy library and deployed via AWS Lambda. An EventBridge trigger is set up to automate data extraction weekly.

Transform
AWS Lambda triggers a transformation process when new data is added to the S3 bucket. This process cleans and prepares the data for analysis, organizing it into structured formats for artists, albums, and songs.

Load
AWS Glue crawlers are used to infer schema and organize metadata in the Glue Data Catalog. Data can then be queried using Amazon Athena.

Data Model
(Provide a data model diagram or description here)

Setup and Configuration
Step 1: Lambda Layer for Spotipy
Create a Lambda layer for the Spotipy library to use with your Lambda functions.
Step 2: Environment Variables
Configure environment variables for Spotify API credentials in the Lambda function settings.
Step 3: S3 Bucket Structure
Organize your S3 bucket with folders for raw data, processed data, and transformed data.
Steps to Deploy the ETL Pipeline
(Include detailed steps for setting up the ETL pipeline, configuring triggers, and deploying code.)

Additional Improvements
Setup a dashboard for data visualization, potentially using AWS Quicksight or other BI tools.
Explore handling of special characters (like commas) in data extraction and transformation processes.
Questions & Research
Impact of running the crawler without data changes.
Handling values with commas in AWS Glue.
