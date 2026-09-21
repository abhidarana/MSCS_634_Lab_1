# MSCS 634 - Lab 1: Data Visualization, Preprocessing, and Statistical Analysis

## Purpose
This lab explores data preprocessing, visualization, and statistical techniques using Python in Jupyter Notebook. The workflow cleans incomplete data, identifies extreme outliers, scales features, performs dimensionality reduction, and evaluates summary statistical profiles.

---

## Key Insights

### 1. Exploratory Data Analysis
* **Scatter Plot:** Visualized department level behavior showing moderate income customers in *Sports* and *Clothing* exhibit high spending scores, whereas higher income customers in *Home* display lower relative spending scores.
* **Box Plot:** Highlighted scale variations across numerical features and flagged an extreme income outlier ($250,000) that skewed distribution parameters.

### 2. Statistical Metrics
* **Distribution Symmetry:** The median age (~35 years) closely matched the sample mean following missing value imputation, demonstrating a symmetric age distribution.
* **Outlier Filtering:** Applying IQR thresholding ($IQR = Q3 - Q1$) successfully isolated points beyond $1.5 \times IQR$, reducing feature variance prior to scaling.

---

## Technical Decisions

1. **Missing Value Imputation:** Used median imputation for missing `Age` values to maintain central tendencies without being skewed by extreme values.
2. **Outlier Mitigation:** Removed the high-leverage income outlier ($250,000) to prevent compression during Min-Max normalization.
3. **Feature Scaling:** Standardized numerical columns using Min-Max Scaling to compress inputs onto a $[0, 1]$ interval.

---

## Folder Structure
```text
├── Lab_1_Notebook.ipynb   # Main Jupyter Notebook
├── README.md              # Summary documentation
└── screenshots/           # Captures of all required notebook execution steps
