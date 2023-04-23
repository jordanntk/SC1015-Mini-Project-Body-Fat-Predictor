# SC1015-Mini-Project-Body-Fat-Predictor
Body Fat Predictor for SC1015 Mini Project

![1946445](https://user-images.githubusercontent.com/131585577/233834977-b1341a70-0a2a-4359-80b2-376feced3154.jpg)


## About

This is a Mini-Project for SC1015 on predicting body fat using body measurements with the help of machine learning. The contents of this README are as follows:

1. [Problem Definition](#1-Problem-Definition)
2. [Exploratory Data Analysis](#2-Exploratory-Data-Analysis)
3. [Machine Learning Models Used](#3-Machine-Learning-Models-Used)
4. [Conclusion](#4-Conclusion)
5. [References](#5-References)

  
## Contributors

- [jordanntk](https://github.com/jordanntk)
- [dlee580](https://github.com/dlee580)

## 1. Problem Definition

- Obesity is a major public health concern worldwide, as its prevalence has been increasing rapidly over the past few decades. Obesity can increase the risk of developing chronic health conditions such as heart disease, stroke, type 2 diabetes, certain types of cancer, and more.
- Body Mass Index (BMI) is often used to assess our body as it is simple and inexpensive. However, BMI is not an accurate measure of body composition or overall health as it does not take into account factors such as muscle mass, body shape or fat distribution.

- Body Fat percentage is a better indicator of overall health and obesity risk as it considers body composition more accurately, but it is expensive and time-consuming.
- Thus, our motivation for our project is to use machine learning to predict body fat percentage through simple body measurements

## 2. Exploratory Data Analysis
- We used [Pandas-Profiling](https://pypi.org/project/pandas-profiling/) in order to quickly gain insights into the data which allows us to quickly sift through multiple datasets and find a suitable one.
- It can be installed with the command `pip install pandas-profiling` in the python terminal or `!pip install pandas-profiling` in jupyter notebook.
- We have chosen [Body Fat Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/body-fat-prediction-dataset) uploaded by user *fedesoriano* in [Kaggle](https://www.kaggle.com/)
- After exploring and analysing the dataset, we discovered that there are some issues such as multicollinearity.
- As such, we have cleaned the data to better fit our requirements for conducting our machine learning models in order to improve reliability and accuracy.
## 3. Machine Learning Models Used

1. Linear Regression
- **Note:** After running the linear regression model to predict 'BodyFat', we found that the *Root Mean Squared Error* (RMSE) is relatively high. Instead, we used 'Density' because 'BodyFat' is calculated from 'Density' and 'Density' has a narrower range of values that will make the prediction easier.
2. Ridge Regression

3. K-Nearest Neighbor (KNN) Regression

## 4. Conclusion

- Ridge Regression was the best machine learning model, followed by Linear Regression and K-Nearest Neighbor Regression being the worst.
- This could be explained by the fact that:
  - Firstly, most of the predictors (independent variables) have a linear relationship with 'Density' which KNN would underperform against more appropriate models such as Linear and Ridge Regression.
  - Secondly, Linear Regression model might have overfitted the data points and failed to properly generalise while running with the training data which Ridge Regression is a modified version of Linear Regression that aims to tackle the issue of overfitting by applying a regularisation/penalty term. 
  
- Finally, with the ability to calculate one's body density, we can calculate body fat percentage using the [*Siri Equation*](https://www.topendsports.com/testing/siri-equation.htm) and many other calculations.


## What did we learn from this project?
- Quick Exploratory Data Analysis on datasets using [Pandas-Profiling](https://pypi.org/project/pandas-profiling/)
- Handling imbalanced datasets through Exploratory Data Analysis via cleaning
- Making informed decisions on which variables need to be dropped
- Linear Regression, **Ridge Regression** and **K-Nearest Neighbor Regression**
- Collaborating using GitHub
- Concepts about least sum of squares, overfitting, L2 regularisation, penalty term, explained variance, root mean squared error, non-parametric classification/regression


## 5. References
- http://clipart-library.com/clipart/1946445.htm
- https://pypi.org/project/pandas-profiling/
- https://scikit-learn.org/stable/
- https://www.kaggle.com/datasets/fedesoriano/body-fat-prediction-dataset


