# IT-Specialist-Data-Analytic-2

Welcome to "IT Specialist Data Analytics 2"! 🛫

Step directly into a wealth of resources and code snippets designed to deepen your understanding of the foundational concepts of Data Analytics, essential for honing your skills in data analysis.

We've assembled a diverse selection of subjects, spanning comprehension of the Varieties of Data Analysts, Relationship Analysis, Data Characterization, Statistical Inference (Paired T-test), Machine Learning Regression - Basic Linear Regression.

Let's commence this thrilling data Journey Together! 📊✨

Thanks for visiting! 🙌

## Types Of Data Analysis
Analyzing raw data to find patterns, trends, and insights that can provide important information about a certain business area is known as data analytics. Following that, deft, data-driven decisions are made using these insights. 
- Descriptive :
  `Descriptive` analytics condenses large volumes of data into a clear, simple overview of what has happened. 
- Diagnostic : 
   Descriptive analytics looks at what happened, `diagnostic` analytics explores why it happened.
- Predictive : 
  `Predictive` analytics seeks to predict what is likely to happen in the future. Based
- Prespective : 
  `Prescriptive` analytics looks at what has happened, why it happened, and what might happen in order to determine the best course of action for the future.

## Correlation

Correlation is the relationship of two or more variables in a dataset.
> Example: the relationship between salary amount and employee work experience.

Type:
1. Positive correlation (1)
2. Negative Correlation (-1)

<div align="center"><img src="https://github.com/salsanssp/IT-Specialist-Data-Analytic-2/assets/166114037/cffa4c51-a097-4731-b806-c6812afe6d3e" /></div>

## Data Profiling

### Outlier and Anomaly

An outlier is a value in a random sample or collection of observations that is abnormally far from other values. The distance that’s classified as abnormal depends on the dataset and use case. 

> Not all outliers are anomalies

Use boxplot to see anomalies and outliers in variables

<div align="center"><img src="https://github.com/salsanssp/IT-Specialist-Data-Analytic-2/assets/166114037/f184f9c1-41f3-403d-a42c-8248d4485737" /></div>

# Evaluate and explain the results of data analyses
Evaluate and explain the results of data analyses is an important process in interpreting the meaning of data that has been collected and analyzed. It involves identifying patterns, trends, relationships, or significant findings in data and providing an understanding of the significance of those findings.

## Hypothesis Testing
Hypothesis testing is a statistical technique utilized to evaluate assertions or hypotheses about a population through the examination of sample data. The primary objective is to determine if there's enough evidence to support or reject a claim regarding a particular population parameter.

This process generally involves two hypotheses:

* the null hypothesis (H0), and

* the alternative hypothesis (H1).

>First, import and execute the library:
```python
import pandas as pd
from scipy import stats
from statsmodels.stats import weightstats as stests
```

>load a dataset and checking:
<div align="center"><img src="https://github.com/Vanz92x/IT-Specialist-Data-Analytics-2/assets/165736197/e7ac8f41-452b-4f51-b7f3-71b9988c10fb" /></div>

## Paired Sample T-Test
* The paired sample t-test is also called dependent sample-t test.
  
* Its an uni-variate that test for a significant difference between 2 related variables.

> Here's an example, to see if the new coating does have a significant effect on driving range.

H0: is there's no significant difference between the distance traveled by the current ball without coating and the new ball with coating

H1: is there's a significant difference between the distance traveled by the current ball without coating and the new ball with coating

<div align="center"><img src="https://github.com/Vanz92x/IT-Specialist-Data-Analytics-2/assets/165736197/8a3f43e3-0f70-44ee-801c-6a8f08dda214" /></div>

* Alpha is a significance level that indicates the limit for accepting or rejecting the null hypothesis in statistical analysis. Commonly used alpha values are 0.05 or 5%, although sometimes other values such as 0.01 or 0.10 may also be used depending on the context.

<div align="center"><img src="https://github.com/Vanz92x/IT-Specialist-Data-Analytics-2/assets/165736197/cb95e45d-6144-4d3b-9379-5f99d29f702c" /></div>

After we use an alpha of 5 percent or 0.05, it turns out that the p-value is 0.209 > alpha 0.05, so that means we accept H0, which means there's no significant difference between the distance traveled by the current ball without coating and the new ball with coating.

## Machine Learning Regression 
Machine learning regression is a type of supervised learning technique used to model the relationship between a dependent variable and one or more independent variables. The goal of regression is to predict a continuous outcome variable based on the input features. `Simple Linear Regression` : This is one of the simplest regression algorithms. It assumes a linear relationship between the dependent variable and the independent variables. The goal is to find the best-fitting line through the data points.
Mathematically, the simple linear regression equation can be written as:
`Y= β0 ​+ β1​X + ε`
- Y : is the dependent variable (output) to be predicted.
- X: is the independent variable (input).
- β0: is the intercept (constant).
- β1​X : is the regression coefficient (slope)
- ε : Random error

### Exploratory Data Analysis
Before exploring the data, make sure the data is clean. 
- Discribe dataset
- `sns.distplot(df['YearsExperience'])`
<div align="center"><img src= "https://github.com/difasafrina/IT-SPECIALIST-Data-Analytic-1IT-SPECIALIST-Data-Analytic-2/assets/113273578/a11f2132-a8ef-4d5c-ae37-e7c38b66ab78" /></div>

- `sns.distplot(df['Salary'])`
<div align="center"><img src="https://github.com/difasafrina/IT-SPECIALIST-Data-Analytic-1IT-SPECIALIST-Data-Analytic-2/assets/113273578/8bc11892-5414-4c2a-9ba2-f83d36402f06" /></div>
- Preposcessing Modeling
```python
  x = df.drop(['Salary'], axis=1)
  y = df['Salary']
```
- Splitting Training and Test Set. 
  Syntax:
  `x_train, x_test, y_train, y_test = train_test_split(x,y, train_size = 1/2, random_state = 42)`
  
- Fitiing Into Traning
  <div align="center"><img src= "https://github.com/difasafrina/IT-SPECIALIST-Data-Analytic-1IT-SPECIALIST-Data-Analytic-2/assets/113273578/c086cbd7-dd59-48b4-ae83-8379a65144df" /></div>

- Predict The Result
 ```python
y_pred = regressor.predict(x_test)
result = pd.DataFrame({'Actual': y_test, 'Predict': y_pred})
result
```
 <div align="center"><img src="https://github.com/difasafrina/IT-SPECIALIST-Data-Analytic-1IT-SPECIALIST-Data-Analytic-2/assets/113273578/eb39706c-ccdf-426f-b281-3e4b0f3fbd77"  /></div>
  <div align="center"><img src="https://github.com/difasafrina/IT-SPECIALIST-Data-Analytic-1IT-SPECIALIST-Data-Analytic-2/assets/113273578/4f6c23f1-bfd9-45b3-a010-3afb9e982378" /></div>

- Evaluation Model
   - `np. sqrt(mean_squared_error(y_test, y_pred))`
   - `mean_absolute_error(y_test, y_pred)`
   - `mean_absolute_percentage_error(y_test, y_pred)`
   - `r2_score(y_test, y_pred)`

# Data Analytics Journey 🌟
Thank you for diving into "IT Specialist Data Analytics 2" where you'll find a treasure trove of resources and code snippets to master data analytics. From Varieties of Data Analysts to Machine Learning Regression, let's embark on this thrilling journey together! 🚀 Happy analyzing! 📊✨
