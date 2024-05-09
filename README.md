# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## Aim:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1. Import pandas and matplotlib.pyplot
2. Read the dataset and transform it
3. Import KMeans and fit the data in the model
4. Plot the Cluster graph

## Program:
```
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SWATHI D
RegisterNumber: 212222230154

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range (1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
KMeans(n_clusters=5)
y_pred=km.predict(data.iloc[:,3:])
y_preddata["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
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

```

## Output:
### data.head() function:
![ml exp 8-1](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/3d6ac8bb-d029-4fc1-b997-c1c9d07a41b1)

### data.info():
![ml exp 8-2](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/66906869-bd6c-4943-93b7-dbbf583e482d)

### data.isnull().sum():
![ml exp 8-3](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/0c33297e-fb59-4a10-bc9c-00ba10bd655b)

### Elbow Method Graph:
![ml exp 8-4](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/d9ced2d7-d1c0-43b4-b665-d94ed9c20067)

### KMeans Clusters:
![ml exp 8-5](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/2deac3d6-08e1-4ca6-a4de-d8bff1bd3a4f)

### y-pred:
![ml exp 8-6](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/5a256c69-0b0e-4d80-8fb1-31c33559c036)

### Customer Segment Graph:
![ml exp 8-7](https://github.com/Gopika-9266/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/122762773/366e8ed4-75ee-45c3-855c-6150d74a536b)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
