# SVM - Support Vector Machine

  - Powerful classification algorithm
  - Finds best possible bounday among the model and classes
  - Maintains largest distance from the datapoint
  
 ### Project
 
  In this project , we are going to classify the species of Iris flower. To view the project [Click Here](https://github.com/young-ai-expert/Assignment_Explanation/blob/main/Support_Vector_Machines_Assignment.ipynb)
 
 ### Getting the DataSet
 
  Seaborn has some datasets , from that we are loading *Iris* dataset.
  
    `iris = sns.load_dataset('iris')`
 
 ### Importing Libaries
 
  `import pandas as pd`
  
  `import numpy as np`
  
  `import seaborn as sns`
  
  `import matplotlib.pyplot as plt`
  
  ### EDA (Exploratory Data Analysis)
  
  *Pairplot* is used , to get a glance of relations of each features. We can easily see which features are affecting one another.
  ![image](https://user-images.githubusercontent.com/78351203/122786007-7baf0e80-d2d1-11eb-8641-ce18ea004d6b.png)

  ### Train Test Split
  
  Dividing our dataset for training and testing.
  
  *X* is input and *Y* is output.
  
  `from sklearn.model_selection import train_test_split`
  
  `x = iris.drop('species',axis = 1)`
  
`y = iris['species']`

`xtrain , xtest , ytrain ,ytest = train_test_split(x , y , test_size = 0.3)`

### Training and Fiting a Model

  Creating an instance of the model and fitting it.
  
  `from sklearn.svm import SVC`
  
  `svm = SVC()`
  
  `svm.fit(xtrain ,ytrain)`

### Model Evaluation

  Seeing the perfofrmance of the model using confusion matrix and classification report.
  
  `pred = svm.predict(xtest)`
  
  `from sklearn.metrics import classification_report,confusion_matrix`
  
  `print(confusion_matrix(ytest,pred))`
  
  `print(classification_report(ytest,pred))`
  
 ### Parameter Tuning
 
  #### Grid Seacrh
  
  Let's import grid search and create a dictionary with all the parameters like *C,kernel,gamma*.
  
  `from sklearn.model_selection import GridSearchCV`
  
  `param_grid = {'C':[0.01,0.1,1,10,100,1000],
              'gamma':[1000,100,10,1,0.1,0.01],
              'kernel':['rbf']}`
  
  Fitting Grid Seacrh in the training data. The parameters are instance of our model , the dictionary with parameters , refit and verbose.
  
  `grid = GridSearchCV(SVC(),param_grid,refit = True , verbose = 3)`
  
  `grid.fit(xtrain,ytrain)`
  
  Finding out which parameters worked out well with `grid.best_params_`
  
  We are making a prediction and getting an insight from the confusion matrix and classification report after tuning the parameters.
  
  Thank you!
  
