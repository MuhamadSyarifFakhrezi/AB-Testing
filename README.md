# AB Testing
## Experiment Overview
This project aims to evaluate the effectiveness of a new application layout in  increasing user engagement compared to the previous version, measured primarily through Click-Through Rate (CTR) which was expected to increase by at least 5%.

## Experiment Design
- Variant: Control Group (old version) vs. Test Group (old version)
- Sample size per group required: 51,258 (calculated using Cohen's d)
- Data collected: 60,000 per group
- Users were randomly devided into two groups
- Duration: 13-day estimate assuming an average of 8000 users per day

## Hypothesis
### Business Hypothesis
H₀: There is no difference between control group and test group.

H₁: Control group has at least 5% higher CTR than test group.

### Statistical Hypothesis
H₀: There is no statistically significant difference between control group and test group in CTR.

H₁: There is statistically significant difference between control group and test group in CTR.

## Metrics
| **Metric** | **Type** | **Hypothesis Tested** | **Test Used** |
| --- | --- | --- | --- |
| CTR (Primary) | Continuous | Test CTR ≠ Control CTR | Mann-Whitney U test |
| Views (Guardrail) | Continuous | Test views ≥ Control views | One-sided test |
| Clicks (Secondary) | Continuous | Test clicks > Control clicks | One-sided test |

`CTR is calculated per user as clicks/views, treated as a continuous variable.`

## Power Analysis
To ensure sufficient sensitivity in detecting meaningful changes:
- Significance level (α): 5%
- Power (1-β): 80%
- Minimum Detectable Effect: 5%
- Baseline CTR: 3.5%

## Key Result
- **CTR uplift**: +11.52% with p-value = 0.00

- **Views**: No significant decrease (guardrail passed)

- **Clicks**: Increased significantly (secondary metric supported)

## Conclusion
Based on the statistical significance and positive uplift in the primary metric (CTR), the new layout can be recommended for broader rollout. Additionally, the stability of the views metric and the increase in clicks strengthen confidence in the feature’s positive user impact.

## Repository Structure
├── ab_test_results_aggregated_views_clicks_2.csv
├── notebook.ipynb
├── README.md
└── images
