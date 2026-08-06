# loan-default-classification

## Project Overview
This is my notebook project in Python, reading data of customer loans, the target variable being whether or not they defaulted. I make and execute multiple models to find the best one.

## Setup

bash
conda env create -f environment.yml
conda activate datascience


## Dataset
Dataset taken from https://www.kaggle.com/datasets/prakashraushan/loan-dataset

Important information about dataset, as per link:

"This dataset contains information about customer loans, including customer demographics, loan details, and default status. The dataset can be used for various data analysis and machine learning tasks, such as predicting loan default risk."

Columns include customer_age, customer_income, loan_intent, loan_grade, and more.

## Goal
My goal with this project overall is to experiment with multiple models on this dataset while also dabbling in data cleaning, exploratory analysis, feature selection and transformation. For results, I'm searching for the model that will give me the best recall while also preserving precision, f1 and accuracy, avoids overfitting, and runs in a short amount of time. 

## Models Used 
1. K Nearest Neighbors
2. Decision Trees (2 versions)
3. Random Forest (2 versions)

## Best Model
The findings of my project demonstrate that the two Random Forest models beat out the other models handily. They avoid overfitting, process in a short amount of time, and yield the best results, boasting the best overall scores. The Precision-Recall curves of the two models also reinforce this, with an AP of 0.84 (while KNN = 0.77 and DT = 0.82). 

Out of the two models, the 1st Modest RF has the more balanced output, with recall at .78, precision at .67 and F1 at .72. The 2nd model is more biased for recall, at .85, while precision is .53, and F1 .65. Assuming that False Negatives are more costly for the hypothetical loaning firm than False Positives are (fair assumption), the 2nd Hyperoptimized model is my pick for the best model of this project.

## Key Metrics
Recall: all true positives / true positives + false negatives

Precision: all true positives / true positives + false positives

Accuracy: total # of correct predictions / all predictions

F1-Score: harmonic mean of precision and recall, balancing both metrics.

Time: The time it takes a model to run.

## Future Improvements
1. More robust preprocessing pipeline
2. Use class imbalance methods
3. Add ROC-AUC 
4. Deploy a simple prediction app with Streamlit.
