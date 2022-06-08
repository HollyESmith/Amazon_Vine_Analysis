# Amazon_Vine_Analysis

## Overview

In this project, I am an analyst in a startup company that helps businesses optimize marketing activities. The company has requested an analysis of how their products compare to their competitors. In addition, the company wants to know whether it would be worth the cost of enrolling in a program that gives free products to select reviewers.

Amazon Vine is a service that pays customers for their product reviews; companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. My assignment is to analyze reviews written by members to determine bias. 

For the analysis, I used PySpark to perform the ETL process (extract, transform and load) to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then I used PySpark to determine whether there is any bias toward favorable reviews from Vine members in the dataset. The product category I chose to evaluate was “Kitchen.”

## Results

The total number of reviews was determined by first eliminating records with < 20 votes and then filtered to reflect those that received 50% or more “helpful” up-votes.

<p align="center">
<img src="https://user-images.githubusercontent.com/97558998/172716335-1a18699a-e280-4267-b64a-17cfaba64806.png">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/97558998/172720093-d5e415fe-b8d8-49a4-947d-33060e20d02a.png">
</p>

 - Total number of reviews: 99,017. Of these, 1,207 were Vine (paid) reviews, and 97,810 were non-Vine reviews (unpaid):

<p align="center">
<img src="https://user-images.githubusercontent.com/97558998/172716634-2acc40f8-f513-45bd-a59f-3f441219a03e.png">
</p>

- There were a total of 46,355 five-star reviews; 509 were from Vine members and 45,846 were unpaid:

<p align="center">
<img src="https://user-images.githubusercontent.com/97558998/172716725-acb34a22-894e-470a-897a-bdfd1b83152c.png">
</p>

- 42.17% of Vine reviews were rated 5 stars and 46.87% of non-Vine (unpaid) reviews were rated 5 stars:

<p align="center">
<img src="https://user-images.githubusercontent.com/97558998/172716799-26dfcf59-6547-4b11-af4a-dcb6193158c2.png">
</p>

## Summary

No bias was detected between Vine (paid) and unpaid reviewers in this dataset. In fact, paid reviewers awarded fewer 5-star evaluations (approximately 42%) compared to unpaid reviewers (approximately 47%).

Additional statistical analyses such as mean, median, and standard distribution may provide further insight.
