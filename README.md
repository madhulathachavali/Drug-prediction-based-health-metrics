# Drug-prediction-based-health-metrics

## Dataset Description
This dataset contains 200 rows and 6 columns. It is used to predict the type of drug prescribed to a patient based on various health-related features. Source: Kaggle

Age: The age of the patient (numeric).

Sex: The gender of the patient. This is a categorical variable with two possible values: F (Female), M (Male)

BP (Blood Pressure): The blood pressure level of the patient, which is a categorical variable with three possible levels: HIGH, LOW, NORMAL

Cholesterol: The cholesterol level of the patient, a categorical variable with two possible values: HIGH, NORMAL

Na_to_K (Sodium-to-Potassium Ratio): A numeric value representing the ratio of sodium to potassium levels in the patient's blood.

Drug: The target variable, indicating the type of drug prescribed to the patient. This is a categorical variable with the following classes: drugA, drugB, drugC, drugX
and drugY

## Summary statistics: 
Age: The patients' ages range from 15 to 74, with a mean age of 44.32 years.

Na_to_K: The sodium-to-potassium ratio varies between 6.27 and 38.25, with a mean of 16.08.

Drug: The target variable is imbalanced: drugY being the most common (91), drug X (54), drug A (23), drug B (16) and drug C (16)

Sex: The dataset contains slightly more male patients (M: 104) than female patients (F: 96).

BP: HIGH (77) blood pressure is the most common, followed by LOW(64) and NORMAL(59) blood pressure.

Cholesterol: HIGH (103) cholesterol is slightly more common than NORMAL (97) cholesterol levels.

<img width="1151" alt="image" src="https://github.com/user-attachments/assets/a11e5ad6-fca8-499d-863e-9051c2038538" />

## Model Overview

Using the health-related variables Age, Sex, BP (Blood Pressure), Cholesterol levels, and Na_to_K (Sodium-to-Potassium ratio), models are developed to predict the Drug prescription (the dependent variable) for patients. The target variable, Drug, represents the prescribed medication, and the goal is to build predictive models that accurately classify the type of drug prescribed based on these health metrics. To achieve this, various machine learning models, including Decision Trees, Random Forests, and XGBoost, were employed, with particular attention given to model performance and addressing the imbalanced dataset.


## Summary of Results:
### Decision Tree:

Accuracy: 1.0000 (perfect on test set)
Cross-validation accuracy: 0.9938 (slightly lower, indicating minimal overfitting)
Classification report: Precision, recall, and F1-score all 1.00 for all classes.

### Random Forest:

Accuracy: 1.0000
Cross-validation accuracy: 0.9938 (similar to Decision Tree)
Classification report: Precision, recall, and F1-score all 1.00 for all classes.

### XGBoost:

Accuracy: 0.9750 (slightly lower than Decision Tree and Random Forest)
Classification report: Precision 1.00 for most classes, but recall for class 2 is 0.80, indicating some misclassification.

While all models show excellent performance on the test set (accuracy near 100%), the slight drop in cross-validation accuracy and minor misclassification (class 2 in XGBoost) suggests overfitting. More data could help improve generalization and reduce overfitting, especially for underrepresented classes.

## Prediction on New Patient: 
Based on the health metrics of the patient (Age: 45, Sex: Male, Blood Pressure: High, Cholesterol: High, Sodium-to-Potassium ratio: 15.5), the predicted prescription drug is drugY. This prediction was made using the trained Random Forest model, which classifies the drug prescription based on the input health variables.











