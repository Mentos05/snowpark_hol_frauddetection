# Snowpark Handson-Lab (HOL) for Fraud Detection
This repository contains resources to get first handson experience with Snowpark.

### Dataset
The dataset was taken from:<br>
https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction

### Task
Build a machine learning model to predict if an applicant is 'good' or 'bad' client, different from other tasks, the definition of 'good' or 'bad' is not given but must be defined by you.

### What you'll learn
* Loading and transforming data via Snowpark
* Defining Stored Procedures for non-SQL-based Data Transformations
* Defining Stored Procedures for training different machine learning models
* Defining User Defined Functions for distributed scoring of machine learning models
* Using hyper paratemer tuning in Stored Procedures

### Requirements
* [Docker](https://www.docker.com/)
* [Snowflake Account](https://signup.snowflake.com/)

### Setup
1. Pull this repository<br>
```
git clone https://github.com/Mentos05/snowpark_hol_frauddetection.git
cd snowpark_hol_frauddetection
```
2. Build your own Docker container containing Snowpark and other 3rd Party packages:
```
docker build -t pysnowpark_hol michaelgorkowsnowflake/pysnowpark_hol:latest
```
3. Run your container with 
```
docker run -v ${PWD}:/snowpark_dev --rm -p 9998:9998 -ti michaelgorkowsnowflake/pysnowpark_hol:latest
```
4. Access Jupyter Lab via: 
```
http://localhost:9998
```
5. Run through the notebooks.<br>

Alternatively you can try pulling the docker container via:<br>
```
docker pull michaelgorkowsnowflake/pysnowpark_hol:latest
```
