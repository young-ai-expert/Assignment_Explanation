# DBSCAN

#### Density-Based Spatial Clustering Application with Noise
  
  DBSCAN does not include all the data points in the clusters. It considers the tightly packed data points as clusters and others as noise. It only considers the data points which are matching with the given **epsilon** and **minimum points**. If not, they are considered to noise. 
  
  This project is about the correlation between **Annual Income** and **Spending Score** of the customers. Here, we are dealing with **Mall_Customers.csv**. The very first step is to import the required libraries.
  <br>
  
`import numpy as np`
<br>
`import pandas as pd`
<br>
`import seaborn as sns`
<br>
`import matplotlib.pyplot  as plt`
<br>

##### Reading and Basic Understanding of the Dataset

  `pd.read_csv` is used to read the dataset and store it in a variable **dataset** (You can use any variable name). Use `dataset. head()` to get a jist of the dataset. Use the` info()` method to know about the datatype and non-null values of the dataset.
  
##### Visualization

  I am using `pairplot` to know the data's scatteredness and see how many clusters are formed or can be formed. This is also used to choose the features to train the model.
  
![image](https://user-images.githubusercontent.com/78351203/120265440-ba970900-c2bd-11eb-9ef4-77c5ce7fe2a3.png)
 
 From here we can interpret that Annual Income and Spending Score are forming clusters.
 
##### Training data

  In Unsupervised Learning, we don't have an output variable. We are particularly selecting two columns and all the rows using `iloc` for the input variable.
  
##### Import the model

  To import `DBSCAN` , use `from sklearn.cluster import DBSCAN`.
  
##### Creating an instance

  Create an instance of DBSCAN. Define these two important hyperparameters,
   1. Epsilon - the distance between two data points.
   2. Min_samples - Total number of data points needed to make one cluster.
   
       **Epsilon and minimum samples will vary**
   
   `db = DBSCAN(eps = 8 , min_samples = 8)`
   
##### Fitting the model

  1. Core Point: The data point on which the cluster is formed.
  2. Border Point: The datapoints other than the core point.
  
  Here, each datapoint is scanned and checked whether it is fulfilling the two hyperparameters. Multiple core points are formed and if one or more data centers of one cluster lie on another cluster, these clusters are combined to form one cluster.
  
  `model = db.fit(x)`
  
###### Labels

`model. labels_` is used to know the number of clusters and noise formed. The labels given below depict the number of noises (represented using **-1**) and numbers are the number of clusters formed (represented using whole numbers **0 to 3**). From the labels, we can infer that 4 clusters are made. Here, we are not defining the number of clusters.
          

  `array([-1,  0, -1,  0, -1,  0, -1, -1, -1,  0, -1, -1, -1,  0, -1,  0, -1,
        0, -1, -1, -1,  0, -1,  0, -1, -1, -1, -1, -1, -1, -1,  0, -1, -1,
       -1, -1, -1, -1, -1, -1,  1, -1,  1,  1, -1,  1,  1,  1,  1,  1,  1,
        1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,
        1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,
        1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,
        1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,  1,
        1,  1,  1,  1,  2, -1,  2,  1,  2,  3,  2,  3,  2,  1,  2,  3,  2,
        3,  2,  3,  2,  3,  2, -1,  2,  3,  2, -1,  2, -1,  2,  3,  2, -1,
        2,  3,  2,  3,  2,  3,  2, -1,  2,  3,  2, -1,  2, -1,  2, -1, -1,
       -1, -1, -1,  2, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1,
       -1, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1])`
       
###### VIsualizing the clusters

`plt.scatter(dataset['Annual Income (k)'],dataset['Spending Score (1-100)'],c = label)`

![image](https://user-images.githubusercontent.com/78351203/120265463-c387da80-c2bd-11eb-91d8-d753999a991b.png)


This is a very simple project. The conclusion depends on the problem statement. The important thing to remember is **there is no ideal epsilon value or min_samples**.
