# Healthcare Analysis 

## Project Overview

This project presents a comprehensive analysis of 55,500 anonymized patient records from 10 major hospitals across the United States, focusing on patient demographics, medical conditions, hospital performance, treatment costs, and insurance coverage. Using Excel for data cleaning and feature engineering and Power BI for advanced visualizations and DAX-based analytics, the study uncovers key patterns in healthcare delivery. Findings highlight dominant age groups and chronic conditions like diabetes and hypertension, gender-based disparities in diagnoses, consistently high average treatment costs (~$25K–26K), and standardized hospital stay durations (~15.5 days). Regional differences in hospital admissions, high rates of abnormal test results, and a strong reliance on Medicare (50% of patients) are also revealed. The insights generated offer data-driven recommendations for improving patient care, resource allocation, and healthcare equity nationwide.

### Data Sources

The dataset used in this project consists of 55,500 anonymized patient records collected from 10 major hospitals across the United States. It was obtained from publicly available open data sources intended for public use.

### Tools

- Microsoft Excel
- Power BI

### Data Cleaning/Preparation

1. Handling Missing Values: Identified and addressed missing entries in fields such as gender, blood type, and admission/discharge dates.

2. Standardizing Categorical Variables: Normalized text data for fields like gender, blood type, and admission type to ensure uniformity and avoid duplication due to case or spelling inconsistencies.
3. Parsed and reformatted date columns (admission and discharge dates) to enable temporal calculations.
4. Feature Engineering:
   - Calculated “Days in Hospital” by computing the difference between admission and discharge dates
   - Created age group bins (e.g., 10–19, 20–29, ..., 80–89) using Excel’s XLOOKUP and pivot logic.
5.  Data Validation: Ensured all records had valid entries for critical fields and removed or flagged outliers and duplicates where necessary.

### Data Analysis

Following data cleaning and EDA, targeted analysis was conducted using DAX in Power BI to answer critical questions around patient demographics, hospital operations, treatment costs, and clinical outcomes. Key analyses included:

1. Most Frequent Patient Profiles
   - Identified the most common age group (50–59), gender (female), and blood types (A+, O+) using DAX mode calculations.
   - Created cross-tabulations of medical conditions by gender and age group.
2. Condition and Cost Analysis
   - Computed average billing amounts per condition. Surprisingly, all conditions (diabetes, hypertension, asthma, etc.) averaged around $25K–$26K, indicating potentially standardized billing structures.
   - Evaluated average days spent in hospital by condition (e.g., hypertension had the longest average stay: 15.64 days).
3. Test Results and Analysis
   - Analyzed the distribution of test results (abnormal, normal, inconclusive) by hospital. High abnormal result rates at top facilities (e.g., Houston Methodist, Johns Hopkins) suggest complex case management.
4. Medication Utilization
   - Mapped medication usage across conditions. Diabetes had the highest and most consistent medication use across aspirin, ibuprofen, etc
   - Cancer medication counts were low, reflecting reliance on specialized therapies outside common prescriptions.
5. Trend Analysis
   - Tracked admission and discharge trends over five years.
   - Spotted a dip in 2022 admissions and a decline in discharges from 2020 to 2023.
6. Hospital Load and Geographic Coverage
   - Ranked hospitals by patient volume and overlaid findings on a U.S. map.
   - Found urban hospitals dominate admissions; Houston Methodist treated 10× more patients than some peers.

### Results and Findings
The analysis yielded several impactful insights into patient demographics, clinical trends, and hospital operations across 10 major U.S. hospitals:

1. Patient Demographics
   - The majority of patients were aged 20–79, with the 50–59 age group accounting for the highest admissions (~8.4K).
   - Gender distribution was balanced (50% female, 40% male, 10% non-binary), indicating inclusive data collection.
   - A+ (35%) and O+ (25%) were the most common blood types.

2. Clinical Insights
Chronic conditions dominated the dataset:
   - Diabetes was the most prevalent, especially among female patients.
   - Hypertension was more common in males.
   - Obesity showed equal prevalence among males and females.
   - All major conditions (diabetes, hypertension, cancer, asthma, obesity) had remarkably uniform average billing costs (~$25K–26K).
Hospital stays averaged 15.4–15.6 days across conditions, with slightly longer durations for chronic illnesses like hypertension and arthritis.

3. Medication & Testing Patterns
   - Diabetes required the highest medication volume across standard drugs (e.g., aspirin, paracetamol).
   - Cancer treatments had lower prescription counts, reflecting specialized care.
   - Abnormal test results were disproportionately high at top hospitals (e.g., Houston Methodist), indicating complex case handling.

4. Operational Trends
   - Admissions fluctuated seasonally from 2020–2024, with a sharp dip in 2022 (likely pandemic-related).
   - Discharges declined consistently from 2020 to 2023, suggesting possible policy shifts or care delivery changes.
   - Medicare covered 50% of all patients, revealing a strong elderly or high-risk population segment. Private insurers (UnitedHealthcare, Aetna, Cigna) covered the remaining 50%.

5. Regional Insights
   - Patient volumes were concentrated in urban centers, especially Houston Methodist, which handled over 20K patients—10× more than some peers.
   - Coastal hospitals (NY, CA, MA) also showed high traffic, while rural areas were underrepresented

### Recommendations

Based on the analysis of patient data from 10 major U.S. hospitals, the following strategic recommendations are proposed to enhance healthcare delivery, resource management, and equity:

1. Expand Age-Specific Services:
 - Develop geriatric care outreach for patients aged 80+, where admissions drop sharply—potentially due to access barriers.
 - Launch adolescent-focused programs to improve care engagement for patients aged 10–19, a group significantly underrepresented in the dataset.

2. Address Gender Disparities
   - Implement targeted interventions for chronic conditions with gender skews:
   - Female-focused diabetes prevention and education.
   - Male-oriented hypertension and asthma screening programs.
   - Maintain inclusive gender identity tracking and ensure non-binary patients are considered in health program design.

3. Review Billing Uniformity
   - Investigate the unusually consistent treatment costs (~$25K–$26K) across conditions—this could mask under/overbilling or hinder cost optimization.
   - Conduct condition-specific cost-effectiveness analyses to ensure billing aligns with clinical complexity and outcomes.

4. Audit Test Protocols at High-Volume Hospitals
   - Review testing procedures at hospitals with high abnormal result rates (e.g., Houston Methodist) to assess for over-testing, case complexity, or quality issues.
   - Standardize test interpretation criteria across facilities where appropriate.

5. Balance Hospital Loads & Address Geographic Gaps
    - Support smaller hospitals or rural facilities to reduce overreliance on urban hubs like Houston Methodist.
    - Expand care access in underrepresented regions through telemedicine or satellite facilities.

6. Optimize Medication Use
   - Use consistent prescription patterns for diabetes and hypertension as baselines to assess protocol adherence.
   - Investigate the low medication usage in cancer care to ensure proper tracking of oncology treatments outside the standard formulary.

7. Mitigate Insurance Risk Exposure
   - Diversify hospital reimbursement strategies given the heavy reliance on Medicare (50% of patients).
   - Evaluate how different insurance providers influence treatment patterns and patient outcomes.
  
### Limitations

While this project provides meaningful insights into healthcare operations and patient trends, several limitations should be considered when interpreting the findings:
1. Lack of Population Benchmarks
   - The analysis lacks regional population data to determine whether hospital admissions are proportionate to local healthcare needs.
   - No control group or national average data is available for comparative benchmarking.

2. Limited Clinical Context
   - Test results labeled as “Abnormal,” “Normal,” or “Inconclusive” are not clinically defined in the dataset, limiting medical interpretation.
   - Billing amounts are aggregated and lack itemized breakdowns (e.g., procedures, medications, length of stay costs), hindering cost attribution.

3. Representation & Bias
   - Non-binary patient representation (10%) is relatively small, which may limit the statistical significance of condition-based comparisons.
   - The dataset appears to focus on urban and high-volume hospitals, potentially underrepresenting rural or community healthcare facilities.

4. Static Snapshot
   - The dataset represents a single combined snapshot across multiple years (2020–2024) without dynamic updates. Trends may shift over time due to policy, technology, or external factors (e.g., pandemics).
