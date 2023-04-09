
Other languages: <kbd>[<img title="Read in Spanish" alt="Read in Spanish" src="https://cdn.staticaly.com/gh/hjnilsson/country-flags/master/svg/es.svg" height="20">](../README.md)</kbd>  &emsp;
Follow me on <kbd>[<img title="Mi perfil en LinkedIn" alt="Mi perfil en LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" height="25">](https://www.linkedin.com/in/martinezjesusfl/)</kbd>

# GDELT Project (Global Database of Events, Language, and Tone)
**Tech Stack:**  
<img title="Python" alt="Python" src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" height="20"> &emsp;
<img title="Terraform" alt="Terraform" src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" height="20"> &emsp;
<img title="DBT" alt="DBT" src="https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white" height="20"> &emsp;
<img title="Prefect" alt="Prefect" src="https://img.shields.io/badge/Prefect-5772b0?style=for-the-badge&logo=?logoColor=white" height="20"> &emsp; 
<img title="Google Cloud" alt="Google Cloud" src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white" height="20"> &emsp;

## Index
- [Intro](#intro)
- [Context](#context)
- [Inventory](#inventory)
- [Instructions](#instructions)

## Intro
This ELT (Extract, Load, Transform) project takes datasets from [GDELT](https://www.gdeltproject.org/), stores the data in Google Cloud Storage and loads it to Google BigQuery applying transformations with DBT Cloud so it can be analyzed with Looker Studio.  
To know more about fundamentals of these tools, refer to [Data Engineering Zoomcamp](https://youtube.com/playlist?list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb), and my personal notes on each module available on the repo [Data Engineering Bootcamp](https://github.com/Jebushdd/Data-Engineering-Bootcamp).

## Context
GDELT (Global Database of Events, Language, and Tone) is a global database of events and news that is constantly updated. GDELT monitors news and events from around the world and collects them into a publicly accessible database. The database contains information about events, people, places, and organizations, and uses natural language processing (NLP) techniques to analyze the tone and emotion of news articles. GDELT is used by researchers, journalists, and organizations around the world to analyze patterns and trends in global news and events.

## Inventory
- ```0_environment_setup``` Folder with command lines to create our environment and installing required packages.
- ```1_infrastucture``` Folder with a Terraform script and commands to build our infrastructure on Google Cloud.
- ```2_pipeline``` Folder with the script to build and deploy the extraction and load pipeline using Prefect.
- ```3_transformation``` Folder with DBT process to transform the data and having it ready to analyze.
- ```4_dashboard_connection``` Folder with the connection process between BigQuery and Looker Studio.

## Instructions