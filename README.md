# Amazon_Vine_Analysis
Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. 


# Overview of Project

The objective of the project is to analyze Amazon reviews written by members of the paid Amazon Vine program to determine if there is any bias toward favorable reviews from Vine members. In this project, I have chosen the cameras dataset. 

# Resources
Data: Amazon Review Datasets

Software: Google Colab Notebook. PostgresSQL, pgAdmin4, Amazon Web Services AWS.


# Results: 
PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to AWS RDS instance, and then load the transformed data into pgAdmin and and calculate different metrics.

## Deliverable 1
In this deliverable we did the following steps:
-Extracted the "kitchen" reviews dataset from the list of review datasets from AWS S3 bucket and loaded into a DataFrame.
-Conducted necessary transformations of the extracted dataset to make sure that the DataFrames match in both data type and column name. 
-Loaded the DataFrames that correspond to tables in pgAdmin.

## Customer table
![customertable](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/customertable.jpg)

## Product table
![products](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/products.jpg)

## Review by ID table
![review](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/review.jpg)

## Vine table
![vine](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/vine.jpg)



##  Deliverable 2 Total Reviews

![image1total](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/image1total.jpg)


- Vine reviews: 607 / non-Vine reviews: 50,522

![image2reviews](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/image2reviews.jpg)


- Vine
** 5 stars reviews: 257 ** Percentage of Vine reviews 5 stars: 42.3%

![image3v](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/image3v.jpg)


- Non-Vine
** 5 stars reviews: 25,220 ** Percentage of Non-Vine reviews 5 stars: 49.9%

![image4nv](https://github.com/acegal1/Amazon_Vine_Analysis/blob/main/images/image4nv.jpg)



## Summary: 
To start the number of Vine reviews is only 607 from 1,807,974 reviews. It is very small and not representative. Unable to see bias since the average star rating is very similiar on both Vine and Non-Vine Users (Vine average rating: 4,09 & Non-Vine average rating: 3.86), also 5 star reviews percentage is higher on Non-Vine users is higher than on Vine ones (Vine rating: 42.3% Non-Vine rating: 49.9%)

When comparing the percentage of reviews that were 5 stars from Amazon Vine members and non-Vine members, it can be concluded that there is no positive bias for reviews of cameras in the Vine program.
