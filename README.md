# Data Analysis with Python

This project focuses on data analysis of a messy and raw dataset from EA Sports' FIFA 21 using Python.

## Dataset Overview

**DATA** - The dataset, sourced from [Kaggle](https://www.kaggle.com/), contains detailed information about players in EA Sports' FIFA 21. It includes **18,979 rows** and **77 columns**, featuring attributes such as player positions, wages, value, release clauses, and many more performance and contract details.

## Data Analysis Steps
**DATA CLEANING AND ANALYSIS** - Understanding the dataset is a crucial step in the data analysis process. I took time to understand the dataset and set up series of questions that could be answered by the dataset. Since the dataset is in a very raw form it requires a very through data cleaning.

## QUESTIONS

## PROCESS

Before questions can be answered it is important to understand that dataset must be as clean and comprehensive as possible to help. 

### Data Cleaning
Here are the steps below in cleaning the dataset:

* Split Column- I split the Team and Contract column into clubs and contract
* Stanardize Column- I converted the height column from feet and inches to inches so there is consitency in the column
* - I also standadize the weight column the only the weight and removed lbs so it can be used in calculation
  - I removed the stars after the rating for the following columns W/F, SM and IR
* normalized monetary values - I converted the wage, value and release clause column into pure numerical values, removing the K, M
*  Rename Column- I renamed some columns to make it easier for individuals to understand what a column represents
*  Dropped Column- I dropped a few columns e.g photourl, playerurl
*  Standadize Column Name- I convert all column name to small letter to allow consistency in the data
*  Dropped Duplicate - I checked if we have duplicated rows and dropped them

  ### Exploratory Data Analysis
  After Cleaning the data I then proceeded to answer some questions
  1. Club with maximum number of players
  2. Club with maximum number of players
  3. Club with youngest average players
  4. Team with oldest average players
  5. Check for the most valuable player
  6. list of underpaid players
  7. does attributes like height and strength correlate with player's overall_rating
  8. does player wage correlate with age
  9. Correlation between 'overall_rating', 'player_potential', 'value', 'release_clause', 'wage'
  10. nation with the maximum best players with criteria that best players is considered to over overall rating of 80 and above
  11. What position is most paid and least paid
  12. 
