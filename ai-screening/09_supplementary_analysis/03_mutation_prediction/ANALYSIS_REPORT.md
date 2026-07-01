# 突变预测分析报告

## 野生型分数

| WT | RF | XGB | avg |
|---|---|---|---|
| P04_NTQIDNL | 0.8960 | 0.9796 | 0.9378 |
| P01_NTQIENL | 0.8940 | 0.9729 | 0.9335 |
| P03_TLTQTVENIR | 0.8800 | 0.9597 | 0.9199 |
| P02_EVDATVKSL | 0.8500 | 0.9692 | 0.9096 |
| P05_NSQIENL | 0.8700 | 0.9328 | 0.9014 |

## 突变统计

- 总突变体: 774
- 提升 > 0.02: 37
- 提升 > 0.05: 0
- 下降 > 0.02: 385

## Top 10 提升突变

| mutant_id            | wt_seq    | mutant_seq   |   RF_score |   XGB_score |   avg_score |   delta_avg |
|:---------------------|:----------|:-------------|-----------:|------------:|------------:|------------:|
| P02_EVDATVKSL_Sat_7R | EVDATVKSL | EVDATVRSL    |      0.952 |    0.984589 |    0.968295 |   0.0478727 |
| P01_NTQIENL_Sat_6E   | NTQIENL   | NTQIEEL      |      0.944 |    0.991225 |    0.967613 |   0.0471908 |
| P02_EVDATVKSL_Sat_7V | EVDATVKSL | EVDATVVSL    |      0.934 |    0.986445 |    0.960222 |   0.0398007 |
| P02_EVDATVKSL_Sat_7P | EVDATVKSL | EVDATVPSL    |      0.93  |    0.985558 |    0.957779 |   0.0373572 |
| P01_NTQIENL_Sat_6L   | NTQIENL   | NTQIELL      |      0.932 |    0.981223 |    0.956612 |   0.0361898 |
| P02_EVDATVKSL_Sat_7S | EVDATVKSL | EVDATVSSL    |      0.924 |    0.988332 |    0.956166 |   0.0357444 |
| P02_EVDATVKSL_Sat_7H | EVDATVKSL | EVDATVHSL    |      0.936 |    0.974829 |    0.955415 |   0.0349928 |
| P02_EVDATVKSL_Sat_7T | EVDATVKSL | EVDATVTSL    |      0.934 |    0.976686 |    0.955343 |   0.0349213 |
| P02_EVDATVKSL_S8L    | EVDATVKSL | EVDATVSL     |      0.92  |    0.98659  |    0.953295 |   0.0328734 |
| P02_EVDATVKSL_Sat_7Y | EVDATVKSL | EVDATVYSL    |      0.936 |    0.968435 |    0.952217 |   0.0317957 |

## 每个 WT 的 Top 3 提升突变


### P01_NTQIENL

| mutant_id            | mutant_seq   |   avg_score |   delta_avg |
|:---------------------|:-------------|------------:|------------:|
| P01_NTQIENL_Sat_6E   | NTQIEEL      |    0.967613 |   0.0471908 |
| P01_NTQIENL_Sat_6L   | NTQIELL      |    0.956612 |   0.0361898 |
| P01_NTQIENL_Ascan_6A | NTQIEAL      |    0.94856  |   0.0281378 |
### P02_EVDATVKSL

| mutant_id            | mutant_seq   |   avg_score |   delta_avg |
|:---------------------|:-------------|------------:|------------:|
| P02_EVDATVKSL_Sat_7R | EVDATVRSL    |    0.968295 |   0.0478727 |
| P02_EVDATVKSL_Sat_7V | EVDATVVSL    |    0.960222 |   0.0398007 |
| P02_EVDATVKSL_Sat_7P | EVDATVPSL    |    0.957779 |   0.0373572 |
### P03_TLTQTVENIR

| mutant_id               | mutant_seq   |   avg_score |   delta_avg |
|:------------------------|:-------------|------------:|------------:|
| P03_TLTQTVENIR_Sat_1E   | ELTQTVENIR   |    0.949293 |   0.0288716 |
| P03_TLTQTVENIR_Sat_7Q   | TLTQTVQNIR   |    0.944962 |   0.0245401 |
| P03_TLTQTVENIR_Ascan_5A | TLTQAVENIR   |    0.942054 |   0.021632  |
### P04_NTQIDNL

| mutant_id          | mutant_seq   |   avg_score |   delta_avg |
|:-------------------|:-------------|------------:|------------:|
| P04_NTQIDNL_Sat_4M | NTQMDNL      |    0.951315 |   0.0308933 |
| P04_NTQIDNL_Sat_4V | NTQVDNL      |    0.950549 |   0.0301269 |
| P04_NTQIDNL_Sat_4N | NTQNDNL      |    0.950108 |   0.0296865 |
### P05_NSQIENL

| mutant_id          | mutant_seq   |   avg_score |   delta_avg |
|:-------------------|:-------------|------------:|------------:|
| P05_NSQIENL_Sat_6E | NSQIEEL      |    0.947311 |  0.0268892  |
| P05_NSQIENL_Sat_2T | NTQIENL      |    0.933457 |  0.0130347  |
| P05_NSQIENL_Sat_6L | NSQIELL      |    0.930178 |  0.00975592 |

## 特征重要性 Top 20

| feature               |   avg_importance |
|:----------------------|-----------------:|
| net_charge_approx_pH7 |       0.033862   |
| sequence_length       |       0.0252191  |
| basic_residue_count   |       0.019625   |
| molecular_weight      |       0.0190078  |
| acidic_ratio          |       0.0167245  |
| AAC_K                 |       0.0127261  |
| glycine_ratio         |       0.0124278  |
| AAC_E                 |       0.0120374  |
| AAC_F                 |       0.0101911  |
| hydrophobicity_GRAVY  |       0.0100027  |
| AAC_Q                 |       0.00992498 |
| DPC_KK                |       0.00939043 |
| AAC_G                 |       0.00938459 |
| basic_ratio           |       0.00903604 |
| AAC_R                 |       0.0085567  |
| AAC_I                 |       0.00805942 |
| AAC_L                 |       0.00746795 |
| DPC_EL                |       0.00739879 |
| DPC_GK                |       0.00736848 |
| AAC_C                 |       0.00735541 |

## 结论

**最佳突变**: P02_EVDATVKSL_Sat_7R (EVDATVKSL → EVDATVRSL), avg=0.9683, Δ=+0.0479

该突变通过单点饱和突变获得，位于第7位 K→R 替换。
