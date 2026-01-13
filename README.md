# ML-Heart-Disease-Prediction
Heart Disease Prediction using the Cleveland Dataset​

## 📌 Project Overview

This project applies machine learning techniques to the **Cleveland Heart Disease dataset** to predict the presence of heart disease in patients. The goal is to build a reliable classification model that can distinguish between patients with and without heart disease based on medical attributes.

The project covers the full data science lifecycle: data cleaning, exploratory data analysis (EDA), model building, and result interpretation using SHAP values.

## 📂 Dataset

The dataset used is the **Cleveland Heart Disease dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/45/heart+disease).

* **Source:** UCI Machine Learning Repository
* **Rows:** 297 (after preprocessing)
* **Columns:** 14 (13 features + 1 target)
* **Target Variable:** `num` (converted to binary: 0 = No Disease, 1 = Disease)

### Key Features

* **Age** & **Sex**
* **Chest Pain Type (cp)**
* **Resting Blood Pressure (trestbps)**
* **Cholesterol (chol)**
* **Max Heart Rate Achieved (thalach)**
* **Exercise Induced Angina (exang)**
* **ST Depression (oldpeak)**
* **Number of Major Vessels (ca)**
* **Thalassemia (thal)**

## 🛠️ Technologies & Libraries

* **Python 3**
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Visualization)
* **Scikit-Learn** (Modeling & Evaluation)
* **SHAP** (Model Interpretation)

## 📊 Methodology

1. **Data Preprocessing:**
* Handled missing values (e.g., in `ca` and `thal` columns).
* Converted the multi-class target (0-4) into a binary classification problem.


2. **Exploratory Data Analysis (EDA):**
* Analyzed feature distributions and correlations.
* Visualized class balance (approx. 54% No Disease vs. 46% Disease).


3. **Model Training:**
* Tested multiple algorithms including **Logistic Regression**, **Random Forest**, **K-Nearest Neighbors (KNN)**, and **Support Vector Machines (SVM)**.
* Used **PCA** and **t-SNE** for dimensionality reduction and visualization.


4. **Evaluation & Interpretation:**
* Evaluated models using Accuracy, Precision, Recall, and ROC-AUC.
* Interpreted model decisions using **Feature Importance** and **SHAP values**.


## 📈 Key Results
* **Feature Importance:** The Random Forest model identified **Thalassemia (thal)**, **Chest Pain Type (cp)**, and **Number of Major Vessels (ca)** as the strongest predictors of heart disease.
* **Medical Relevance:** SHAP analysis showed that higher age and specific chest pain types push predictions toward the positive class, aligning with established medical knowledge.
* **Performance:** The models successfully learned meaningful patterns, providing consistent evidence that the predictions are medically sound.
  

## 🚀 Future Work
* Test advanced ensemble models like **XGBoost** or **LightGBM** to potentially boost accuracy.
* Experiment with domain-informed feature engineering.
* Deploy the model as a simple web app using Streamlit.
  

## 💻 How to Run

1. Click the badge above to open the notebook in Google Colab.
2. Run the cells sequentially to download the dataset and execute the analysis.
3. Alternatively, clone this repo and run the Jupyter Notebook locally:
```bash
git clone https://github.com/your-username/my-final-project.git
cd my-final-project
jupyter notebook Project_1.ipynb
