# Customer Segmentation Analysis

## Overview
Segments mall customers by annual income and spending behaviour to identify high-value customers, growth opportunities, and segment-specific marketing strategies for a simulated mall marketing use case.

## Business problem
The mall wants to increase sales by understanding customer purchasing behaviour and identifying distinct customer segments.

## Objective
Segment customers according to income and spending patterns to identify high-value customers, growth opportunities, and segment-specific marketing strategies.

## Key questions
1. Who are the highest value customers?
2. What customer segments exist?
3. Which segments have the greatest spending potential?
4. How should marketing engage each segment?

## Dataset
`Mall_Customers.csv` — 200 customers, with:
- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

**Data limitations:** no transaction amounts, no product preference, no visit frequency. The analysis focuses on segmentation rather than retention as a result.

## Method
1. **EDA**,  plotted income vs. spending score, visually identified ~5 natural customer groups.
2. **Segmentation**, used K-Means clustering (`n_clusters=5`) on income and spending score, rather than a manual threshold split, so the algorithm could find the actual cluster shapes instead of forcing rectangular boundaries onto the data.
3. **Cluster naming**,  named clusters by reading each cluster's own center values (average income/spending) rather than by their arbitrary KMeans index, so labels stay correct even if cluster numbering changes on a rerun.
4. **Interpretation**,  described each segment's characteristics and a targeted marketing recommendation.

## Segments identified
- **Premium Customers** = high income, high spending
- **Average Customers** = mid income, mid spending
- **Affluent Low Spenders** = high income, low spending
- **High-Spending Budget Customers** = low income, high spending
- **Budget Customers** = low income, low spending

## Key findings 
- High-Spending Budget Customers make up the highest percentage of customers
- Average Customers make up the least percentage of customers
- female customers dominate

## Tech stack
Python
pandas
matplotlib
scikit-learn (KMeans)

## How to run
1. Place `Mall_Customers.csv` in the same directory (or update the file path in the load cell).
2. Run all cells top to bottom in `customer_segmentation_analysis.ipynb`.

## Files
- `customer_segmentation_analysis.ipynb`, full analysis notebook
