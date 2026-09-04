# HealthConnect Clinic – Week 5 Data Science Internship Project by AnalystLab Africa

## 📋 Project Overview
**HealthConnect Clinic** is a fictional healthcare provider seeking to reduce missed appointments and improve patient support. This project focuses on using appointment data to understand factors associated with appointment attendance and no-shows.

## 🎯 Week 5 Objective
The main objective of Week 5 was to move from the problem definition completed in Week 4 into practical **data preparation, feature engineering, and baseline machine-learning development**.

---

## 🛠️ Work Completed

### Data Cleaning & Quality Checks
* **Target definition:** Confirmed `appointment_outcome` as the target-related variable and created a binary `no_show` target for modelling.
* **Outcome review:** Reviewed appointment outcomes, including cancelled appointments.
* **Integrity checks:** Checked for missing values, duplicate records, data types, and inconsistent categorical values.
* **Standardisation:** Standardised categorical text values.
* **Anomaly detection:** Investigated unique and high-cardinality values, potential outliers, and impossible or negative values.

### Feature Engineering & Selection
* **Time-based features:** Created features such as waiting time and appointment day.
* **Leakage assessment:** Assessed and mitigated potential data leakage.
* **Feature selection:** Selected candidate features for modelling.

### Preprocessing & Modelling
* **Pipeline preparation:** Prepared numerical and categorical preprocessing workflows.
* **Transformations:** Applied imputation and One-Hot Encoding where appropriate.
* **Baseline development:** Developed an initial baseline classification model.
* **Evaluation:** Evaluated the initial model using standard classification metrics.

---

## 📊 Initial Baseline Model Performance
Our initial computer model is currently struggling to guess who will show up to appointments, performing only slightly better than a random 50/50 coin flip.

To fix this, we are moving on to more advanced and powerful machine learning methods next week.

By upgrading our approach and cleaning up our data, we look forward to making our predictions much more accurate and reliable.

---

## 🧰 Tools Used
* **Languages:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn
* **Environment:** Google Colab

---

## 📊 Dataset
* Uses the fictional and anonymized **HealthConnect Appointment Dataset**.
* **Data Integrity:** The original dataset is never overwritten; all processed and derived files are saved separately.

### Key Focus Areas
The analysis heavily focuses on pre-appointment predictors:
* Previous attendance behaviour
* Waiting time
* Appointment characteristics
* Reminder information
* Accessibility-related variables

---

## 🚀 Week 5 Outcome
Week 5 successfully established the engineering foundation for further machine-learning development. The **baseline model provides an initial benchmark** that will be iteratively improved and evaluated in Week 6.
