# Weather-Data-Analysis-Big-Data

This project involves the development of a Python-based data processing application to analyze weather data from the National Climatic Data Center (NCDC) records. In the first part, a Mapper and Reducer application is designed to calculate the average wind direction for each observation month from each year, with specific handling of missing and good-quality values. The second part extends the analysis to PySpark, where a Python application is implemented to determine the range of sky ceiling height for each USAF weather station ID, leveraging the distributed computing capabilities. These tasks contribute to a holistic understanding of weather patterns and conditions over time.

Continuing with the project's scope, the third part introduces a Mapper and Reducer application to extract USAF weather station ID and visibility distance data from NCDC records, subsequently writing this information into a text file. The fourth part shifts the data processing to Pig, where the text file is loaded, and the range of visibility distance for each weather station is calculated. Lastly, the fifth part utilizes Hive to load the text file and compute the average visibility distance for each USAF weather station ID. This multi-step approach showcases the versatility of different tools and frameworks in handling diverse aspects of weather data analysis, providing valuable insights for further research and decision-making.
 Yearly Temperature Analysis using Hadoop, Pig, and Hive
This repository contains the solution for the course project, which involves retrieving and analyzing temperature data from NCDC records using a combination of Hadoop, Pig, and Hive.

Project Overview:
The project is divided into three parts:

Python Application with Hadoop Streaming:

A Python mapper and reducer are developed to extract the year and temperature data from NCDC records.
The data is processed in Hadoop, and the results are written into an output file.
Data Processing with Pig:

The output file is loaded into Apache Pig to calculate the highest and lowest temperatures for each year.
Data Querying with Hive:

The output file is loaded into Hive to calculate the average temperature for each year.
Contents:
Python Mapper and Reducer Scripts: These scripts are used to extract and process temperature data in a Hadoop environment.
Execution Commands: Commands for running the Hadoop job, Pig script, and Hive queries are provided.
Output Files: Includes sample output of the Hadoop, Pig, and Hive queries.
Screenshots: Screenshots showing the creation of the output files and the final results from Pig and Hive queries.
Execution Steps:
Copy Data to HDFS:

hdfs dfs -copyFromLocal /home/student44/CourseProjectData /home/44student44/
Run Hadoop Job:

hadoop jar hadoop-streaming-2.9.0.jar -input /home/44student44/CourseProjectData -output /home/44student44/projectOutput -file temperature_map.py -mapper temperature_map.py -file temperature_reduce.py -reducer temperature_reduce.py
Pig Script Execution:

Load the data, group by year, and compute maximum and minimum temperatures.
Hive Queries:

Load the data into Hive and compute the average temperature for each year.
