# Final Results Summary

## 1. Internal Grouped Cross-Validation
| Model | ROC-AUC | PR-AUC | MCC | Brier | Sensitivity | Specificity |
|-------|---------|-------|-----|-------|-------------|-------------|
| Handcrafted 433 XGBoost | 0.9189±0.0152 | 0.9159±0.0211 | 0.6920±0.0353 | 0.1124±0.0113 | 0.8448±0.0385 | 0.8477±0.0187 |
| Nested Late Fusion | 0.9272±0.0134 | 0.9280±0.0185 | 0.7087±0.0424 | 0.1056±0.0109 | 0.8578±0.0331 | 0.8514±0.0277 |

Training: 2,350 DLAVP sequences. Evaluation: 25-fold grouped cross-validation (no homologous peptides across folds).

## 2. External DBAASP Validation (Frozen Model)
### Plan A (Primary, n=695: 510 positive / 185 negative)
| Metric | Estimate | 95% CI |
|--------|:--------:|:------:|
| ROC-AUC | 0.5938 | [0.5484, 0.6402] |
| PR-AUC | 0.8198 | [0.7931, 0.8459] |
| MCC | 0.0597 | [-0.0215, 0.1414] |
| Brier | 0.2475 | [0.2286, 0.2662] |
| Sensitivity | 0.8451 | — |
| Specificity | 0.2054 | — |
| PPV | 0.7457 | — |
| NPV | 0.3248 | — |

### Plan B (Balanced, n=200: 100 positive / 100 negative, seed=42)
ROC-AUC = 0.5454 [0.4626, 0.6265]

### Plan C (Stratified, n=160: 80 positive / 80 negative)
ROC-AUC = 0.5519 [0.4633, 0.6430]

## 3. Threshold Sensitivity
Primary threshold: 0.50 (pre-specified). Exploratory range: 0.10–0.90.
At t=0.50 (Plan A): Sensitivity = 0.8451, Specificity = 0.2054
All non-0.50 thresholds are exploratory; no threshold was selected as "optimal."

## 4. Calibration Transport (Plan A)
- Brier: 0.2475
- Calibration intercept: 0.75 (ideal: 0)
- Calibration slope: 0.16 (ideal: 1)
External calibration is degraded relative to internal, consistent with distribution shift.

## 5. Similarity Stratification (Plan A)
| Strata | n | Pos | Neg | ROC-AUC |
|--------|---|-----|-----|---------|
| <0.70 | 457 | 339 | 118 | 0.6235 |
| 0.70–<0.85 | 122 | 81 | 41 | 0.4532 |
| ≥0.85 | 116 | 90 | 26 | 0.6410 |

## 6. Internal-External Comparison (Handcrafted 433 XGBoost → Plan A)
| Metric | Internal | External | Difference |
|--------|:--------:|:--------:|:----------:|
| ROC-AUC | 0.9189 | 0.5938 | −0.3251 |
| MCC | 0.6920 | 0.0597 | −0.6323 |
| Brier | 0.1124 | 0.2475 | +0.1351 |
| Sensitivity | 0.8448 | 0.8451 | +0.0003 |
| Specificity | 0.8477 | 0.2054 | −0.6423 |

## 7. Baselines
The frozen model (Plan A ROC-AUC 0.5938) exceeds prevalence-only (0.5000),
constant 0.5 (0.5000), and random (0.5087) baselines. This observation is descriptive;
no statistical significance test was performed.

## Limitations
See FINAL_CLAIM_BOUNDARY.md and post76 manuscript documents for full limitations.
