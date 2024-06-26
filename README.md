# State and UT Election Winner Education Level Prediction

## Overview

This project aims to predict the education level of winners in the recent State and UT elections across India. The dataset used for this task is sourced from the Election Commission of India website. The dataset contains various features related to the election winners, such as their party affiliation, criminal cases, total assets, and liabilities.

## Methodology

### Data Preprocessing

1. **Data Loading and Cleaning**: 
    - Loaded the training and test datasets using Pandas.
    - Removed irrelevant columns like 'Candidate' and 'Constituency ∇'.

2. **Feature Engineering**: 
    - Converted string values in 'Total Assets' and 'Liabilities' columns to numerical values using a custom function.
  
3. **Encoding Categorical Features**: 
    - Used Ordinal encoding for 'Party' and 'State' columns to convert categorical data into a numerical format.

### Model Selection and Training

1. **Model**: K-Nearest Neighbors (KNN) Classifier.
    - Utilized KNN Classifier from scikit-learn for its simplicity and effectiveness in handling classification tasks.

2. **Pipeline**: 
    - Created a pipeline that includes preprocessing steps like imputation and scaling followed by the KNN classifier.
  
3. **Cross-validation**: 
    - Employed 5-fold cross-validation for model evaluation to ensure robustness and avoid overfitting.

### Evaluation Metrics

- **F1-score**: Used F1-score as the evaluation metric to measure the model's accuracy in predicting the education level of the election winners.

## Libraries Used

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **scikit-learn**: For machine learning modeling, evaluation, and preprocessing.

## Usage

1. **Dataset**: 
    - Download the training and test dataset files from the provided paths.

2. **Execution**: 
    - Run the preprocessing code to clean and encode the data.
    - Train the KNN model using the encoded data and the defined pipeline.
    - Use cross-validation to evaluate the model and compute the F1-score.
    - Make predictions on the test data and save the results to a CSV file.

3. **Evaluation**: 
    - Evaluate the model's performance by comparing the predicted F1-score with the actual education levels.

## Output

- **Predictions**: 
    - The predictions are saved in a CSV file named `submission.csv`.
    - The file contains two columns: 'ID' and 'Education', where 'Education' is the predicted education level.

