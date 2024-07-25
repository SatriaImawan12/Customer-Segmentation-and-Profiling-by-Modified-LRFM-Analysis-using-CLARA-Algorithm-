# Customer Segmentation and Profiling by Modified LRFM Analysis using CLARA Algorithm to Optimize Marketing Strategy

## Table of Contents
- [Introduction](#introduction)
- [Problem Analysis](#problem-analysis)
- [Goals](#goals)
- [Solution](#solution)
- [Data Source](#data-source)
- [Workflow](#workflow)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Modelling](#modelling)
- [Model Evaluation](#model-evaluation)
- [Profiling](#profiling)
- [Business Recommendations](#business-recommendations)
- [Dashboard](#dashboard)
- [References](#references)
- [Important Note](#important-note)

## Introduction
This project aims to enhance the marketing strategy of a company by understanding customer behavior more deeply through customer segmentation and profiling. We utilize a modified LRFM (Length, Recency, Frequency, Monetary) analysis and the CLARA (Clustering Large Applications) algorithm to achieve this.

## Problem Analysis
### Retention Issues
- Users with their first transaction using a discount show similar or worse retention compared to non-discount users.
- The existing discount promotions are not optimal in attracting new customers and retaining them in the long term.

## Goals
- Understand customer purchasing behavior to optimize promotional strategies for better targeting.
- Increase customer retention and maintain existing customer loyalty.

## Solution
A more personalized promotional strategy analysis by segmenting customers based on purchasing behavior patterns using the modified LRFM metrics.

## Data Source
- [Dataset Superapp](https://drive.google.com/file/d/1-xTSpkU5joEFftCPyrM0o9Ek3hh2Zc1k/view)

## Workflow
1. **Business & Data Understanding**
2. **Data Preprocessing**
3. **Feature Engineering**
4. **Modelling (CLARA)**
5. **Model Evaluation**
6. **Profiling**
7. **Business Recommendation & Solution**

## Data Preprocessing
- **Data Cleaning**: Handling missing values, invalid data, and outliers.
- **Data Merging**: Standardizing column names and formatting data.
- **Feature Engineering**: Creating and modifying features for clustering.

### Data Cleaning
- Removed transactions with zero gross amount (0.57%).
- Replaced missing discount values with 0 (69.83%).
- Deleted rows with invalid data (4,991 rows).
- Kept outliers to preserve valuable transaction information.

## Feature Engineering
- **Length**: Difference between the last and first transaction dates.
- **Recency Score (1/R)**: Inverse of the number of days since the last transaction.
- **Monetary per Frequency (M/F)**: Average amount spent per transaction.

### Importance of LRFM Metrics
- Target promotional strategies accurately.
- Identify customers at risk of churn and the most valuable customers.

## Modelling
### Algorithm: CLARA
- A modification of the PAM (Partitioning Around Medoids) algorithm.
- Uses medoids as cluster centers and sampling methods for efficiency with large datasets.

### Default Parameters
- `n_clusters = 8`
- `init = ‘build’`
- `n_sampling = None`

### Best Parameter Combination
- `n_clusters = 4`
- `n_sampling = 300`
- `init = k-medoids++`
- `random_state = 42`
- Silhouette Score: 0.652

## Model Evaluation
### Cluster Profiles
1. **At Risk** (413 customers): Long-lasting, medium spenders, last transaction a long time ago.
2. **Potential Loyalist** (452 customers): Long-lasting, small spenders, most recent transactions.
3. **Lost** (111 customers): Short-term, very small spenders, last transaction a long time ago.
4. **Loyal** (453 customers): Long-lasting, medium spenders, most recent transactions.

## Profiling
- **At Risk**: Re-engage with personalized offers.
- **Potential Loyalist**: Encourage repeat purchases with targeted campaigns.
- **Lost**: Reactivate with exclusive discounts and limited-time offers.
- **Loyal**: Reward loyalty with community-building initiatives and early access programs.

## Business Recommendations
### At Risk
- Special treatment to make customers feel valued, such as early access to new products or exclusive member offers.

### Potential Loyalist
- Personalized offers, nostalgic campaigns, and customer education.

### Lost
- Exclusive large discounts and time-limited offers to entice customers to return.

### Loyal
- Community-building initiatives, customer appreciation programs, and early access to new collections.

## Dashboard
- [Dashboard Customer Segmentation and Profiling by Modified LRFM Analysis using CLARA Algorithm to Optimize Marketing Strategy](https://public.tableau.com/app/profile/rahmad.kholid/viz/DashboardDatAvengers/Promotion1?publish=yes)

## References
- Zhang, C., Huang, W., Niu, T. et al. (2023). Review of Clustering Technology and Its Application in Coordinating Vehicle Subsystems. *Automot. Innov.*, 6, 89–115. [https://doi.org/10.1007/s42154-022-00205-0](https://doi.org/10.1007/s42154-022-00205-0)

## Important Note
All datasets and project results are used solely for educational purposes and do not reflect actual values. Please do not use this project as a reference or recommendation.

## Acknowledgments
Mentors: Kak Bachtiyar, Kak Renita
Team: Andri Maulana, Nadia Adyutarahma P., Nabila Amina R. Syifa Mufidah Rahmad, Kholid, Satria Imawan

---

Thank you for checking out our project! We hope this work contributes to the optimization of marketing strategies through effective customer segmentation and profiling.
