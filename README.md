## Project 2: Trojan Horse Network Traffic Detection

## Project Description
This project applies data mining and machine learning techniques to detect **Trojan horse network traffic**. The goal is to classify network flows as either **Trojan** or **Benign** based on traffic features extracted from network data.

The project follows a complete data mining pipeline including:
- data auditing and preprocessing
- feature reduction and selection
- training and comparing multiple classifiers
- selecting the best model for final evaluation
- generating predictions for a class competition

This work was completed as part of **CSE 632 – Data Mining** at the
University of Louisville.


## Dataset
The dataset contains approximately **160,000 samples** with **85 features** and a binary target variable (`Class`: Trojan or Benign).

Due to file size limitations, the datasets are **not stored in this GitHub repository**.

You can download the datasets from the links below:

** dataset**:  
 <(https://www.kaggle.com/datasets/rupaghosh/trojan-dataset)>


## Project Workflow
1. **Data Audit**
   - checked missing values
   - analyzed feature types
   - examined class distribution
   - detected constant, near-zero variance, and ID-like features
   - analyzed feature correlations

2. **Data Preprocessing**
   - removed constant, NZV, and ID-like features
   - handled missing values using median/mode
   - scaled numeric features using RobustScaler
   - removed highly correlated features

3. **Dimensionality Reduction**
   - step 1: domain-based feature cleaning
   - step 2: feature selection using Mutual Information (top 25 features)

4. **Model Training & Evaluation**
   - logistic regression
   - random forest
   - xgboost
   - evaluation metrics: accuracy, f1-score, roc-auc

5. **Final Model Selection**
   - XGBoost achieved the best ROC-AUC
   - the trained XGBoost model was saved and used for the class competition


## Best Model
**XGBoost** was selected as the final model because it achieved the highest ROC-AUC score and handled complex, nonlinear patterns in the data better than the other models.

## how to run
1. download the datasets CSVs and place them inside the `data/` folder
2. run scripts from the `src/` directory
3. all generated files (cleaned data, figures, models, predictions) will be saved in the `output/` folder

## Notes
- Raw datasets are not included in this repository.
- Model files (`.joblib`) are generated locally and excluded from GitHub.
- This repository focuses on **reproducibility and clarity** of the data
  mining workflow.
