
# 🧠 Parkinson’s Disease Dataset: Exploratory Data Analysis (EDA)

## 📊 Overview

This project focuses on conducting a comprehensive **Exploratory Data Analysis (EDA)** of the Parkinson’s Disease dataset. Parkinson’s Disease is a chronic and progressive neurodegenerative disorder that affects movement and speech, among other functions. Early detection and diagnosis play a crucial role in managing the condition.

The dataset used in this project contains biomedical voice measurements from individuals with and without Parkinson’s disease. These measurements are derived from sustained phonation and include variables such as jitter, shimmer, harmonic-to-noise ratios, and non-linear signal dynamics. 

By analyzing these features, we aim to uncover meaningful patterns and correlations that distinguish patients with Parkinson’s disease from healthy individuals. This analysis lays the groundwork for future predictive modeling and feature selection.

---

## 🧾 Dataset Description

- **Source**: UCI Machine Learning Repository / Kaggle
- **Instances**: 195 voice recordings
- **Features**: 24 columns (including 22 biomedical voice measures, 1 target column `status`, and 1 name column)
- **Target Variable**: `status` 
  - `1` = Parkinson’s disease
  - `0` = Healthy control

### 🔑 Key Features

| Feature Name           | Description                                                   |
|------------------------|---------------------------------------------------------------|
| `MDVP:Fo(Hz)`          | Average vocal fundamental frequency                           |
| `MDVP:Fhi(Hz)`         | Maximum vocal fundamental frequency                           |
| `MDVP:Flo(Hz)`         | Minimum vocal fundamental frequency                           |
| `MDVP:Jitter(%)`       | Frequency variation (jitter)                                  |
| `MDVP:Shimmer`         | Amplitude variation (shimmer)                                 |
| `NHR`, `HNR`           | Noise-to-harmonics and harmonics-to-noise ratios              |
| `RPDE`, `DFA`          | Measures of signal complexity and nonlinear dynamics          |
| `spread1`, `spread2`   | Nonlinear measures of voice signal                             |
| `PPE`                  | Pitch Period Entropy – indicative of voice irregularity       |

---

## 🎯 Project Objectives

- ✅ Perform data inspection and identify structural and statistical characteristics of the dataset.
- ✅ Use statistical summaries and visual tools to uncover data distribution and potential anomalies.
- ✅ Identify features that show significant differences between Parkinson’s and non-Parkinson’s cases.
- ✅ Visualize inter-feature relationships and investigate redundancy or multicollinearity.
- ✅ Summarize observations that may guide downstream modeling or biomarker discovery.

---

## 📁 Repository Structure

| File Name                          | Description                                                                 |
|-----------------------------------|-----------------------------------------------------------------------------|
| `Exploratory_Data_Analysis.ipynb` | Jupyter Notebook with code and visualizations for EDA                       |
| `parkinsons.data`                  | Input dataset used for the analysis                                        |
| `EDA_Report.pdf`                  | Summary report of EDA findings and visual outputs                          |
| `README.md`                       | This documentation file                                                    |

---

## 🛠️ Tools and Libraries Used

- **Python 3.10+**
- **Jupyter Notebook**
- **Pandas** – data wrangling and manipulation
- **NumPy** – numerical operations
- **Matplotlib & Seaborn** – visualizations and plots

---

---

## ✅ Key EDA Steps Performed

### 🔹 Step 1: Data Inspection
- Checked shape, data types, and null values using `.info()` and `.isnull().sum()`.
- Reviewed class distribution to assess balance between Parkinson’s and healthy samples.

### 🔹 Step 2: Descriptive Statistics
- Calculated mean, median, and standard deviation using `.describe()`.
- Identified skewness and outliers using histograms and boxplots.

### 🔹 Step 3: Data Visualization
- Plotted **histograms** to view individual feature distributions.
- Used **boxplots** to explore variation across `status` groups.
- Created a **correlation heatmap** to visualize inter-feature dependencies.
- Generated **pairplots** and **scatterplots** to observe bivariate relationships.

### 🔹 Step 4: Observations
- Strong correlations observed among **jitter** and **shimmer-based** features.
- **High values of PPE, spread1, and DFA** were more common in Parkinson’s patients.
- **Lower HNR** values were noted in individuals with Parkinson’s, indicating vocal noise.

---

## 🔍 EDA Summary & Insights

- Individuals diagnosed with Parkinson’s exhibit **increased jitter, shimmer, and PPE**, suggesting irregular vocal pitch and amplitude.
- **Spread1 and DFA** serve as significant discriminators between Parkinson’s and healthy voices.
- The dataset is **clean**, with **no missing values**.
- Several features are **highly correlated**, indicating potential for **dimensionality reduction** or **feature elimination** in machine learning workflows.

---


## 🔁 Reproducibility Guide

To reproduce the analysis:

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/parkinsons-eda.git
cd parkinsons-eda
```

### 2. Install Required Libraries
```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Run the Notebook
```bash
jupyter notebook Exploratory_Data_Analysis.ipynb
```

