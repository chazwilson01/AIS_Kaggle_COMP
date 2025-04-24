# 🧠 Spinal Cord Injury Recovery Prediction - Kaggle Competition

## Overview

This repository contains my solution for the [Spinal Cord Injury Functional Recovery Prediction Challenge](https://www.kaggle.com/competitions/spinal-cord-injury-functional-recovery-prediction), hosted by the American Spinal Cord Injury Association (ASIA). The goal of the competition is to predict long-term walking function 6–12 months after a traumatic spinal cord injury using data collected during the acute phase (within the first month of injury).

## 🩺 Challenge Background

Spinal cord injury can drastically alter an individual's function and independence. Accurate early prediction of long-term outcomes is critical for guiding rehabilitation strategies, counseling patients and families, and optimizing care.

This challenge involves predicting the **modified Benzel classification**, an ordinal walking score, based on clinical data collected one week post-injury. Participants were provided anonymized patient data from the Sygen clinical trial, including:

- ISNCSCI motor and sensory assessments
- Surgical and comorbidity information
- Demographics and medical complications

Evaluation is based on **Spearman's rank correlation coefficient** between predictions and actual outcomes on held-out test data.

## 🧠 My Approach

I used the **CatBoost** machine learning model for this competition, due to its robustness to categorical features, strong handling of missing data, and great out-of-the-box performance for tabular datasets.

### Key Steps:
- **Model**: `CatBoostClassifier` (ordinal classification treated as multiclass)
- **Evaluation Metric**: F1 Score
