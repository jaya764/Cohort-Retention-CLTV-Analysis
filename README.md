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
  
