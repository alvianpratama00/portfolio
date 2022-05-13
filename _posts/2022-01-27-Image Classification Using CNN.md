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

{: .box-note}
**Note:** As you can see, there are a lot of libraries that we need to import, especially the keras one. The reason why we need a lot of libraries is because deep learning requires many processes from the input process to the output, which requires many layers in order to run properly.

<br />

After we imported the library, we need to import the dataset for this project. In this project, we will use the dataset from a collaboration between P&D Laboratory and Pathological Anatomy and Cytopathology, Parana, Brazil. 

~~~
df = pd.read_csv("input/breakhis/Folds.csv")
df = df.sample(frac=1)
path = "input/breakhis/BreaKHis_v1/" 
~~~

### Dataframe from dataset
![df_image](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Gather_data.png?raw=true)

Next, we need to classify between the pictures to know which is benign and malignant cells. 

~~~
train_image = []
y = []

for i in tqdm(range(df.shape[0])):
    img = image.load_img(path + df['filename'].iloc[i], target_size=(28,28,1), grayscale=False)
    img = image.img_to_array(img)
    img = img/255
    train_image.append(img)
    
    if (df['filename'].iloc[i].find('benign') != -1): 
        y.append(0) 
    else:
        y.append(1)
~~~

Here are some example pictures of benign and malignant cells. 

### Benign Cell
![benign](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Gather_data.png?raw=true)


### Malignant cell
![malignant](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Gather_data.png?raw=true)


After that, we need to split the data for data training and data validation.  
