---
layout: post
title: Data Mining Using Twitter API
tags: [Twitter, Python, API, Jupyter Notebook]
comments: true
---

## Attention

{: .box-note}
**Note:** You will need to apply to Twitter for permission before you use their API.


**In this article we will discuss how to fetch the data using Twitter API in Jupyter Notebook. We will create a collection of tweets using a pre determined keyword in this project.**

First of all, we need to import the libraries

## Import libraries
~~~
import tweepy
import csv
import pandas as pd
import datetime
~~~


Then, we have to use the key or token given by twitter.

## Use the token or key
~~~
consumer_key = "***********************"
consumer_secret = "***********************"
access_token = "***********************"
access_token_secret = "***********************"
~~~

![Key](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/Tf_Installed.png?raw=true)

After that we need to authenticate and verify the API by using this code :

## Verify The API
~~~
# Create the authentication object
auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
# Set the access token and access token secret
auth.set_access_token(access_token, access_token_secret)
# Create api object
api = tweepy.API(auth, wait_on_rate_limit=True)
~~~

Next thing, we have to determine the words that will be used as a benchmark in collecting data. In this case we will use "Julian Assange" as the keywords.
~~~
search_key = "Julian Assange"
~~~



