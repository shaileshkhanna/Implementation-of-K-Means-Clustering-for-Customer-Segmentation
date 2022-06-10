# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file and print the number of contents to be displayed.
3. Import KMeans and use for loop to cluster the data.
4. Predict the cluster and plot data graphs.
5. Display the result.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: S.SHAILESH KHANNA
RegisterNumber: 212220040152
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wess=[]
for i in range(1,11):
    kmeans=KMeans(n_clusters=i,init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wess.append(kmeans.inertia_)
plt.plot(range(1,11),wess)
plt.xlabel("no of clusters")
plt.ylabel("wess")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income"],df0["Score"],c="red",label="cluster0")
plt.scatter(df1["Annual Income"],df1["Score"],c="black",label="cluster1")
plt.scatter(df2["Annual Income"],df2["Score"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income"],df3["Score"],c="green",label="cluster3")
plt.scatter(df4["Annual Income"],df4["Score"],c="magenta",label="cluster4")
plt.legend() 
plt.title("Customer Segments")
*/
```

## Output:
ELBOW METHOD:
![7-1](https://user-images.githubusercontent.com/103241457/173100939-ad14a2d5-9a04-4f92-8b04-4635f7ca720f.png)

CLUSTER:
![7-2](https://user-images.githubusercontent.com/103241457/173100981-e0957b97-0fe7-46f0-8cbb-cde60a009b18.png)




## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
