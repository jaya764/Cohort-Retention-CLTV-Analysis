# Cohort-Retention-CLTV-Analysis

## Project Goal
This project analyzes customer purchase behabior to understand retention patterns and calculate Customer Lifetime Value (CLTV). By grouping customers based on their acquisition month (cohort), we identify when and why customers churn, and provide data-backed recommendations to improve retention.

## Tech Stack
- Python(Pandas)
- Jupyter Notebook

## Week 1 Summary - Data Cleaning & Cohort Assignment
- Loaded raw dataset: 541,909 rows
- Removed 135,080 rows with missing CustomerID
- Filtered out 8,905 cancelled transactions(InvoiceNo starting with 'C')
- Converted InvoiceDate to proper datetime format
- Removed 5,192 duplicate rows
- Calculated Cohort Month for each customer(the month of their first purchase)
- Final cleaned dataset: 392,732 rows

## Key Findings
- Nearly 25% of transactions had missing customer identifiers, confirming the need for careful filtering before customer-level analysis.
- Cancellations were cleanly identifiable via the InvoiceNo prefix, avoiding reliance on negative Quantity alone.

## Week 2 Summary - Cohort Retention Matrix
- Loaded the cleaned dataset (392,732 rows) from week 1
- Calculated CohortIndex (number of months between each transaction and the customer's first purchase)
- Grouped customers by CohortMonth and CohortIndex to count unique active customers per month
- Built a cohort matrix using pivot_table (absolute retained customer counts)
- Converted the matrix into percentages to build the retention matrix
- Bonus: Added an average retention curve, a retention heatmap, and a best vs worst cohort comparison chart

 ## Key Findings
  - Retention drops sharply from Month 0(100%) to Month 1(~20-37%) across nearly every cohort - most customers do not return after their first purchase.
  - The December 2010 cohort showed the strongest retention, consistently staying between 30-40% across most months.
  - The March 2011 cohort showed weaker retention by comparison, mostly staying in the 15-25% range.
  - Customers who survive past Month 1 tend to remain fairly steady long-term customers rather than continuing to drop off.
  - Recent cohorts (Oct-Dec 2011) have limited data and should be interpreted cautiously due to small sample sizes.
    
