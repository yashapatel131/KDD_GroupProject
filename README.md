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
We have obtained the dataset from Kaggle. This dataset contains song attributes, popularity, Grammy award-winning songs, and other aspects. 

## Date Preprocessing
Pre Processing is used at the beginning stages to prepare the data for evolution and modeling. The song data that was used did not have any missing values, so due to that we did not have to deal with the issue of missing data. A new column was created called popularityLabel which is the values from the popularity column that was calculated so that if the popularity value of the song is greater than 20 then the song is given the label of “Popular” and if less than 20 then the value is given the label of “Unpopular”.  

## Data Understanding and Exploration
With the different tastes in music there is for sure a variation in the different types of attributed that compose each individual song. Through the use of visualizations the underlying trends within the data were able to be presented.

Through the use of different types of charts we are able to see the data in a more visual state. The use of these e visualizations was a key aspect in seeing the trends occurring such as correlation between two attribute, the effect that one attribute has on the target variable of popularity, or just the overall comparison of all our attributes. A more detailed analysis can be seen by visiting the link below:

## Data Preparation for Modeling
