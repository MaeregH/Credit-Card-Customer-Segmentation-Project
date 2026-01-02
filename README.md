# Customer Segmentation using K-Means Clustering
Overview

This project performs customer segmentation on a credit card customer dataset using unsupervised machine learning. The goal is to identify distinct groups of customers based on their spending behavior, balance patterns, and credit usage, without relying on predefined labels.

By applying K-Means clustering and Principal Component Analysis (PCA), the project uncovers meaningful customer segments that can be used for business insights such as targeted marketing, risk assessment, and customer profiling.

Dataset

The dataset contains anonymized credit card customer information, including:

Account balance

Purchase amounts and frequency

Cash advance behavior

Credit limits

Payment behavior

Various usage frequency metrics

Each row represents a customer, and all features are numerical.

Methodology
1. Data Preprocessing

The dataset is inspected for structure and data types.

Features are standardized using StandardScaler to ensure all variables contribute equally to distance calculations, which is essential for K-Means clustering.

2. Selecting the Number of Clusters

The Elbow Method is used to determine a suitable number of clusters.

K-Means is run for multiple values of k, and inertia (within-cluster sum of squares) is plotted.

Based on the elbow point, 8 clusters are selected.

3. K-Means Clustering

K-Means is applied with the chosen number of clusters.

Each customer is assigned a cluster label.

Cluster centroids are transformed back to the original scale for interpretability.

4. Cluster Analysis

Cluster labels are merged with the original dataset.

Feature distributions are visualized using histograms to analyze behavioral patterns within each cluster.

This step helps identify distinct customer profiles such as:

High spenders

Low-usage customers

Customers with high cash advance usage

Customers who carry high balances

5. Dimensionality Reduction and Visualization

Principal Component Analysis (PCA) reduces the data to two dimensions.

Customers are plotted in PCA space and colored by cluster assignment.

This visualization helps assess the separation and structure of the clusters.

Results

The analysis reveals multiple distinct customer segments with different financial behaviors. These segments can be used to:

Improve customer targeting strategies

Identify high-risk or high-value customers

Support data-driven decision-making in finance and marketing contexts

Technologies Used

Python

NumPy

Pandas

Scikit-learn

Matplotlib

Seaborn

How to Run

Clone this repository

Install the required dependencies:

pip install numpy pandas scikit-learn matplotlib seaborn


Open and run the Jupyter notebook:

jupyter notebook CustomerProject2.ipynb

Future Improvements

Experiment with alternative clustering methods (e.g., DBSCAN, Hierarchical Clustering)

Add quantitative cluster validation metrics (Silhouette Score, Davies–Bouldin Index)

Perform deeper business-oriented interpretation of each cluster

Incorporate time-based customer behavior if available
