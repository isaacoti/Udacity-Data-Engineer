Purpose of database
This aim of this database is to serve as a respository for Sparkify's data on songs and user activity. Implementing the data model using an ETL pipeline in Redshift would help to optimize queries for Sparkify's song play analysis.

Database schema design and ETL pipeline
I defined fact and dimension tables for a Star Schema. Using ETL pipeline modelled with python and SQL, data is transferred from the files into the fact and dimension tables. Database Design is optimized for easy access to information, having used a star schema with well defined dimension tables. ETL pipeline is also designed to be intuitive and organised to read json files and parse information to tables. Such design ensured information is accessed within a practical time frame.

Fact Table: songplays records in log data 
Dimension Tables: users in the app, songs in database, artists in database, time: timestamps of records in songplays 


Project structure
This project includes the following files:
1. create_table.py that has the fact and dimension tables for the schema
2. etl.py where data gets loaded from S3 into staging tables on Redshift 
3. sql_queries.py containing the SQL statements used by etl.py, create_table.py and analytics.py.
4. README.md (this file).

How to run the scripts
1. Setup AWS Redshift Cluster and IAM role.
2. Run the create_tables script to set up the database tables.
3. Run the etl script to extract data from the files in S3, stage them in redshift and store them in the dimensional tables.








