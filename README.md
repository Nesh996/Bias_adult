Bias Audit Report: Adult Census Income Dataset
Introduction

This project audits a machine learning model trained on the Adult Census Income dataset to detect and mitigate bias. The model predicts whether an individual earns more than $50,000 per year based on demographic and employment features, including age, education, occupation, race, and sex.

Historical income disparities exist in this dataset, especially along gender and racial lines, so evaluating fairness is essential before deploying such models in real-world systems.

📄 Full Bias Audit Report

Protected Groups

The audit focuses on groups historically subject to discrimination:

Sex (Female vs Male)
Race
Baseline Model
Algorithm: Logistic Regression
Accuracy: 78.8%
Fairness Metrics:
Statistical Parity Difference: -0.139
Disparate Impact: 0.144
Equal Opportunity Difference: -0.228

Analysis shows men have higher predicted income rates than women, highlighting bias in the model.

Bias Mitigation
Reweighing: Adjusted sample weights to reduce bias.
Accuracy remains 78.8%
Fairness metrics show minor changes.
No-Sex Model: Removed sex as a feature.
Accuracy: 78.6%
Slight improvement in fairness, but bias persists due to proxy variables (e.g., occupation, education).
Key Insights
Removing sensitive attributes alone is not enough; indirect bias persists.
Features that correlate with protected attributes can reproduce discrimination.
Continuous monitoring and evaluation are essential to maintain fairness.
Recommendations
Increase representation of underrepresented groups in data collection.
Audit and review proxy variables for bias.
Include socio-economic factors that affect income predictions.
Regularly recalculate fairness metrics to track improvements.
Conclusion

Bias in income prediction models can cause real-world harm, particularly to women and racial minorities, affecting employment and financial opportunities.
Even after mitigation, indirect bias can remain, showing the importance of fairness auditing and ethical considerations in machine learning.
This audit highlights that responsible model development requires accuracy, fairness, transparency, and accountability.
