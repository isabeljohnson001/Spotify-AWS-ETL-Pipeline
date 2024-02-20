# Spotify Data Engineering Project with AWS

This project demonstrates the development of an ETL (Extract, Transform, Load) pipeline using Python and AWS services to process data from Spotify's "Discover Weekly" playlist. The pipeline extracts artist, album, and song information, transforms this data for analysis, and loads it into Amazon S3, with querying capabilities via Amazon Athena.

## Objective

The main goal is to leverage the Spotify API and AWS services to build an ETL pipeline that processes data from the "Discover Weekly" playlist, which updates every Monday with 30 personalized songs for each user.

## Architecture Overview

![Architecture Diagram](path/to/your/architecture/diagram/image)

### Tools and Services Used

- <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg"  title="Python" alt="Python" width="40" height="40"/>&nbsp; **Python**: For scripting the ETL process.
- **AWS S3**: To store raw and processed data.
- **AWS Lambda**: To run Python code for data extraction and transformation.
- **AWS CloudWatch**: For monitoring and logging.
- **AWS EventBridge**: To schedule data extraction.
- **AWS Glue**: For data cataloging and running crawlers to infer schema.
- **Amazon Athena**: To query transformed data.
- **🛠  Languages and Tools :**
<br/>
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/csharp/csharp-original.svg"  title="C#" alt="C#" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg"  title="Python" alt="Python" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/r/r-original.svg"  title="R" alt="R" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/html5/html5-original.svg" title="HTML5" alt="HTML" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/css3/css3-plain-wordmark.svg"  title="CSS3" alt="CSS" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/react/react-original-wordmark.svg" title="React" alt="React" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL"  alt="MySQL" width="40" height="40"/>&nbsp;
</div>
<br/>

## Pre-requisites

- Spotify API credentials (Client ID and Client Secret).
- AWS account setup with permissions for Lambda, S3, Glue, and Athena.
- Python environment for initial script development.

## ETL Process

### Extract

Data is extracted from the Spotify API using the `Spotipy` library and deployed via AWS Lambda. An EventBridge trigger is set up to automate data extraction weekly.

### Transform

AWS Lambda triggers a transformation process when new data is added to the S3 bucket. This process cleans and prepares the data for analysis, organizing it into structured formats for artists, albums, and songs.

### Load

AWS Glue crawlers are used to infer schema and organize metadata in the Glue Data Catalog. Data can then be queried using Amazon Athena.

## Data Model

(Provide a data model diagram or description here)

## Setup and Configuration

### Step 1: Lambda Layer for Spotipy

- Create a Lambda layer for the Spotipy library to use with your Lambda functions.

### Step 2: Environment Variables

- Configure environment variables for Spotify API credentials in the Lambda function settings.

### Step 3: S3 Bucket Structure

- Organize your S3 bucket with folders for raw data, processed data, and transformed data.

### Steps to Deploy the ETL Pipeline

(Include detailed steps for setting up the ETL pipeline, configuring triggers, and deploying code.)

## Additional Improvements

- Setup a dashboard for data visualization, potentially using AWS Quicksight or other BI tools.
- Explore handling of special characters (like commas) in data extraction and transformation processes.
- 
![Python](URL_to_Python_icon)
![AWS S3](URL_to_AWS_S3_icon)
![AWS Lambda](URL_to_AWS_Lambda_icon)
![AWS Glue](URL_to_AWS_Glue_icon)
![Amazon Athena](URL_to_Amazon_Athena_icon)

