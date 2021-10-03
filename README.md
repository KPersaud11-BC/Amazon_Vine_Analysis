# Amazon_Vine_Analysis by Kieran Persaud

## Overview of the Amazon Vine Analysis
For the Challenge, I was tasked with analyzing Amazon reviews written by members of the Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. From the 50 datasets, I selected the **Watch** dataset to analyze. Using PySpark and AWS RDS, I performed the ETL process to extract the dataset, transform it, and load it into pgAdmin. I then used PySpark again to recreate the vine table, filter it by certain conditions, in order to determine if there is any bias toward favorable reviews from Vine members.

## Results
The ```vine_df``` was created, and then filtered for more than 20 total votes, and more than 50% helpful. This became the ```vine_helpful_df```, and all calculations were performed on this dataframe. The Vine and Non-Vine dataframes were created by filtering the vine column for Y and N respectively.

**Vine**

![image](https://user-images.githubusercontent.com/84286467/135745611-90c2df71-d6a7-463c-a4ad-84c54973542d.png)

**Non-Vine**

![image](https://user-images.githubusercontent.com/84286467/135745621-38f201a1-3ab2-497d-8ee1-c5cf4123fd7d.png)

### How many Vine reviews and non-Vine reviews were there?

![image](https://user-images.githubusercontent.com/84286467/135745526-aa8509ae-ee85-4d34-9d14-8f275ab25aff.png)

For the Watch dataset, there were 47 Vine reviews and 8,362 Non-Vine reviews.

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

