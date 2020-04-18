# Introduction

For the Module 3 Project, I performed a supervised binary classification exercise on a dataset to predict whether a household earns below or above the median household income in the Philippines. 

My aim as a Data Science student with this exercise is to identify the features of a household that are the strongest indicators of whether a family is earning above the median through several different modeling techniques. 

## Libraries
For data cleaning/exploration: Pandas
For plotting: Matplotlib.pyplot, Seaborn
For modeling: scikit-learn, XGBoost

# The Dataset 
The Family Income and Expenditure Survey (FIES) from 2015 is available [here on Kaggle](https://www.kaggle.com/grosvenpaul/family-income-and-expenditure) consists of over 40K rows and 60 columns and is collected by the Philippine Statistics Authority every three years. 

## Target
**Total Household Income** consists of continuous data which I initially converted into two classes (0/1), with 1 indicating that a makes above the median income. 

## Features
The 59 features are all descriptive of households through spend, household structure, possessions, and living conditions, as I categorize them below. 

* **Expenditures**: Total Food Expenditure, Bread and Cereals Expenditure, Total Rice Expenditure, Meat Expenditure, Total Fish and  marine products Expenditure, Fruit Expenditure,Vegetables Expenditure, Restaurant and hotels Expenditure, Alcoholic Beverages Expenditure, Tobacco Expenditure, Clothing, Footwear and Other Wear Expenditure, Housing and water Expenditure, Transportation Expenditure, Communication Expenditure, Education Expenditure, Miscellaneous Goods and Services Expenditure, Special Occasions Expenditure, Medical Care Expenditure, Crop Farming and Gardening expenses
* **Household Descriptions**: Region, Main Source of Income, Agricultural Household indicator, Imputed House Rental Value, Total Income from Entrepreneurial Acitivites, Household Head Sex, Household Head Age, Household Head Marital Status, Household Head Highest Grade Completed, Household Head Job or Business Indicator, Household Head Occupation, Household Head Class of Worker, Type of Household,Total Number of Family members, Members with age less than 5 year old, Members with age 5 - 17 years old, Total number of family members employed
* **Possessions**: Number of Television, Number of CD/VCD/DVD, Number of Component/Stereo set, Number of Refrigerator/Freezer, Number of Washing Machine,Number of Airconditioner, Number of Car, Jeep, Van, Number of Landline/wireless telephones, Number of Cellular phone, Number of Personal Computer, Number of Stove with Oven/Gas Range, Number of Motorized Banca, Number of Motorcycle/Tricycle
* **Living Conditions**:Type of Building/House, Type of Roof,Type of Walls, House Floor Area, House Age,Number of bedrooms, Tenure Status, Toilet Facilities, Electricity,Main Source of Water Supply,

# EDA

I eliminated 10 columns during my EDA phase in three phases. 
1) Object columns with missing values
2) Object columns with no clear correlation with Household Income based on a countplot
3) Continuous columns with very few non-zero values

I also converted several columns from object values to one-hot encoded variables where there was a high likelihood of correlation between a variable and income.

# Modeling 

I used scikit-learn's train-test split (70/30) to enable model validation for every estimator, and used Pipeline to condense normalization/estimation/grid searching for all models except for LogisticRegression.

## Logistic Regression

For my baseline model I used scikit-learn's LogisticRegression class, and normalized the data using. To improve on this estimator I used Recursive Feature Elimination to identify the top 30 variables, which I continued to use throughout the rest of my models. 

## Random Forest
Show decision tree 

## XGBoost


### Evaluation

Dataframe of the scores of each model


 - "Why did you select those visualizations and what did you learn from each of them?"
 - "Why did you pick those features as predictors?"
 - "How would you interpret the results?"
 - "How confident are you in the predictive quality of the results?"
 - "What are some of the things that could cause the results to be wrong?"