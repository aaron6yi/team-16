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


# 🔍 Explanation of the Visualization


### 🖼️ Visualization Explanation: Box Plots of Selected Numeric Features by Heart Disease

The box plots provide a comparative analysis of numeric features between patients with (`HeartDisease = 1`) and without (`HeartDisease = 0`) heart disease. Here’s what the data tells us:

#### **1. Age vs Heart Disease**
- Patients with heart disease tend to be slightly older on average compared to those without heart disease.
- The interquartile range (IQR) of age for both groups overlaps significantly, but the median age is higher in the heart disease group.

#### **2. RestingBP (Resting Blood Pressure) vs Heart Disease**
- The median resting blood pressure is slightly higher in patients with heart disease, but the range of values is similar for both groups.
- There are several outliers in both groups with extremely low or high blood pressure values.

#### **3. Cholesterol vs Heart Disease**
- Patients with heart disease exhibit a wider range of cholesterol levels, with some having exceptionally high values.
- The median cholesterol level is also higher for heart disease patients, though there is substantial overlap in the IQR.

#### **4. MaxHR (Maximum Heart Rate) vs Heart Disease**
- The maximum heart rate is notably lower in patients with heart disease, as indicated by the lower median and IQR in the heart disease group.
- This difference suggests that reduced maximum heart rate is a strong indicator of heart disease.

#### **5. Oldpeak (Exercise-Induced ST Depression) vs Heart Disease**
- Patients with heart disease have significantly higher Oldpeak values, indicating more exercise-induced ST segment depression.
- This feature exhibits a clear separation between the two groups, making it a strong predictor of heart disease.


### 📊 Distribution of Key Features by Heart Disease Status

This figure presents the **distribution of variables by heart disease status**, highlighting the differences between patients with and without heart disease. Each subplot visualizes the distribution of a key demographic or health-related variable using histograms and kernel density estimates (KDEs).  


#### **Key Observations**

#### **1. Sex**
- The majority of individuals with heart disease are **male (Sex = 1)**.  
- Women (Sex = 0) have a relatively lower representation among heart disease patients.  

#### **2. Chest Pain Type**
- Patients with heart disease are more likely to have specific chest pain types (e.g., **Type 0 and 3**).  
- For **Type 2**, heart disease patients are significantly fewer compared to those without heart disease.  

#### **3. Fasting Blood Sugar (FastingBS)**
- A higher percentage of patients with fasting blood sugar ≥ 120 mg/dL (**FastingBS = 1**) are diagnosed with heart disease.  
- The majority of patients without heart disease have normal fasting blood sugar levels (**FastingBS = 0**).  

#### **4. Resting Electrocardiographic Results (RestingECG)**
- RestingECG = 1 (ST-T wave abnormalities) is slightly more common among heart disease patients.  
- RestingECG = 0 (normal ECG) has a more balanced distribution between both groups.  

#### **5. Exercise-Induced Angina**
- **ExerciseAngina = 1** (presence of angina during exercise) is strongly associated with heart disease.  
- **ExerciseAngina = 0** (no angina) is more prevalent in patients without heart disease.  

#### **6. ST Slope**
- Patients with heart disease are more likely to have **ST_Slope = 0 or 1** (flat or downsloping ST segments).  
- **ST_Slope = 2** (upsloping) is more common in patients without heart disease.  

#### **7. Age**
- Heart disease patients are generally older, with peaks around **50–60 years**.  
- Younger patients (below 50) are less likely to have heart disease.  

#### **8. Resting Blood Pressure (RestingBP)**
- The distributions of RestingBP are similar for both groups, though heart disease patients show a slightly higher frequency at the higher range of blood pressure.  

#### **9. Cholesterol**
- Cholesterol levels are widely distributed for both groups, with no strong separation.  
- Very high cholesterol levels (>300 mg/dL) are more frequent among patients without heart disease.  

#### **10. Maximum Heart Rate Achieved (MaxHR)**
- Heart disease patients tend to have lower maximum heart rates (**MaxHR < 140**).  
- Patients without heart disease often achieve higher heart rates (**MaxHR > 150**).  

#### **11. ST Depression (Oldpeak)**
- Higher **Oldpeak** values (e.g., > 2) are strongly associated with heart disease.  
- Lower Oldpeak values are more common in individuals without heart disease.  

---

### **Key Features of the Heatmap**
- **Purpose**: It shows the strength and direction of linear relationships between pairs of variables.  
- **Correlation Coefficients**:  
  - Values range from **-1 to +1**:  
    - **+1**: Perfect positive correlation (both variables increase together).  
    - **-1**: Perfect negative correlation (one increases while the other decreases).  
    - **0**: No linear relationship.  
  - **Color Scale**:  
    - **Red**: Strong positive correlation.  
    - **Blue**: Strong negative correlation.  
    - **White/Neutral**: Weak or no correlation.  
- **Focus**: The last row and column show the relationship of each variable with **HeartDisease**.

---

### 🖼️ Count of Categorical Features by Heart Disease

The visualization provides insights into the distribution of key categorical features across patients with and without heart disease:

#### **1. Sex**
- A significantly higher number of males (Sex = 1) have heart disease compared to females (Sex = 0). 
- This suggests that males are more prone to heart disease.

#### **2. Chest Pain Type**
- Chest pain types `2` (non-anginal pain) and `3` (asymptomatic) are more prevalent in heart disease patients, while type `0` (typical angina) is more common in patients without heart disease.
- This indicates that specific types of chest pain are strong indicators of heart disease.

#### **3. Fasting Blood Sugar (FastingBS)**
- Patients with high fasting blood sugar levels (`FastingBS = 1`) are more likely to have heart disease compared to those with normal levels (`FastingBS = 0`).
- This reinforces the link between diabetes or hyperglycemia and heart disease.

#### **4. Resting ECG**
- Heart disease is more common in patients with certain resting ECG patterns (`RestingECG = 1` or `2`), while patients without heart disease are more evenly distributed across ECG categories.
- Abnormal resting ECG patterns are a useful diagnostic factor.

#### **5. Exercise-Induced Angina**
- Exercise-induced angina (`ExerciseAngina = 1`) is significantly more common in heart disease patients, whereas most patients without heart disease do not report this symptom.
- This highlights exercise-induced angina as a key symptom for diagnosis.

#### **6. ST Slope**
- A steep slope (`ST_Slope = 2`) is highly associated with heart disease, while patients without heart disease are more likely to have a flat slope (`ST_Slope = 1`).
- The slope of the ST segment is a critical indicator of cardiac health.

---

## 💡**General Insights**
- **Sex, Chest Pain Type, Exercise Angina, ST Slope, and MaxHR** show clear distinctions between the two groups and are strong predictors of heart disease.  
- **Age** and **Oldpeak** also demonstrate meaningful trends, with higher age and ST depression levels associated with increased heart disease risk.  
- Some variables, like **RestingBP** and **Cholesterol**, show weaker separation and may not be as predictive.  

This visualization highlights the key factors that differentiate patients with and without heart disease, offering insights for targeted diagnosis and predictive modeling.

---

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




