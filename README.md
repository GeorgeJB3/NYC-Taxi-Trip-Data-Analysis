# NYC Taxi Trip Analysis

## Description

This project is to analyse NYC taxi trips from September 2024 to December 2024. 
I got the data from https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page using only the Yellow Taxi Trip Records.



## How I would scale and optimise this code to include data all the way from 2009

### Storage

To make storage more efficieient I would use a clud service such as AWS. 
Store csv files in an S3 bucket and extract to begin the clean and transformation. 
Once complete load into a data warehouse such as Redshoft or Snowflake.

### Automation

There are various ways to automate tasks. Apache Airflow is an orchestration tool used to set schedules for a Directed Acyclic Graph (DAG) to execute Python and sql scripts. 
Airflow has dependancy checks, so once data lands in the source bucket, a DAG is triggered to start the ETL process.

### Data Warehouse

I would use a Data warehouse such as Snowflake to store the clean data. 
This would provide a quick and effiecient platform to query large volumes of data.

### Data Modelling

I would use a star schema with the fact tables being used for trips and fares. Then Dimension tables for information such as time, area, route and driver. 
This would allow for effieicient querying and analysis over the large amount of data. This would improve data quality and scalability. 
If a customer requests for there data to be removed it would be an easy task as the data is orgaised and traceable.
