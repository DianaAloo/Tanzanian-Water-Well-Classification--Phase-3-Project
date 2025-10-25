# Tanzanian Water Well Classification — Phase 3 Project

### Using Machine Learning to Improve Access to Clean Water in Tanzania

This project applies machine learning and data analysis to predict the functionality of water wells across Tanzania.  
By identifying non-functional and at-risk wells, it enables stakeholders : including the Tanzanian Ministry of Water and NGOs , to make data-driven decisions on maintenance and resource allocation.

---

##  Project Overview

Access to safe and reliable water remains a critical issue in Tanzania.  
This project leverages the **Tanzania Water Point Mapping** dataset to classify wells into three groups:

- **Functional**
- **Functional Needs Repair**
- **Non-Functional**

By training predictive models on well characteristics, we aim to predict well status and support preventive maintenance strategies.

---

##  Objectives

- Explore and visualize key factors affecting water well functionality.  
- Build and compare machine learning models for classification.  
- Recommend practical interventions for improving water well reliability.

---

## Data Overview

The dataset contains well attributes such as:

- GPS coordinates  
- Water quality  
- Installation year  
- Management type  
- Construction material  

The target variable is **`status_group`**.

---

##  Exploratory Data Analysis (EDA)

###  Distribution of Target Classes & Water Quality vs Status Group

<img width="402" height="384" alt="Distribution of Target Classes" src="https://github.com/user-attachments/assets/d0ef9e12-d1cc-46cb-a718-49a9bda10fe6" />

**Interpretation:**  
Most wells are functional, but a significant proportion are non-functional or need repair.  
Wells with poor or salty water quality are often non-functional — suggesting a link between contamination, equipment degradation, and well failure.

---

###  GPS Height vs Status Group & Model Comparison

<img width="508" height="333" alt="GPS Height vs Status Group" src="https://github.com/user-attachments/assets/49fe16fd-b1aa-41b8-a991-8972c3f283bf" />

**Interpretation:**  
Wells in low-altitude regions tend to fail more frequently, possibly due to salinity or groundwater issues.  
The Random Forest model achieved the highest F1-score, balancing precision and recall effectively.

---

##  Modeling

The models trained were:

- Logistic Regression  
- Decision Tree Classifier  
- **Random Forest Classifier (Best Model)**
- 

---

##  Model Evaluation

### Confusion Matrix & Precision–Recall Curve

<img width="428" height="357" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/ffd46ede-2e2f-4865-bdc0-4f510fd692f9" />

<img width="386" height="333" alt="Precision Curve" src="https://github.com/user-attachments/assets/b4ebca0a-1f9d-4506-9b78-32af51c2ebb4" />

**Interpretation:**  
The Random Forest correctly classifies most functional wells.  
Misclassifications mainly occur between “needs repair” and “non-functional,” which are closely related operationally.  
It maintains high precision and recall for detecting non-functional wells — essential for early maintenance alerts.

---

### ROC Curve (All Models)

<img width="497" height="387" alt="ROC Curve" src="https://github.com/user-attachments/assets/3badee37-ecd1-4857-a29a-44b990bcdc67" />


**Interpretation:**  
The Random Forest has the highest AUC, confirming its superior performance across all well categories.

---

##  Insights and Recommendations

###  Key Findings
- Management type, construction quality, and geographic location strongly influence functionality.  
- Water quality and installation year are important predictors of well failure.  
- The Random Forest model performed best with approximately **78% accuracy** and balanced class prediction.

###  Recommendations
- Prioritize preventive maintenance for wells predicted as “needs repair” or “non-functional.”  
- Focus on **low-altitude** and **poor-water-quality** regions for inspection and resource allocation.  
- Use the **Random Forest model** for real-time risk prediction.  
- Deploy the model as a **Flask** or **Streamlit** app for field teams to access through mobile devices.

---

##  Next Steps

- Develop a simple Flask web app for prediction.  
- Integrate real-time data input







