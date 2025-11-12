# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print head,info of the dataset
2.check for null values
3.Import kmeans and fit it to the dataset
4.Plot the graph using elbow method
5.Print the predicted array
6.Plot the customer segments

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: KAILASH PRABHU S
RegisterNumber:212224240068

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

plt.xlabel("No_of_Clusters")

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

plt.title("Customer Segment")
*/
```

## Output:
## 1.DATA.HEAD():
<img width="653" height="247" alt="500343163-38a2b3df-6ec6-44cc-9473-b39e4dc99bcd" src="https://github.com/user-attachments/assets/c9134218-ce31-4770-b462-2b245cdde58c" />


## 2.DATA.INF0():
<img width="522" height="263" alt="500343138-04ef251b-84ad-4ec1-a6b7-4545bbaaa167" src="https://github.com/user-attachments/assets/41424537-5be3-4f0e-af0c-2a1ca604e36c" />

## 3.DATA.ISNULL().SUM():
<img width="291" height="150" alt="500343116-89334a10-7823-482b-bd07-a100e4e9d3fe" src="https://github.com/user-attachments/assets/405f22e0-c959-4e27-acdf-539d2f401734" />

## 4.PLOT USING ELBOW METHOD:

<img width="877" height="613" alt="500343073-e6bbabc3-aff9-48b3-a52f-c75196a74eb4" src="https://github.com/user-attachments/assets/7cfec740-5c57-4172-898b-458678631fa1" />

## 5.K-MEANS CLUSTERING:
<img width="252" height="91" alt="500343043-ae66e730-b1e4-485f-a458-3defa507e9b8" src="https://github.com/user-attachments/assets/3090a7e4-c3bb-4b1e-a19e-9cb0e425fdff" />

## 6.Y_PRED ARRAY:

<img width="752" height="226" alt="500343010-db0e347d-662f-4a11-bfaa-3519a600c5c7" src="https://github.com/user-attachments/assets/5ce90f5d-c4cb-427e-b3c0-5a0496476d47" />


## 7.CUSTOMER SEGMENT:
<img width="740" height="555" alt="500342929-d50db9e4-84a0-49a0-a0e6-dc0a1144408f" src="https://github.com/user-attachments/assets/76bfd2ad-b944-46ed-8695-c08d1d59a190" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
