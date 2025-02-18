# CHURN-ANALYSIS
Weekly Retention Analysis

Project Overview

This project focuses on analyzing subscription churn from a weekly retention perspective. The goal is to calculate weekly retention rates for cohorts of users who started their subscriptions within a specific week and track their retention over the following six weeks. This approach allows for quicker insights into user engagement trends compared to a monthly retention analysis.

Data Source

The analysis is based on the turing_data_analytics.subscriptions table in BigQuery. This table contains subscription start and end dates, along with user pseudo IDs, which are essential for tracking cohort retention.

Tools Used

SQL (BigQuery): To extract cohort-based retention data.

Excel: For visualization and trend analysis.

Methodology

1. Understanding the Table Structure

Before running queries, a thorough exploration of the subscriptions table was conducted to check for missing values, duplications, and ensure data consistency. Key columns considered:

subscription_start_date

subscription_end_date

user_pseudo_id

2. Calculating Retention for a Single Cohort

To establish a baseline, retention was first calculated for a single cohort of users who started their subscriptions within a given week (e.g., 2021-01-04 to 2021-01-11). Users were tracked for the next six weeks to determine the proportion still active each week.

3. Extending the Analysis to Multiple Cohorts

The SQL query was modified to compute retention across all cohorts dynamically. Conditional aggregation was used to count active users for each week (Week 0 to Week 6).

4. Exporting the Data

Once the SQL query was executed, the results were exported to CSV format and later imported into Excel for visualization.

5. Visualization Techniques

To effectively communicate insights, the following visualization techniques were applied:

Heatmap: Displaying retention rates across different cohorts and weeks, using a gradient color scale (e.g., green for high retention, red for low retention).

Line Chart: Tracking retention trends over time for each cohort.

Bar Chart: Comparing retention rates across different weeks.

Key Insights

Seasonal Impact: Certain cohorts experienced lower retention rates, potentially influenced by external factors such as holiday promotions.

Early Drop-off: A significant number of users tend to churn after the first week, suggesting an opportunity for early engagement strategies.

High-Retention Cohorts: Identifying cohorts with higher-than-average retention provides insights into successful subscription strategies.

Next Steps & Recommendations

Improve Onboarding Experience: Enhance the initial user experience to reduce early churn.

Introduce Retention Strategies: Implement targeted engagement campaigns (e.g., loyalty programs, personalized outreach) for at-risk cohorts.

A/B Testing: Test different pricing models or promotional offers to analyze their impact on retention.

Further Segmentation: Break down cohorts by customer demographics or acquisition channels for deeper insights.

Conclusion

This project successfully demonstrates the power of weekly retention analysis in identifying trends and informing strategic decisions. By shifting from a monthly to a weekly analysis, businesses can react faster to retention challenges and improve long-term customer engagement.



