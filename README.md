# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Data Collection.
2. Data Preprocessing.
3. Choose the Number of Clusters (K).
4. Initialize Cluster Centers.
5. K-Means Algorithm.
6. Evaluate Cluster Quality.
7. Interpret and Label Clusters.
8. Visualize the Clusters.
9. Apply Customer Segmentation.
10. Monitor and Refine.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SYED ADIL BASHA
RegisterNumber:  212221043008

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
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
## 1.data.head() function:
![ex8 1](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/042b2ac9-8bc8-43b9-8e6a-1880bc7fd08d)
## 2.data.info():
![ex 8 2](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/d68b6489-59d0-404c-a9a2-cf308d3c31c6)
## 3.data.isnull().sum() function:
![ex 8 3](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/93e4f90b-2c88-4562-af24-1da9673bb6e6)
## 4.Elbow method graph:
![ex 8 4](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/2ff017d8-51b6-400f-ab86-daac8a4adf4d)
## 5.KMeans clusters:
![ex 8 5](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/12f4422f-f938-4967-beb9-4d7e372cb31d)
## 6.y_pred:
![ex 8 6](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/83d00473-796f-4a1b-b492-b931b0576758)
## 7.Customers Segments Graph:
![ex 8 7](https://github.com/SYEDADILBASHA1/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/134796157/01a91a8e-b382-4c0b-87d8-ab8344e89601)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
