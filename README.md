# Pulmonology-Data-analysis-
Respiratory diseases (such as COPD, Asthma, Pneumonia, and ARDS) represent a significant portion of hospital admissions and intensive care unit (ICU) usage. The aim of the project to analyze clinical factors affecting Length of Stay (LOS), total billing charges, 30-day readmission, and Diagnostic patterns using spirometry.
Dataset Features & SchemaThe dataset contains 3,200 rows across 19 clinical and administrative attributes:
Encounter_ID	Identifiers	Unique visit ID (PENC-XXXXX)
Patient_ID	Identifiers	Patient ID (PULM-XXXXX) — enables longitudinal cohort tracking.
Age & Gender	Demographics	Patient age (22–88) and gender classification.
Smoking_History	Risk Factors	Never, Former, Current
Primary_Pulmonary_Diagnosis	Clinical	Primary diagnosis (e.g., COPD, Pneumonia, ARDS, Asthma, Pulmonary Embolism, IPF)
Condition_Severity	Clinical	Acuity level (Mild, Moderate, Severe, Critical)
SpO2_Admission_Pct	Vitals	Baseline pulse oximetry saturation on admission (%)
FEV1_FVC_RatioBiomarkerSpirometry ratio ($FEV_1 / FVC$) — used to assess airway obstruction.
Oxygen_Therapy_Type	Interventions	Room Air, Nasal Cannula, HFNC, BiPAP/CPAP, Mechanical Ventilation.
Primary_Prescribed_Medication	Pharmacology	Primary drug therapy (e.g., Tiotropium, Ceftriaxone, Methylprednisolone, Enoxaparin)
Secondary_Maintenance_Medication	Pharmacology	Maintenance / Rescue regimen (e.g., Fluticasone/Salmeterol, Rescue Inhalers).
Care_Unit	Operations	Pulmonary Ward, Respiratory Care Unit (RCU), Medical ICU (MICU), Step-Down, Outpatient.
Admission_Date / Discharge_Date	Temporal	Encounter start and end dates
Length_of_Stay_Days	Operations	Inpatient duration (days)
Total_Billing_USD	Financial	Total hospital billing charges
Insurance_Provider	Financial	Medicare, Medicaid, Private Insurance, Uninsured
Discharge_Outcome	Quality Metrics	Discharged Home, Rehab, Readmitted within 30 Days, Deceased
Key Analytical Focus Areas: 
Spirometry & Airway Obstruction Analysis:Categorize patients with $FEV_1 / FVC < 0.70$ as having an Obstructive Pattern (COPD, Severe Asthma) vs. Restrictive / Normal Patterns (Pulmonary Fibrosis, Pneumonia).
Clinical Acuity vs. ICU Escalation:
Analyze the relationship between admission $SpO_2$ levels and required oxygen delivery methods (HFNC, Mechanical Ventilation) across care units (MICU vs. Ward). 
Readmission & Outcome Drivers:
Investigate risk factors (such as smoking history, severe exacerbations, and specific diagnoses) associated with 30-day readmissions and mortality.
Financial & Operations Modeling:
Assess healthcare cost distribution across insurance payers, severity tiers, and length of stay.
Data Cleaning & Imputation:Handle realistic missingness in diagnostic tests (e.g., missing $FEV_1 / FVC$ ratios due to acute respiratory distress) and missing medication records.
