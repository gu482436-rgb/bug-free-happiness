# Final Reviewer Risk Points

## 1. "Internal CV (ROC-AUC 0.92) vs external (0.59). Why such a large gap?"
**Response:** The gap reflects distribution shift between DLAVP and DBAASP data — different sources, assays, label definitions, and peptide families. External evaluation measures transfer performance under shift, not replication of internal results. The gap is expected and reported transparently.

## 2. "Specificity drops from 0.85 (internal) to 0.21 (external). Is the model broken?"
**Response:** No. The model was trained on DLAVP where active/inactive distributions differ from DBAASP. The model's sensitivity transfers well (0.845 both internal and external), but the false positive rate increases on DBAASP data. This is characteristic of a screening model under distribution shift.

## 3. "Calibration is poor. Why not recalibrate?"
**Response:** Recalibration on external data would violate the frozen-model protocol. External calibration degradation is expected under distribution shift and is reported to inform interpretation.

## 4. "Why use old M71 data?"
**Response:** We do not. M71 (692 records, CI errors) is explicitly excluded. All external results use M73 corrected predictions (695/200/160 records) with verified CI integrity.

## 5. "Threshold t=0.90 shows better MCC. Why not use it?"
**Response:** The 0.50 threshold was pre-specified. Post-hoc threshold selection would constitute undisclosed multiple testing. t=0.90 is exploratory only and comes at the cost of reduced sensitivity.

## 6. "Baseline comparison shows model > random. Does this confirm the model works?"
**Response:** The model captures signal beyond random chance on this specific external dataset. However, no pre-registered significance test was performed. This observation is descriptive, not confirmatory.

## 7. "Has raw DBAASP data been published?"
**Response:** No. Only derived fields (accession, binary label, aggregated statistics) are included. Raw sequences remain in protected local storage per DBAASP academic use terms.
