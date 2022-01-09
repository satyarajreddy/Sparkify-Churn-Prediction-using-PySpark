# *Sparkify-Churn-Prediction-using-PySpark*

## **Project Overview**
- The imaginary start-up company Sparkify offers music streaming service to users in the USA. Many users stream their favourite songs to our service every day either using the free tier that places advertisements between the songs, or using the premium subscription model, where they stream the music for free but pay a monthly flat rate.
- Every time a user interacts with the service, such as playing songs, liking a song with a thumps-up, hearing an ad, or downgrading their service, it generates data. All this data contains key insides for keeping the users satisfied and helping Sparkify’s business thrive. Sparkify keeps a user log file with 18 fields for every user interaction (e.g., userId, name of song played, length of song played, name of artist).
- The company uses the distributed file system Apache Spark to store and analyse the user data. Apache Spark is an open-source distributed cluster-computing framework. Spark is a data processing engine developed to provide faster and easy-to-use analytics than Hadoop MapReduce.

## **Problem Statement**
- It is our task to classify users who are at risk to churn, either downgrade from premium to free tier or cancelling their service altogether. Users can upgrade, downgrade, or cancel their service at any time. If we can accurately classify vulnerable users before they leave (i.e., classifying “true positives”), Sparkify can offer them discounts and incentives, potentially saving the business millions in revenue. 
- In this case we are going to predict potential churner subscribers. If Sparkify detects the subscriber who will be churner, they can take actions to labeled subscribers like discount, no ads and so on.

<img src="https://user-images.githubusercontent.com/16171971/148663848-43038e6f-b422-45e9-927a-9679d557141d.png" width=50% height=50%>

## **Data Source(s)**
- Data Lineage: We have used data provided by Udacity. There are 3 versions of the dataset: a small cluster of 128 MB, a medium size of data of about 6 GB and complete data of 12 GB. We have used the medium sized data in this Spark notebook to perform explanatory data analysis and implement the appropriate models.
- The data can be downloaded from the below web source link: https://video.udacity-data.com/topher/2018/December/5c1d6681_medium-sparkify-event-data/medium-sparkify-event-data.json

## **Data Exploration and Preprocessing**

**Number of rows: 543,000**

**The 18 features are:**
- Artist — which has 17656 unique artists in it
- Auth — authentication level
- firstName — first name of the user
- gender — gender of the user
- itemInSession — log count in a session
- length — length of the song played (in seconds)
- location — user location
- method — GET or PUT HTTP request method
- page — page with which user is currently interacting
- registration — timestamp of user’s registration
- sessionId — session of the log
- song — song played by user
- status — HTTP code of status — 200, 307, 404
- ts — timestamp of a given interaction
- userAgent — what user used as streaming service (Mac/Linux/Windows/iPhone/etc.)
- userId — unique id of the user
- Auth — authentication level
- firstName — first name of the user

## **Data Cleaning & Transformation**
- **StringIndexing – using StringIndexer()**
- **OneHotEncoding – using OneHotEncoder()**
- **Dropna(): Dropping the unnecessary columns from the dataset**

## **Data Visualizations**

**OS & Browser Distribution**

<img src="https://user-images.githubusercontent.com/16171971/148664944-46dcd301-bfbf-4a55-a7f9-d5596a95b2bb.png" width=50% height=50%>


**Gender Distribution**

<img src="https://user-images.githubusercontent.com/16171971/148665133-16fc2580-a2df-4af1-b720-1f5f6af025a0.png" width=50% height=50%>


**Location**

<img src="https://user-images.githubusercontent.com/16171971/148665157-be9483e4-d60a-40f4-98aa-0ae3010129cf.png" width=50% height=50%>


## **Modelling**
### *The below models were developed:*
- Random Forest Classifier
- Logistic Regression
- GBT Classifier
- Naive Bayes 

**Model Results**

<img src="https://user-images.githubusercontent.com/16171971/148665369-9c04e46f-7975-4d1b-a2b7-15e6d987d406.png" width=50% height=50%>

<img src="https://user-images.githubusercontent.com/16171971/148665378-68445875-a5d9-40d8-80dc-a00128452e69.png" width=50% height=50%>


## **Conclusion**
- **GBTClassifier Churn Prediction model** can help Sparkify to identify approx. 98% of the users who would churn.
- **F1 Score: ~98.92%**
- **Accuracy: ~98.93%**
- The company can use special promotions or other measures to prevent them from cancelling the service.

## **Future Work**
- Try other models such as **XGBoost, LightGBM** to obtain more precise results.
- Ensembling approaches to train several classifiers and combining their predictions.
