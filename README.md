# Instructor Effectiveness Prediction using Machine Learning

An end-to-end machine learning project that predicts instructor effectiveness in an EdTech environment by analyzing learner outcomes, engagement metrics, and feedback data. The project demonstrates the complete data science workflow—from exploratory data analysis and feature engineering to model building, evaluation, and business interpretation.

---

## Project Overview

Online learning platforms often have multiple instructors teaching different batches of the same course. Measuring instructor effectiveness objectively can help improve learner outcomes, identify training opportunities, and support data-driven decision-making.

This project develops a machine learning model to classify instructors into effectiveness tiers based on aggregated batch-level performance metrics.

---

## Objectives

- Perform Exploratory Data Analysis (EDA)
- Define an Instructor Effectiveness Score
- Aggregate batch-level data to instructor-level
- Build a classification model to predict effectiveness tiers
- Evaluate model performance
- Interpret feature importance
- Generate business recommendations

---

## Dataset

Each record in the dataset represents a **course batch** taught by an instructor.
- <a href="https://github.com/mohdnaved04/Instructor-Effectiveness-Classification/blob/main/Assignment.xlsx">Edtech Dataset
### Identifier Features

- Batch ID
- Instructor ID
- Course ID

### Learner Outcome Metrics

- Completion Rate
- Dropout Rate
- Average Score Improvement
- Average Quiz Score

### Engagement Metrics

- Average Watch Time
- Assignment Submission Rate
- Forum Activity Rate

### Feedback Metrics

- Average Feedback Score
- Feedback Response Rate

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Machine Learning Pipeline

- Data Cleaning
- Missing Value Analysis
- Exploratory Data Analysis
- Correlation Analysis
- Feature Engineering
- Instructor-Level Aggregation
- Label Generation
- Random Forest Classification
- Model Evaluation
- Feature Importance Analysis

---

## Exploratory Data Analysis (EDA)

The dataset was explored to understand its structure, quality, and relationships before model development.

### Data Quality

- Checked dataset dimensions and feature data types.
- Examined missing values and duplicate records.
- Verified that numerical features were within expected ranges.

### Distribution Analysis

- Visualized the distribution of learner outcome, engagement, and feedback metrics.
- Identified variations in completion rates, quiz scores, and watch time across course batches.
- Reviewed feature distributions to detect skewness and potential outliers.

### Correlation Analysis

- Generated a correlation heatmap to identify relationships among numerical variables.
- Observed that learner outcome and engagement metrics showed stronger associations with instructor effectiveness than individual feedback metrics.
- Checked for multicollinearity before model training.

### Key Findings

- No major data quality issues were observed after preprocessing.
- Completion rate, assignment submission rate, and average watch time appeared to be strong indicators of instructor effectiveness.
- Feedback metrics were informative but less predictive when considered independently.
- The dataset was suitable for feature engineering and supervised classification.

## Results

A Random Forest Classifier was trained to predict instructor effectiveness across three categories: **Low**, **Medium**, and **High**.

### Model Performance

| Metric | Value |
|--------|------:|
| Accuracy | **91.67%** |
| Weighted Precision | **0.93** |
| Weighted Recall | **0.92** |
| Weighted F1-Score | **0.91** |

### Classification Performance

| Class | Precision | Recall | F1-Score |
|------|----------:|-------:|---------:|
| High | 1.00 | 0.67 | 0.80 |
| Medium | 0.86 | 1.00 | 0.92 |
| Low | 1.00 | 1.00 | 1.00 |

### Summary

- Achieved an overall **91.67% classification accuracy** on the test dataset.
- The model perfectly identified **Low** effectiveness instructors, achieving **100% precision and recall**.
- **Medium** effectiveness instructors were classified with high reliability (F1-score: **0.92**).
- Predictions for **High** effectiveness instructors were highly precise, although a few instances were classified into another category, resulting in lower recall.
- Overall, the model demonstrates strong predictive performance and can effectively distinguish instructor effectiveness tiers using learner outcomes, engagement, and feedback metrics.

---

## Key Insights

- Learner completion rate strongly influences instructor effectiveness.
- Engagement metrics such as watch time and assignment submissions are significant predictors.
- Feedback scores alone are insufficient for evaluating instructor performance.
- Combining multiple educational metrics produces more reliable predictions than relying on a single indicator.

---

## Business Applications

This model can support EdTech organizations by:

- Identifying high-performing instructors
- Detecting instructors who may benefit from additional support
- Improving learner success through data-driven interventions
- Supporting instructor development with objective performance insights

> **Note:** The model should assist decision-making rather than replace human evaluation.

---
