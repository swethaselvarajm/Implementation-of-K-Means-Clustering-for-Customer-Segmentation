# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1.Import pandas and matplot libraries.

2.import Kmeans algorithm to solve customer segmentation.

3.Using the for loop cluster the given data

4.Predict the output and plot data graphs.

5.Display the outputs

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SWETHA.S
RegisterNumber: 212222230155
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("Number of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
Km = KMeans(n_clusters = 5)
Km.fit(data.iloc[:,3:])
y_pred=Km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:

data.head() :

![Screenshot 2023-10-26 091304](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/cfb46b4e-e42d-453d-813e-23aba948a696)

data.info() :

![Screenshot 2023-10-26 091340](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/7afb4a0d-eb36-41af-9d83-d0f9e8589c1a)

data.isnull().sum() :

![Screenshot 2023-10-26 093059](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/0611075e-d334-494c-b6b5-e6fa07410f0e)

Elbow method graph:

![Screenshot 2023-10-26 091427](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/daeb2cbd-90e9-4780-8fb9-e81dc442f074)

KMeans clusters:

![Screenshot 2023-10-26 091639](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/3e8af482-e921-4eaa-9d82-25b73a1b1928)

y_pred array:

![Screenshot 2023-10-26 091823](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/6ce1eae6-eefb-4e47-ad95-d037f141c88e)

Customer segements graph:

![Screenshot 2023-10-26 092513](https://github.com/swethaselvarajm/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119525603/9198ad1a-18ca-487a-8a82-5266f929f9b6)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
