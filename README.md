# Databuzz_March_PowerBI: Clinical Triage & System Analytics

![Project Status] Completed
![Developer] Zaheera Ganie
![Tools] Power BI, DAX, Python

## 📋 Executive Summary
This project represents a comprehensive milestone in clinical data analytics, bridging the gap between raw medical datasets and actionable healthcare insights. Developed as a high-performance interactive system, the dashboard enables healthcare providers to transition seamlessly from macro-level facility trends to micro-level patient diagnostics.

## 🐍 Data Science & Validation (Python / Google Colab)
Before visualization, I performed a rigorous **5-Phase Validation** using a Python/Pandas stack to ensure the synthetic dataset adhered to realistic clinical benchmarks.

### The 5-Phase Validation Process:
1. **Structural Validation:** Verified 20,200 rows and 25 columns with zero null values.
2. **Statistical Integrity:** Confirmed realistic distributions for Age (1–85) and Temperature (37°C–41°C).
3. **Medical Consistency:** Used grouping and aggregation to prove clinical patterns:
    * **Pass:** High-Risk patients correctly showed higher mean Glucose (209 mg/dL) and Systolic BP (130 mmHg).
    * **Pass:** Dengue cases showed the lowest mean Platelets (59k), while Bacterial infections showed the highest WBC (14.9k).
4. **Relational Integrity:** Validated 100% ID matching between `Patient_Symptoms` and `Blood_Test_Results`.
5. **Coverage Gap Analysis:** Identified and addressed missing indicators (Thyroid, Asthma, Medication Usage) to meet the 2026 competition brief.

*The Jupyter Notebook (`Patient_Data_Validation.ipynb`) containing the Python scripts and Seaborn distributions is included in this repository.*

---

## 📊 Dashboard Architecture

### Page 1: Main Dashboard (High-Level Overview)
* **Dynamic Risk Scoring:** Developed a DAX-based Triage Score that updates in real-time based on user-adjustable sliders for Fever and Glucose thresholds.
* **Real-time Triaging:** Utilized visual-level filters to isolate and highlight "At-Risk" populations for immediate clinical attention.

### Page 2: Patient Diagnostic Detail (Deep-Dive)
* **Drill-through Capability:** Implemented a seamless transition from the main table to a specialized history view for individual patients.
* **Clinical Observations Timeline:** Reshaped "wide" symptom data into a "long" format via Power Query to create a vertical, scalable observation log.

### Page 3: Clinical Performance & Trend Insights (AI-Driven)
* **Root Cause Analysis:** Utilized a **Decomposition Tree** to map the "Path to Risk," breaking down patient volume by Location, Gender, and Illness.
* **AI-Driven Influencers:** Leveraged the **Key Influencers AI Visual** to identify that Bacterial infections and Asthma history are the primary drivers of High-Risk classifications.
* **Temporal Ranking:** Implemented a **Ribbon Chart** to visualize the shifting dominance of different fever types (e.g., COVID vs. Malaria) across the calendar year.

---

## 🏗️ The Model (Star Schema)
The project utilizes a robust star schema to ensure high performance and filter integrity:
* **Fact_Symptoms:** Centralized table unpivoted for granular symptom and blood test analysis.
* **Dim_Patient:** Demographic hub containing age, gender, and location data.
* **Dim_Date:** A dedicated calendar table enabling Time Intelligence (MoM growth).
* **Risk_Legend:** A specialized dimension table for dynamic risk-tiering.



---

## 💡 Key Technical Learnings
* **Full-Stack Data Workflow:** Mastering the transition from Python-based data cleaning to Power BI visualization.
* **DAX Optimization:** Overcoming circular dependencies and mastering Row vs. Filter context for reactive triage scores.
* **Advanced AI Visuals:** Implementing machine learning visuals (Key Influencers) to automate the discovery of clinical correlations.
* **UI/UX Design:** Designing a professional, high-contrast interface tailored for fast-paced medical environments.

---
**Developer:** [Zaheera Ganie](https://github.com/YourGitHubUsername)  
**Project Date:** March 2026
