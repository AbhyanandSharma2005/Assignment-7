<div align="center">

# 🛍️ Customer Segmentation Engine
### Unsupervised Learning for Data-Driven Retail Marketing

**K-Means Clustering × Principal Component Analysis (PCA)**

![Python](https://img.shields.io/badge/Python-3.13-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-4CAF50?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

</div>

---

## 📌 Overview

Retail businesses generate massive volumes of customer data — but data alone doesn't drive
revenue, **segmentation** does. This project builds an unsupervised machine learning pipeline
that automatically discovers hidden customer segments from raw transactional and demographic
data, enabling precision marketing instead of one-size-fits-all campaigns.

The pipeline clusters mall customers using **K-Means**, validates cluster quality with the
**Elbow Method**, and applies **Principal Component Analysis** to compress high-dimensional
customer profiles into an interpretable 2D visualization — turning an abstract dataset into a
decision-ready map of customer behavior.

> **Business framing:** Given a customer's income and spending patterns, which segment do they
> belong to, and what marketing strategy should be applied to them?

---

## 🎯 Problem Statement

A shopping mall wants to divide its customer base into behaviorally distinct groups using
**annual income** and **spending score**, so its marketing team can run targeted campaigns
instead of broadcasting generic promotions to everyone.

---

## 🧠 Approach

| Stage | What Happens |
|---|---|
| **1. Data Understanding** | Load and profile the dataset — feature types, distributions, summary stats |
| **2. Preprocessing** | Clean nulls, drop identifiers, encode categoricals, standardize features |
| **3. Cluster Discovery** | Use the Elbow Method to identify the statistically optimal number of segments |
| **4. Modeling** | Train K-Means to assign each customer to a segment |
| **5. Dimensionality Reduction** | Apply PCA to project the customer feature space into 2D |
| **6. Visualization** | Plot the elbow curve and cluster maps to make segments interpretable at a glance |

---

## 🛠️ Tech Stack

| Layer | Tools |
|---|---|
| **Language** | Python 3.13 |
| **Data Handling** | Pandas, NumPy |
| **Machine Learning** | scikit-learn (`KMeans`, `PCA`, `StandardScaler`, `LabelEncoder`) |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Jupyter Notebook |

---

## 📊 Results

- **Optimal cluster count:** `K = 5`, determined via the Elbow Method (WCSS inflection point)
- **Dimensionality reduction:** 4 features compressed into 2 principal components for visualization
- **Output:** 5 behaviorally distinct, marketing-ready customer segments, e.g.:

| Segment | Income | Spending | Suggested Strategy |
|---|---|---|---|
| High-Value | High | High | Loyalty programs, premium offers |
| Price-Sensitive Affluent | High | Low | Upsell campaigns, targeted incentives |
| Impulse Spenders | Low | High | Value bundles, flash promotions |
| Low Engagement | Low | Low | Low-priority, reactivation campaigns |
| Balanced | Mid | Mid | Standard engagement, seasonal offers |

---

## 📁 Repository Structure

```
.
├── Assignment-7.ipynb   # End-to-end analysis: EDA → Preprocessing → Modeling → Visualization
├── README.md            # Project documentation
└── requirements.txt     # Python dependencies
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/<your-username>/customer-segmentation-kmeans-pca.git
cd customer-segmentation-kmeans-pca

# Install dependencies
pip install -r requirements.txt

# Download the dataset (not included in this repo — see Dataset section)
# Place Mall_Customers.csv in the project root

# Launch the notebook
jupyter notebook Assignment-7.ipynb
```

---

## 📦 Dataset

**Mall Customer Segmentation Dataset** — [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

The raw dataset is intentionally excluded from this repository in line with Kaggle's
redistribution policy. Download it directly from the link above.

---

## 💡 Key Insights

- **Why K-Means:** Fast, scalable, and interpretable — well suited to well-separated, roughly
  spherical customer segments like income/spending groups.
- **Why PCA:** Reduces multi-dimensional customer profiles into a 2D space that preserves the
  bulk of the variance, making clusters visually verifiable rather than a black box.
- **Limitation acknowledged:** K-Means requires K to be chosen in advance and assumes
  isotropic clusters — a constraint addressed here through Elbow-Method validation rather than
  an arbitrary choice.

---

## 🔭 Future Enhancements

- [ ] Benchmark against DBSCAN / Hierarchical Clustering for non-spherical segment detection
- [ ] Incorporate RFM (Recency, Frequency, Monetary) features for deeper behavioral modeling
- [ ] Deploy as an interactive Streamlit dashboard for live segment exploration
- [ ] Add silhouette score analysis to complement the Elbow Method

---

<div align="center">

### 👤 Author

**Abhyanand Sharma**
[LinkedIn](https://www.linkedin.com/in/abhyanand-sharma-7279182b3/) · [GitHub](https://github.com/AbhyanandSharma2005)

</div>