# Amazon_Vine_Analysis

## Project Overview

The purpose of this project is to analyze Amazon reviews posted by reviewers who are members of Amazon’s Vine program.  In this program, members are paid to try out products that are sent to them and to post reviews of those products.  The purpose of the analysis is to determine if bias exists in the paid reviews.

## Results

The pet products dataset was used for this analysis.  The dataset was uploaded to Amazon’s S3 and then manipulated using an AWS RDS.  The data was filtered so that reviews with greater than or equal to 20 votes and where the ratio of helpful_votes to total_votes is greater than or equal to 50%.  This was to avoid division by zero errors and use influential reviews.  Here are the results of the analysis:

- The total number of reviews used for this analysis equals 38,010.  Of those reviews, 170 were done by Vine members, and 37,840 were done by non-Vine members.

- The total number of 5-star reviews equals 20,677.  Of that, 65 reviews were done by Vine members, and 20,612 were done by non-Vine members.

- The percentage of Vine reviews with 5 stars comes to 38.2%, and the percentage of non-Vine reviews with 5 stars comes to 54.5%.

## Summary

Based on the results of the analysis of reviews for the pet products dataset, there appears to be no bias for reviews in the Vine program.  The reason for this is that only 38.2% of the reviews done by Vine members had 5 stars.  If bias were to exist, one would expect a higher percentage of Vine reviews to have 5 stars.  That being said, the number of Vine reviews is extremely small compared to the number on non-Vine reviews and therefore really not enough to determine if there’s bias in Vine reviews.  To get a better picture of whether bias exists in the Vine program, other datasets should be analyzed using the same methods there and then combined to really see if bias exists.