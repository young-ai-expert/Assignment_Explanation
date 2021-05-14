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
