# KNN

#### K Nearest Neighbors

It is a simple supervised learning technique that can be used for both classification and regression. It is affected by
outliers which might give a wrong classification or prediction. The 'K' in KNN stands for the number of neighbors.

##### Starting with the Project Explanation

###### Importing Libraries

`import numpy as np`
<br>
`import pandas as pd`
<br>
`import seaborn as sns`
<br>
`import matplotlib.pyplot  as plt`
<br>

###### Reading and Basic Understanding of the Dataset

Use  `pd.read_csv` to read the dataset and I am storing it in variable `df`. Use `df.head()` to see the first five rows. Though it's a labeled dataset we can't really
understand what each feature represents.

###### Pairplot

`sns.pairplot(df,hue = 'TARGET CLASS')`

![image](https://user-images.githubusercontent.com/78351203/124530369-05aabb80-de2a-11eb-9803-be9c1e6d6545.png)

From the pairplot we can infer that there is overlapping of datapoints.

###### Standardizing

We standardize the dataset to reduce the dominance of large numbers and to range them from 0 to 1. Here, `StandardScaler` is used.
Create an instance of `StandardScaler` and fit the scalar by dropping the **Target Class**. Use the `.transform()` method to transform the features to a scaled version.

###### Train Test Split

`from sklearn.model_selection import train_test_split`

Splitting the dataset in the ratio of 70:30.

###### KNN

Import KNN, create an instance with k as 1 and fit the model.

`from sklearn.neighbors import KNeighborsClassifier`<br>

`knn = KNeighborsClassifier(n_neighbors=1)`<br>

`knn.fit(xtrain,ytrain)`<br>

###### Prediction and Evaluation

For Prediciton, use

`prediction = knn.predict(xtest)`

The Evaluation Part

`from sklearn.metrics import classification_report,confusion_matrix`<br>

`print(confusion_matrix(ytest,prediction))`<br>

`print(classification_report(ytest,prediction))`<br>

** You Might Think, How to choose a perfect K value? It's simple, with some PYTHON skills we can choose**

###### Choosing K value 

To choose K value, a for loop is iterated over a range of numbers in which the K value is changed in each iteration, fitting, predicting and appending the mean.
With the error rate, a graph is drawn to seen which value of K has given less error. The K value which got the lowest error rate, the model is retrained on the new K value.

![image](https://user-images.githubusercontent.com/78351203/124532377-07767e00-de2e-11eb-9a65-c5c0e82b4e8d.png)
<br>The Graph


