[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/sRMOJrsa)


# Twitter Disaster Detection - Model Evaluation Report

## Introduction
The objective of this analysis is to build a machine learning model that can accurately predict whether tweets are about real disasters or not. Accurate detection of disaster-related tweets can help in identifying and responding to real-time emergencies and improve crisis management. In this report, we will present the results of our analysis, including the dataset description, model evaluation metrics, and a summary of the findings.

## Dataset Description
The dataset used for this analysis consists of 10,000 hand-classified tweets. The training dataset has the following shape: (7613, 5), and consists of the following columns: `id`, `keyword`, `location`, `text`, and `target`. The `target` column represents the binary label indicating whether the tweet is about a real disaster (1) or not (0). The class distribution in the training data is as follows: Non-Disaster Tweets (Class 0): 4342, and Disaster Tweets (Class 1): 3271. The test dataset has the shape (3263, 4) and contains columns: `id`, `keyword`, `location`, and `text`.

## Model Evaluation Results
We evaluated three different models using the TF-IDF vectorization technique. The models used were Logistic Regression, Naive Bayes, and Support Vector Classifier (SVC). Here are the results of the model evaluation:

### Logistic Regression Model
- Accuracy: 0.7806479859894921
- F1 Score: 0.7364544976328249
- Precision: 0.7486631016042781
- Recall: 0.7246376811594203

### Naive Bayes Model
- Accuracy: 0.8012259194395797
- F1 Score: 0.7440811724915444
- Precision: 0.8168316831683168
- Recall: 0.6832298136645962

### Support Vector Classifier (SVC) Model
- Accuracy: 0.8016637478108581
- F1 Score: 0.7367809413131902
- Precision: 0.8397350993377484
- Recall: 0.6563146997929606
  
  

The logistic regression and SVC models achieved similar accuracies of approximately 80%, while the Naive Bayes model performed slightly better with an accuracy of 80.12%. The precision, recall, and F1-scores for both classes varied across the models.

## Training Data Overview
The training dataset has the following structure:

Shape: (7613, 5)

Head:
   id keyword location                                               text  target
0   1     NaN      NaN  Our Deeds are the Reason of this #earthquake M...       1
1   4     NaN      NaN             Forest fire near La Ronge Sask. Canada       1
2   5     NaN      NaN  All residents asked to 'shelter in place' are ...       1
3   6     NaN      NaN  13,000 people receive #wildfires evacuation or...       1
4   7     NaN      NaN  Just got sent this photo from Ruby #Alaska as ...       1

Class Distribution:
0    4342
1    3271
Name: target, dtype: int64


## Test Data Overview
The test dataset has the following structure:

Shape: (3263, 4)

Head:
   id keyword location                                               text
0   1     NaN      NaN                 Just happened a terrible car crash
1   2     NaN      NaN  Heard about #earthquake is different cities, s...
2   3     NaN      NaN  there is a forest fire at spot pond, geese are...
3   9     NaN      NaN           Apocalypse lighting. #Spokane #wildfires
4  11     NaN      NaN      Typhoon Soudelor kills 28 in China and Taiwan




## Conclusion
In this analysis, we successfully built and evaluated machine learning models for Twitter disaster detection. The logistic regression, Naive Bayes, and Support Vector Classifier (SVC) models demonstrated accuracies above 80% on the test data. However, further improvements can be made to enhance the model's performance, particularly in correctly identifying disaster-related tweets.

This analysis highlights the potential of machine learning in real-time disaster management through the classification of tweets. By accurately identifying tweets related to real disasters, emergency responders and relevant authorities can respond more effectively to crisis situations.

For the complete code and implementation details, please refer to the [code notebook]

