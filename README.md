# Upgrade Propensity Model

## Overview

This project focuses on predicting customer upgrade propensity based on provided data. The task includes data exploration, cleaning, feature engineering, model building, and performance evaluation. The project utilizes logistic regression, random forest, and XGBoost algorithms to identify the most effective model for predicting customer upgrades.

## Problem Statement

The goal is to predict which customers are most likely to upgrade their services. Using the provided dataset, the task is to build a model that identifies customers with the highest propensity to upgrade, enabling targeted marketing and retention strategies.

## Task List

1. **Data Exploration, Cleaning, and Feature Engineering:**
   - Explore the dataset to understand its structure and content.
   - Clean the data by addressing missing values, outliers, and inconsistencies.
   - Engineer features to improve model performance.

2. **Explanatory Analysis:**
   - Analyze the data to uncover key insights and trends.
   - Document key features and their importance in predicting upgrades.

3. **Modeling/Training:**
   - Implement and train logistic regression, random forest, and XGBoost models.
   - Evaluate model performance using relevant metrics, with a focus on recall due to the classification nature of the problem.

4. **Documentation and Reporting:**
   - Summarize findings and provide actionable insights for business strategies based on model performance.

## Project Files

- **`DATA.xlsx`**: Contains sample data used for analysis and model building.
- **`UPGRADES.xlsx`**: Additional data related to customer upgrades.
- **`CustomerUpgradePrediction.ipynb`**: Jupyter notebook with code for data exploration, cleaning, feature engineering, and model training.
- **`result.csv`**: Output file containing the results of the model predictions.
- **`README.md`**: Documentation for the project.

## Data Exploration, Cleaning, and Feature Engineering

1. **Data Exploration:**
   - Conducted exploratory data analysis to understand the dataset’s structure and content.
   - Identified key features and their distributions.

2. **Data Cleaning:**
   - Addressed missing values through imputation or removal.
   - Handled outliers and corrected any inconsistencies.

3. **Feature Engineering:**
   - Created features such as average spend, voice off-net duration, number of upgrades, and calls to customer care counts.
   - Applied transformations to enhance model performance.

## Explanatory Analysis

- **Key Insights:**
  - Important features for predicting customer upgrades include `AVERAGE_SPEND`, `VOICE_OFFNET_DUR_L3M`, `NUM_OF_UPGRADES`, and `CALLS_CARE_CNTS_L6M`.
  - Coefficients for these features indicate their influence on predicting upgrades, with positive coefficients predicting class 1 and negative coefficients predicting class 0.

## Modeling/Training

1. **Model Building:**
   - Implemented logistic regression, random forest, and XGBoost algorithms.
   - Focused on recall as the primary performance metric to maximize the detection of upgrade propensity.

2. **Model Evaluation:**
   - Logistic Regression: Achieved a recall of 0.66, indicating the model successfully classifies 66% of the upgrade instances. Despite a lower precision of 0.23 and an F1-score of 0.35, the model's recall performance is deemed acceptable for this task.
   - Random Forest and XGBoost: Both models showed signs of overfitting compared to logistic regression.

## Key Findings and Recommendations

- **Feature Importance:**
  - `AVERAGE_SPEND`, `VOICE_OFFNET_DUR_L3M`, `NUM_OF_UPGRADES`, and `CALLS_CARE_CNTS_L6M` are crucial for predicting customer upgrades. These features should be prioritized in any customer targeting or marketing strategy.

- **Model Performance:**
  - Logistic regression provides a good balance between recall and complexity, making it the preferred model despite its lower precision and F1-score.
  - Consider using logistic regression for predicting customer upgrades, given its performance and interpretability.

- **Business Recommendations:**
  - Focus on customers with high values in key features such as average spend and recent interactions with customer care.
  - Use the model's predictions to tailor marketing strategies and retention efforts, aiming to convert high-propensity customers.

## How to Run the Project

1. **Install Dependencies:**
   - Ensure all required libraries are installed. Use the `requirements.txt` file if available or install packages manually.

2. **Run the Notebook:**
   - Open `CustomerUpgradePrediction.ipynb` in Jupyter Notebook.
   - Execute the cells to perform data exploration, cleaning, feature engineering, and model training.

3. **View Results:**
   - Check `result.csv` for the model’s predictions and output.

## Author

Ramesh S
