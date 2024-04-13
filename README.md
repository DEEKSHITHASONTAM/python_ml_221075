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

1. **Model**: RandomForestClassifier from scikit-learn.
    - Chose RandomForestClassifier for its ability to handle categorical data and non-linearity in the dataset.
  
2. **Cross-validation**: 
    - Utilized 5-fold cross-validation for model evaluation to ensure robustness and avoid overfitting.

### Evaluation Metrics

- **F1-score**: Used F1-score as the evaluation metric to measure the model's accuracy in predicting the education level of the election winners.

## Libraries Used

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **scikit-learn**: For machine learning modeling and evaluation.

## Usage

1. **Dataset**: 
    - Download the training and test dataset files from the provided paths.

2. **Execution**: 
    - Run the preprocessing code to clean and encode the data.
    - Train the RandomForestClassifier model using the encoded data.
    - Use cross-validation to evaluate the model and compute the F1-score.

3. **Evaluation**: 
    - Evaluate the model's performance by comparing the predicted F1-score with the actual education levels.

## Restrictions

- Only the libraries mentioned in the Rules section are allowed.
- No deep learning methods/libraries are allowed (e.g., ANN, Pytorch, Keras, Tensorflow).
