High-Precision Survey Data Quality Pipeline
Project Overview

This project builds a robust, automated data-quality pipeline for large-scale survey data.
The goal is to identify, diagnose, and remove structured noise from real-world survey responses while preserving statistical reliability for downstream analysis.

The pipeline was designed with a multi-signal approach, avoiding reliance on any single heuristic for response filtering.

Dataset

53,981 survey responses

Multi-dimensional Likert-scale questionnaire data

Demographic variables (age, gender, country, etc.)

Presence of:

Missing and inconsistent entries

Repetitive and low-effort responses

Structured noise patterns not detectable via simple thresholds

Methodology
1. Data Exploration & Validation

Initial schema inspection and exploratory analysis

Distributional checks to understand raw response behavior

SQL-based validation for cross-checking aggregates and consistency

2. Multi-Layered Anomaly Detection

Implemented independent noise-detection signals, including:

Demographic sanity checks

Long-string and repetitive sequence detection

Variance-based inconsistency thresholds

Joint probability density diagnostics to flag implausible response combinations

3. Signal Independence Verification

Constructed correlation heatmaps across all anomaly flags

Verified low overlap between signals, confirming that each method captured distinct noise patterns rather than redundant artifacts

4. Robustness Testing

Compared cleaned vs. raw distributions

Used randomly generated response baselines to distinguish structured noise from expected randomness

Performed controlled distributional comparisons to validate filtering decisions

Results & Insights

Removed 2,707 high-noise responses (~5%)

Preserved core statistical properties of the dataset

Demonstrated that a multi-signal pipeline outperforms single-heuristic filtering

Identified demographic-linked noise trends, including:

U-shaped noise risk curves

Inverse relationships between age and specific response inconsistencies

Visualized findings using Power BI dashboards for interpretability

Tools & Technologies

Python (Pandas, NumPy)

SQL (data exploration & validation)

Statistical analysis

Power BI (distribution comparison, dashboarding, validation)

Jupyter Notebook

Why This Project Matters

This project reflects real-world analytics work:

Messy, high-volume data

Ambiguous quality issues

Need for defensible, statistically grounded decisions

The approach mirrors how production analytics pipelines are built in survey research, product analytics, and applied data science roles.

Author

Gagandeep Singh
MSc Physics (TIFR) | B.Tech (IIT Mandi)
Aspiring Data Analyst / Business Analyst
Based in Bangalore
