# Project Data Codebook (Version 1.0)

This codebook defines the standardized variables for the international multi-site cluster-randomized trial (CRCT) testing the **Small Batch Size Model (≤12)**. All collaborating sites must format their local CSV data exports to match this schema precisely to ensure seamless data aggregation and reproducibility via the GitHub analysis stack.

## 📊 Variable Definitions

| Variable Name | Data Type | Units / Format | Description |
| :--- | :--- | :--- | :--- |
| `student_id` | String | Encrypted/Anonymized Hash | Unique identifier for each student to protect local privacy. Do not use real names. |
| `cluster_id` | String | SiteCode-BatchNumber | Unique ID for the specific classroom cohort (e.g., `TEZ-01`, `US-A-04`). |
| `arm` | Integer | 0 = Control, 1 = Intervention | `0` represents a standard mass batch (≥25 students). `1` represents a micro-batch (≤12 students). |
| `pretest_score` | Float | Percentage (0.00 - 100.00) | Baseline score on the standardized PCMB concept test administered prior to the cohort phase. |
| `posttest_score` | Float | Percentage (0.00 - 100.00) | Immediate post-intervention score on the identical or parallel concept test. |
| `retention_score_3m` | Float | Percentage (0.00 - 100.00) | Mid-term retention score administered exactly 3 months post-intervention. |
| `turns_per_hour` | Float | Count / Instructional Hour | Average number of discrete verbal/academic interaction loops recorded per student, per hour. |
| `extraneous_load_score` | Float | Scale (1.00 - 7.00) | Standardized self-report metric tracking perceived mental overload during complex STEM tasks. |
| `learned_helplessness_score` | Float | Scale (1.00 - 5.00) | Post-test affective scale capturing problem-avoidance behaviors and perceived task efficacy. |
| `teacher_experience_years` | Integer | Total Years | Total years of professional secondary or university-level STEM teaching experience (Covariate). |
| `fidelity_score` | Float | Percentage (0.00 - 100.00) | External observer audit score tracking adherence to the 5-second wait time and Neuro-Map updating protocols. |

---

## 🛠️ Implementation Note for Thinkers & Researchers
When exporting your site-level data for central aggregation, please ensure your local database columns map exactly to the `Variable Name` keys listed above. This codebook guarantees that your data can be piped instantly into our upcoming multilevel mixed-effects models without manual data cleaning.
