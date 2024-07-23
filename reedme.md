## Business Overview 

In a professional data engineering career, you have various scenarios where data gets collected every day. The data can be processed once a day, i.e., batch processed, and the processed results are stored in a location to derive insights and take appropriate action based on the insights. In this project, we will learn how to implement this using AWS services. We will take a day’s worth of data related to Wikipedia, and we will perform batch processing on it. 

 ## Aim 

In this project, you will learn to do batch processing using AWS services: S3 as storage,  EMR as processing cluster, and Athena for querying the processed results. 

 

## Data Pipeline 

The sample data will be put into a folder in the S3 bucket. We will have PySpark code that will run on the EMR cluster. This code will fetch the data from the S3  bucket, perform filtering and aggregation on this data, and push the processed data back into  S3 in another folder. We will then use Athena to query this processed data present in S3. We will create a table on top of the processed data by providing the relevant schema and then use  ANSI SQL to query the data. 




##### process wikipedia data on a daily basis to get the following two datasets:

* Data set aggregated by "channel".

* Data set containing the records filtered by the following conditions:

   * isRobot: False

   * countryName:  United States
