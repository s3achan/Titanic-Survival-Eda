# 🚢 Titanic Survival Analysis – Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project presents an exploratory data analysis (EDA) of the Titanic passenger dataset with the goal of identifying patterns and factors associated with passenger survival. The analysis focuses on demographic, socioeconomic, and travel-related attributes to understand how different variables influenced survival outcomes during the disaster.

## 📂 Dataset

- **Source**: Kaggle – Titanic: Machine Learning from Disaster  
- **File used**: `train.csv`  
- **Records**: 891 passengers  
- **Link**: [https://www.kaggle.com/competitions/titanic/data](https://www.kaggle.com/competitions/titanic/data)

### Main features
- `Survived` (target): 0 = No, 1 = Yes  
- `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)  
- `Sex`  
- `Age`  
- `SibSp`: # of siblings / spouses aboard  
- `Parch`: # of parents / children aboard  
- `Fare`  
- `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)  
- `Cabin`, `Name`, `Ticket`, `PassengerId`

## 🎯 Objectives

- Understand dataset structure, quality and completeness  
- Clean and prepare the data for meaningful analysis  
- Identify strong patterns and relationships with survival  
- Highlight the most influential factors on survival probability  
- Create clear, publication-quality visualizations

## 🧹 Data Cleaning & Preprocessing

Performed steps:

- Dropped non-informative / high-cardinality columns: `PassengerId`, `Name`, `Ticket`  
- Removed `Cabin` column (≈77% missing values)  
- Imputed missing `Age` values using **median age per gender and class**  
- Imputed the 2 missing `Embarked` values using random sampling from observed distribution  
- Converted `Survived` and `Pclass` to appropriate types when needed  
- Created new derived features (see below)

## 🛠 Feature Engineering

- **AgeGroup**: Binned continuous age into meaningful categories  
  - Child (0–12)  
  - Teen (13–19)  
  - Young Adult (20–29)  
  - Adult (30–49)  
  - Senior (50+)  


## 📊 Exploratory Data Analysis – Key Visualizations

Explored survival patterns through:

- Gender distribution and survival rates  
- Passenger class vs survival (strongest socioeconomic signal)  
- Age distribution + survival by age group  
- Survival by embarkation port  
- Interaction effects: gender × class, class × age group, etc.

Visual styles used:
- Count plots with hue = Survived  
- Bar plots showing survival percentages  
- Histograms + KDE for age 
- Grouped bar charts with value annotations

## 🔍 Key Findings

1. **Gender** was the strongest single predictor  
   → Females: ~74% survival  
   → Males: ~19% survival

2. **Passenger Class** showed clear social stratification  
   → 1st class: ~63% survival  
   → 2nd class: ~47%  
   → 3rd class: ~24%

3. **Women and children first** policy is visible in the data  
   - Very high survival among 1st & 2nd class females and children  
   - Extremely low survival for 3rd class adult males

4. **Age effect** is non-linear  
   - Children had better survival rates  
   - Elderly passengers had very low survival

5. **Embarkation port** showed differences (mostly proxy for class & nationality)  
   - Cherbourg (C) → highest survival rate (~55%)  
   - Southampton (S) → lowest (~34%)

## 🧰 Technologies & Libraries

```text
Python 3.8+
├── pandas               → data manipulation & cleaning
├── numpy                → numerical operations
├── matplotlib           → base plotting
├── seaborn              → statistical visualizations
└── jupyter              → interactive notebook environment
