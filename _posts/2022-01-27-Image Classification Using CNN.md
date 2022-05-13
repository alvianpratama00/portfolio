---
layout: post
title: Breast Cancer Classification Using Convolutional Neural Network
tags: [Deep Learning, Image Classification, Jupyter Notebook, Python]
comments: true
---


**In this article we will discuss how to do image classification in Jupyter Notebook. We will create a classification using pictures from breast cells for predicting breast cancer disease.**

First of all, let's import the libraries to start the project. 

## Import libraries
~~~
import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
#import keras
#from keras.utils import to_categorical
from tensorflow.keras.utils import to_categorical
from keras.models import Sequential
from keras.layers import Dense, Dropout, Conv2D, MaxPool2D, Flatten
from keras.layers import Conv2D, MaxPooling2D
from keras.datasets import mnist
from keras.preprocessing import image
from keras.utils import np_utils
from tqdm import tqdm

~~~

## Attention

{: .box-note}
**Note:** As you can see, there are a lot of libraries that we need to import, especially the keras one. The reason why we need a lot of libraries is because deep learning requires many processes from the input process to the output, which requires many layers in order to run properly.

After we imported the library, we need to import the data for this project. 
