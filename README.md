# Stock Price Reaction to Earnings Announcements
Machine learning analysis evaluating whether earnings surprise metrics can predict short-term stock price movements following corporate earnings announcements.

## Overview
Financial markets often react to corporate earnings announcements, but the extent to which earnings surprises can predict short-term stock price movement remains uncertain. This project evaluates whether earnings-related variables alone can be used to forecast stock performance following earnings releases. Using historical stock market and earnings announcement data, I developed machine learning and statistical models to analyze the relationship between earnings surprises and subsequent stock price reactions.

## Business Question 
Can earnings suprise metrics reliably predict whether a stock price will increase or decrease following an earnings announcement? 

## Dataset

The analysis combines:

- Historical stock price data
- Corporate earnings announcement data
- Reported Earnings Per Share (EPS)
- Analyst EPS estimates

After merging and cleaning the datasets, several custom features were created:

- EPS Surprise
- Absolute EPS Surprise
- Surprise Percentage
- Stock Price Percentage Change
- Binary Stock Movement Indicator (Up/Down)

## Tools & Technologies

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Machine Learning, Statistical Analysis and Feature Engineering

## Methodology

### Data Preparation 
- Cleaned missing and invalid observations
- Created custom earnings surprise metrics
- Standardized features
- Split data into training and testing datasets (80/20)

### Exploratory Data Analysis
- Correlation analysis
- Scatterplots
- Summary statistics
- Earnings surprise grouping analysis

### Machine Learning Models

**Linear Regression:** Used to predict the magnitude of stock price changes following earnings announcements.

**Logistic Regression:** Used to classify whether stock prices would move up or down after earnings releases.

**Random Forest Classifier:** Applied to capture potential nonlinear relationships between earnings surprise variables and stock price movement.

**Hierarchical Clustering:** Performed exploratory segmentation of earnings events to identify patterns in market reactions.

## Results

**Linear Regression:**   

R² = -0.0004  
MAE = 0.0596  
RMSE = 0.1081

The regression model demonstrated virtually no predictive power. Results indicated that earnings surprise variables alone explained almost none of the variation in short-term stock price movement.

### Random Forest: 

Accuracy: 56.82%  
AUC: 0.58  

**Feature Importance**

Random Forest identified Surprise Percentage as the most influential predictor, suggesting that earnings surprises relative to expectations may be more informative than raw EPS differences.

### Logistic Regression:  

Accuracy: 56.34%  
AUC: 0.63  

While both models performed slightly better than random guessing, predictive performance remained limited.

## Key Findings
- Earnings surprise metrics alone are weak predictors of short-term stock price movement.
- Financial markets are influenced by many additional factors, including investor sentiment, economic conditions, industry trends, and company guidance.
- Percentage-based surprise measures contained more predictive information than raw earnings surprises.
- Machine learning models only slightly outperformed random classification, highlighting the complexity of financial forecasting.


## Future Improvements

Future iterations could incorporate:

- Trading volume
- Volatility indicators
- Analyst sentiment
- Macroeconomic variables
- Earnings call transcripts
- Financial news sentiment analysis

These additional variables may improve predictive performance and better capture market behavior surrounding earnings announcements.

### Repository Contents
Jupyter Notebook containing full analysis and modeling workflow
Final project report
Dataset used for analysis
Visualizations and model evaluation outputs

