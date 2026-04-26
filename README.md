# Data-Cleanser
#  Data Cleanser Project (Patient Dataset)

##  Project Objective

The goal of this project is to **clean and preprocess a healthcare dataset** by:

* Handling missing values
* Detecting and treating outliers
* Preparing a clean dataset for analysis and machine learning

---

##  Dataset Information

The dataset contains patient health records with the following features:

* **patient_id** → Unique ID of patient
* **age** → Age of patient
* **gender** → Male / Female
* **region** → North, South, East, West
* **bmi** → Body Mass Index
* **blood_pressure** → Blood pressure value
* **cholesterol** → Cholesterol level
* **glucose** → Glucose level
* **disease_risk** → Target (0 = Low, 1 = High)

---

##  Problems in Dataset

* Missing values in:

  * gender (high missing)
  * region
  * bmi, cholesterol, glucose
* Presence of **outliers** in:

  * BMI
  * Cholesterol
  * Glucose

---

##  Techniques Used

###  Handling Missing Values

1. **Simple Imputer**

   * Numerical → Mean
   * Categorical → Mode

2. **KNN Imputer**

   * Uses nearest neighbors

3. **MICE (Iterative Imputer)**

   * Best method used (captures relationships)

---

###  Handling Outliers

1. **Z-Score Method**

   * Detects extreme values using standard deviation

2. **IQR Method**

   * Caps values using quartile range

3. **Percentile Method**

   * Clips values between 1% and 99%

4. **Winsorization (Final Method)**

   * Replaces extreme values instead of removing them

---

##  Final Approach

* Missing values handled using **MICE**
* Outliers handled using **Winsorization**

---

##  Final Output

* No missing values
* Outliers controlled
* Dataset ready for ML models

---

##  Output File

```bash
final_cleaned_dataset.csv
```

---

##  Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* SciPy

---

##  How to Run the Project

1. Install dependencies:

```bash
pip install pandas numpy scikit-learn scipy
```

2. Run your Python file or Jupyter Notebook

3. Final dataset will be generated:

```bash
final_cleaned_dataset.csv
```

---

##  Conclusion

This project improves data quality by:

* Removing missing values
* Handling outliers effectively
* Making data suitable for analysis and machine learning
