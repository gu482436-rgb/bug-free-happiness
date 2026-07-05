# 第一章 AI 筛选修订包说明（2026-07-05）

这个文件夹是对 Claude Science 两轮输出的人工复核与整合版本。核心原则是：保留有证据支持的计算筛选结果，删除或改写容易被理解成实验验证的表述。

## 目录

- `manuscript/chapter1_manuscript_insert_clean.md`：可直接放入论文第一章的英文段落底稿。
- `manuscript/figure_captions_clean.md`：4 张图的保守图注。
- `manuscript/nsqienl_status_note.md`：NSQIENL 的最终统一口径。
- `manuscript/overclaiming_replacement_list.md`：网页或论文中需要替换的高风险词。
- `tables/table_1_v2_algorithmic_top5_clean.csv`：严格按 V2 算法结果保留的 Top5。
- `tables/table_2_synthesis_priority_shortlist_clean.csv`：实验合成优先级清单，和算法 Top5 分开。
- `figures/`：只保留新版图，文件名已经重命名，避免和旧图混淆。
- `source_claude_outputs/`：Claude Science 原始输出，作为审计来源备份。

## 关键口径

1. V2 算法 Top5 是：
   `NTQIENL`, `EVDATVKSL`, `NTQIDNL`, `TLTQTVENIR`, `MNDRDNEVDATLKTL`。

2. `NSQIENL` 不能写成 V2 Top5、Top20 或 Top100。它是 V2 肽库中的独立 7 aa 条目，但没有进入 V2 Top100，因此没有 V2 外部验证结果。

3. `NSQIENL` 只能作为“三文鱼场景合成优先候选假设”保留，前提是后续要补做等同于 V2 Top100 的外部验证。

4. 所有 AI4AVP、ToxinPred、AllerCatPro、hemotoxicity、docking 结果都只能写成 computational prediction，不得写成实验有效、安全、不过敏或确证结合。

## 推荐下一步

先把 `chapter1_manuscript_insert_clean.md` 和 `figure_captions_clean.md` 作为第一章正文和图注底稿。如果要更新网页或 HTML 报告，再按 `overclaiming_replacement_list.md` 做定点替换。
