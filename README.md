# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1) **Load and prepare data:** Read the dataset (Mall_Customer.csv) and select relevant features (Annual Income, Spending Score).

2) **Initialize K‑Means:** Set the number of clusters (n_clusters=5) and random state for reproducibility.

3) **Fit and predict clusters:** Apply K‑Means to the feature matrix, obtain cluster labels, and compute centroids.

4) **Visualize results:** Plot data points colored by cluster and mark cluster centroids, labeling axes and title.

## Program:

Program to implement the K Means Clustering for Customer Segmentation.

Developed by: PORCHEZIAN S

RegisterNumber:  212225040304

```
# Simple K-Means Clustering Program for Customer Segmentation

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Mall_Customer.csv")

X = data.iloc[:, [3, 4]].values

kmeans = KMeans(n_clusters=5, random_state=0)

y_kmeans = kmeans.fit_predict(X)

plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')

# Labels
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()
```

## Output:

<img width="783" height="529" alt="image" src="https://github.com/user-attachments/assets/306a379f-df7f-413b-928d-499b5369e40c" />

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
