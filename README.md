Door2Door - Data Engineering Tech Assessment

--- Challange

We would like to ask you to develop a solution that:
1. Fetches the data from the bucket on a daily basis and stores it on a data lake;
2. Processes and extracts the main events that occurred during operating periods;
3. Store the transformed data on a data warehouse. The data warehouse should be SQL-queriable

--- Technical assumptions

• The fetching process should only get data from a certain day on each run and should run every day;
• Files on the ”raw” S3 bucket can disappear but we might want to process them differently in the
future;

• No need to answer the question stated in the introduction;
• If your solution is setup to run locally, it must be containerized;
• There is no need for paid, expensive and highly performant data warehouses. You can use a ”standard”
SQL database.

--- Bonus points

• Sketch how you would set up the application on the cloud (AWS, GCP, etc);
• It is encouraged to simplify the data by a data model on the data warehouse layer.
