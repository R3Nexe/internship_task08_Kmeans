# Customer Segmentation using K-means Clustering

## Overview

This project applies K-means clustering to segment customers based on their demographic and spending patterns.  

---

## Tools & Libraries Used

- VS Code, Python, Pandas
- Scikit-learn (StandardScaler, KMeans, silhouette_score)
- Matplotlib & Seaborn (for visualization)

---

## Dataset Used
[Customer Segmentation dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
### Features
- Gender
- Age
- Annual Income ($)
- Spending Score (1–100)

---

## Steps Performed

### 1. Data Preprocessing & Cleaning
- Loaded dataset using pandas.
- Encoded categorical variables ('Gender') into numerical form.

---
### 2. Cluster Testing

#### Elbow Method & Silhouette Score (All Features)
- Used Gender, Age, Annual Income, Spending Score.
- Elbow curve was inconclusive (no sharp bend).
- Silhouette scores showed k=5 as a strong candidate.
- <img width="876" height="701" alt="image" src="https://github.com/user-attachments/assets/8abad5d6-cad0-4994-bf62-19df2b4404f6" />

#### Elbow Method & Silhouette Score (2 Features)
- Selected Annual Income and Spending Score.
- Elbow curve showed a clear bend at k=5.
- Silhouette score confirmed good separation at k=5.
- <img width="877" height="701" alt="image" src="https://github.com/user-attachments/assets/f3bc385f-fe0e-4d75-abb7-7777c6e5f9b2" />

---
### 3. Model Training
- Fitted K-means with 'n_clusters = 5' (optimal k).
- Stored cluster labels for each type of customer.

---
### 4. Visualization
- Scatter plots for Cluster Visualisation
- Used color coding to distinguish clusters.
- Displayed centroids for interpretability.
- <img width="850" height="701" alt="image" src="https://github.com/user-attachments/assets/ee3987ca-b802-4051-bf14-4fb179cf996c" />



---
### 5. Interpretation of Clusters

| Cluster | Gender Majority | Age (avg) | Annual Income ($) | Spending Score | Description                                           |
| ------- | --------------- | --------- | ----------------- | -------------- | ----------------------------------------------------- |
| 0       | Male            | 41.1      | 88.2              | 17.1           | High income, low spenders. Potential target.          |
| 1       | Female          | 32.7      | 86.5              | 82.1           | High income, high spenders. Best group for retention. |
| 2       | Female          | 45.2      | 26.3              | 20.9           | Low income, low spenders. Low commercial potential.   |
| 3       | Female          | 42.7      | 55.3              | 49.5           | Mid income, mid spenders. Average engagement.         |
| 4       | Female          | 25.3      | 25.7              | 79.4           | Young, low income, high spenders. Impulse buyers.     |

---

## Overall Conclusion

- k=5 was the optimal number of clusters for both 2-feature and all-feature experiments.
- Best target group: Cluster 1 — high-income, high-spending women.
- Potential opportunity: Cluster 0 — wealthy but low spending.


---
