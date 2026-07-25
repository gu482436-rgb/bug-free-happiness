# Final Master Evidence Handoff Package

**Status:** COMPLETE_FINAL_HANDOFF_READY
**Generated:** 2026-07-25 12:31:42

## Purpose
This package consolidates all valid computational evidence for the antiviral peptide
AI screening project. It includes internal grouped cross-validation results,
external DBAASP validation, threshold sensitivity, calibration transport analysis,
similarity stratification, and baselines.

## Contents
1. **final_master_metrics.csv** — All metrics from internal (M57/M58) and external (M73/M74/M76/post76) evaluations.
2. **final_module_dependency_graph.csv** — Complete dependency chain from sequence data to final handoff.
3. **final_file_index.csv** — Index of all files in this package.
4. **final_sha256_manifest.csv** — SHA256 integrity manifest.
5. **FINAL_RESULTS_EN.md / FINAL_RESULTS_ZH.md** — Results summaries in English and Chinese.
6. **FINAL_CLAIM_BOUNDARY.md** — Permitted and prohibited claims.
7. **FINAL_REVIEWER_RISK_POINTS.md** — Anticipated reviewer questions.
8. **mobile_summary/** — Mobile-friendly summaries.
9. **website_pending/** — Website preview data and release checklist.

## Key Results
### Internal (Grouped CV, 25-fold)
- Handcrafted 433 XGBoost: ROC-AUC = 0.9189 ± 0.0152, MCC = 0.6920 ± 0.0353
- Nested Late Fusion: ROC-AUC = 0.9272 ± 0.0134, MCC = 0.7087 ± 0.0424

### External (Locked DBAASP)
- Plan A (n=695, 510 pos / 185 neg): ROC-AUC = 0.5938 [95% CI: 0.5484–0.6402]
- Plan B (n=200, 100/100): ROC-AUC = 0.5454 [95% CI: 0.4626–0.6265]
- Plan C (n=160, 80/80): ROC-AUC = 0.5519 [95% CI: 0.4633–0.6430]

### Baseline Comparison
- Frozen model (Plan A ROC-AUC 0.5938) > prevalence (0.5000) and random (~0.50) baselines.
- No statistical significance test performed; observation is descriptive.

## Exclusions
- M71 (old 692-count results, CI errors) — EXCLUDED
- M72 (DUPLICATE_MODULE_ID_DATA_LOCK_RECORD) — EXCLUDED
- DBAASP raw sequences and experimental records — NOT PUBLISHED

## Claim Scope
This evidence package supports computational reproducibility and methodological transparency.
It does NOT establish:
- Real antiviral activity in clinical settings.
- Clinical utility or therapeutic efficacy.
- Universal model generalization.
- Causal mechanisms for predicted peptides.

## Data Sources
- Internal: M57 (Handcrafted 433 XGBoost, 25-fold grouped CV), M58 (Nested Late Fusion)
- External predictions: M73 (corrected, 695/200/160)
- External metrics: M74, A1-75 (metric recheck + transportability)
- Supplement: post76 (figures S1–S7, manuscript documents)
