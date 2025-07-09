# Retail Intelligence System – RFM-Based Customer Segmentation

This project demonstrates a complete end-to-end data science pipeline to analyze customer behavior using transactional data from a retail store. The focus is on RFM analysis (Recency, Frequency, Monetary value) and customer segmentation using unsupervised machine learning.

## Overview

The objective of this project is to extract meaningful business insights from raw transactional logs by:
- Cleaning and preprocessing the dataset
- Engineering customer-level features (RFM)
- Applying K-Means clustering to identify customer segments
- Visualizing clusters and behavioral trends
- Recommending personalized retention strategies based on customer type

## Dataset

**Source**: [Online Retail II - UCI Dataset on Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)  
This dataset contains transactions from a UK-based online retailer between 2009 and 2011.

- Rows: 786,000+
- Columns: 8 (Invoice, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country)

## Technologies Used

- Python (Pandas, NumPy)
- Data Visualization: Matplotlib, Seaborn, Plotly
- Machine Learning: Scikit-learn (KMeans)
- Jupyter Notebook
- VS Code

## Project Structure

<pre lang="markdown">
```
retail-customer-segmentation/
│
├── data/
|   ├── online_retail_II.csv (link externally)
|   ├── cleaned_retail_data.csv (link externally)
|   ├── rfm_customer_segments.csv
│   └── segmented_customers.csv
|   
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   └── 02_customer_segmentation.ipynb
│
├── output/
│   ├── Behavioral_Trend plot
|   ├── Clustering plot
|   ├── Customer Distribution Across Clusters plot
|   ├── Elboe_Curve plot
│   └── Bussiness_Insights plot
│
|
├── requirements
|
|
| 
└── README.md
```
</pre>


## Due to GitHub's file size limitations, the full dataset files are hosted externally:

- [Download online_retail_II.csv (Google Drive)]([https://drive.google.com/file/d/your_file_id/view?usp=sharing](https://drive.google.com/file/d/1g5ij4Q_E1VgY6KKB6IlvlNJD-RJFOLNb/view?usp=sharing))
- [Download cleaned_retail_data.csv (Google Drive)]([https://drive.google.com/file/d/your_file_id/view?usp=sharing](https://drive.google.com/file/d/14E1EbjEUyLp9bOxjvdKxYTFc31hmNi-S/view?usp=drive_link))

## Key Steps

### 1. Data Cleaning & Preprocessing
- Removed nulls, negative quantities, and duplicates
- Parsed dates and ensured correct data types
- Created clean base table for further analysis

### 2. RFM Feature Engineering
- Recency: Days since last purchase
- Frequency: Total number of invoices
- Monetary: Total spend

### 3. K-Means Clustering
- Standardized RFM values using MinMaxScaler
- Used Elbow Method to select optimal clusters (k=4)
- Clustered customers into 4 behavioral segments

### 4. Insights & Visualization
- Visualized segments using seaborn pairplots and interactive 3D scatterplots
- Identified high-value customers, loyal buyers, and at-risk segments
- Built retention strategy framework for each cluster

## Deliverables

- Cleaned RFM-labeled customer file
- Visualizations for internal stakeholder reporting
- Strategy recommendations for targeted marketing

## Business Impact

This segmentation enables retailers to:
- Improve personalization and targeting
- Increase customer retention and lifetime value
- Allocate marketing spend more effectively
