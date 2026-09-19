# HealthConnect Clinic — Week 7: Model Testing, Refinement & Validation

This project is part of the **HealthConnect Clinic Data Science track**.

## Objective
The goal was to test and refine the Week 6 no-show prediction model and determine whether it remained reliable for supporting appointment attendance and administrative planning.

## What I Tested
* **Week 6 Random Forest candidate model evaluation:**
  * Accuracy, precision, recall, F1-score, and ROC-AUC
  * Confusion matrix (False positives and false negatives)
  * Error patterns
  * Segment performance
  * Training vs. test performance
* **Model Robustness & Comparison:**
  * Five-fold cross-validation
  * Input robustness
  * Classification threshold behaviour
  * Week 5 baseline vs. Week 6 candidate comparison
* **Refined Random Forest model**

## Refinement
A controlled Random Forest refinement was tested by limiting the maximum tree depth. The refined model was then re-tested using the same held-out test data and cross-validation approach.

## Key Outputs
The notebook produces the following deliverables:
* Candidate model test results
* Error analysis & segment performance results
* Baseline and refinement comparisons
* Before/after error analysis
* ROC curves
* Feature-quality checks
* Input and threshold robustness results

## Business Relevance
The model is intended to help HealthConnect identify appointments with an increased predicted risk of No-Show so that appropriate administrative support can be considered. The prediction is not treated as certainty and should support human decision-making.

## Limitations
The model is based on the available HealthConnect dataset and requires further validation before real-world deployment. Additional testing of data quality, pipeline integration, operational thresholds, and cross-track dependencies is required.

## Next Steps: Week 8
Before final integration, the remaining testing evidence, cross-track validation, model limitations, and operational requirements should be reviewed and documented.

## Tools Used
* **Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Environment:** Google Colab

---
**Project Stage:** Week 7 — Testing → Refinement → Validation
