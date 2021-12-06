# KDD Group 14 Project
This project is part of the Knowledge Discovery in Databases (DSBA 6162) course from University of North Carolina at Charlotte.

## Team Members
- Vathsavi Venkat
- Yash Patel
- Zubin Ladwa

## Introduction to Problem or Opportunity
Music is all around us and plays a vital part in today’s culture. Popularity in music is always hard to determine. It is unpredictable determining which song is going to be a hit. Music popularity also plays a crucial role in establishing if the song is going to be a Grammy award winner. There are different perspectives we need to take into consideration such as how music taste changes during a pandemic, or how seasonality affects it. We will look at the popularity of music based on the song’s attributes.

## Research Question
Given the past 20 years of data, we want to determine what effect song attributes (Danceability, Energy, Tempo, etc.) have on the popularity of a song that has been obtained from the US population. Can the song attributes predict whether it will be a Grammy award winner?

## Data Resources
We have obtained the dataset from Kaggle. This dataset contains song attributes, popularity, Grammy award-winning songs, and other aspects. The datasets can be found here: [Datasets](https://github.com/yashapatel131/KDD_GroupProject/blob/main/Data)

## Data Preprocessing
Preprocessing is used at the beginning stages to prepare the data for evolution and modeling. The SongAttributes dataset did not have any missing values, due to which we did not have to deal with the issue of missing data. A new column called popularityLabel was created. This column was calculated based on the Popularity rating. If the popularity value of the song was greater than 20 then the song was given the label of 'Popular' and if less than 20 then, the value was given the label of 'Unpopular.' The new CSV file that was created can be found here: [Song_Atrributes.csv](https://github.com/yashapatel131/KDD_GroupProject/blob/main/Data/Song_Attributes.csv)

## Data Understanding and Exploration
There are different types of music, which leads to variation in the attributes that compose each song. Through the use of visualizations, the underlying trends within the data were presented. By using different types of charts, we were able to see the data in a visual state. The use of these visualizations was an important aspect in seeing the trends. A few of the charts that were created were:

The correlation between all the attributes:

<img src="Image/Corr.png" width= "500">

The effect that Loudness and  Danceability attributes had on the target variable:

<img src="Image/Comp.png" width= "500">

The overall comparison of the attributes:

<img src="Image/histo.png" width= "500">

A more detailed analysis can be seen by visiting the link: [EDA and Data Preparation](https://github.com/yashapatel131/KDD_GroupProject/blob/main/src/EDA_and_DataPrep.ipynb)

# Data Preparation
Data Preparation included many steps to get the data ready for our modeling. The first task we took on was dropping a few columns that did not have a direct impact on the models. A few of these columns included: 'ID', 'Album', 'Mode’, and 'Name'. These columns were removed due to them being too broad and not having any significance in the modeling process. Another action that was taken in the preparation process was the dummying of variables. A few variables that we took into consideration for dummying were: 'Artist', 'TimeSignature', and 'Explicit'. These were dummied due to them having a large impact but not having a format compatible with the model.

# Machine Learning
The machine learning models that were used in this project were: decision tree, random forest, and deep neural network.
With the decision tree model, we used a 70/30 split of the data allocating 70% to the training data and 30% to the testing. During the process, we created a function to obtain the best depth for the model. With these results, we were then able to create two decision trees with the top two depths. 
For the second model, we created a random forest using a 70/30 split like the previous model. A max depth of 10 with an estimator of 50 was used as the inputs for the creation of the model. 
A deep neural network was created to find the predictions of the popularity of the songs. With this model, a 70/30 split was used and was conducted along with a sequential model with an input dimension of 1002 due to that being the number of columns in the dataset post dummying. Furthermore, the model was fit on the training data with an iteration of 100 epochs. 

# Evaluation
Decision Tree: 

<p float="left">
<img src="Image/Decision Tree Max 1.png" width= "500">
<img src="Image/Decision Tree Max 2.png" width= "500">
</p>

Here we have the accuracy scores that were presented from our two decision tree models with the top two max depths. We can see that the one with the higher depth had a greater accuracy score at a 59.1% compared to the second depth at a 58.7%.

Random Forest: 

<img src="Image/Random Forest.png" width= "500">

From the random forest model, we obtained an accuracy score of 60.5%.

Deep Learning Neural Network:

<img src="Image/Neural Network.png" width= "500">

With this neural network, we were able to obtain an accuracy of 72.6%.

With the comparison of these three models, we can see that the random forest performed slightly better than the decision tree between these two models. Overall, the deep learning neural network outperformed when comparing all three models with about a 10% higher accuracy score than the other two. 

# Conclusion
Through our findings, we have come across many new realizations such as how interesting and unique this data was due to it having so many different attributes that had a direct impact on the actual popularity of a song. While taking a deep dive into the data we noticed some imbalance in the data with there being more unpopular songs compared to popular, so appropriate measures were taken to balance out the data to prevent skewing. For our models to run smoothly we took the initiative of creating a new variable to use as our target. This variable was used in every model as the target, and it was the indicator of whether a song was popular or unpopular. 

There were many challenges that we faced when working with this data such as how we went about figuring out how to create the model and the appropriate features to use while creating the models. Some other challenges that we faced were deciding which variables we would find the most important and how to use them in the models such as the dummying process and so forth. The way we overcame these trials was by doing some research and finding possible solutions that we could use to implement. Also, we were able to rank the variable from most important to least and the ones that were least important were removed. 

In conclusion, we would continue this modeling process by going a few steps further and predicting the possibility of these attributes winning a Grammy award. Although we were not able to provide the results this time; we have an idea of how to possibly take the data and do some predictive modeling.
