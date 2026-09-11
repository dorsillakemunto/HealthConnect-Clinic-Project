# HealthConnect Week 6 — Model Improvement & Validation Project Overview

HealthConnect Clinic wants to reduce missed appointments and improve appointment attendance. The Week 6 focus is **Model Improvement, Error Analysis, and Validation**.

## Week 5 → Week 6 Transition 

At the end of Week 5, a **Logistic Regression** baseline was established for predicting appointment no-shows. The main limitation was that this baseline required further testing and improvement. 

In Week 6, the project moved beyond the baseline by:
* Analyzing model errors
* Reviewing features
* Developing an improved model
* Validating the results

---

## Week 6 Objectives 

The main objectives were to:
* Analyze baseline model weaknesses.
* Identify false positives and false negatives.
* Review the existing features.
* Develop an improved model.
* Compare the improved model with the baseline.
* Use stronger validation methods.
* Interpret the results from a HealthConnect business perspective.
* Select a candidate model for Week 7 testing.

---

## Baseline Model 

The Week 5 **Logistic Regression** model serves as the comparison baseline. The Week 6 work does not simply retrain this same model; instead, the baseline results are used to pinpoint specific areas that require improvement.

---

## Error Analysis 

Model predictions are separated into four distinct outcomes:
* **True Positive:** Correctly predicted No-Show.
* **True Negative:** Correctly predicted Attended.
* **False Positive:** Predicted No-Show when the appointment was attended.
* **False Negative:** Predicted Attended when the appointment was actually a No-Show.

> ⚠️ **Note:** False negatives are particularly critical because they represent missed appointments that the model failed to identify.

---

## Feature Review 

Existing modeling features were reviewed to determine whether they provide useful information for predicting appointment attendance. Features were checked for:
* Predictive value
* Missing information
* Unusual values
* Potential leakage
* Availability *before* the appointment

> 🚫 **Constraint:** Features that could reveal the outcome after the appointment occurs are strictly excluded to prevent target leakage.

---

## Improved Model 

The improved model selected for Week 6 is the **Random Forest Classifier**. 

* **Why Random Forest?** It captures more complex, non-linear relationships between variables than Logistic Regression.
* **Explainability:** It provides feature importance scores to help identify which variables contribute most to predictions.
* **Testing:** The Random Forest model was tested directly against the Logistic Regression baseline.

---

## Model Evaluation & Cross-Validation

### Evaluation Metrics
The models are compared using standard evaluation metrics:
* Accuracy
* Precision
* **Recall** (Primary focus)
* **F1-score** (Primary focus)
* **ROC-AUC** (Primary focus)

*Accuracy alone is not sufficient to decide whether a model is suitable for this imbalanced problem.*

### Cross-Validation
Cross-validation is used to ensure the improved model produces consistent results across different training and validation splits. This provides stronger statistical evidence than relying on a single train/test split.

---

## Model Comparison 

The core comparison evaluates the following roles:

| Model | Role |
| :--- | :--- |
| **Logistic Regression** | Week 5 baseline |
| **Random Forest** | Week 6 improved model |

*The Random Forest model will only be recommended if the results show a meaningful performance gain. If Logistic Regression performs better or equal, it will remain the candidate model based on the evidence.*

---

## Business Relevance 

The purpose of the model is to help HealthConnect identify appointments that have a higher risk of becoming No-Shows. A useful model supports staff decisions by allowing them to:
* Prioritize appointment reminders.
* Identify appointments needing additional support.
* Improve the utilization of appointment slots.
* Support better administrative planning.

*The model is designed to support staff decisions rather than automatically make administrative choices about patients.*

---

## Cross-Track Integration 

* **Track Collaborated With:** Data Analytics
* **Project Dependency:** Data Analytics findings regarding attendance patterns help determine whether the model features and results align with the core HealthConnect business problem.

### Information Flow
* **Information Received:** Relevant analytical findings and attendance patterns will be incorporated where available.
* **Information Provided:** The Data Science track provides model performance results, error-analysis findings, feature importance, candidate model selection, and validation metrics.
* **Integration Activity:** Analytical findings are compared with model findings to check whether the predictive results are consistent with the wider HealthConnect business landscape.
* **Result:** This integration ensures that model development is connected to actual clinic operations rather than being evaluated strictly on technical model scores.

---

## Week 6 Key Decisions 

1. Keep **Logistic Regression** as the baseline for comparison.
2. Use **Random Forest** as the improved modeling approach.
3. Analyze false positives and false negatives intentionally.
4. Give particular attention to **No-Show recall**.
5. Use **cross-validation** to strengthen model evaluation.
6. Avoid features that could cause **target leakage**.
7. Select the final candidate model based on **empirical evidence** rather than assuming Random Forest will win.

---

## Limitations and Risks 

The current solution contains several risks that must be managed:
* The dataset may not perfectly represent real-world appointment behavior.
* Some useful predictive information may remain unavailable in the current systems.
* Model performance may degrade when deployed on new data.
* False predictions will still occur and must be handled operationally.
* Random Forest may overfit the training data if hyperparameters are not controlled.
* Model predictions reflect correlations and do not prove *why* a patient misses an appointment.
* Fairness across different patient demographics requires further testing.
* More robust testing is required before operational clinical use.

---

## Week 7 Testing Requirements 

The selected candidate model must undergo rigorous testing in Week 7, including:
* Evaluation on completely unseen data.
* False-positive and false-negative operational impact testing.
* Prediction probability threshold analysis.
* Model stability and variance testing.
* Demographic fairness and bias analysis.
* Data-quality and pipeline robustness testing.
* Explicit target-leakage validation checks.
* Testing behavior with unexpected or new categorical variables.
* Comparison against specific HealthConnect business thresholds.
* Comprehensive documentation of remaining operational risks.

---

## Week 6 Outcome 

Week 6 successfully advances the HealthConnect Data Science pipeline from an unvalidated baseline model toward a thoroughly tested candidate solution. 

The main improvement is the addition of the **Random Forest architecture**, backed by error analysis, feature review, direct model comparison, and rigorous validation. The final candidate model will be selected purely based on evaluation results and its practical utility for the HealthConnect clinic.
