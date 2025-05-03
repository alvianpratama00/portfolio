---
layout: post
title: How to Use Scheduled Queries in BigQuery
tags: [Scheduled Queries, BigQuery, SQL]
comments: true
---

**In this article, we’ll discuss how to set up scheduled queries in BigQuery.**

## Create and Execute the Query

Start by writing your query in the BigQuery editor and executing it to ensure it works correctly.

![ScheduledBQ_Part1](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part1.png?raw=true)

Once the query is working as expected, hover over the **Schedule** tab and select **Create new scheduled query**. If this is your first time setting it up, you’ll need to enable scheduled queries by agreeing to activate the necessary API.

![ScheduledBQ_Part2](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part2.png?raw=true)

## Set Up the Scheduled Query

First, configure the schedule. In this example, I set the start date to July 14 at 3 AM, and the query will continue to run until manually stopped.

![ScheduledBQ_Part3](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part3.png?raw=true)

Next, define the destination for your query results. You can choose to **append** or **overwrite** the table. You can also specify the data location, though in this example, we'll use the **automatic location** option.

![ScheduledBQ_Part4](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part4.png?raw=true)

For additional setup, you can select a service account for authentication, specify encryption options, and configure notifications for your scheduled query.

![ScheduledBQ_Part5](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part5.png?raw=true)

## Check Scheduled Queries

After setup, go to the **Scheduled Queries** tab on the left panel. Select your query to view its status and verify that it's running as expected.

![ScheduledBQ_Part6](https://github.com/alvianpratama00/portfolio/blob/master/assets/img/ScheduledBQ_Part6.png?raw=true)

From the scheduled query details, you can perform a **backfill** if data was missed, or enable/disable the scheduled query as needed.

## Conclusion

Scheduled queries in BigQuery are a powerful feature that help automate and orchestrate repetitive tasks. They can save setup time and reduce costs, making your workflows more efficient and reliable.
