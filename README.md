# 🏌️‍♂️ Exploratory Data Analysis of PGA Tour Data: Revealing Insights and Patterns within the Game of Golf

### An exploratory data analysis (EDA) exploring the raw data from all Professional Golf Association (PGA) Tour tournaments between the 2015 - 2022 seasons to discover trends and insights into the game of professional golf and which factors might influence a player's success on the tour.

> ***Note:** For a more detailed analysis of the EDA findings, refer to the [Complete Executive Summary](Complete_Execitive_Summary_of_PGA_Tour_EDA.md) in this repository.*

## 📂 Included in this Repository

- ***PGA_Tour_EDA_Full_Data_Cleaning_and_Analysis_Process.ipynb***: This file includes the initial inspection of the original raw dataset, exploratory analysis of the individual variables, data cleaning, tailoring of the datasets for different data analyses, and the full data analysis that is ultimately included in the executive summary.
- ***PGA_Tour_EDA_Executive_Summary_(w_Python_Code).ipynb***: This is an executive summary of the data cleaning and exploratory data analysis process that was conducted in the previously listed file. This Jupyter Notebook contains introductory information about the project, the Python code used for the data analysis of the cleaned datasets created in the full data cleaning file, and the interpretation of the EDA results.
—***Complete_PGA_Tour_EDA_Executive_Summary_Write_Up.md***: This file includes the EDA results, the project background information, and the interpretation of the executive summary results, but as a Markdown file, it doesn't include the Python code used to execute the EDA.
- ***PGA_Tour_Raw_Data.csv***: this is the original raw data file that I started with.
- ***pga_clean.csv***: this was the final version of all the cleaned data, even with those tournaments missing strokes gained information.
- ***pga_sg.csv***: this file only contained the cleaned data from tournaments in which strokes gained data are available.
- ***season_2022_exp.csv***: This file only contains tournaments from the 2022 season. It also contains a new variable entitled "course experience," which is based on the previous seven years of experience at a given golf course.

## 🔍 Abstract

[NEED TO ADD AT THE END!]

## 🧭 Introduction

I conducted an exploratory data analysis (EDA) on a raw dataset of PGA Tour Golf. The dataset covers all the rounds played by every golfer in all the tournaments held between the professional seasons of 2015 and 2022. My aim for this analysis was to gain insights into which aspects of players’ golf games most impact their performance in tournaments. Additionally, I aimed to identify characteristics of various courses on the PGA Tour schedule, such as determining which courses favor golfers with more course experience and the courses where putting plays a crucial role in contending in the tournament.

> _For background information about the sport of golf and a complete description of strokes gained measurements, please refer to section 1 of the Complete Executive Summary._

### 💡 Project Hypotheses
I have several hypotheses for this EDA, including the following:

1. **Hypothesis #1**: When it comes to winning professional golf tournaments, certain aspects of a player’s game are more essential than others. Specifically, there are particular strokes gained measurements that have a more significant impact on a player’s overall performance in a tournament.
2. **Hypothesis #2:** Golfers with more course experience will perform better, and there are specific courses on the PGA tour schedule that reward players with the most experience on that course. 
3. **Hypothesis #3:** There are specific courses on the PGA tour schedule in which it is important to be “hot with the putter” (have high strokes gained - putting statistic).

## 🧱 Explanation of PGA Tour Dataset

### 🔗 Data Source

The data used for the analysis was initially obtained from [advancedsportsanalytics.com](http://advancedsportsanalytics.com/), which is now offline. However, the dataset is still available thanks to a [Kaggle.com](http://kaggle.com/) user who has uploaded it. The dataset can be accessed through the following link:

https://www.kaggle.com/datasets/robikscube/pga-tour-golf-data-20152022

### 🧹 Data Cleaning Process

Upon my first examination of the dataset, I observed that several of the earlier tournaments lacked strokes gained data. To avoid omitting important data from these tournaments in my analysis of course experience, I decided to create two separate DataFrames for my analysis. One of the DataFrames excluded tournaments without strokes gained information, while the other included a value of 0 for all missing strokes gained data. This way, I could still analyze the other relevant data from those tournaments.

### *️⃣ Overview of Data Cleaning Steps

1. Dropped empty variables
2. Dropped undesired variables
3. Identified and changing identifying variables
4. Addressed missing values in the full dataset
5. Created a new stroked gained DataFrame
6. Created a “total rounds” and “course experience” variables

### 📘 PGA Tour Data Dictionary

| Variable | Description | Data Type |
| --- | --- | --- |
| Player_initial_last | Initial of player's first name and their full last name | string |
| player | The player's full name | string |
| player id | A unique ID assigned to each individual player | string |
| tournament name | The name of a tournament | string |
| tournament id | A unique ID assigned to each individual tournament | string |
| course | The name of the course the tournament is being played at | string |
| date | The date the tournament is being played | string |
| season | The year the tournament is being played | string |
| purse | The total prize money available for the tournament | float |
| hole_par | The number of stroke expected for a player to get throughout tournament | integer |
| strokes | The actual number of stroke the player had over the course of a tournament | integer |
| n-rounds | The number of golf round a player completed in a tournament | integer |
| made_cut | Whether a player made the cut after the second round to continue onto the weekend rounds | integer |
| Finish | The position a player finished in a tournament (indicates whether they tied for that position) | string |
| pos | The numerical position a player finished (exclusing whether they tied for that position) | float |
| no_cut | Whether or not the event included a cut after the first two days | integer |
| sg_putt | Strokes gained: putting | float |
| sg_arg | Strokes gained: around the green | float |
| sg_app | Strokes gained: approach the green | float |
| sg_ott | Strokes gained: off the tee | float |
| sg_t2g | Strokes gained: tee to green | float |
| sg_total | The total strokes gained over the round | float |
| total round | The total number of rounds a player has completed on a given golf course between the 2015 and 2021 season to be used as a reference for their performance in the 2022 season | integer |
| course experience | The label assigned to a player in the 2022 season based on the experience they had with the course between the 2015 and 2021 seasons | string |


