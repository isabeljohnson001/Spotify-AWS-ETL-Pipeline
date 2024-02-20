# Spotify Data Engineering Project with AWS

This project demonstrates the development of an ETL (Extract, Transform, Load) pipeline using Python and AWS services to process data from Spotify's "Discover Weekly" playlist. The pipeline extracts artist, album, and song information, transforms this data for analysis, and loads it into Amazon S3, with querying capabilities via Amazon Athena.

Tools and Services Used - Python,AWS S3,AWS Lambda,AWS CloudWatch,AWS EventBridge,AWS Glue,Amazon Athena

### Pre-requisites

- [Spotify API](#spotify-api) credentials setup (Client ID and Client Secret)
- AWS account setup with permissions for Lambda, [S3 folder stucture](#S3-Bucket-folder-structure), Glue, and Athena.
- Python environment for initial script development.

### Architecture Overview

![Architecture Diagram](spotify_to_aws_etl/Spotify-AWS-ETL.png)

### Pre-requisites Setup

### 1. Spotify API

For interacting with the Spotify API, it's necessary to first secure authentication credentials. This involves setting up an account on the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/)
 and registering your application there. Upon registration, we 'll recieve a pair of api credentials: a Client ID and a Client Secret, which are essential for application's authentication and authorization processes.


### 2.S3 Bucket folder structure

In the S3 bucket I set up, the structure is organized as follows:
```
discover_weekly/
├── raw_data/
│   ├── to_process/       # Data from the API is saved here upon extraction
│   └── processed/        # Data from 'to_process' is moved here after transformation
└── transformed_data/
    ├── album_data/       # Contains transformed album data
    ├── artist_data/      # Contains transformed artist data
    └── song_data/        # Contains transformed song data


  
