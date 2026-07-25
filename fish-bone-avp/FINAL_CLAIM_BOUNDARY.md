# Final Claim Boundary

## Permitted Statements
- "The Handcrafted 433 XGBoost model achieved ROC-AUC = 0.9189 ± 0.0152 in 25-fold grouped cross-validation on the DLAVP training set."
- "On the locked DBAASP external dataset (Plan A, n=695), the frozen model achieved ROC-AUC = 0.5938 [95% CI: 0.5484–0.6402]."
- "External performance is lower than internal grouped CV, consistent with distribution shift between DLAVP (training) and DBAASP (external) data."
- "The frozen model's ROC-AUC on DBAASP exceeds that of no-training baselines (prevalence, constant, random)."
- "Calibration is degraded externally (intercept=0.75, slope=0.16 vs ideal 0, 1), consistent with distribution shift."

## Prohibited Statements
- ❌ "The model demonstrates real antiviral activity." — No clinical validation was performed.
- ❌ "The model has clinical utility." — This is a computational screening study.
- ❌ "The model generalizes universally." — External data shares similarity with training.
- ❌ "The model establishes causal mechanisms." — No causal inference methods were used.
- ❌ "Threshold optimization at t=0.90 confirms model validity." — Thresholds are exploratory only.
- ❌ "Baselines prove model superiority." — Baselines are simple references.
- ❌ "External data is completely independent." — Similarity overlap exists at ≥0.70 and ≥0.85.

## Scope
This evidence package supports computational reproducibility and methodological transparency.
All results are for research purposes only and should not be used for clinical decision-making,
regulatory submission, or therapeutic development without independent experimental validation.
