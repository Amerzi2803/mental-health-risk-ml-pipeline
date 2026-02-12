# mental-health-risk-ml-pipeline
End-to-end ML pipeline for mental health risk prediction with reproducible data cleaning and classification workflow.

# Mental Health Risk ML Pipeline

Predict depression risk from behavioral and demographic data using a clean, reproducible ML pipeline.

##  Hook

A model is only as good as the data you feed it. This project shows the full journey: noisy raw data → cleaning → reliable ML predictions.

##  Problem

Mental health datasets are often noisy and incomplete. Predicting depression risk reliably requires handling missing values, correcting categorical errors, and building a robust ML pipeline. Most beginner-friendly ML tutorials skip these crucial steps.

**Target Audience:** Researchers, Students, Developers, Startups.

##  Solution

- End-to-end reproducible ML pipeline  
- Data cleaning and preprocessing for realistic datasets  
- Baseline Logistic Regression + evaluation metrics  
- Optional advanced model experiments (Boosting)  
- Text-based and visual insights to understand feature importance

##  Key Features

- Clean, reusable code in Jupyter Notebooks  
- Handles missing values, categorical encoding, and numeric rounding  
- Train/test split with stratification  
- Confusion matrix & classification report  
- Modular structure for easy extension  
- Beginner-friendly + research-ready


## Model Performance

Baseline Model: Logistic Regression  

| Metric        | Score |
|--------------|--------|
| Accuracy     | 0.875  |
| Precision    | 0.56   |
| Recall       | 0.71   |
| F1 Score     | 0.62   |

The model achieves strong overall accuracy while maintaining reasonable recall for high-risk individuals, which is important in mental health screening scenarios.

## Confusion Matrix

                Predicted
                0      1
Actual 0      138     12
Actual 1       15     35

- True Negatives: 138  
- False Positives: 12  
- False Negatives: 15  
- True Positives: 35  

The model correctly identifies most non-risk individuals while capturing a significant portion of high-risk cases.

## Classification Report

              precision    recall    f1-score    support

           0       0.90      0.92       0.91        150
           1       0.56      0.71       0.62         50

    accuracy                           0.88        200
   macro avg       0.73      0.82       0.76        200
weighted avg       0.86      0.88       0.87        200


##  Architecture Overview

```text
Data (noisy CSV)
       │
       ▼
Data Cleaning Notebook
       │
       ▼
Cleaned Dataset CSV
       │
       ▼
ML Pipeline Notebook
       │
       ▼
Model Evaluation

