Customer Segmentation using K-Means Clustering
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Project Overview
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
This project applies K-Means Clustering to retail transaction data to identify distinct customer segments based on their purchasing behavior.
The analysis enables businesses to:

Understand different customer types.

Design targeted marketing campaigns.

Improve customer retention and sales strategies.

Dataset

File Used: online_retail_II.xlsx

Source: UCI Machine Learning Repository – Online Retail II Dataset (if that’s your dataset source)

Description:
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Transactions from a UK-based online retail store.

Features include: Invoice, StockCode, Description, Quantity, InvoiceDate, Price, CustomerID, and Country.

Data Preprocessing

Data Cleaning

Removed missing values (especially in CustomerID).

Filtered out negative or zero quantities and prices (returns/cancellations).

Feature Engineering

Created RFM metrics:

Recency: Days since last purchase.

Frequency: Number of purchases.

Monetary: Total spending.

Scaling

Standardized RFM features using StandardScaler for equal weighting in clustering.

Exploratory Data Analysis

Checked customer distribution by country.

Analyzed sales over time.

Plotted histograms of Recency, Frequency, and Monetary values.

K-Means Clustering Process

Elbow Method:

Plotted inertia values for different k to find optimal cluster number.

Selected k = 4 clusters.

Model Training:

Applied KMeans algorithm from scikit-learn.

Assigned cluster labels to each customer.

Cluster Profiling:
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Interpreted each cluster based on average RFM values:

Cluster 0 – High spenders, frequent buyers.

Cluster 1 – Low spenders, infrequent buyers.

Cluster 2 – Dormant customers.

Cluster 3 – Occasional mid-range buyers.

Visualizations
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Elbow Curve for optimal k.

Scatter plots of R vs. F, F vs. M, colored by cluster.

Boxplots of R, F, M by cluster.

Key Insights
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
High-value customers can be targeted with loyalty programs.

Dormant customers can be re-engaged with special offers.

Low-value customers might respond to promotions for higher frequency.

Technologies Used

Python: pandas, numpy, matplotlib, seaborn, scikit-learn

Jupyter Notebook for analysis

Excel for initial data storage

How to Run

Clone this repository:

git clone https://github.com/<your-username>/<your-repo-name>.git


Install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn


Place the dataset file online_retail_II.xlsx in the project folder.

Run the Jupyter notebook:

jupyter notebook Untitled10.ipynb

Future Improvements if the dataset included additional details
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Automate RFM calculation for any dataset.

Try other clustering algorithms (DBSCAN, Hierarchical Clustering).

Deploy as a dashboard using Power BI or Streamlit for business users.
