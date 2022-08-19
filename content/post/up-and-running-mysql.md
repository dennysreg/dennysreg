---
title: "Up and Running Mysql"
date: 2020-05-16T00:50:18-05:00
draft: true
---

# Airflow Metadata Store

Our pipeline orchestrator runs on Google Cloud Platform under Google Cloud Composer product name. For short Composer is an environment used for [Apache Airflow](https://airflow.apache.org/) deployment and the following diagrame ilustrate its components:

![Cloud Composer Environment RSQesources](https://cloud.google.com/composer/docs/images/architecture.svg)


Cloud SQL stores the Airflow metadata and that database could be:

- MySQL
- PostgreSQL

Since our current configuration uses MySQL is important to brush up the dialect. Remember that every database engine implement their own features and I strongly recommend use standard SQL syntax in order to make it cross-database queries.

## Installation

### Ubuntu 

{{< highlight bash "linenos=table,hl_lines=8 15-17,linenostart=1" >}}
lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 18.04.4 LTS
Release:        18.04
Codename:       bionic
{{< / highlight >}}

### Mac OS
