# Udacity_data_science_capstone

### Project Motivation 
In this project we our motivation is to check whether an offer is sent to be a customer or not we aslo check how much an offer is sucessful or what is the count of offers sent.
We then made a classifier which feed on our processed data and then tell us wether an offer is sucessful or not.

### Data Preparation 
There are three datasets provided and each dataset is cleaned and preprocessed for further analysis:

- In portfolio file we create dummy for channels column and then merge it with the file and drop that channel .

- In Profile file we remove rows that contain null values and age greater than 100 years , while observing null containing row we came to know that values are null only when age is greater than 100 so after this information we drop all null columns or age greater than 100. We convert became member on column to days old that a user has been member from the latest member in data and in last we create dummies for gender column.
- In Transcript data we seprate different columns for offer and amount and then drop all customer ids that were not in profile processed data. Then, we convert time in days then seprate transaction and offer data.
- Offer portfolio, customer profile and transaction data are combined to form a single dataset and train models. In the combined dataset, each row will describe an offer’s attributes, customer demographic data, and whether the offer was successful and through which channels the offer was advertised. An offer is said to be successful only if it is viewed and completed within a given duration.



### File Descriptions
There is a notebook available here where we work on our motivation and wrangling process. 
There is a csv file containing final dataset that is going to be feed for model training.

### Results
In this project I use Random forest classifier to prdict the result. This model gives a training data accuracy of 0.763 and an F1-score of 0.748 and  test data set accuracy of 
0.736 and F1-score of 0.716 suggests that the random forest model did not overfit the training data.
- Blog Post of this project is at medium : [Starbucks Offer Success Prediction](https://medium.com/@imhimanshurajonly/starbucks-offer-success-prediction-451a1d13cb6d)


