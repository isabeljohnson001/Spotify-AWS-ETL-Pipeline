# ETL Setup Instructions
## Table of Contents
1. [Creating a Lambda Layer](#creating-a-lambda-layer)
2. [Configuring the Lambda Function](#configuring-the-lambda-function)
3. [Deployment and Testing](#deployment-and-testing)
### 1. Spotify API

For interacting with the Spotify API, it's necessary to first secure authentication credentials. This involves setting up an account on the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/)
 and registering your application there. Upon registration, we 'll recieve a pair of api credentials: a Client ID and a Client Secret, which are essential for application's authentication and authorization processes.


### 2.Create a bucket in S3

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
```
### 3.Create a bucket in S3



## Creating a Lambda Layer
Content for creating a Lambda layer...

## Configuring the Lambda Function
Details on configuring the Lambda function...

## Deployment and Testing
Instructions for deployment and testing...
