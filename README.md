<p align="center">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/xgboost-%2319A96E.svg?style=for-the-badge&logo=xgboost&logoColor=white">
  <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white">
  <img src="https://img.shields.io/badge/geospatial-%2393b023?&style=for-the-badge&logo=qgis&logoColor=white">
</p>

# 🏡 Philippine Real Estate Price Predictor (Sparta Capstone)

<p align="center">
<img width="500" height="200" alt="Sparta Logo" align="center" src="https://github.com/user-attachments/assets/b2bc9012-fa31-40a3-a708-dd1c0d15e88b" />
</p>

<p align="center">
  <b>Author:</b> Lance Asher M. Elloso <br>
  <b>Pathway:</b> Data Scientist
</p>

## 📌 Overview
This project focuses on predicting real estate prices across the Philippines using machine learning. By addressing the unpredictability of local house prices, this predictive analytics solution aims to assist homebuyers, sellers, developers, and policymakers in making well-informed investments and fostering a more robust real estate market.

---

## 🔬 Research & Documentation
The full end-to-end process from data cleaning and feature engineering to model comparison is documented in the following files:

- 📓 **[View the Analysis Notebook](./SPCapstone002_LA,Elloso.ipynb)**: Contains the Python implementation, data cleaning logic, and model training cells.

- 📄 **[Download the Presentation Report (PDF)](Real_Estate_Market_Predictive_Analysis_PH_Report.pdf)**: A formal breakdown of the project objectives, methodology, and final recommendations.

---

## 📊 Dataset
The analysis utilizes the **"House Prices in the Philippines"** [dataset]( retrieved from Kaggle (originally scraped from Lamudi). It encompasses comprehensive information on local housing markets, including:
* Property Category (e.g., Commercial, Land)
* Land Size
* Building Size
* Location (Geospatial data)
* Car Space

---

## 🛠️ The Machine Learning Pipeline

### 1. Data Cleaning & Preprocessing
Real-world scraped data requires rigorous cleaning. The following steps were taken to ensure data integrity:
* **Limiting Price Values & Column Selection:** Filtering out irrelevant data to focus on core predictive features.
* **Missing Value Imputation & Car Space Handling:** Standardizing nulls and formatting features for modeling.
* **Outlier Removal:** Trimming extreme outliers that skew regression outputs.

### 2. Feature Selection & EDA
Exploratory Data Analysis was conducted to understand the underlying patterns:
* Correlation Matrices & Heatmaps
* Pair plots & Boxplots of numerical columns
* Geospatial visualization mapping property prices to locations

### 3. Model Training & Evaluation
Multiple regression algorithms were trained and cross-validated to find the most accurate predictor for the Philippine market:
* Linear Regression
* **Random Forest Regression (Top Performer)**
* **XGBoost Regressor (Top Performer)**
* Support Vector Machines (SVM)
* Neural Networks
* Elastic Net

Models were rigorously evaluated using **MAE, MSE, RMSE, R²**, and **RMSE Cross-Validation**.

---

## 🏆 Key Results & Insights

**Random Forest Regression** and **XGBoost** yielded the highest $R^2$ scores and the lowest Cross-Validated RMSE, making them the most reliable models for this dataset.

<p align="center">
<img width="700" height="500" alt="Model Result" src="https://github.com/user-attachments/assets/18c234bc-74e1-4733-b112-dd30b538f6f1" />
</p>

### 🔍 Feature Importance Analysis
Analyzing the top models revealed what truly drives property prices in the Philippines:
1. **Land Size** (Highest impact in Random Forest)
2. **Building Size**
3. **Property Category** (Specifically 'Land' and 'Commercial' categories heavily influenced the XGBoost model)
   
| Geospatial Visualization | Feature Importance |
| :---: | :---: |
| <img src="./Geospatial Distribution.png" width="450"> | <img src="/Feature Importance.png" width="450"> |
| *Shows how property prices vary across different geographic locations.* | *Land size is the top Feature that affects price.* |

---

## 🚀 Future Roadmap & Recommendations
While this project establishes a strong baseline for forecasting local house prices, future iterations will focus on:
* **Time-Series Integration:** Enhancing data collection by incorporating timestamps to monitor ongoing housing price trends and applying advanced time-series forecasting.
* **Advanced Geospatial Mapping:** Developing highly detailed and interactive geospatial visualizations to map price density across different regions in the Philippines.

*(Note: The insights from this project's data engineering pipeline will be adapted for a future **Vehicle Price Predictor** project.)*
