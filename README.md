# Machine Learning Project: Breast Cancer Coimbra Diagnosis

This repository contains the midterm and final project materials for the Machine Learning course. The core objective of this project is to predict and diagnose Breast Cancer using clinical features and routine blood analysis data.

---

## 📌 Project Overview

The project relies on the **[Breast Cancer Coimbra Dataset](https://archive.ics.uci.edu/dataset/451/breast+cancer+coimbra)** from the UCI Machine Learning Repository (Patrício et al., 2018). The dataset consists of 116 instances and 9 clinical predictors gathered in routine blood analysis:

**Original Features:**
- **Age:** Age of the patient (years)
- **BMI:** Body Mass Index ($kg/m^2$)
- **Glucose:** Blood sugar level ($mg/dL$)
- **Insulin:** Insulin level ($\mu U/mL$)
- **HOMA:** Insulin resistance indicator
- **Leptin:** Adipose tissue hormone ($ng/mL$)
- **Adiponectin:** Insulin sensitivity hormone ($\mu g/mL$)
- **Resistin:** Protein associated with insulin resistance ($ng/mL$)
- **MCP.1:** Inflammation biomarker ($pg/dL$)

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
- **Threshold Optimization:** Shifted the decision thresholds (default 0.5) to maximize Accuracy and F1-scores. *(Clinical Significance: In medical diagnosis, predicting a sick patient as healthy (False Negative) is highly dangerous. Thresholds were optimized to minimize this specific risk.)*

### 🤖 Machine Learning Models Used:
- **Logistic Regression (LR)**
- **Support Vector Machines (SVM)**
- **Artificial Neural Networks (ANN / MLP)**
- **Voting Classifier (Ensemble)**

### 📈 Final Model Performances (After Threshold Optimization):
After rigorous 10-fold Cross-Validation and threshold tuning, the models achieved the following improvements on the test set:

| Model | Accuracy | F1-Score | Highlights |
| :--- | :---: | :---: | :--- |
| **Logistic Regression** | `81.82%` | `84.62%` | - |
| **Voting Ensemble** | `81.82%` | `84.62%` | AUC: `0.8333` |
| **ANN (MLP)** | `81.82%` | `85.71%` | Dramatic improvement from 68.18% (Acc) & 72.00% (F1) |
| **Support Vector Machines (SVM)** | `77.27%` | `81.48%` | Improved from 80.00% (F1) |

### 📂 Final Project Documents (`final/` and `docs/` folders):
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

### 📂 Midterm Project Documents (`vize/` and `docs/` folders):
- `*.ipynb`: The Jupyter Notebook containing the initial EDA and baseline models.
- `*.pdf`: Midterm project report detailing the initial findings and data understanding.

---

## 📁 Repository Structure

```text
📦 MachineLearning_project
 ├── 📂 data/
 │   └── 📜 dataR2.csv
 ├── 📂 docs/
 │   ├── 📕 midterm_report.pdf
 │   ├── 📕 final_report.pdf
 │   ├── 📕 academic_article.pdf
 │   └── 📕 final_presentation.pdf
 ├── 📂 final/
 │   └── 📜 final_model_training.ipynb
 ├── 📂 vize/
 │   └── 📜 midterm_analysis.ipynb
 ├── 📜 .gitignore
 └── 📜 README.md
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
