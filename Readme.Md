# Customer Segmentation using K-Means Clustering and PCA

## Objective
To segment mall customers into distinct groups based on their annual income and spending
behavior using K-Means Clustering, and to visualize these clusters in two dimensions using
Principal Component Analysis (PCA). The goal is to support the mall's management in designing
targeted marketing campaigns for different customer segments.

## Dataset Link
Mall Customer Segmentation Dataset (Kaggle):
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

> **Note:** The dataset is not included in this repository. Download `Mall_Customers.csv` from
> the Kaggle link above and place it in the project root before running the notebook.

## Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn (`StandardScaler`, `LabelEncoder`, `KMeans`, `PCA`)

## Methodology
1. **Data Understanding** — Loaded the dataset, inspected the first five records, identified
   numerical and categorical features, and reviewed dataset info and summary statistics.
2. **Data Preprocessing** — Checked for missing values, dropped the `CustomerID` column,
   label-encoded the `Gender` column, and standardized numerical features using `StandardScaler`.
3. **Model Development** — Used the Elbow Method to identify the optimal number of clusters (K),
   trained a K-Means model on `Annual Income` and `Spending Score`, assigned cluster labels to
   each customer, and applied PCA to reduce the data to 2 principal components.
4. **Visualization & Evaluation** — Plotted the Elbow Curve, a scatter plot of customer clusters
   (Income vs Spending Score), and a PCA-based 2D visualization of the clusters.
5. **Conclusion** — Summarized key findings, business applications, and the trade-offs of the
   methods used.

## Results
- The Elbow Method indicated **K = 5** as the optimal number of clusters.
- Five customer segments were identified, ranging from high-income/high-spending customers to
  low-income/low-spending customers, each with distinct marketing implications.
- PCA reduced the feature space to 2 components while preserving most of the variance, enabling
  clear visual separation of the clusters.

## Conclusion
K-Means clustering combined with PCA effectively segmented mall customers into actionable groups
based on income and spending behavior. These segments allow the mall's marketing team to design
targeted campaigns instead of a one-size-fits-all approach. A key limitation of K-Means is that
it requires the number of clusters to be pre-specified and assumes roughly spherical, equally
sized clusters. PCA's main advantage is that it reduces dimensionality while retaining most of
the variance in the data, making high-dimensional patterns easier to visualize and interpret.

## Repository Structure
```
.
├── Assignment-7.ipynb
└── README.md
```