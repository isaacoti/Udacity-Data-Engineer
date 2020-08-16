Purpose of database
The aim of this database is to serve as a respository for Sparkify's data on songs and user activity. Implementing the data model on Amazon S3 using AWS Cluster and Spark would help to optimize queries for Sparkify's song play analysis.

Data schema

Fact table
TABLE songplays
start_time: timestamp 
userId: string 
level: string 
sessionId: long 
location: string 
userAgent: string 
song_id: string 
artist_id: string 
songplay_id: long 


Dimension tables
TABLE users
firstName: string 
lastName: string 
gender: string 
level: string 
userId: string 


TABLE songs
song_id: string 
title: string
artist_id: string 
year: long 
duration: double 


TABLE artists
artist_id: string 
artist_name: string 
artist_location: string 
artist_latitude: double 
artist_longitude: double 

TABLE time
start_time: timestamp 
hour: integer 
day: integer 
week: integer 
month: integer 
year: integer 
weekday: integer 