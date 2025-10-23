# Tanzanian-Water-Well-Classification--Phase-3-Project
# Tanzanian Water Well Classification — Phase 3 Project  

### Using Machine Learning to Improve Access to Clean Water in Tanzania

This project applies machine learning and data analysis to predict the functionality of water wells across Tanzania.  
By identifying non-functional and at-risk wells, it enables stakeholders — including the Tanzanian Ministry of Water and NGOs — to make data-driven decisions on maintenance and resource allocation.

---

## Project Overview  

Access to safe and reliable water remains a critical issue in Tanzania.  
This project leverages the Tanzania Water Point Mapping dataset to classify wells into three groups:

- Functional  
- Functional Needs Repair  
- Non-Functional  

By training predictive models on well characteristics, we aim to predict well status and support preventive maintenance strategies.

---

## Objectives  

1. Explore and visualize key factors affecting water well functionality.  
2. Build and compare machine learning models for classification.  
3. Recommend practical interventions for improving water well reliability.  

---

## Data Overview  

The dataset contains well attributes such as:
- GPS coordinates  
- Water quality  
- Installation year  
- Management type  
- Construction material  

The target variable is `status_group`.

---

## Exploratory Data Analysis (EDA)

### 1. Distribution of Target Classes
<p align="center">
  <img src="images/Distribution%20of%20Target%20Classes.png" width="500">
</p>

**Interpretation:**  
Most wells are functional, but a significant proportion are non-functional or need repair.  
This imbalance impacts model training and evaluation.

---

### 2. Water Quality vs Status Group
<p align="center">
  <img src="images/Water%20Quality%20vs%20Status%20%20Group.png" width="500">
</p>

**Interpretation:**  
Wells with poor or salty water quality are often non-functional.  
This suggests a link between contamination, equipment degradation, and well failure.

---

### 3. GPS Height vs Status Group
<p align="center">
  <img src="images/GPS%20Height%20vs%20Status%20%20Group.png" width="500">
</p>

**Interpretation:**  
Wells in low-altitude regions tend to fail more frequently, possibly due to salinity or groundwater issues.

---

## Modeling  

The models trained were:
- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier (Best Model)

### Model Comparison by F1 (Macro)
<p align="center">
  <img src="images/Model%20Comparison%20by%20F1(Macro).png" width="500">
</p>

**Interpretation:**  
The Random Forest model achieved the highest F1-score, balancing precision and recall effectively.  
It outperformed both Logistic Regression and Decision Tree models.

---

## Model Evaluation  

### Confusion Matrix (Random Forest)
<p align="center">
  <img src="images/Confusion%20Matrix.png" width="500">
</p>

**Interpretation:**  
The Random Forest model correctly classifies most functional wells.  
Misclassifications mainly occur between “needs repair” and “non-functional,” which are closely related operationally.

---

### Precision–Recall Curve (Non-Functional Wells)
<p align="center">
  <img src="images/Precision%20Curve.png" width="500">
</p>

**Interpretation:**  
The Random Forest maintains high precision and recall for detecting non-functional wells,  
which is essential for early maintenance alerts.

---

### ROC Curve (All Models)
<p align="center">
  <img src="images/ROC%20Curve.png" width="500">
</p>

**Interpretation:**  
The Random Forest has the highest AUC, confirming its superior performance across all well categories.

---

## Insights and Recommendations  

### Key Findings
1. Management type, construction quality, and geographic location strongly influence functionality.  
2. Water quality and installation year are important predictors of well failure.  
3. The Random Forest model performed best with approximately 78% accuracy and balanced class prediction.

### Recommendations
- Prioritize preventive maintenance for wells predicted as needs repair or non-functional.  
- Focus on low-altitude and poor-water-quality regions for inspection and resource allocation.  
- Use the Random Forest model for real-time risk prediction.  
- Deploy the model as a Flask or Streamlit app for field teams to access through mobile devices.  

---

## Next Steps  
- Develop a simple Flask web app for prediction.  
- Integrate real-time data input from inspection teams.  
- Address data imbalance with SMOTE or cost-sensitive modeling.  
- Expand model use to other East African regions.  

---

## Tools and Technologies  

| Category | Tools Used |
|-----------|-------------|
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Deployment | Flask |
| Environment | Jupyter Notebook, Visual Studio Code |

---

## Author  

**Diana Aloo**  
Data Analyst | Machine Learning Enthusiast  
Nairobi, Kenya  

---

<p align="center">
  <i>“Empowering clean water access through data-driven decisions.”</i>
</p>








