**Table of Contents**

- [Introduction](#-introduction)
- [Objectives](#-objectives)
- [Dataset introduction](#-dataset-introduction)
  - [Dataset](#dataset)
- [Dataset exploration and visualization](#-data-viz)
  - [Visualization](#-viz)
- [Modeling](#-modeling)
  - [First model](#-first-steps)
  - [Final model](#-final-model)
-[Conclusion](#-conclusion)

## Introduction

Made by :

 * Lucas Enard
 * Myriam Essafoui

## Objectives
The objective is to use python for data analysis and modeling differents machine learning models around a given dataset.

## Dataset introduction
### Dataset
We selected the following [dataset](https://archive.ics.uci.edu/ml/datasets/Estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition+) which include data for the estimation of obesity levels in individuals from the countries of Mexico, Peru and Colombia, based on their eating habits and physical condition.

The first thing we did was to try and understand the content of the dataset, the records are labeled with the class variable NObesity (Obesity Level), that allows classification of the data using the values of Insufficient Weight, Normal Weight, Overweight Level I, Overweight Level II, Obesity Type I, Obesity Type II and Obesity Type III. 

## Dataset exploration and visualization
### Visualization
After seeing the dataset, we decided to visualize it by plotting, for each variables, a bar plot of the percentage of NObesity and by creating a heatmap of the different variables.
You can find them in the ipynb.
## Modeling
The first thing we had to do was to encode the qualitative data.
We decided to go for an encoding that remplaced string value by numeric values. This method doesn’t lose any information since there was already an order in the data, for instance the frequencies would be no : 0, sometimes : 1 ,frequently : 2 and always : 3.
### First model
At first, the model seemed obvious, we would just predict the label using all the columns.
However, we quickly saw that predicting the BMI using the height and the weight of the subject was of course not that hard and machine learning wasn’t needed for that since our not optimized random forest got an accuracy of 0.966

### Final Model
The problematic was now :
Can we predict the BMI of a subject using only his habits and practices?

To explore more in details this problematic we used different models to predict he outcomes to then do a gridsearch and optimize the best of them.

## Conclusion
With a knn having an accuracy of 0.82 and a mean absolute error of 0.35 after a gridsearch we can conclude that it is indeed possible to to predict the BMI of a subject or to be near it using only his habits and practices.
