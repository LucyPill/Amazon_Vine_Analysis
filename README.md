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
### Deliverable 1: Perform ETL on Amazon Product Reviews
