# Symptom-Based Diagnosis Predictor

## Overview

This project uses a machine learning model to predict a potential health diagnosis based on a patient's reported symptoms. It demonstrates a complete data project workflow, from data preparation with SQL to model training and evaluation with Python.

---

## Project Workflow

The project followed these key steps:

1.  **Data Generation:** A synthetic dataset of 10,000 records was generated using Gemini. This dataset simulated patient information, including demographics, various symptoms (`fever`, `cough`, `headache`, etc.), and a final `diagnose`.

2.  **Data Ingestion:** The generated data was exported to a CSV file and loaded into a raw data layer for initial storage.

3.  **Data Preparation (SQL):** An SQL script was executed to clean and transform the raw data. This process involved creating a new table, adding unique IDs (`patient_pk` and `patient_id`) for each record, and translating all relevant fields from Portuguese to English for standardization.

4.  **Modeling (Python):** Finally, a Python script loaded the prepared data to train and evaluate a `RandomForestClassifier` model, which learned to predict diagnoses based on the reported symptoms.

---

## Model Results

The model was trained on 80% of the data and tested on the remaining 20%. The key results are presented below.

### Model Accuracy

```
Model Accuracy: 0.85
```

### Classification Report

This report shows the model's performance for each diagnosis class, detailing its precision and recall.

```
                  precision    recall  f1-score   support

    Common Virus       0.69      0.72      0.70       386
  Food Poisoning       0.94      0.95      0.94       311
         Healthy       0.96      0.93      0.94       771
Seasonal Allergy       0.73      0.85      0.78       201
      Severe Flu       0.77      0.70      0.73       331

        accuracy                           0.85      2000
       macro avg       0.82      0.83      0.82      2000
    weighted avg       0.85      0.85      0.85      2000
```

### Confusion Matrix

The confusion matrix helps visualize the model's performance, showing where it made correct and incorrect predictions.

-> adicionar foto aqui

### Feature Importance

This chart illustrates which symptoms were most influential for the model's predictions.


-> adicionar foto aqui

