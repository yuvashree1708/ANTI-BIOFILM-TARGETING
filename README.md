# Anti-Biofilm Target Prediction Using Machine Learning

This project explores a computational approach for predicting **biological targets of anti-biofilm compounds** using molecular descriptors and a gradient boosting classification model. By learning patterns between chemical structure descriptors and known protein targets, the model predicts potential targets for previously uncharacterized compounds.

The workflow demonstrates how machine learning can assist **drug discovery and biofilm inhibition research** by linking molecular properties to biological activity.

---

# 📊 Project Overview

Biofilms are structured microbial communities that are resistant to conventional antimicrobial treatments. Identifying molecular targets for compounds with anti-biofilm activity is an important step toward discovering new therapeutic strategies.

This project implements a **target prediction pipeline** that:

1. Uses a curated descriptor database to train a machine learning classifier  
2. Learns relationships between molecular descriptors and known biological targets  
3. Applies the trained model to predict targets for new compounds with potential anti-biofilm activity  

---

# ⚙️ Methodology

The workflow consists of the following stages.

## 1. Data Preparation

Two datasets are used in this project:

**TargIDe_Database_Descriptors.xlsx**  
Contains compounds with known biological targets and molecular descriptors.

**compound_database.xlsx**  
Contains compounds whose targets are to be predicted.

Both datasets include calculated molecular descriptors representing physicochemical and structural properties of molecules.

---

## 2. Feature Selection

Ten molecular descriptors were selected as the most relevant predictors:

- MATS4p  
- R_TpiPCTPC  
- cLogS  
- GATS3m  
- MDEO-12  
- HybRatio  
- GATS4p  
- MLFER_A  
- GATS6m  
- GATS2e  

These descriptors encode structural and physicochemical characteristics of the molecules.

---

## 3. Model Training

A **Gradient Boosting Classifier** is used to learn relationships between molecular descriptors and known targets.

Model parameters:

- n_estimators = 100  
- learning_rate = 1.0  
- max_depth = 1  

The dataset is divided into:

- **70% training data**
- **30% testing data**

---

## 4. Model Evaluation

The model performance is evaluated using several classification metrics:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Jaccard Similarity  

These metrics provide insight into how well the model predicts the correct biological targets.

---

## 5. Target Prediction

After training, the model is applied to compounds in the compound database to predict **potential biological targets associated with anti-biofilm activity**.

---

# 📂 Repository Structure

```
ANTI-BIOFILM-TARGETING
│
├── anti_biofilm_target_prediction.ipynb
├── compound_database.xlsx
├── TargIDe_Database_Descriptors.xlsx
├── predicted_targets_antibiofilm.csv
└── README.md
```

---

# 🧪 Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Gradient Boosting Classifier  

---

# 🚀 How to Run the Project

Clone the repository:

```
git clone https://github.com/yourusername/ANTI-BIOFILM-TARGETING.git
```

Install required libraries:

```
pip install pandas numpy scikit-learn matplotlib seaborn
```

Run the notebook:

```
anti_biofilm_target_prediction.ipynb
```

---

# 🔬 Applications

This workflow demonstrates a simple machine learning framework that can be extended for:

- Drug target prediction  
- Anti-biofilm compound screening  
- Structure–activity relationship studies  
- Computational drug discovery  

---


