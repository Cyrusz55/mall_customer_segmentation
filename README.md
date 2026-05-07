# Customer Segmentation using K-Means and Hierarchical Clustering

A machine learning project for segmenting mall customers based on their
demographic and spending behavior using unsupervised learning techniques.

This project explores and compares:

- K-Means clustering
- Hierarchical clustering
- Elbow method for choosing the number of clusters
- Silhouette score evaluation
- Customer profiling and visualization

---

## Dataset

The project uses the **Mall Customers** dataset (`Mall_Customers.csv`).

### Features
- `CustomerID`
- `Gender`
- `Age`
- `Annual Income (k$)`
- `Spending Score (1-100)`

The goal is to identify meaningful customer groups based on income, age, and
spending patterns.

---

## Project Objectives

1. Load and explore the dataset
2. Encode categorical features
3. Standardize the data
4. Use the elbow method to choose the best number of clusters
5. Apply K-Means clustering
6. Build customer segment profiles
7. Evaluate clustering quality using silhouette scores
8. Apply Hierarchical Clustering
9. Compare K-Means and Hierarchical clustering results visually

---

## Techniques Used

### K-Means Clustering
K-Means is used to group customers into clusters based on similarity in their
scaled feature space.

### Hierarchical Clustering
Agglomerative clustering with Ward linkage is used to build a hierarchy of
customer groups.

### Elbow Method
The elbow plot is used to inspect inertia values across different `k` values
and estimate the optimal number of clusters.

### Silhouette Score
Silhouette scores are computed for multiple values of `k` to evaluate cluster
quality.

---

## Workflow

### 1. Load the dataset
The CSV file is loaded using `pandas`.

### 2. Explore the data
Basic inspection is done using:
- `head()`
- `shape`
- `info()`
- `describe()`

### 3. Encode categorical variables
The `Gender` column is one-hot encoded using `OneHotEncoder`.

### 4. Scale the features
Standardization is applied with `StandardScaler` to ensure all features are on
the same scale before clustering.

### 5. Find the optimal number of clusters
The elbow method is used by fitting K-Means for `k = 1` to `10` and plotting
the inertia values.

### 6. Train the final K-Means model
A final K-Means model is trained using the chosen number of clusters.

### 7. Create customer profiles
Cluster-wise statistics are computed, including:
- average age
- average annual income
- median spending score
- gender counts
- customer count

### 8. Evaluate clustering
Silhouette scores are computed for different values of `k` to assess cluster
separation and cohesion.

### 9. Hierarchical clustering
Agglomerative Clustering is applied and compared with K-Means.

### 10. Visualize clusters
Cluster plots are created using:
- Annual Income
- Spending Score

---

## Results

The notebook produces the following outputs:

- Dataset inspection summary
- Elbow plot for determining `k`
- K-Means customer segments
- Cluster profile table
- Silhouette score comparison
- Dendrogram for hierarchical clustering
- Side-by-side cluster visualizations for K-Means and hierarchical clustering

---

## Customer Segmentation Insight

The clusters can be interpreted as different customer types such as:

- Low Spenders
- Medium Spenders
- High Spenders
- Elite Spenders

These segments can help businesses better understand customer behavior and
support targeted marketing strategies.

---

## Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `scipy`

---

## Installation

Install the required dependencies:

```bash
pip install pandas numpy matplotlib scikit-learn scipy