---
layout: post
title: Predicting Heart Disease Using C5.0 Algorithm
subtitle: Analyzing Data Using R Language
cover-img: /assets/img/prediction.jpg
thumbnail-img: /assets/img/heart.jpg
share-img: /assets/img/prediction.jpg
tags: [R Language, Data Analytics]
---

 This project aims to detect "Heart Disease"
by using the algorithm used in data mining. This project offers how to detect the disease 
using the decision tree method in the form of C5.0 algorithm. 

In this project, the variable used is a variable that denoted by “0” and “1”. “0” means no heart disease and “1” means to
have a heart disease, which are categorized as categorical data and numerical data. In this project there are 3 independent variables such as heart rate, 
blood pressure, and cholesterol level in the blood.

This project resulting in an accuracy of 62% which is a fairly low level of accuracy. The accuracy is so small because it uses a categorical variables
with different levels, which tends to decrease the accuracy.

In this article, I want to explore in the matter of predicting the heart disease using R Language. I want to know if there are variables 
that are influencing heart disease conditions.  Therefore, I created a project in regards to predicting the heart disease using R Language.

In this project, the first thing to do is prepare the library that are facilitating me to do the analysis.

## Import the packages

~~~
require(C50)
require(caret)
require(e1071)
require(caTools)
~~~

After importing the packages, we need to import the data that will be used for analysis. We uses heart_dataset.csv which are contains many variables related to heart disease.

