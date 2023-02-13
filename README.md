Door2Door - Data Engineering Tech Assessment


--- Challange

We would like to ask you to develop a solution that:
1. Fetches the data from the bucket on a daily basis and stores it on a data lake;

!! For this point i used the transfer service between Amazon S3 to Google Cloud Storage to fetch the JSON files into the datalake. 

2. Processes and extracts the main events that occurred during operating periods;

!! To Process and Extract the data and events I pulled all the JSON files into Bigquery and unnested the data into 
organization_id, captured_at, captured_on, event, data_id, data_location_at, data_location_longitude, data_location_latitude Columns.


3. Store the transformed data on a data warehouse. The data warehouse should be SQL-queriable

!! The full amounts of data is then stroed into a Bigquery Table to make it easily accessible and SQL-queriable.

--- Technical assumptions

4. The fetching process should only get data from a certain day on each run and should run every day;
!! All Files are fetched daily through the Amazon S3 and Cloud Storage Transfer  Service

5. Files on the ”raw” S3 bucket can disappear but we might want to process them differently in the
future;

!! Through the transfer process into Cloud Storage the data is automatically saved there but as an added point of security, everytime the raw data is pulled from the Google Bucket into Bigquery the data is saved in a table. 

6. What is the average distance traveled by our vehicles during an operating period?;
!! BI Dashboard - https://lookerstudio.google.com/u/1/reporting/e99a38e0-c02a-4e21-a7e7-fa6edbe23c0a/page/TJCFD/ 

!! Used only the two farthest points of Geo Data to calculate distance through the Haversine formula

--- Bonus points

7. Sketch how you would set up the application on the cloud (AWS, GCP, etc);


!! Sketch made through C4 Architecture Diagrams and is saved as a JPG image in the repo and email attachment.

8. It is encouraged to simplify the data by a data model on the data warehouse layer.
!! The data is simplifyed through the process of extracting it, its also activated for use through a dashboard.
Some joins in the dashboard are modeled on Timestamp and ID columns.
