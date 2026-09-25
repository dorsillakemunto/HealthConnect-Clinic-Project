HealthConnect Clinic — No-Show Prediction
Week 8 Final Model, Integration & Presentation
📋 Project Overview

HealthConnect Clinic is a fictional healthcare provider seeking to:

Reduce missed appointments

Improve patient attendance

Make better use of available appointment capacity

Provide more effective administrative support to patients

This project forms part of an Experience Lab multidisciplinary HealthConnect solution addressing the following question:

How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?

The Data Science contribution focuses on developing and validating a machine-learning model that predicts the likelihood of an appointment resulting in a No-Show.

📅 Project Timeline
Week	Stage	Description
Week 4	Problem Understanding & Planning	Defined the problem, objectives and modelling approach
Week 5	Analysis & Initial Implementation	Performed initial analysis and developed the first model
Week 6	Integration & Validation	Integrated outputs and validated the modelling approach
Week 7	Testing & Refinement	Tested, evaluated and refined the candidate models
Week 8	Final Model, Integration & Presentation	Finalised the model, documented integration and prepared presentation materials

The Week 8 work represents the final stage of the project.

🎯 Data Science Objective

The objective of the Data Science track is to provide HealthConnect with a validated predictive model that can be used as an administrative decision-support signal.

The model is intended to help identify appointments that may require additional confirmation or reminder activity.

⚠️ The Model Is Not Intended To

Determine whether a patient will definitely attend

Replace administrative staff judgement

Make clinical decisions

Determine patient eligibility or treatment

Guarantee that an intervention will improve attendance

📦 Week 8 Final Deliverables

The final Data Science package includes:

✅ Final candidate model

✅ Baseline model

✅ Baseline-versus-final comparison

✅ Model evaluation

✅ Threshold analysis

✅ Error analysis

✅ False-positive and false-negative analysis

✅ Feature and preprocessing decisions

✅ Business interpretation

✅ Model limitations and risks

✅ Operational-use boundaries

✅ ML Engineering handoff requirements

✅ Final HealthConnect workflow

✅ Presentation materials

✅ Lessons learned

✅ Future improvement recommendations

🤖 Modelling Approach

The project progressed from an initial baseline model to a Random Forest candidate and subsequently through testing and refinement.

Modelling Workflow
Data Preparation
       ↓
Feature Review
       ↓
Leakage Screening
       ↓
Train/Test Splitting
       ↓
Preprocessing
       ↓
Candidate Model Development
       ↓
Threshold Analysis
       ↓
Error Analysis
       ↓
Refinement
       ↓
Retesting
       ↓
Final Model Selection
       ↓
Business Interpretation
       ↓
Integration Documentation


The final model is selected using the documented Week 7 testing evidence, rather than simply selecting a model because it was developed later.

📊 Model Evaluation

The final model is evaluated using multiple performance measures:

Evaluation Area	Metric / Method
Classification Performance	Accuracy
Positive Prediction Quality	Precision
Detection Performance	Recall
Overall Classification Balance	F1 Score
Ranking Performance	ROC-AUC
Classification Breakdown	Confusion Matrix
Error Assessment	False-Positive Analysis
Error Assessment	False-Negative Analysis
Model Stability	Cross-Validation
Generalisation	Training-vs-Test Comparison

Multiple metrics are used because no single metric fully describes the operational usefulness of a No-Show prediction model.

🔍 Error Analysis

Particular attention is given to the two main types of prediction errors.

False Positives

Definition: Appointments predicted as No-Shows that were actually attended.

False positives may result in unnecessary reminder or confirmation activity.

False Negatives

Definition: Appointments that were actually No-Shows but were not identified by the model.

False negatives represent missed opportunities to provide additional appointment support.

Why Error Analysis Matters

Both error types have operational implications and therefore need to be considered when designing any intervention workflow.

💼 Business Interpretation

The model can support an administrative workflow such as:

Appointment Data
       ↓
Risk Prediction
       ↓
Administrative Prioritisation
       ↓
Appropriate Reminder / Confirmation Activity
       ↓
Attendance Outcome
       ↓
Monitoring


The prediction should be treated as a prioritisation signal rather than a certainty.

The effectiveness of the complete solution should ultimately be evaluated using operational outcomes, not predictive metrics alone.

🔗 Cross-Track Integration

The Data Science component forms part of a broader multidisciplinary HealthConnect solution.

📈 Data Analytics

Provides validated analytical findings that help:

Contextualise the modelling results

Identify relevant appointment patterns

Support interpretation of model outputs

⚙️ ML Engineering

Uses the documented final model requirements to support:

Reproducible implementation

Deployment

Model monitoring

Technical handoff

🤖 Generative AI

Can support appropriate:

Patient-facing communication workflows

Administrative communication

Appointment-support workflows

📋 Project Management

Coordinates:

Requirements

Deliverables

Dependencies

Risks

Final project readiness

The Week 8 documentation records the actual outputs exchanged between tracks and distinguishes confirmed evidence from planned integration.

⚠️ Model Limitations and Risks

The model has several important limitations:

Predictions are probabilistic rather than certain.

Historical data may not represent future appointment behaviour.

Model performance can change when data distributions change.

False positives and false negatives remain.

Segment-level performance may vary.

Predictive performance does not prove that reminders or other interventions will cause attendance to improve.

Production use would require monitoring and periodic evaluation.

Features must be available before the appointment outcome is known.

Any operational deployment should include appropriate governance and human oversight.

✅ What the Model Can Be Used For

The model can support:

Appointment-risk prioritisation

Administrative planning

Reminder prioritisation

Confirmation workflows

Capacity-management analysis

Monitoring of prediction performance

🚫 What the Model Cannot Be Used For

The model should not independently be used to:

Make clinical decisions

Diagnose patients

Determine treatment

Penalise patients

Treat a predicted No-Show as a confirmed outcome

Replace human administrative judgement

Claim that an intervention will definitely prevent a missed appointment

🏥 Final HealthConnect Value

The Data Science contribution provides a predictive layer within the wider HealthConnect solution.

The intended value is to help the clinic move from a purely reactive appointment process toward a more data-informed administrative workflow.

The final solution combines:

Analytical Insight
       +
Predictive Modelling
       +
Engineering Implementation
       +
AI-Supported Communication
       +
Project Coordination
       ↓
Integrated HealthConnect Solution

📁 Project Structure
HealthConnect/
│
├── notebooks/
│   └── WEEK_8_ANALYSTLAB_AFRICA_HEALTH_CONNECT_CLINIC.ipynb
│
├── outputs/
│   ├── Week6/
│   ├── Week7/
│   └── Week8/
│
├── README.md
│
└── presentation/
    └── HealthConnect_Week8_Data_Science_Presentation

🎓 Week 8 Outcome

The Week 8 Data Science contribution moves the project from a tested predictive model toward a documented, business-oriented and integration-ready component.

The final deliverable demonstrates the following progression:

Model
  ↓
Evidence
  ↓
Interpretation
  ↓
Integration
  ↓
Business Value

📚 Lessons Learned

The project demonstrated that developing a useful predictive solution involves more than selecting an algorithm.

Important lessons included:

Business context should guide modelling decisions.

Baseline comparison is important when assessing model development.

Multiple evaluation metrics are required to understand model performance.

Error analysis provides information that aggregate metrics can hide.

Threshold selection affects operational behaviour.

Feature availability and data leakage must be considered carefully.

Cross-track collaboration requires actual exchange and use of outputs.

A technically strong model still requires appropriate governance and operational validation.

🚀 Future Improvements

Future iterations could investigate:

Larger and more recent datasets

Additional validated appointment features

Segment-level monitoring

Probability calibration

Alternative modelling approaches

Automated monitoring for data and model drift

Controlled evaluation of reminder interventions

Integration with operational appointment systems

Continuous model performance monitoring

Periodic model review and retraining

📝 Final Statement

The HealthConnect Data Science contribution demonstrates how predictive analytics can form one component of a broader multidisciplinary healthcare-support solution.

The model is intended to support better administrative prioritisation while keeping human judgement at the centre of operational decisions.

The overall project demonstrates the progression from:

Data → Modelling → Evidence → Interpretation → Integration → Business Value

The final Data Science component therefore provides a foundation for a more data-informed, monitored and human-centred appointment-support workflow.
