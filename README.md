# Udacity_data_science_capstone
### Introducing a Dataset
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

### Project Motivation 
I chose this project to understand the success rate of offers being sent and analysis is done through addressing the following questions.
1. How many customers were provided with a specific offer?
2. What's the performance level of an offer?

### Data Preparation 
There are three datasets provided and each dataset is cleaned and preprocessed for further analysis. The target features for analysis are offer_success, percent_success.

1. Portfolio - renaming id column name to offer_id, one-hot encoding of channels and offer_type columns
2. Profile - profile: renaming id column name to customer_id, replacing age value 118 to nan, creating readable date format in became_member_on column, dropping rows with no gender, income, age data, converting gender values to numeric 0s and 1s, adding start year and start month columns (for further analysis)
3. Transcript - renaming person column name to customer_id, creating separate columns for amount and offer_id from value col, dropping transaction rows whose customer_id is not in profile:customer_id, converting time in hours to time in days, segregating offer and transaction data, finally dropping duplicates if any

### File Descriptions
There is a notebook available here to showcase work related to the above questions and wrangling process. 
There is a csv file containing final dataset that is going to be feed for model training.

### Results
In this project I use Random forest classifier to prdict the result. This model gives a training data accuracy of 0.763 and an F1-score of 0.748 and  test data set accuracy of 
0.736 and F1-score of 0.716 suggests that the random forest model did not overfit the training data.
-Blog Post of this project is at medium : [Starbucks Offer Success Prediction](https://medium.com/@imhimanshurajonly/starbucks-offer-success-prediction-451a1d13cb6d)


