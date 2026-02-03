🚢 Titanic Survival Analysis
Exploratory Data Analysis (EDA)
📌 Overview

This project presents an exploratory data analysis (EDA) of the Titanic passenger dataset with the goal of identifying patterns and factors associated with passenger survival. The analysis focuses on demographic, socioeconomic, and travel-related attributes to understand how different variables influenced survival outcomes during the disaster.

📂 Dataset

Source: Kaggle — Titanic: Machine Learning from Disaster

Competition: Titanic: Machine Learning from Disaster

File Used: train.csv

Link: https://www.kaggle.com/competitions/titanic/data

The dataset contains 891 passenger records with information such as age, gender, passenger class, fare, family size, and embarkation port.

🎯 Objectives

Understand the structure and quality of the dataset

Handle missing and inconsistent data appropriately

Explore relationships between passenger attributes and survival

Identify key factors associated with survival outcomes

🧹 Data Cleaning & Preprocessing

The following preprocessing steps were applied:

Removed non-informative identifier columns (Name, Ticket, PassengerId)

Dropped the Cabin column due to a high proportion of missing values

Imputed missing age values using gender-based median imputation

Handled missing embarkation values through random sampling from existing categories

Created derived features such as age groups to improve interpretability

🛠 Feature Engineering

Age Grouping: Continuous age values were binned into meaningful categories (Child, Teen, Young Adult, Adult, Senior) to capture non-linear survival patterns.

📊 Exploratory Analysis

The analysis explores survival patterns across multiple dimensions, including:

Gender: Comparison of survival outcomes between male and female passengers

Passenger Class: Survival trends across first, second, and third class

Age & Age Groups: Distribution of age and its relationship with survival

Embarkation Port: Differences in survival outcomes by port of embarkation

Family Composition: Impact of traveling with siblings, spouses, parents, or children

Visualizations include histograms, count plots, and grouped bar charts with annotated counts and percentages for clarity.

🔍 Key Observations

Female passengers exhibited significantly higher survival rates than males

Survival likelihood decreased from first to third class

Younger passengers, particularly children, showed higher survival rates

Embarkation port showed variation in survival, likely driven by class and demographic differences


s🧰 Tools & Libraries
Python

Pandas

NumPy

Matplotlib

Seaborn