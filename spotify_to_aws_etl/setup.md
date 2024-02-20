# ETL Setup Instructions

## 1.Create a bucket in S3
This is the folder structure in the S3 bucket I created:
/discover_weekly: Main folder in bucket
/raw_data: Raw data is stored here
* to_process: When the data extraction function is invoked, data extracted from the API will be stored here
* processed: When the transformation function is invoked, files in to_process folder will be copied to this folder and the file in to_process will be deleted. We are just moving data from one folder to another.
/transformed_data: These 3 folders will contain the transformed dataset where basic cleaning and transformation have been applied.
* /album_data
* /artist_data
* /song_data
