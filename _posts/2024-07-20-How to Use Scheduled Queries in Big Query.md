---
layout: post
title: How to Use Scheduled Queries in BigQuery
tags: [Scheduled Queries, BigQuery, SQL]
comments: true
---

**In this article, we’ll discuss how to set up scheduled queries in BigQuery.**

First of all, we need to import the libraries

## Create and Execute the Query

Start by writing your query in the BigQuery editor and executing it to ensure it works correctly.

![ScheduledBQ_Part1](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part1.png?raw=true)

Once the query is working as expected, hover over the **Schedule** tab and select **Create new scheduled query**. If this is your first time setting it up, you’ll need to enable scheduled queries by agreeing to activate the necessary API.

![ScheduledBQ_Part2](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part2.png?raw=true)

## Create and Execute the Query

First, configure the schedule. In this example, I set the start date to July 14 at 3 AM, and the query will continue to run until manually stopped.

![ScheduledBQ_Part3](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part3.png?raw=true)
