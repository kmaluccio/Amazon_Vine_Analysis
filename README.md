# Amazon_Vine_Analysis
In this project, we take reviews of a specific product such as clothing apparel or wireless products and use PySpark to perform ETL to extract the data, transform the data and connect to an AWS RDS instance and finally load the transformed data into pgAdmin. Lastly, using either PySpark, Pandas, or SQL we determine if there is any bias toward favorable reviews from Vine members.

## Overview of the analysis
The purpose of this analysis is to look at all of the reviews for pet products and perform ETL on this data to learn more about the ratings of the reviews and present the data in filtered dataframes. We will investigate the reviews that are and are not vine reviews (paid vs unpaid) and compare the percentage of 5-star reviews for paid vs unpaid to see the influence vines have on the customer reviews.

## Results
The results of our analysis tell us that there are 39,376 total pet reviews with 172 Vine reviews and 39,204 non-Vine reviews. With 20,797 of the total number of reviews being 5-star reviews, we get about 53% of the reviews are 5-stars. Focusing on the vine reviews only, we found 65 of them are 5-stars and so this leaves 20,732 non-vine reviews that are 5-stars. Thus, we calculate 37.8% of Vine reviews are 5-stars while 52.88% of the non-Vine reviews are 5-stars. Based on these numbers, it seems like paying for Vine helps with some reviews, there are many non-Vine reviews with 5-star ratings. This implies that over half of the unpaid customers who review the pet products are satisfied with the product.

![Pet Reviews Data](https://github.com/kmaluccio/Amazon_Vine_Analysis/blob/main/pet-reviews.png)

- Above is the output after calculating the numbers mentioned above
- Looking at the Vine_Review_Analysis.ipynb file, written in Colab and added to the repo, you can see the specific filters for the original data frame and view each filtered table.

## Summary
The Vine program does not seem to have positivity bias since the majority of the Vine reviews are not all 5-stars (the highest rating). The reason for this is because we calculated about 38% of the Vine reviews were 5-stars. Since this percentage is less than half, it seems that there is no positivity bias for these reviews. If this percentage was greater than 50%, then one could argue the Vine program has a positive bias toward the pet product.
