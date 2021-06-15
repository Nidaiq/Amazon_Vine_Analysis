
# **Amazon Vine Analysis**

#Background:

As a data expert at Big Market, a start-up that helps businesses optimize their marketing efforts.  One of Big Market’s clients, $ellby is releasing a large catalogue of products on a retail website.  They would like to know how the review of their products compare to the reviews of the competitor products. With the project being successful I have been tasked with another project.  This project analyzes the reviews written by members of the paid Amazon Vine program, which is a service that allows manufactures and publishers to receive reviews of their products.  For this service companies like $ellby pay a fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

## Purpose:

The purpose of this project is to extract dataset for **jewellery products** ,transform the data, connect to AWS RDS and load to transformed data to pgAdmin.  PySpark was then used to determine if the paid Vine program by Amazon has more positive reviews for the product.

# Results:

[Image 1]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image1-customer_table.png) shows the customer_table, [Image 2]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image2-review_id_table.png) shows the review_id table, [Image 3]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image3-products_table.png) shows the products_table and [Image 4]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image4-vine_table.png) shows the vine_table in pgAdmin.  The RDS created on AWS can be seen in [Image 5]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image5-RDS.png).

[Image6]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image6-total%20paid%20and%20unpaid%20.png) shows that there were only 21 paid vine reviews as oppose to 7689 unpaid reviews when it comes to jewellery product.  There were 11 five-star reviews from vine and 4444 five-star from the unpaid reviews as seen in [Image 7]( https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image7-five%20star%20paid%20and%20upaid%20reviews.png).

When it come to the percentage reviews, in [Image 8](https://github.com/Nidaiq/Amazon_Vine_Analysis/blob/78d359f4d45fc149496ca0acd3489650d6af55ed/image8-percent%20five%20star%20paid%20and%20unpaid%20.png) it can be seen that the unpaid service five start reviews are slightly higher at 57.8% vs. the paid reviews at 52.4%.  

## Analysis:

It should be noted that the number of unpaid reviews are over 360 times more than the paid reviews. The dataset for the paid reviews for jewellery product is so small that even one positive or negative review can potentially change the overall percentage by 5%.  Therefore, more vine reviews are needed for an informed decision and would deem the data to be inconclusive.  If a decision has to be made with the numbers available, it could be concluded that here was no positive bias for jewellery products in the vine reviews. 

A two-sample t test could be performed comparing the mean of the paid vs. unpaid reviews.  The null hypothesis could be that the paid review have the same mean as the unpaid reviews.  Again, the low sample size of the vine reviews would make it tough for an informed decision to be reached especially given the sample size of the unpaid reviews.
