# Asteroid Diameter Prediction

This repository contains a machine learning project to predict the diameter of asteroids using various regression models. The project leverages a dataset available on Kaggle that includes physical and orbital parameters of asteroids.

## Project Overview

The goal of this project is to predict the diameter of an asteroid based on features such as absolute magnitude (`H`), albedo, and other orbital parameters. The project follows these key steps:

1. **Data Inspection & Cleaning**  
   - Load and inspect the dataset.
   - Clean the data by converting columns to appropriate data types.
   - Handle missing values and outliers.

2. **Exploratory Data Analysis (EDA)**  
   - Analyze the distribution of the target variable (diameter) and apply a log transformation to address skewness.
   - Visualize relationships between features and the target using histograms, boxplots, and scatter plots.
   - Evaluate feature correlations.

3. **Feature Engineering & Selection**  
   - Engineer new features using a physics-based formula:
       `computed_diameter = 1329 / sqrt(albedo) * 10^(-0.2 * H)`
   - Create a log-transformed version of the computed diameter.
   - Select the most relevant features for the regression model based on correlation analysis.

4. **Data Splitting**  
   - Split the dataset into training (80%), validation (10%), and testing (10%) sets.

5. **Model Building**  
   - Build baseline and advanced regression models (Linear Regression, Random Forest, Gradient Boosting).
   - Evaluate models using RMSE, MAE, and R² metrics.

6. **Hyperparameter Tuning & Evaluation**  
   - Tune hyperparameters using RandomizedSearchCV.
   - Evaluate the best model on the test set and generate an accuracy report.
   - Analyze feature importances for model interpretation.

**Dataset**
   Download the dataset from Kaggle and place it in the project directory:\
   [Asteroid Dataset on Kaggle](https://www.kaggle.com/datasets/sakhawat18/asteroid-dataset)
