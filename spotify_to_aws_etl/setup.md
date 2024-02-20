# ETL Setup Instructions

## 1.Create a bucket in S3

In the S3 bucket I set up, the structure is organized as follows:

<b>discover_weekly</b>: This is the primary directory within the bucket.</br>
<b>raw_data</b>: This directory holds the initial data gathered.</br>
<b>to_process</b>: Data fetched from the API is stored here upon triggering the data extraction function.</br>
<b>processed</b>: After the transformation function runs, the data from the to_process directory is moved here, effectively transferring files from one location to another while the originals in to_process are removed.</br>
<b>transformed_data</b>: This directory is segmented into three subdirectories, each dedicated to holding datasets that have undergone basic cleaning and structuring.
</br>
<b>album_data</b>
</br>
<b>artist_data</b>
</br>
<b>song_data</b>
</br>
