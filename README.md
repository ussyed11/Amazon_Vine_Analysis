# Amazon_Vine_Analysis

## Overview of the analysis:
The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program, a service that allows manufacturers and publishers to receive reviews of their products and determine if there are any biases between Vine members and Non-Vine member's reviews.

Companies that will pay a fee to Amazon and may provide free products to Vine members who are then required to publish a review. In order to determine if there is any bias towards favorable reviews from Vine members vs. non-members, we need to identify the percentage of 5 star ratings to total rating. As part of this exercise, we were asked to choose from 50 datasets to extract, transform and load into a dataframe in order to complete our analysis. Throughout this analysis, we use:

* PySpark to extract the dataset, transform the data, connect to AWS RDS instance and load the transformed data into pgAdmin.
* Google Colaboratory to import PySpark libraries and connect to Postgres in order to create SQL tables and export the results.

Out of the 50 datasets, I chose to analyze reviews that were made by users in the "grocery" category.

The url for the Dataset used for this analysis is https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Grocery_v1_00.tsv.gz



## Results: 

Our chosen dataset has around 2.4 million reviews recorded.  We filtered our results to keep the most helpful ones by Count of Total Votes equal to or greater than 20 and Percent of Helpful Votes to Total Votes equal or greater than 50%.

![Screen Shot 2022-06-07 at 2 57 04 PM](https://user-images.githubusercontent.com/98566486/172460897-4e3018b4-773d-4d5d-a2cc-361f3d27d487.png)

Our findings are as follow:

* There are 61 total paid Vine members reviews and 28287 unpaid Vine members reviews as shown in the code below.

![Screen Shot 2022-06-07 at 3 08 08 PM](https://user-images.githubusercontent.com/98566486/172463047-e1a42fee-3b3e-442a-b5e3-e9dc04092bca.png)


![Screen Shot 2022-06-07 at 3 10 46 PM](https://user-images.githubusercontent.com/98566486/172463150-1feda01a-2012-4441-8b9f-bd6e04dc07d2.png

* There are 20 five stares paid Vine members reviews and there are 15,689 five stares paid Vine members reviews.

![Screen Shot 2022-06-07 at 3 12 18 PM](https://user-images.githubusercontent.com/98566486/172463549-706b439d-6ad6-4f8a-886f-2f398b93cef7.png)
![Screen Shot 2022-06-07 at 3 12 26 PM](https://user-images.githubusercontent.com/98566486/172463556-a1080229-86b8-4a7b-9fdc-f1598bbcbbf4.png)

* 33 percentage of Vine reviews were 5 stars and  55 percentage of non-Vine reviews were 5 stars.

![Screen Shot 2022-06-07 at 3 14 24 PM](https://user-images.githubusercontent.com/98566486/172463929-71c18189-038b-4679-8c66-3d484c1bb70c.png)

![Screen Shot 2022-06-07 at 3 14 32 PM](https://user-images.githubusercontent.com/98566486/172463976-725922e9-6d3f-484f-aa70-06859b67d475.png)



## Summary: 

Our analysis shows that there is no strong bias toward five-star reviews from paid Amazon Vine reviewers according to the results of 33 percentage of Vine reviews were 5 stars and  55 percentage of non-Vine reviews were 5 stars.  This conclusion could be further examined by looking at the distribution of all star-levels across paid and unpaid reviews. Also, for a more thorough analysis, this same meta-analysis should be conducted across a few different grocery product catagories.
