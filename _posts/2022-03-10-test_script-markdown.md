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

## Import the data

~~~
heart <- read.csv(file.choose(),sep=',')
~~~

Once you have imporrted the data, split the data into train and test data

~~~
c𝑜𝑏𝑎 < − 𝑠𝑎𝑚𝑝𝑙𝑒(1: 𝑛𝑟𝑜𝑤(ℎ𝑒𝑎𝑟𝑡), 𝑠𝑖𝑧𝑒
= 250 , 𝑟𝑒𝑝𝑙𝑎𝑐𝑒 = 𝑇𝑅𝑈𝐸)
𝑡𝑟𝑎𝑖𝑛_𝑑𝑎𝑡𝑎 < − ℎ𝑒𝑎𝑟𝑡[ 𝑐𝑜𝑏𝑎,]
𝑡𝑒𝑠𝑡_𝑑𝑎𝑡𝑎 < − ℎ𝑒𝑎𝑟𝑡[−𝑐𝑜𝑏𝑎,]
~~~

Then, create the model using C5.0 Algorithm

~~~
m𝑜𝑑 < − 𝐶5.0(𝑥 = 𝑡𝑟𝑎𝑖𝑛_𝑑𝑎𝑡𝑎[, 𝑣𝑎𝑟𝑠], 𝑦
= 𝑡𝑟𝑎𝑖𝑛_𝑑𝑎𝑡𝑎$𝑡𝑎𝑟𝑔𝑒𝑡)
~~~

Here are the model which have been created 
![Model](assets/img/model_R.png)



