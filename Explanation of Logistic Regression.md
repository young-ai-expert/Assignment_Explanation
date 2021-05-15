# Explanation of Logistic Regression

This assignment is about using **Logistic Regression** , it's a classification algorithm. We use _Logistic Regression_ in this assignment to find out _**whether or not a particular internet user clicked on an Advertisement**_. To see the project [click here](https://github.com/young-ai-expert/Assignment_Explanation/blob/main/Logistic_Regression_Assignment.ipynb).

## Why Linear Regression is not used for classification ??

Linear Regression is a 'Prediction Algorithm' ,in predictions we can have negatives but in the case classification it does not make any sense. It will not be appropriate for binary classification . To solve this problem the mathematicians came up with an Idea which we'll see in the later part.

Before seeing the explanation of the assignmnet , I would like to give a breif insight about **Logistic Regression** so that you can understand it with ease.

## Logistic Regression

It is a binary classification algorithm and cousin of Linear Regression . It uses 'Log Loss' function and 'Gradient Descent' to minimize the error. It uses 'confusion matrix' as it's evaluation metrics . Linear Regression changes to Logisitic Regression using an interesting function called 'Sigmoid Function'.
    
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

  ##### How error is calculated ??
  
  The _miscalculated_ datapoints are counted as errors.
  
  ##### Minimizing the error

   _Logisitic Regression_ uses **Log Loss** and **Gradient Descent** .
   
   ###### Log Loss
   
   _Log Loss_ function punishes all the datapoints whether it's a misclassifed or correctly classified one but the miscalulated points are penalized more.
   
   ###### Gradient Descent 
   
   _Gradient Descent_ reduces or minimizes error .
 
   ##### Logisitc curve

   ![Logisitc curve](https://user-images.githubusercontent.com/78351203/118348479-455ed080-b568-11eb-9ab6-b40a5314a7df.png)
   
   _Source : https://saedsayad.com/_



   This curve or cap will restrict the datapoints in between 0 and 1 . This will make the classification smooth.This is the Idea mathematicians came up with.

   ##### Sigmoid or Logisitc Function

   ![image](https://user-images.githubusercontent.com/78351203/118348771-19444f00-b56a-11eb-836e-46e697fd7848.png) is the linear regression model. This value is substituted in the place of 'z',by this linear regression is converted into logisitc regression.

   ![image](https://user-images.githubusercontent.com/78351203/118348651-6ffd5900-b569-11eb-9eeb-fb2c3b7c3f36.png)
   
   _Source : https://saedsayad.com/_



##### Prediction and Evaluation

After the model is trained ,it's time for prediciton and evaluation . Prediciton is done using the method `LogisitcRegression.predict()` . Using Confusion Matrix and Classification Report , the metrics like _precision , recall , accurary , f1-score_ are calculated. With the help of these metrics , we can get a good grasp of our model , how it's performing , whether it's a high recall or high precision model.

This is the simple explanation of the assignment . Hope you understood !

