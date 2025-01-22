# Home_Sales
# Module 22 Big Data Assignemnt
#
In this challenge, I used the SparkSQL to determine key metrics about home sales data. I also used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

Answered the following questions using SparkSQL:

What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
![image](https://github.com/user-attachments/assets/fa6b42b9-c2e8-4a5c-90e6-9b9c207e16e5)


What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
![image](https://github.com/user-attachments/assets/1c2a885c-1588-481f-89b1-02eaa8d23b95)


What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

![image](https://github.com/user-attachments/assets/a700805e-0d8e-4152-a59b-9f0198fd2b9a)


What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

![image](https://github.com/user-attachments/assets/4e0ccd5c-01d2-453d-bc2f-fc6660773564)
# on second run, the runtime was 0.64 seconds.


Cache your temporary table home_sales.

Check if your temporary table is cached.

Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
![image](https://github.com/user-attachments/assets/016f73a9-7aef-4593-89a6-2452022c8d7d)
# on second run from cached table data, the runtime was 0.3644 seconds, significant improvment from 0.6412 seconds without caching the data.

Partition by the "date_built" field on the formatted parquet home sales data.

Create a temporary table for the parquet data.

Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
![image](https://github.com/user-attachments/assets/febacc1a-4541-4906-804d-44ff8431404e)
# on second run from parquet table data, the runtime was 0.3262 seconds, which is better than 0.3644 seconds from cached data alone. Though the runtime varied among several reruns.

Uncache the home_sales temporary table.

Verify that the home_sales temporary table is uncached using PySpark.
