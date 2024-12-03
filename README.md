<div style="display: flex; gap: 20px;">
  <img src="https://learn.utoronto.ca/themes/custom/de_theme/logo.svg" alt="UofT Logo" height="50">
  <img src="https://datasciences.utoronto.ca/wp-content/uploads/2021/12/Logo.png" alt="Data Sciences Logo" height="50">
</div>

# UofT | DSI - Team 16 Project: 🔎 Heart Failure Prediction


---

## 🔍 Research Question
**What demographic and health-related factors significantly predict the occurrence of heart failure in patients?**

---

## 🎯 Project Overview
Heart disease is a serious health concern, and early detection is critical for better outcomes. In this project, we’re working with a dataset containing 11 clinical features to figure out which factors are most important in predicting heart disease. Our goal is to create a machine learning model that’s not only accurate but also easy to use, relying on basic patient information. This way, we can potentially eliminate the need for complex and invasive tests, making heart disease screening more accessible to everyone.
---

## 📊 Dataset
**Dataset Source:** [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction/data)  
This dataset includes:
- **11 features**: 2 demographic and 9 health-related factors
- **Binary classification**: 1 (Heart Disease) or 0 (Normal)

---

## 👥 Contributions

| Task                             | Team Member |
|----------------------------------|-------------|
| Data Cleaning                    | Emily       |
| Data Visualization               | Brigette    |
| Data Splitting & Framework Setup | Ada         |
| Initial Model Development        | Aaron       |

---

## 💡 Key Takeaways for Heart Disease Prediction

The findings from the EDA analysis highlight the following factors as significant predictors of heart disease:

### **1. Demographic Factors**
- **Sex:** Men are at a notably higher risk compared to women.
- **Age:** The risk of heart disease peaks in individuals aged 50–60.

### **2. Health-Related Factors**
- **Fasting Blood Sugar (FastingBS):** Elevated blood sugar levels strongly correlate with diabetes and heart disease.
- **Chest Pain Type:** Certain types, like atypical angina, are strong indicators of heart disease.
- **Exercise-Induced Angina:** A critical symptom highly associated with heart disease.
- **Maximum Heart Rate (MaxHR):** Lower maximum heart rates are indicative of higher risk.
- **ST Segment Changes (Oldpeak & ST Slope):** Abnormal ST depression and slope values signal potential cardiac issues.

These insights lay a strong foundation for understanding heart disease and building predictive models. By targeting these key factors, we can enhance risk assessment, prevention, and treatment strategies.


## 🏗️ Project Folder Structure

```plaintext
|-- data/
|   |-- raw_data/
|   |   |-- heart.csv
|   |-- cleaned_data/
|       |-- heart_cleaned.csv
|-- src/
|   |-- notebooks/
|       |-- EDA_visualization.ipynb
|       |-- HeartDiseasePredictionModel.ipynb
|       |-- HeartDiseasePredictionModel_pyspark.ipynb
|   |-- data_cleaning.ipynb
|-- README.md

---




