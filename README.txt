README.txt
==========

Title: Clustering the Moroccan Stock Market Using KMeans

Author: Umar Kashif
Date: 13 April 2024

Description:
-------------
This notebook performs an unsupervised machine learning analysis on the Moroccan Stock Market data using KMeans clustering. The goal is to cluster similar dates based on the stock values of selected companies to uncover patterns and trends in the market.

Dataset:
--------
- Source: Kaggle
- Description: Daily stock price data of 75 Moroccan companies.
- Shape: 1244 rows × 76 columns (after cleaning: 1244 × 70)

Notebook Steps:
---------------
1. **Data Import and Exploration**:
   - Load and preview the dataset using `pandas`.
   - Assess null values and data types.

2. **Data Cleaning**:
   - Drop columns with more than 25% missing values.
   - Drop the date column to focus only on stock price features.
   - Impute missing values using interpolation followed by mean imputation.

3. **Feature Scaling**:
   - Normalize all numeric columns using `StandardScaler` to prepare data for PCA and KMeans.

4. **Dimensionality Reduction with PCA**:
   - Principal Component Analysis (PCA) is used to identify the top 10 most influential features.

5. **KMeans Clustering**:
   - Elbow method and silhouette scores are used to determine the optimal number of clusters.
   - 3 clusters are selected based on silhouette score.

6. **Visualization**:
   - t-SNE is used to visualize high-dimensional clusters in 2D.
   - Line plots show mean and median values of selected features per cluster.

7. **Interpretation**:
   - Clusters are described based on their average feature values, revealing potential patterns across time in the market.

Requirements:
-------------
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

How to Run:
-----------
1. Ensure the dataset `stocks.csv` is in the same directory as the notebook.
2. Open the notebook in JupyterLab or VS Code.
3. Run all cells sequentially to reproduce the analysis.

Output:
-------
- A labeled dataset with a `cluster` column indicating the assigned cluster for each date.
- Visualizations showing the effectiveness and interpretation of the clusters.

Notes:
------
- The analysis only includes numeric features and does not incorporate external financial indicators or events.
- You may adapt the feature selection method or clustering algorithm for further insights.

Contact:
--------
UmarK2707

