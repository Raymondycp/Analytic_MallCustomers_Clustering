# Mall Customers Segmentation

## Overview

This project focuses on segmenting mall customers using the K-Means clustering algorithm to identify distinct customer groups based on their demographic and behavioral characteristics. The analysis includes exploratory data analysis (EDA) to understand customer profiles and clustering to group customers for targeted marketing. 

## Objectives

- **Exploratory Data Analysis (EDA)**: Analyze customer demographics (age, gender), income, and spending behavior.  
- **Customer Segmentation**: Apply K-Means clustering to group customers based on age, annual income, and spending score.  
- **Visualization**: Create 2D and 3D visualizations to interpret clusters and their characteristics.  
- **Business Insights**: Provide recommendations for targeted marketing strategies based on cluster profiles.

## Dataset

The dataset, `Mall_Customers.csv`, contains 200 customer records with the following columns:

- `CustomerID`: Unique customer identifier (1 to 200).  
- `Gender`: Customer gender (Male or Female).  
- `Age`: Customer age (18 to 70 years).  
- `Annual Income (k$)`: Annual income in thousands of dollars (15 to 137 k$).  
- `Spending Score (1-100)`: Score assigned based on spending behavior (1 to 100).

**Key Details**:

- The dataset includes categorical (`Gender`) and numerical (`Age`, `Annual Income (k$)`, `Spending Score (1-100)`) features.  
- No missing values are present, as confirmed during EDA.  
- The clustering analysis focuses on `Age`, `Annual Income (k$)`, and `Spending Score (1-100)` for segmentation, with `Gender` used in EDA but not clustering.  
- The dataset is relatively small (200 records), suitable for unsupervised learning tasks like clustering.

## Key Steps

1. **Data Loading and Preprocessing**:  
     
   - The dataset is loaded using `pandas` into a DataFrame (`data`).  
   - EDA includes:  
     - Checking for missing values (none found).  
     - Visualizing distributions of `Age`, `Annual Income (k$)`, and `Spending Score (1-100)` using histograms.  
     - Exploring relationships between variables using scatter plots and pair plots, with `Gender` as a hue.

   

2. **Clustering**:  
     
   - **Feature Selection**: The features `Age`, `Annual Income (k$)`, and `Spending Score (1-100)` are used for clustering.  
   - **K-Means Clustering**: The K-Means algorithm is applied to group customers into clusters (the number of clusters is determined using the elbow method, though not shown in the provided snippet, typically resulting in 5 clusters).  
   - **Cluster Labels**: The resulting cluster labels are stored in the `labels` column of the DataFrame.

   

3. **Visualization**:  
     
   - **2D Scatter Plots**: Scatter plots of `Annual Income (k$)` vs. `Spending Score (1-100)` are created, colored by cluster labels.  
   - **3D Scatter Plot**: An interactive 3D scatter plot is generated using `plotly`, visualizing clusters based on `Age`, `Annual Income (k$)`, and `Spending Score (1-100)`. The plot includes:  
     - Custom hover text showing `Age`, `Spending Score`, and `Annual Income (k$)` for each customer.  
     - A `Viridis` colorscale for cluster differentiation.  
     - A colorbar indicating cluster IDs.  
   - The 3D plot is styled with a clear layout, balanced margins, and an optimized camera angle for better interpretation.

   

---

