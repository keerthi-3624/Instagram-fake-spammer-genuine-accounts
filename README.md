# README for Instagram Account Classification Project

## Project Overview

This project aims to classify Instagram accounts as **Fake** or **Genuine** using machine learning techniques. The classification is based on various features extracted from account metadata, such as profile picture presence, username characteristics, follower counts, and more.

## Features of the Dataset

The dataset consists of two files:
- **train.csv**: Contains 576 rows and 12 columns.
- **test.csv**: Contains 120 rows and 12 columns.

### Columns in the Dataset:
1. **profile pic**: Binary indicator (1 = profile picture present, 0 = none).
2. **nums/length username**: Ratio of numerical characters to username length.
3. **fullname words**: Number of words in the full name.
4. **nums/length fullname**: Ratio of numerical characters to full name length.
5. **name==username**: Binary indicator if username matches full name (1 = yes, 0 = no).
6. **description length**: Number of characters in the bio.
7. **external URL**: Binary indicator for external URL presence (1 = yes, 0 = no).
8. **private**: Binary indicator for account privacy (1 = private, 0 = public).
9. **#posts**: Total number of posts.
10. **#followers**: Total number of followers.
11. **#follows**: Total number of accounts followed.
12. **fake**: Target variable (1 = fake account, 0 = genuine account).

## Libraries Used

The following Python libraries are used in this project:
- **pandas**: For data manipulation and handling DataFrames.
- **matplotlib.pyplot & seaborn**: For data visualization.
- **numpy**: For numerical operations.
- **sklearn.model_selection.train_test_split**: For splitting datasets into training and testing sets.
- **sklearn.preprocessing.StandardScaler**: For feature scaling.
- **sklearn.ensemble.RandomForestClassifier**: For building the classification model.
- **sklearn.metrics (accuracy_score, classification_report, confusion_matrix)**: For model evaluation.

## Workflow

### 1. Data Loading
The training and testing datasets are loaded using `pandas.read_csv()`.

### 2. Exploratory Data Analysis (EDA)
- Summary statistics are calculated to understand the distribution of data.
- Missing values are checked (none found in both datasets).
- Visualizations are created to analyze relationships between features and the target variable.

### 3. Preprocessing
Features are scaled using `StandardScaler` for better performance during modeling.

### 4. Model Building
A Random Forest Classifier is employed to classify accounts as fake or genuine.

### 5. Evaluation
The model is evaluated using metrics such as:
- Accuracy
- Confusion Matrix
- ROC Curve and AUC Score

## Results
The project successfully classifies Instagram accounts with high accuracy based on the provided features.
