

# UofT | DSI - Team 16 Project: ❤️‍🩹 Heart Failure Prediction


---

## ❓ Research Question
**What demographic and health-related factors significantly predict the occurrence of heart failure in patients?**

---

## 🎯 Project Overview
Heart disease is a serious health concern, and early detection is critical for better outcomes. In this project, we’re working with a dataset containing 11 clinical features to figure out which factors are most important in predicting heart disease. Our goal is to create a machine learning model that’s not only accurate but also easy to use, relying on basic patient information. This way, we can potentially eliminate the need for complex and invasive tests, making heart disease screening more accessible to everyone.

---

## 📂  Dataset
**Dataset Source:** [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction/data)  
This dataset includes:
- **11 features**: 2 demographic and 9 health-related factors
- **Binary classification**: 1 (Heart Disease) or 0 (Normal)

---

## 👨‍💻 Contributions

| Task                             | Team Member |
|----------------------------------|-------------|
| Data Cleaning                    | Emily       |
| Data Visualization               | Brigette    |
| Data Splitting & Framework Setup | Ogechi      |
| Machine Learning Development     | Aaron       |

---

## 📊 Exploratory Data Analysis

**We compared the distribution of features for patients with and without heart disease. Each feature's role in distinguishing between the two groups was visualized using histograms and kernel density estimation plots (KDE).**

![Distribution of Variables by Heart Disease](./pics/Distribution%20of%20Variables%20by%20Heart%20Disease.png)


### Observations

- **ChestPainType**: Certain types strongly correlate with heart disease.
- **Fasting Blood Sugar**: Elevated levels (coded as 1) are more common in heart disease patients.
- **ExerciseAngina**: A critical indicator, with a strong link to heart disease.
- **Oldpeak**: Higher values strongly associate with heart disease.

---
## 👫 Gender-Based Analysis
**How do risk factors differ between genders?**

![Categorical Features Distribution by Gender](./pics/Categorical%20Features%20Distribution%20by%20Gender.png)

### Insights

- **ChestPainType**: Typical angina (TA) is more common in males with heart disease, while females tend to present with non-typical angina (NAP) or asymptomatic (ASY) pain types.
- **FastingBS**: High fasting blood sugar is a stronger risk factor for heart disease in males, while it is less pronounced in females.
- **RestingECG**: Abnormal ST readings are frequent in both genders, but females show a higher proportion of Left Ventricular Hypertrophy (LVM).
- **ExerciseAngina**: Males with heart disease frequently report exercise-induced angina, while females are less likely to exhibit this symptom, potentially leading to under-diagnosis.
- **ST_Slope**: A downward slope is a strong and consistent indicator of heart disease across genders, though males show a higher prevalence of this marker.



## 📈 Proportion of Features in Heart Disease Cases
**The analysis focused on key features that differentiate individuals with heart disease, aiming to identify the most reliable indicators for early diagnosis and prediction.**

![Proportion of Each Variable in Heart Disease Cases](./pics/Proportion%20of%20Each%20Variable%20in%20Heart%20Disease%20Cases.png)


### Insights:

- **ChestPainType**: typical angina is the most common type (77.2%) in heart disease cases, making it a reliable marker, while other types like non-anginal pain or asymptomatic chest pain are less prevalent.  
- **ExerciseAngina**: reported by 62.2% of patients, exercise-induced angina is a critical indicator of heart disease risk.  
- **ST_Slope**: a flat ST slope (75.0%) is the most frequent, followed by downward slopes (15.4%), both of which are strongly associated with heart disease.  
- **RestingECG**: ST-T wave abnormalities (56.1%) are the most common finding, emphasizing their diagnostic importance.  
- **Fasting Blood Sugar**: elevated levels (33.5%) highlight its role as a metabolic risk factor for heart disease.  

## 🧑‍🤝‍🧑 Demographic Insights
- **Age and Gender Imbalance**: Most cases involve middle-aged to older men. This could influence model predictions and requires careful consideration for bias mitigation.


<div style="display: flex; justify-content: space-around; align-items: center;">

<img src="./pics/Heart Disease Distribution by Age Group.png" alt="Heart Disease Distribution by Age Group" height="270px">

<img src="./pics/Heart Disease Count by Gender.png" alt="Heart Disease Count by Gender" height="270px">

</div>

---

## 🤖 Heart Failure Prediction Model

This experiment aimed to predict heart failure using three machine learning models: **Random Forest**, **XGBoost**, and **MLP (Multi-Layer Perceptron)**. The models were trained on clinical features such as **ChestPainType**, **FastingBS**, **RestingECG**, **ExerciseAngina**, and **ST_Slope**, which were identified as critical predictors during the exploratory analysis. Each model leverages unique principles for making predictions:

1. 🌲**Random Forest** is a tree-based ensemble method that builds multiple decision trees and averages their outputs to improve accuracy and reduce overfitting. It also provides interpretable feature importance scores, making it useful for understanding key predictors.

2. 📈**XGBoost** is a gradient boosting algorithm that sequentially builds trees, optimizing errors from previous iterations. It is particularly effective for handling imbalanced datasets and complex patterns in the data.

3. 🧠**MLP (Multi-Layer Perceptron)** is a feedforward neural network that captures non-linear relationships through multiple hidden layers and activation functions. It relies on backpropagation to optimize weights and minimize prediction errors.

### 🏆 Model Results

- **Accuracy**: XGBoost outperformed other models.  
- **Feature Importance**: ST_Slope, ExerciseAngina, and ChestPainType were the most predictive features.  

#### 🔍✨ Focus on Type II Error  
Among the models, **XGBoost** demonstrated a strong tendency to minimize type II errors (false negatives) in the confusion matrix. This makes it particularly valuable in clinical settings where failing to identify true heart failure cases could have severe consequences. By achieving a balance between recall and precision, XGBoost is well-suited for applications where accurate detection of high-risk patients is critical. Future work will involve testing the model on external datasets and integrating it into decision-support systems for real-world healthcare applications.

---

### 🌟 Reflections on Teamwork  
<a href="https://www.loom.com/share/a2ae9ed1c99d47f4bc0109f7436a5766?sid=6c62565c-d94e-4ad2-9897-5fcc6b811747" target="_blank">
  <img src="https://img.youtube.com/vi/6EUUGq8oldo/0.jpg" alt="Reflections on Teamwork" width="720">
</a>

---
### 💡 Project Insight
<a href="https://youtu.be/fbHedUM_ucc" target="_blank"> <img src="https://img.youtube.com/vi/fbHedUM_ucc/0.jpg" alt="Project Insight from Ogechi" width="720"> </a>

---

### 📽️ Project Overview  
<a href="https://youtu.be/CUds0OJGxjU" target="_blank">
  <img src="./pics/DSI_Project.png" alt="Project Presentation" width="720">
</a>

## 🏗️ Project Folder Structure

```plaintext
|-- data/
|   |-- raw_data/
|   |   |-- heart.csv
|   |-- cleaned_data/
|       |-- heart_cleaned.csv
|-- pics/
|   |-- Categorical Features Distribution by Gender.png
|   |-- Confusion Matrix of MLP model.png
|   |-- Distribution of Variables by Heart Disease.png
|   |-- Heart Disease Count by Gender.png
|   |-- Heart Disease Distribution by Age Group.png
|   |-- Proportion of Each Variable in Heart Disease Cases.png
|   |-- SHAP value plot.png
|-- EDA_visualization.ipynb
|-- HeartDiseasePredictionModel.ipynb
|-- HeartDiseasePredictionModel_pyspark.ipynb
|-- data_cleaning.ipynb
|-- README.md






