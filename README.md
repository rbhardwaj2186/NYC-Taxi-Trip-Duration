# Predicting and Analyzing NYC Taxi Trip Durations

![Untitled](https://github.com/user-attachments/assets/1c2b5644-8bab-40c9-b2fa-be2267051c34)


## Business Problem

### The goal of this project is to analyze and predict NYC taxi trip durations. By identifying patterns such as peak hours, typical trip lengths, and other influencing factors, the project aims to optimize fleet management, implement dynamic pricing strategies, and improve overall operational efficiency. Additionally, insights from this analysis will help stakeholders understand customer behavior and improve service delivery.

## Approach to the Problem

Data Exploration:

![Untitled](https://github.com/user-attachments/assets/f4372c8e-c4d5-437f-b85f-56ec6e7d460b)


    Analyze the distribution of trip durations.
    Identify temporal patterns such as peak hours and daily trends.

Feature Engineering:



    Create additional features like pickup_hour and pickup_dayofweek to capture temporal effects.
    Categorize trips into short, medium, and long durations for simplified analysis.

Outlier Removal:

    Use the Interquartile Range (IQR) method to remove extreme trip durations, ensuring the data focuses on representative patterns.

Statistical Testing:

    Perform A/B testing to evaluate the influence of categorical variables like pickup hour parity on trip duration.

## Statistical Understanding

Trip Duration Distribution:

    Log transformation was applied to the trip_duration to reduce skewness and stabilize variance. This allowed better visualization and modeling of the data.

Outlier Removal:

    Outliers were removed using the IQR method, ensuring extreme values did not dominate the analysis or skew results.

A/B Testing:

    The average trip durations for two groups (even vs. odd pickup hours) were compared. Minimal differences were observed, indicating pickup hour parity does not significantly impact trip lengths.

## Modeling
Decision Tree Classification:

    Trips were categorized as short (≤10 minutes), medium (10–30 minutes), or long (>30 minutes).
    The model used pickup_hour and pickup_dayofweek as predictors.
    Achieved an accuracy of 51%, better than random guessing (33%), but with room for improvement.

Clustering with K-Means:

    Trips were grouped into four clusters based on trip_duration, pickup_hour, and pickup_dayofweek.
    Clusters revealed patterns such as shorter trips during peak hours and longer trips during off-peak times.

## Visualizations

Clusters of NYC Taxi Trips:

    Visualized trips grouped by pickup hour and trip duration. Colors represented clusters, highlighting distinct trip patterns.

A/B Testing Results:

    Compared average trip durations for groups A (even pickup hours) and B (odd pickup hours). The results showed minimal variation.

Heatmaps and Box Plots:

    Created to analyze hourly and daily trends, highlighting variability in trip durations and pickup activity.

Hypothesis Testing Results:

Compared average trip durations across the days of the week. The results showed significant variation, with the ANOVA test confirming that trip durations differ statistically between weekdays and weekends. This indicates that trip patterns are influenced by the day, reflecting shorter commutes during weekdays and longer trips on weekends.

## Business Insights 

Operational Planning:

    Insights from clustering and classification guide fleet allocation, ensuring enough drivers are available during peak hours and for longer trips.

Dynamic Pricing:

    Short trips during peak hours can use surge pricing, while discounts can encourage longer trips during off-peak times.

Customer Experience:

    Improved driver availability and efficient pricing lead to better customer satisfaction.

## Summary
### This project provides a comprehensive approach to understanding and optimizing NYC taxi operations. Using data-driven insights from statistical analysis, machine learning, and A/B testing, the project delivers actionable recommendations for fleet management, pricing strategies, and customer service improvements.


