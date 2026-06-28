
# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Project Overview

This project evaluates the effectiveness of a new onboarding campaign introduced by a subscription-based digital product company. An A/B experiment was conducted to compare the existing onboarding experience (Control Group) with a redesigned onboarding flow (Treatment Group). The objective was to determine whether the new onboarding process should be rolled out to all users based on statistical evidence and business impact.

---

## Business Problem

The company aims to increase the number of users who convert into paying customers without negatively impacting customer experience. Before launching the new onboarding experience, leadership requires evidence that the treatment delivers a measurable improvement in business performance while maintaining acceptable levels of customer satisfaction and revenue quality.

The analysis addresses the following business question:

**Should the new onboarding experience be launched to all users based on the experiment results?**

---

## Dataset

**Dataset Used:** `campaign_experiment_data.xlsx`

The dataset contains user-level experiment data including:

- User ID
- Signup Date
- Experiment Group
- Region
- Device Type
- Traffic Source
- Plan Type
- Landing Page Visits
- Trial Starts
- Onboarding Completion
- Paid Conversion
- Revenue (30 Days)
- Support Tickets
- Refund Requests
- Days to Convert
- Engagement Score

---

## Tools & Technologies

- Google Colab
- Python
- Pandas
- NumPy
- SciPy
- Microsoft Excel
- GitHub

---

## Data Preparation

The dataset was validated before analysis to ensure data quality and consistency.

The following validation steps were performed:

- Checked for missing values
- Identified duplicate User IDs
- Removed 8 exact duplicate records
- Verified binary variables contained only valid values (0 and 1)
- Reviewed revenue distribution for potential outliers
- Verified segment distribution across Region, Device Type, Traffic Source and Plan Type
- Standardized the Signup Date format (DD-MM-YYYY)

The final analytical dataset contains **1,400 unique user records**.

---

## North Star Metric

### Paid Conversion Rate

Paid Conversion Rate was selected as the North Star Metric because it directly measures the percentage of users who become paying customers after completing the onboarding journey. Improving this metric contributes directly to subscription growth, recurring revenue and long-term business growth.

---

## KPI Framework

### Primary KPI Drivers

- User Acquisition
- User Activation
- Monetization

### Supporting Metrics

- Landing Page Visit Rate
- Trial Start Rate
- Onboarding Completion Rate
- Average Revenue per User
- Average Revenue per Converted User

### Guardrail Metrics

The following metrics were monitored to ensure conversion improvements did not negatively impact customer experience:

- Refund Rate
- Support Ticket Rate
- Engagement Score

---

## Experiment Analysis

The Control and Treatment groups were compared using:

- User Count
- Landing Page Visit Rate
- Trial Start Rate
- Onboarding Completion Rate
- Paid Conversion Rate
- Average Revenue per User
- Average Revenue per Converted User
- Refund Rate
- Support Ticket Rate
- Average Engagement Score
- Average Days to Convert

Additional segment-level analysis was completed across Region, Device Type and Traffic Source.


---

## Hypothesis Testing

An Independent Two-Sample Welch's t-test was performed.

### Hypotheses

**Null Hypothesis (H₀):**
There is no statistically significant difference in Paid Conversion Rate between the Control and Treatment groups.

**Alternative Hypothesis (H₁):**
The Treatment group achieves a higher Paid Conversion Rate than the Control group.

### Test Details

- Statistical Test: Independent Two-Sample Welch's t-test
- Test Direction: One-tailed
- Significance Level (α): 0.05

### Results

| Metric | Value |
|---------|------:|
| Control Paid Conversion Rate | **3.19%** |
| Treatment Paid Conversion Rate | **7.04%** |
| T-Statistic | **3.291** |
| P-Value | **0.001** |

Since the P-value is less than 0.05, the null hypothesis was rejected.

The analysis demonstrates that the Treatment onboarding experience produced a statistically significant improvement in Paid Conversion Rate compared with the existing onboarding process.

---

## Business Recommendation

Based on the statistical evidence, the Treatment onboarding experience is recommended for rollout.

The Treatment group achieved a Paid Conversion Rate of **7.04%**, compared with **3.19%** for the Control group. The hypothesis test confirmed that this improvement is statistically significant (t = 3.291, p = 0.001), indicating that the observed difference is unlikely to have occurred by chance.

Although the results support deployment, the business should continue monitoring Refund Rate, Support Ticket Rate and Engagement Score after rollout.

---

## Assumptions

- Duplicate User IDs identified in the dataset were exact duplicates and were removed.
- Binary variables contained only valid values (0 or 1).
- Users were randomly assigned to Control and Treatment groups.
- The dataset accurately represents user behaviour during the experiment period.

---

## Limitations

- The analysis is limited to the provided dataset.
- External business factors such as seasonality and marketing campaigns were not considered.
- Statistical significance does not guarantee identical future business performance.
- Long-term customer retention was outside the scope of this experiment.

---

## Repository Structure

part2_kpi_experiment/

├── data/
│   └── campaign_experiment_data.xlsx

├── analysis/
│   ├── experiment_analysis.xlsx
│   └── hypothesis_test_notes.md

├── outputs/
│   ├── experiment_summary.xlsx
│   ├── kpi_tree.png
│   └── recommendation_memo.md

├── screenshots/
│   ├── summary_metrics.png
│   ├── hypothesis_test_output.png
│   └── kpi_tree_preview.png

└── README.md

---

## Repository Contents

- Original experiment dataset
- Analysis workbook
- KPI Tree
- Experiment Summary
- Hypothesis Test Notes
- Recommendation Memo
- Supporting Screenshots
- README Documentation

---

## Screenshots Included

- summary_metrics.png
- hypothesis_test_output.png
- kpi_tree_preview.png

---

## Conclusion

The experiment demonstrates that the redesigned onboarding experience significantly improved Paid Conversion Rate compared with the existing onboarding process. Based on statistical evidence and business impact, the Treatment onboarding flow is recommended for deployment. Continued monitoring of guardrail metrics will help ensure that increased conversions are achieved while maintaining customer satisfaction and revenue quality.
