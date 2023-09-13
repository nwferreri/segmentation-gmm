# Segmentation - Gaussian Mixture Model (Credit Card Customers)

## Goal

Use clustering to create segments of credit card customers. Uses Gaussian Mixture Model (GMM).

## Data

A cross-section of data on the credit history for a sample of applicants for a type of credit card.  ~1300 entries with the following features:
* `card` - Was the application for a credit card accepted?
* `reports` - Number of major derogatory reports
* `age` - Age in years plus twelfths of a year
* `income` - Yearly income (in USD 10,000)
* `share` - Ratio of monthly credit card expenditure to yearly income
* `expenditure` - Average monthly credit card expenditure
* `owner` - Does the individual own their home?
* `selfemp` - Is the individual self-employed?
* `dependents` - Number of dependents
* `months` - Months living at current address
* `majorcards` - Number of major credit cards held
* `active` - Number of active credit accounts

## Analysis

First the optimal number of components for the GMM was determined using AIC and BIC metrics.<br>
![image](https://github.com/nwferreri/segmentation-gmm/assets/112211174/e003be4c-795f-4594-8c89-5e0586248972)<br>
Based on the graph, 3 and 8 components have similar values.  3 was chosen for simplicity.

The GMM was run using 3 components and clusters were predicted for each customer.

## Results

Based on the feature averages for each cluster, the following groups were assigned:
* Cluster 0: Non-credit Users
* Cluster 1: Successful Entrepreneurs
* Cluster 2: Young Employees
