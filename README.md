# KDD Group 14 Project
This project is part of the Knowledge Discovery in Databases (DSBA 6162) course from University of North Carolina at Charlotte.

## Team Members
- Vathsavi Venkat
- Yash Patel
- Zubin Ladwa

## Introduction to Problem or Opportunity
Music is all around us and plays a key part in today’s culture. Popularity in music is always hard to determine. It is unpredictable determining which song is going to be a hit. Music popularity also plays a crucial role in establishing if the song is going to be a Grammy award winner. There are different perspectives we need to take into consideration such as how music taste changes during a pandemic, or how seasonality affects it. We will look at the popularity of music based on the song’s attributes.

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
Data Preparation included many steps in order to get the data ready for a model. The first task we took on was dropping a number of columns that did not have a direct impact on the model. A few of these columns included: 'ID', 'Album', 'Mode',  and 'Name'. These columns were removed due to them being too broad and not having any significance in the modeling process. Another action that was taken in the preparation process was the dummying of variables. A few variables that we took into consideration of dummying were: 'Artist', 'TimeSignature', and 'Explicit'. These were dummied due to them having a large impact but not having a format compatible with the model. 

# Machine Learning
The machine learning models that were used in this modeling process were: decision tree, random forest,  and a deep neural network.

With the decision tree model we used a 70/30 split of the data allocating 70% to the training data and 30% to the testing. During the process we were also able to create a function to obtain the max depth for the model. With these results we were then able create two decision trees with the top two max depths. 

For the second model we were able to create a random forest using a 30/70 split similar to the previous decision tree model. A max depth of 10 with an estimator of 50 as the inputs for the creation of the model. 

# Evaluation

# Conclusion
''' What was unique about the data?  Did you have to deal with imbalance? What data cleaning did you do? Outlier treatment?  Imputation?
    Did you create any new additional features / variables?
    What was the process you used for evaluation?  What was the best result?
    What were the problems you faced? How did you solve them?
    What future work would you like to do? 
    Instructions for individuals that may want to use your work '''
