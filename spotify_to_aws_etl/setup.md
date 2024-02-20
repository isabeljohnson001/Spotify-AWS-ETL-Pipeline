# ETL Setup Instructions

## 1.Create a bucket in S3

In the S3 bucket I set up, the structure is organized as follows:

discover_weekly: This is the primary directory within the bucket.
raw_data: This directory holds the initial data gathered.
to_process: Data fetched from the API is stored here upon triggering the data extraction function.
processed: After the transformation function runs, the data from the to_process directory is moved here, effectively transferring files from one location to another while the originals in to_process are removed.
transformed_data: This directory is segmented into three subdirectories, each dedicated to holding datasets that have undergone basic cleaning and structuring.
album_data
</br>
artist_data
</br>
song_data
</br>
