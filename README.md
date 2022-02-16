# Overview

The purpose of this analysis is perform an ETL process one Amazon Reviews. Through Google Colab, using PySpark and a Postgres driver to extract a dataset of Amazon reviews, transform the data into dataframes that distinguish relational trends, and load the transformed dataframes into pgAdmin tables by coonecting through an AWS RDS instance. We're essentially analyzing differences, particularly any bias, between regular Amazon reviews and Amazon Vine reviews. The Amazon Vine program invites the most trusted reviewers on Amazon to post opinions about new and pre-release items to help fellow customers make informed purchase decisions. A vine review is identified with the green stripe customer review from the Amazon Vine Program.



# Results

- How many Vine reviews and non-Vine reviews were there?
	- Of the 27,884 total reviews, 22 were paid Vine reviews and 27,862 were unapid reviews.

![/Resources/Total_Number_of_Reviews.png](/Resources/Total_Number_of_Reviews.png)


- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
	- 13 of the 22 paid Vine reviews were 5-stars.
	- 14,581 of the 27,862 unpaid Vine reviews were 5-stars.

![/Resources/Total_Number_of_5-star_reviews.png](/Resources/Total_Number_of_5-star_reviews.png)


- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
	- 59.1% of the paid Vine reviews were 5-stars.
	- 52.3% of the unpaid Vine reviews were 5-stars.

![/Resources/Percentage_5-star_Reviews.png](/Resources/Percentage_5-star_Reviews.png)






# Summary

In summary, there is slight positivity bias for reviews in the Vine program, as the paid reviews have a higher precentage of 5-star reviews. One additional analysis that could support this bias would be to unfilter the dataset, as the results are based off a filter dataset that includes reviews with at least 20 votes. The unfilter dataset contains 4,362,074 reviews and the filter of 20 votes per reviews reduced the number down to 27,884 reviews.
