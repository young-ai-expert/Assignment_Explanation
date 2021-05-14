# Explanation of Logistic Regression

This assignment is about using **Logistic Regression** , it's a classification algorithm. We use _Logistic Regression_ to find out _**whether or not a particular internet user clicked on an Advertisement**_. To see the project [click here](https://github.com/young-ai-expert/Assignment_Explanation/blob/main/Logistic_Regression_Assignment.ipynb).

## Why Linear Regression is not used for classification ??

Linear Regression is a 'Prediction Algorithm' , the values can go in negatives and we can't have a negatives in classification which is impossible . It's a bad choice for binary classification and it will not give a good fit .But mathematicians came up with Idea , we'll see that in the later part.

Before seeing the explanation of the assignmnet , I would like to give a breif insight about **Logistic Regression** so that you can understand it with ease.

## Logistic Regression

It is a binary classification algorithm and cousin of Linear Regression . It uses 'Log Loss' function and 'Gradient Descent' to minimize the error. It uses 'confusion matrix' as it's metrics . Linear Regression changes to Logisitic Regression using an interesting function called 'Sigmoid Function'.
    
### Assignment Explanation

#### Libraries Used
    
        The following libraries are used in the assignment:
        
            1. Numpy 
            2. Pandas 
            3. Matplotlib 
            4. Seaborn 

  The very first step in any project is loading the dataset. Using `pd.read_csv()` , we are reading the dataset. With the help of `pd.head()` , we can have a quick glance at the dataset. `pd.info()` gives us information about the dataset like the datatypes , number of non-null values.`pd.describe()` gives statistical values.
  
####  Exploratory Data Analysis (EDA)

It exposes trends, patterns, and relationships between the columns.We can play around with these interesting graphs . A wide range of graphs are available . Some examples are _lmplot , jointplot , countplot, pairplot_ etc...

#### Spliting of Dataset

`train_test_split()` is used for splitting the datapoints for testing and training . The ideal percentage for training and testing is 70% and 30 % respectively . 

We are importing `LogisticRegression` from `sklearn.linear_model`.Then, create an instance of the LogisticRegression class.

#### Fitting the model

Sigmoid Function , Logisitc curve are included in this part.

##### Logisitc curve

![logistic curve](https://user-images.githubusercontent.com/78351203/118303990-b6b86800-b503-11eb-91e0-4dac1d939829.png)

This curve or cap will restrict the datapoints in between 0 and 1 . This will make the classification smooth.

##### Sigmoid or Logisitc Function

Φ(z) =  1/1+c^-z
      
**y = w1x+w2** is the linear regression model. This value is substituted in the place of 'z',by this linear regression is converted into logisitc regression.

Φ(z) =  1/1+c^-(w1x+w2)

##### Prediction and Evaluation

After the model is trained ,it's time for prediciton and evaluation . Prediciton is done using the method `LogisitcRegression.predict()` . Using Confusion Matrix and Classification Report , the metrics like _precision , recall , accurary , f1-score_ . With the help of these metrics , we can get a good grasp of our model.

This is the simple explanation of the assignment . Hope you understood !
