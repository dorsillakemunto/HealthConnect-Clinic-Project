# HealthConnect Project Kickoff and Problem Understanding

## 📋 Project Overview
This project is part of the **HealthConnect Data Science Track**. The primary objective is to explore whether available healthcare appointment data can support a future machine learning solution to predict if a patient is likely to miss a scheduled appointment. 

My contribution specifically focused on **Data/Business Analysis**, which involved:
* Understanding the dataset
* Assessing data quality
* Identifying potential features
* Defining the proposed target
* Checking for data leakage


## 👤 My Role
As a **Data/Business Analyst**, my main responsibilities included:
* Understanding the mechanics of the no-show prediction problem
* Reviewing the HealthConnect appointment dataset and Data Dictionary
* Assessing data quality and profiling variables
* Exploring appointment outcomes and identifying potential input features
* Assessing feature availability *before* an appointment occurs
* Identifying and documenting potential target leakage
* Providing structured recommendations for the future modelling stage

---

## 📊 Dataset and Resources 

The core tools and resources utilized during this analysis:
* **Data Assets:** HealthConnect Appointment Dataset & HealthConnect Data Dictionary 
* **Languages & Libraries:** Python, Pandas, NumPy, Matplotlib, Seaborn 

### Data Assessment Focus 

The dataset was thoroughly reviewed to map its size, structure, column names, data types, missing/duplicate values, and the ratio of numerical to categorical variables. Columns were also cross-referenced with the official Data Dictionary to identify documentation discrepancies. 

### Data Quality Checks 

* Missing-value & duplicate analysis
* Numerical & categorical distribution analysis
* Variable profiling
* Appointment outcome analysis
    
--- 

## 🤖 Proposed Machine Learning Problem 

The objective is to formulate a binary classification problem: **Predict whether a scheduled healthcare appointment will result in a no-show.** 

### Proposed Target Definition 

The target variable is derived directly from the final outcome of the appointment: 
| Appointment Outcome | Proposed Target | Action / Handling | | :--- | :--- | :--- | 
| **No-Show** | `1` | Include in target population | 
| **Attended** | `0` | Include in target population | 
| **Cancelled** | *Handle separately* | Exclude from initial model population | > 📌 


### Handling Cancellations

Cancellations **should not** automatically be treated as no-shows. A cancellation implies a deliberate schedule change, which differs fundamentally from a patient failing to attend. For the initial binary model, cancelled appointments should be excluded unless a specific business rule requires otherwise. 

--- 

## 💡 Potential Features & Leakage Analysis 

### Input Feature Groups 
* **Historical Attendance (High Priority):** Tracks metrics like `previous_no_shows` or past appointment outcomes.
* **Constraint:* Must only aggregate data from appointments occurring chronologically before the current appointment date.
* **Appointment Timing (High Priority):** Waiting time, booking-to-appointment interval, day of the week, and time of day.
* **Reminder Information (Conditional):** Reminders sent, type, and timing. Requires confirmation on exactly *when* this log becomes available.
* **Accessibility:** Physical distance from the patient’s home to the clinic.
* **Booking Characteristics:** Appointment type, category/service, and booking method.
* **Demographic Variables:** Age, gender, etc. These require careful ethical screening before inclusion to prevent bias. 

### 🚫 Target Leakage & Variables to Exclude 

Information that updates only *after* the appointment outcome occurs must be strictly excluded to prevent data leakage. 
* **Variables to drop:** `appointment_outcome`, post-appointment status, attendance confirmations, and post-outcome administrative text.



## 🎯 Feature Recommendations Summary 

| Feature Group | Recommendation | Action | | :--- | :--- | :--- | 
| **Historical attendance** | 🟢 High priority | Include immediately | 
| **Appointment timing** | 🟢 High priority | Include immediately | 
| **Reminder information** | 🟡 Consider | Include after availability timing check | 
| **Accessibility** | 🟡 Consider | Include if data quality allows | 
| **Appointment/booking details**| 🟡 Consider | Include as structural features | 
| **Demographic variables** | 🟠 Review carefully| Screen for fairness and ethical risks | 
| **Final/post-outcome info** | 🔴 Exclude | Drop entirely to avoid leakage | 



