## SparkSQL Challenge: Home Sales
This repository contains the solution to the SparkSQL challenge focusing on analyzing home sales data. The challenge involves utilizing SparkSQL to derive key metrics from the data, creating temporary views, partitioning the data, and managing cached temporary tables.

## Summary
The challenge was completed within a Jupyter Notebook named Home_Sales.ipynb. PySpark dependencies were imported, and a SparkSession was initialized. Key steps and results include:

Data Preparation: Home sales data was read from an AWS S3 bucket into a DataFrame. A temporary view named home_sales was created for querying purposes.

Average Price Analysis:

The average price of a four-bedroom house sold for each year was calculated.
Average prices of homes with three bedrooms and three bathrooms for each year they were built were determined.
Average prices of homes meeting specific criteria (e.g., three bedrooms, three bathrooms, two floors, and >= 2,000 square feet) were computed.


View Rating Analysis:

The 'view' rating for homes with prices greater than or equal to $350,000 was derived.


Caching:

The home_sales temporary table was cached, and its caching status was validated.
The query for the view rating analysis was run on both the cached and uncached temporary tables, with runtime comparisons.


Data Partitioning:

The dataset was partitioned by the date_built field, and formatted Parquet data was read.
A temporary table for the Parquet data was created.


Query Performance Comparison:

The query for the view rating analysis was executed on the partitioned Parquet temporary table, and runtime was compared with the cached temporary table.


Uncaching:

The home_sales temporary table was uncached and verified.

## Results

1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

![Screenshot 2024-01-28 at 6 51 45 PM](https://github.com/mervecelme/Home_Sales/assets/140986062/597c576e-5121-4655-a5a7-f6b0efd1b16b)


2. What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

![Screenshot 2024-01-28 at 6 55 44 PM](https://github.com/mervecelme/Home_Sales/assets/140986062/cd6d5696-6744-43a4-bef6-73143b1cd38c)


3. What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

![Screenshot 2024-01-28 at 6 56 07 PM](https://github.com/mervecelme/Home_Sales/assets/140986062/cee497fd-845b-4470-b777-274ae148f9dd)


4. What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

![Screenshot 2024-01-28 at 6 58 29 PM](https://github.com/mervecelme/Home_Sales/assets/140986062/389dd9f4-9b60-4ea8-a8a0-a23e910b6f74)
   
