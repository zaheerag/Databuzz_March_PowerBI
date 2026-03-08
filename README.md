# Databuzz_March_PowerBI
# Clinical Triage & System Analytics Dashboard
**Project Status:** Completed | **Developer:** Zaheera Ganie | **Tools:** Power BI, DAX, Power Query, Python (Google Colab)

## Executive Summary
This project marks my first milestone in Power BI, developed to bridge the gap between raw medical data and actionable clinical insights. It features a three-page interactive system that allows healthcare providers to move from a high-level view to individual patient diagnostics and facility-wide trend analysis.

---

##  Data Science & Validation (Google Colab)
Before the visualization phase, I performed a rigorous 5-Phase validation using a Python/Pandas stack in Google Colab to ensure the synthetic dataset met clinical benchmarks.

### **The 5-Phase Validation Process:**
1.  **Structural Validation:** Verified 20,200 rows and 25 columns with zero null values.
2.  **Statistical Check:** Confirmed realistic distributions for Age (1–85) and Temperature (37°C–41°C).
3.  **Medical Consistency:** Used grouping and aggregation to prove clinical patterns:
    * **Pass:** High Risk patients correctly showed higher mean Diabetes (209 mg/dL) and Systolic BP (130 mmHg).
    * **Pass:** Dengue cases showed the lowest mean Platelets (59k), while Bacterial infections showed the highest WBC (14.9k).
4.  **Relational Integrity:** Validated 100% ID matching between `Patient_Symptoms` and `Blood_Test_Results`.
5.  **Coverage Gap Analysis:** Identified and addressed missing indicators (Thyroid, Asthma, Medication Usage) to meet the 2026 competition brief.

*The Jupyter Notebook (`Patient_Data_Validation.ipynb`) containing the Python scripts and Seaborn distributions is included in this repository.*



---

## Dashboard Architecture

### **Page 1: Dashboard Overview**
* **Dynamic Risk Scoring:** Developed a DAX-based Urgent Score that updates in real-time based on user-adjustable sliders for Fever and Glucose thresholds.
* **Instant Filtering:** Used visual-level filters to highlight only the "At-Risk" population.

### **Page 2: Patient Diagnostic Detail**
* **Drill-through Capability:** Implemented a seamless transition from the main table to a deep-dive history for specific patients.
* **Unpivoted Symptom Tracking:** Reshaped "wide" data into a "long" format via Power Query to create a clean, vertical Clinical Observations Timeline.

### **Page 3: System Analytics**
* **Outlier Detection:** A Scatter Plot clustering patients by Chronic Condition Score to identify high-complexity health risks.
* **Medication Coverage:** A 100% Stacked Bar chart auditing clinical treatment rates (currently at 100% for high-risk cases).

---

## The Model (Star Schema)
The project utilizes a robust star schema to ensure high performance:
* **`dim_patient`**: Central demographic hub.
* **`patient_symptoms`**: Fact table unpivoted for granular symptom analysis.
* **`patient_last_symptoms`**: Specialized table for "Latest Visit" status cards.



---

## Key Learnings as a First Project
* **Full-Stack Data Workflow:** Bridging the gap between Python validation and Power BI visualization.
* **DAX Optimization:** Mastered Row vs. Filter context for reactive triage scores.
* **Data Reshaping:** Learned that unpivoting is essential for scalable clinical reports.
