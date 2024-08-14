# home_sales

## Project Overview
This repository focuses on analyzing home sales data using SparkSQL. The main objectives of the project include data loading, querying, performance optimization, and comparison of query runtimes. Through this project, I learned to leverage Spark's capabilities, including caching and partitioning, to gain insights into home sales.

## Key Files
The primary file in this repository is Home_Sales.ipynb, a Jupyter notebook created using Google CoLab that contains all the necessary code and documentation for completing the assignment. This notebook includes steps for reading the dataset, creating temporary tables, performing various queries, and optimizing performance with PySpark.

## Steps and Tasks
PySpark SQL functions were then imported to facilitate the analysis of home sales data. Next, the dataset home_sales.csv was read into a Spark DataFrame. From this DataFrame, a temporary SQL table named home_sales was created to enable querying with SparkSQL.

There are several queries to extract insights from the data. First, the average price of four-bedroom houses sold each year was calculated, with results rounded to two decimal places. Then, the average price of homes with three bedrooms and three bathrooms was computed, grouped by the year the home was built, and also rounded to two decimal places.

Additional queries focused on homes meeting specific criteria: three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet. The average price for such homes was calculated for each year they were built, with results rounded to two decimal places. Another query determined the average price of homes per "view" rating for properties with an average price of $350,000 or more, with the runtime for this query recorded and rounded to two decimal places.

To optimize performance, the home_sales temporary table was cached, and its cache status was verified. The runtime of the "view" rating query was then compared between cached and uncached data to assess performance improvements. The data was also partitioned by the date_built field and saved in a parquet format. A new temporary table was created for this parquet data, and the runtime of the query was compared to that of the uncached table to evaluate the impact of partitioning on performance.

The final step involved uncaching the home_sales temporary table and confirming that it was no longer cached using PySpark to ensure a clean state for future operations.
