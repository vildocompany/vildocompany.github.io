---
permalink: /portfolio/churn-prediction/
title: " "
wide: true
toc: true
toc_sticky: true
author_profile: false
---
# Prediction Model
---
Objective of prediction model is to help predict future events by using existing data; the prediction made by the model then would drive decisions made in the present. 

This can be achieved by analysing and engineering data, then projecting the results into machine learning model. The resulting model would then be able to predict outcomes from future data.

**Note:**
This analysis is the second part of a 2-part project: first part [here]( https://alvingiovanni.github.io/portfolio/churn-analysis/).
{: .notice--warning}


# Case Study - Ecommerce Churn Analysis
---
So, what is churn?
Churn is defined as ‘number of users that has stopped using a service; in this case the service is ecommerce platform. 

The company behind the ecommerce platform wants to know their user churn condition. They wanted to know when and where people would drop their platform; if there are any clear differences in user characteristics between those who are classified as churn and aren’t.

**Info:**
Case is part of a study and 'company' mentioned is fictional; data used is a public data that can be accessed through: [dataset](https://www.kaggle.com/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction).
{: .notice--info}

**Note:**
View the full notebook [here](https://github.com/alvingiovanni/portfolio/blob/main/Churn%20Rate%20Analysis.ipynb).
{: .notice--warning}


# Data Cleansing & Pre-Processing
---
Data cleansing and pre-processing are essential steps in preparing data for predictive modelling. This process purpose is to rid the data of incorrect, incomplete, improperly formatted, or duplicative data; these data are useless data or at worst misleading. When data full of ‘junk’ are being used to design a predictive model, the model itself will turn out to be a ‘junk; as many people says “Garbage in, garbage out”.

## Check Duplicate Data
Duplicate datas can introduce bias into the model; since data that are supposed to be occuring only once ends up occuring more than once and weight more on the model's calculation. This particular data have no duplicate values so the data can be left alone.

> - Duplicate Rows: 0
> - Duplicate Rows: 5630


## Dropping Features
Having analysing the data previously in the analysis part, there are a few features that need to be preemptively removed:
1. **CustomerID** - is a random number assigned and will introduce a random element into the model.
2. **Tenure** - this is because keeping this feature will introduce bias in the model; since it was determined that most of the churn users are on `Tenure <=2` its important to be able to predict the users' churn probability as earlu as possible regardless of their tenure.
3. **DaySinceLastOrder** - a feature that indirectly also defines users' tenure; as it is the opposite of tenure.

## Dealing With Missing Values
The data have some features with missing value that needs to be addressed. Firstly it is possible to just drop all the missing value row and check if the row reduction would be too much or not.
> - Rows before drop: 5630
> - Rows left after drop: 4345
> - Data Shrinkage: 22.82 %

Dropping all rows with missing value reduces the data size by 28.28%; which is too much so another treatment for missing values need to be done. Since all the missing values are on numerical columns, there are two choices, to fill all missing values with mean or median. With some of the features needing an integer (rounded non-decimal numbers) `CityTier` or boolean feature that are defined by 0/1; most of the features' mean and median are close to each other; for this case filling missing value with median would be more fitting. By filling missing values, the data wont experience any data shrinkage.


## Outlier filter with Zscore
By definition, an outlier is an object (in this case data) that diverge substantially from the rest of the group's average. Outliers usually introduce noises in data and often something that breaks a pattern.   

It is important to take care of outlier data that are going to be used to design a predictive model. Most of the time, removing outlier value from the whole data will help improve the performance of the model; it is better to remove the outlier in this case.

The outlier filter will be using z-score. Z-scores gives a score of how many `times of standard deviation` the distance of the data is from its dataset average. The break point is on **3 times standard deviation**, since 3 times standard deviation represents 99.7% of the whole dataset on a normal distribution data.

> - Rows before outlier filter: 5630
> - Rows left after outlier filter: 5380


## Class Imbalance
Since this is a classification problem, there is a need to check for class imbalance on the target data. Class imbalance is where the class distribution across the data is knowned to be biased or skewed; in this case the class is the churn data. 

Original data class distribution:
> - Non-Churn Users: 4467
> - Churn Users: 913

The target, churn/non-churn status of users, distribution is biased towards 'non-churn'; it is 83% of the whole sample. With this bias, the 'minority' class could end up being ignored by the model; simply stating that all of the users as 'non-churn' users would result in 83% accuracy.

There are alot of different methods to deal with class imbalance issue, one of them is to oversample the data. In this case oversampling is done with SMOTE. The resulting oversampling is to equalize the data size for both classes.

Data class distribution after oversampling:
> - Non-Churn Users: 4467
> - Churn Users: 4467

# Machine Learning Modelling
---
The classification methods that are going to be used are 2 of the most basic methods; Desicion Tree and Random Forest.
While the scoring would be based on 'Recall', because for predicting churn it is important to get as high a possible of true positive prediction.

Other basic parameters for the model:
1. 80/20 train/test split
2. Model are based on sklearn library

## Decision Tree
**Train Recall:** 1.0

**Test Recall:** 0.9357  

Other tests results:
- Accuracy: 0.93
- Precision: 0.92
- Recall: 0.94
- F1-Score: 0.93
- AUC: 0.93

## Random Forest
**Train Recall:** 1.0

**Test Recall:** 0.95716 

Other tests results:
- Accuracy: 0.97
- Precision: 0.97
- Recall: 0.96
- F1-Score: 0.97
- AUC: 0.97

# Model Tuning
---
Out of the 2 models, Random Forest model results in a better result out of the shelf, so the model would be based on Random Forest.
However, some tuning would still need to be done. Most of the time tree based model out of the shelf tend to overfit; one clear indication is that the train score result is 100%.

## Hyperparameter Tuning
The most important hyperparameter to tune in a tree based model is the `max-depth`. This is because on default the `max-depth` varibale is set to infitie (maximum) value; this lets the model to keep making new tree and leaf to cater to the diff data combinations which ends up overfitting the data. To check check what the best `max-depth` should be, it is possible to check by drawing a graph:

![maxdepth]({{ site.url }}{{ site.baseurl }}/assets/images/maxdepth.png){: .align-center}

From the graph above, there are 2 important thing to observe:
1. Growth of discrepancy between scores of `Train` and `Test` results. For obvious reasons, train score result will often if not always be higher; but the bigger the discrepancy of both scores would indicate the model to be overfitting.
2. Shape of the curve; where the growth in score starts to slows down.
3. Plateu-ing of the scores, where the scores stop improving. 

Considering both points, the best `max-depth` would be n = 14.

## Random Forest (Tuned)
**Train Recall:** 0.96201
**Test Recall:** 0.93123 

Other tests results:
Accuracy: 0.92
Precision: 0.91
Recall: 0.93
F1-Score: 0.92
AUC: 0.92

## Cross Validation
To be able to check if the model is reliable, it is important to do a cross validation. One of the way is to iterate the model into multiple folds.

Folds are designed to split the train data into 2 parts; (1) data that will actually be used to train model; (2) data to validate test results.
Since the original train data is 80% of the total sample, the data are split into 8 parts, each part representing 10% of the sample. Every fold iteration then will select 1 out of 8 parts in turn and designate it to be the validation data; the rest of the 7 parts are combined to be the test data. This will result in 8 different train, test, and validatin scores to be observed.

![cross-validation]({{ site.url }}{{ site.baseurl }}/assets/images/cross-validation.png){: .align-center}

From the graph above, it is clear that the model shows constant results; which means that the model is reliable enough to be used.
