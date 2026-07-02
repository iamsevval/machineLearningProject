# Machine Learning Project: Breast Cancer Coimbra Diagnosis

This repository contains the midterm and final project materials for the Machine Learning course. The core objective of this project is to predict and diagnose Breast Cancer using clinical features and routine blood analysis data.

---

## 📌 Project Overview

The project relies on the **Breast Cancer Coimbra Dataset** from the UCI Machine Learning Repository (Patrício et al., 2018). The dataset consists of 116 instances and 9 clinical predictors, which include anthropometric data and parameters gathered in routine blood analysis (Age, BMI, Glucose, Insulin, HOMA, Leptin, Adiponectin, Resistin, MCP.1).

The primary goal is to accurately classify subjects into two categories:
- **0 = Healthy Controls**
- **1 = Patients with Breast Cancer**

---

## 🚀 Final Project (Advanced Implementation)

The final project extends the initial analyses by incorporating robust modeling, hyperparameter optimization, threshold tuning, and advanced data preprocessing techniques.

### 🔬 Methodology & Key Highlights:
- **Feature Engineering:** Expanded the initial 9 features to capture complex non-linear relationships within the data, creating a richer feature space for the models.
- **Data Balancing (SMOTE):** Handled the inherent dataset imbalance by applying the Synthetic Minority Over-sampling Technique (SMOTE) to the training data.
- **Hyperparameter Tuning:** Conducted extensive Grid Search over the parameter space for each model (e.g., testing `adam` vs `lbfgs` solvers for ANN) to find the absolute best configurations.
- **Threshold Optimization:** Shifted the decision thresholds (default 0.5) to maximize Accuracy and F1-scores.

### 🤖 Machine Learning Models Used:
- **Logistic Regression (LR)**
- **Support Vector Machines (SVM)**
- **Artificial Neural Networks (ANN / MLP)**
- **Voting Classifier (Ensemble)**

### 📈 Final Model Performances (After Threshold Optimization):
After rigorous 10-fold Cross-Validation and threshold tuning, the models achieved the following improvements on the test set:
- **Logistic Regression:** Accuracy: `81.82%` | F1-Score: `84.62%`
- **SVM:** Accuracy: `77.27%` | F1-Score: `81.48%` *(improved from 80.00%)*
- **ANN (MLP):** Accuracy: `81.82%` *(dramatic improvement from 68.18%)* | F1-Score: `85.71%` *(improved from 72.00%)*
- **Voting Ensemble:** Accuracy: `81.82%` | F1-Score: `84.62%` | AUC: `0.8333`

### 📂 Final Project Documents (`final_...` folder):
- `*.ipynb`: The comprehensive Jupyter Notebook containing the full Python source code, EDA, Feature Engineering, Model Training, and Threshold Optimization.
- `*_doküman.pdf`: Detailed project documentation and technical report.
- `*_makale.pdf`: Academic-style article summarizing the research, methodology, and findings.
- `*_sunum.pdf`: Presentation slides used to showcase the project.

---

## 📊 Midterm Project (Preliminary Analysis)

The midterm phase laid the groundwork for the final implementation. It focused on the preliminary Exploratory Data Analysis (EDA) and establishing baseline models to understand the dataset's predictability.

### Models Explored in Midterm:
- **Random Forest Classifier**
- **K-Nearest Neighbors (KNN)**
- **Naive Bayes (GaussianNB)**
- **Decision Tree Classifier**

### 📂 Midterm Project Documents (`midterm_...` folder):
- `*.ipynb`: The Jupyter Notebook containing the initial EDA and baseline models.
- `*.pdf`: Midterm project report detailing the initial findings and data understanding.

---

## 📁 Repository Structure

```text
📦 MachineLearning_project
 ┣ 📂 final_22040301030_Şevval_Arslan_YazılımMühendisliği_ML
 ┃ ┣ 📜 22040301030_Şevval_Arslan_YazılımMühendisliği_ML.ipynb
 ┃ ┣ 📕 22040301030_Şevval_Arslan_YazılımMühendisliği_ML_doküman.pdf
 ┃ ┣ 📕 22040301030_Şevval_Arslan_YazılımMühendisliği_ML_makale.pdf
 ┃ ┗ 📕 22040301030_Şevval_Arslan_final_sunum.pdf
 ┣ 📂 midterm_22040301030_Şevval_Arslan_YazılımMühendisliği_ML
 ┃ ┣ 📜 22040301030_Şevval_Arslan_YazılımMühendisliği_ML.ipynb
 ┃ ┗ 📕 22040301030_Şevval_Arslan_YazılımMühendisliği_ML.pdf
 ┣ 📜 .gitignore
 ┗ 📜 README.md
```

## 🛠 Technologies & Libraries Used
- **Python 3**
- **Pandas & NumPy** (Data manipulation)
- **Matplotlib & Seaborn** (Data visualization)
- **Scikit-Learn** (Machine Learning algorithms, GridSearch, Cross Validation)
- **Imbalanced-learn (SMOTE)** (Handling class imbalance)

## 💡 How to Run
1. Clone this repository to your local machine.
2. Ensure you have Python and Jupyter Notebook installed.
3. Install the required libraries (`pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn`).
4. Place the `dataR2.csv` dataset in the project directories if it's not present.
5. Open the `.ipynb` files via Jupyter Notebook or Jupyter Lab to view and run the code cells.
