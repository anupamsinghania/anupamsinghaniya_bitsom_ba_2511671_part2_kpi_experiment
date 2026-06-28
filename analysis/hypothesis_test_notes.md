
# Hypothesis Test Notes

## Objective

The objective of this analysis was to determine whether the new onboarding campaign (Treatment) improved the Paid Conversion Rate compared with the existing onboarding experience (Control). The results of this experiment support the business decision on whether the new onboarding experience should be rolled out to all users.

---

## Primary Metric

**Paid Conversion Rate**

Paid Conversion Rate was selected as the primary metric because it directly measures the percentage of users who become paying customers after completing the onboarding journey. Improving this metric contributes directly to subscription growth, recurring revenue, and long-term business growth. While other metrics provide supporting evidence, Paid Conversion Rate remains the most appropriate indicator of business success for this experiment.

---

## Hypotheses

### Null Hypothesis (H₀)

There is no statistically significant difference in the Paid Conversion Rate between the Control group and the Treatment group.

### Alternative Hypothesis (H₁)

The Treatment group achieves a higher Paid Conversion Rate than the Control group.

---

## Statistical Test

- **Test Used:** Independent Two-Sample Welch's t-test
- **Test Direction:** One-tailed
- **Significance Level (α):** 0.05

---

## Test Results

| Metric | Value |
|---------|------:|
| Control Paid Conversion Rate | **3.19%** |
| Treatment Paid Conversion Rate | **7.04%** |
| T-Statistic | **3.291** |
| P-Value | **0.001** |

---

## Decision Rule

Reject the null hypothesis if the P-value is less than the significance level of **0.05**.

---

## Decision

The calculated P-value (**0.001**) is significantly lower than the predefined significance level (**0.05**). Therefore, the null hypothesis is rejected.

---

## Business Interpretation

The statistical analysis indicates that the Treatment onboarding experience produced a significant improvement in Paid Conversion Rate compared with the existing onboarding flow. Users exposed to the redesigned onboarding process converted to paid subscriptions at **7.04%**, compared with **3.19%** for the Control group.

The low P-value suggests that the observed improvement is unlikely to have occurred due to random variation. From a business perspective, the new onboarding experience demonstrates stronger commercial performance and provides sufficient evidence to support rollout.

Although the experiment delivered positive results, conversion should not be evaluated in isolation. Following deployment, the business should continue monitoring guardrail metrics such as Refund Rate, Support Ticket Rate and Engagement Score to ensure that higher conversions are achieved without compromising customer experience or revenue quality.

---

## Conclusion

Based on the statistical evidence and observed business improvement, the Treatment onboarding experience is recommended for deployment. The experiment successfully demonstrated a statistically significant increase in Paid Conversion Rate while providing a strong foundation for future optimization and continuous performance monitoring.
