---
layout: post
title: Create Tensorflow Environment For Jupyter Notebook
subtitle: Create Tensorflow Environment using Anaconda Prompt
tags: [Python, Tensorflow, Jupyter Notebook]
comments: true
---

This is a quick tutorial to show you how to create tensorflow environment in Jupyter Notebook.  I strongly encourage you to install Anaconda before creating the tensorflow environment.

First of all, open the Anaconda Prompt and run as administrator 
![Admin](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/RunAdmin.png?raw=true)

After that we need to create the tensorflow environment. In this case, I will name it "tf-env".

## Create the environment
~~~
conda create -n tf-env tensorflow
~~~

After that we need to test whether the installation is good or not by activating the tensorflow.


## Activate the environment
~~~
conda activate tf-env
~~~

Then we need to check if the tensorflow already installed or not by writing this code :
~~~
python
import tensorflow as tf
tf.__version__ #
~~~

This is the result when tensorflow is installed :
![TF_Anaconda](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Tf_Installed.png?raw=true)

After all of that, we can continue to the next step, which is creating a kernel to use tensorflow in Jupyter Notebook.
Here is the code to activate the kernel :

## Install the ipykernel
~~~
conda install -c anaconda ipykernel
~~~

## Activate the kernel
~~~
python -m ipykernel install --user --name tf-env --display-name "TensorFlow Environment"
~~~

Here is the result if the kernel was installed correctly.

### Kernel
![Kernel](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Kernel.png?raw=true)

### Tensorflow in Jupyter Notebook
![TF Test](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Test_Notebook.png?raw=true)


## Additional Information

{: .box-note}
**Note:** This is a clean installation of Tensorflow in Jupyter Notebook. You will need to install various libraries such as : pandas, numpy, matplotlib, etc if you want to properly used the Tensorflow. 

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.
