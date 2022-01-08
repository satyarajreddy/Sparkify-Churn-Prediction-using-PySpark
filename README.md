# *Sparkify-Churn-Prediction-using-PySpark*

## **Project Overview**
- The imaginary start-up company Sparkify offers music streaming service to users in the USA. Many users stream their favourite songs to our service every day either using the free tier that places advertisements between the songs, or using the premium subscription model, where they stream the music for free but pay a monthly flat rate.
- Every time a user interacts with the service, such as playing songs, liking a song with a thumps-up, hearing an ad, or downgrading their service, it generates data. All this data contains key insides for keeping the users satisfied and helping Sparkify’s business thrive. Sparkify keeps a user log file with 18 fields for every user interaction (e.g., userId, name of song played, length of song played, name of artist).
- The company uses the distributed file system Apache Spark to store and analyse the user data. Apache Spark is an open-source distributed cluster-computing framework. Spark is a data processing engine developed to provide faster and easy-to-use analytics than Hadoop MapReduce.

## **Problem Statement**
- It is our task to classify users who are at risk to churn, either downgrade from premium to free tier or cancelling their service altogether. Users can upgrade, downgrade, or cancel their service at any time. If we can accurately classify vulnerable users before they leave (i.e., classifying “true positives”), Sparkify can offer them discounts and incentives, potentially saving the business millions in revenue. 
- However, we should avoid falsely predicting churn for active users who would stay loyal anyway (i.e., avoid classifying “false positives”), because discounts and incentives are expensive.

<img src="https://user-images.githubusercontent.com/16171971/148663848-43038e6f-b422-45e9-927a-9679d557141d.png" width=50% height=50%>

## **Data Source(s)**
- Provided by Udacity
- 6GB, medium size dataset is used in this project
- https://drive.google.com/file/d/16EtjE2Fmo0j8aRPUbIacJT0B-47BIQ63/view?usp=sharing

