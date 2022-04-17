# Amazon_Vine_Analysis

## Overview/Purpose:
The purpose of this analysis is to extract, transform and load the Amazon review dataset
[Amazon Review Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt),
[Amazon Funiture Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Furniture_v1_00.tsv.gz)
from a S3 bucket in an RDS database.
We will use Colab notebooks and PySpark to perform the ETL process; then, we will connect to an AWS RDS instance, load the transformed data into Postgress  to do our analysis to determine is there is bias from favorable reviews from Vine members. 

We will use our knowlwdge of AWS RDS, PySpark, pgAdmin, and Google Colab to perform the following analysis:
* Perform ETL on Amazon Product Reviews
* Determine Bias of Vine Reviews
* A Written Report on the Analysis

## Results:
## Deliverable 1: Perform ETL on Amazon Product Reviews:
For this deliverable I used Google Colab and PySpark to perform the ETL process:

#### We created several tables that matched the schema in pgAdmin.
* The customers_table DataFrame
* The products_table DataFrame
* The review_id_table DataFrame
* The vine_table DataFrame

#### We then, Load the DataFrames into pgAdmin:
* Make the connection to the AWS RDS instance
* Load the DataFrames that correspond to tables in pgAdmin
* In pgAdmin, I ran a query to check that the tables have been populated

#### Deliverable 1 Results: [Amazon_Reviwes_ETL.ipynb](https://github.com/LucyPill/Amazon_Vine_Analysis/blob/main/Amazon_Reviwes_ETL.ipynb) 

## Deliverable 2: Determine Bias of Vine Reviews
For this deliverable, the same data set from deliverable was used and transformed to obtain the data needed for the analysis.

#### Filter the data and create a new DataFrame or table to retrieve all the rows where the total_votes count is equal to or greater than 20
![1.png](https://github.com/LucyPill/Amazon_Vine_Analysis/blob/main/images/1.png)

#### Filter the new DataFrame or table created in Step 1 and create a new DataFrame or table to retrieve all the rows where the number of helpful_votes divided by total_votes is equal to or greater than 50%.
![2.png](https://github.com/LucyPill/Amazon_Vine_Analysis/blob/main/images/2.png)

#### Filter the DataFrame or table created in Step 2, and create a new DataFrame or table that retrieves all the rows where a review was written as part of the Vine program (paid), vine == 'Y'.
Determine the following: 
* Total number of reviews
* The number of 5-star reviews
* The percentage of 5-star reviews
![paid.png](https://github.com/LucyPill/Amazon_Vine_Analysis/blob/main/images/paid.png)
* Filter the DataFrame or table created in Step 2, and create a new DataFrame or table that retrieves all the rows where a review was written as part of the Vine program (paid), vine == 'N'.

* Determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).
