# Tanzanian Water Well Classification — Phase 3 Project

### Using Machine Learning to Improve Access to Clean Water in Tanzania

This project applies machine learning and data analysis to predict the functionality of water wells across Tanzania.  
By identifying non-functional and at-risk wells, it enables stakeholders — including the Tanzanian Ministry of Water and NGOs — to make data-driven decisions on maintenance and resource allocation.

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

<div align="center">
  <img src="images/distribution.png" alt="Distribution of Target Classes" width="45%">
  <img src="images/water_quality.png" alt="Water Quality vs Status Group" width="45%">
</div>

<p align="center">
  <em>Distribution of well functionality and the relationship between water quality and status.</em>
</p>

**Interpretation:**  
Most wells are functional, but a significant proportion are non-functional or need repair.  
Wells with poor or salty water quality are often non-functional — suggesting a link between contamination, equipment degradation, and well failure.

---

###  GPS Height vs Status Group & Model Comparison

<div align="center">
  <img src="images/gps_height.png" alt="GPS Height vs Status Group" width="45%">
  <img src="images/model_comparison.png" alt="Model Comparison by F1" width="45%">
</div>

<p align="center">
  <em>Geographical distribution of failures and model performance comparison.</em>
</p>

**Interpretation:**  
Wells in low-altitude regions tend to fail more frequently, possibly due to salinity or groundwater issues.  
The Random Forest model achieved the highest F1-score, balancing precision and recall effectively.

---

##  Modeling

The models trained were:

- Logistic Regression  
- Decision Tree Classifier  
- **Random Forest Classifier (Best Model)**

---

##  Model Evaluation

### Confusion Matrix & Precision–Recall Curve

<div align="center">
  <img src="images/confusion_matrix.png" alt="Confusion Matrix" width="45%">
  <img src="images/precision_recall.png" alt="Precision–Recall Curve" width="45%">
</div>

<p align="center">
  <em>Confusion matrix and precision–recall curve for Random Forest model.</em>
</p>

**Interpretation:**  
The Random Forest correctly classifies most functional wells.  
Misclassifications mainly occur between “needs repair” and “non-functional,” which are closely related operationally.  
It maintains high precision and recall for detecting non-functional wells — essential for early maintenance alerts.

---

### ROC Curve (All Models)

<p align="center">
  <img src="images/roc_curve.png" alt="ROC Curve for All Models" width="60%">
</p>

<p align="center">
  <em>ROC Curves showing model performance comparison.</em>
</p>

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







