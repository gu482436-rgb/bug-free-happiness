# 项目文件清单 — 给 Codex 用

## 基础路径
BASE = ~/Documents/mimo code/lucaVirus_analysis_20260627/
SYSTEM = ~/Documents/mimo code/

## 一、论文材料

| 用途 | 路径 | 说明 |
|:-----|:-----|:-----|
| 论文草稿 | `BASE/paper_draft.md` | 英文完整草稿，含Abstract/Results/Discussion/Methods |
| Methods段落 | `BASE/Methods_section.txt` | 可直接粘贴 |
| 分析报告 | `BASE/ANALYSIS_REPORT.md` | 中文完整报告 |

## 二、数据表

| 用途 | 路径 | 说明 |
|:-----|:-----|:-----|
| Table 1 | `BASE/Table1_properties.csv` | MW, pI, GRAVY, Charge, Formula |
| 位置重要性 | `BASE/mlm_details_full.csv` | 40位置×概率+Top5+熵 |
| 汇总 | `BASE/mlm_summary.csv` | 5肽汇总 |
| 置换偏好 | `BASE/substitution_preference.csv` | 每位点Top3替代AA |
| 突变方案 | `BASE/mutation_design.csv` | 40位置突变建议 |
| 合成优先级 | `BASE/synthesis_priority.csv` | 排序评分 |
| I4N引物 | `BASE/primers_I4N.csv` | 定点突变引物 |
| 统计检验 | `BASE/statistics_results.csv` | t-test结果 |
| 特征向量 | `BASE/peptide_embeddings_2560d.csv` | 13肽×2560维 |

## 三、图表（论文用）

| 用途 | 路径 | 格式 | 说明 |
|:-----|:-----|:----:|:-----|
| Figure 1 | `BASE/Figure1_position_importance.png` | 300dpi | 位置重要性柱状图 |
| Figure 2 | `BASE/Figure2_comprehensive_panel.png` | 300dpi | 6面板综合 |
| 序列Logo | `BASE/NTQxxxNL_sequence_logo.png` | 300dpi | NTQxxxNL motif |
| 互作网络 | `BASE/network_graph.png` | 200dpi | 候选-已知-随机网络 |
| 热图 | `BASE/similarity_heatmap.png` | 200dpi | 层次聚类 |
| t-SNE | `BASE/tsne_visualization_2560d.png` | 200dpi | 2560维t-SNE |

## 四、交互式（浏览器打开）

| 用途 | 路径 | 大小 | 说明 |
|:-----|:-----|:----:|:-----|
| 综合看板 | `BASE/dashboard.html` | 17KB | 8面板全部结果 |
| t-SNE交互 | `BASE/interactive_tsne.html` | 4.6MB | 悬停显肽名 |
| 热图交互 | `BASE/interactive_heatmap.html` | 4.6MB | 缩放看数值 |
| 重要性交互 | `BASE/interactive_importance.html` | 4.6MB | 滚动看5肽 |

## 五、补充材料

| 用途 | 路径 | 说明 |
|:-----|:-----|:-----|
| 综合Excel | `BASE/Supplement_All_Results.xlsx` | 6 sheets |
| 安全性 | `BASE/Safety_Assessment.xlsx` | 7 sheets |
| 构象分析 | `BASE/conformer_analysis.json` | 数值摘要 |
| 构象能量图 | `BASE/conformer_energy_distribution.png` | WT vs I4N |
| 构象RMSD图 | `BASE/conformer_rmsd_distribution.png` | 柔性对比 |

## 六、分子模拟

### A. AutoDock Vina 结果
路径: `BASE/docking_results/`
| 文件 | 说明 |
|:-----|:-----|
| `4OOS.pdb` | 诺如病毒VP1受体 |
| `NSQIENL_WT_docked.pdbqt` | WT对接构象(9个) |
| `NSQIENL_I4N_docked.pdbqt` | I4N对接构象(9个) |
| `vina_docking_results.txt` | 分数汇总 |
| `VP1_receptor.pdbqt` | 受体PDBQT |
| `complex_viewer.html` | 3D交互视图 |

### B. HDOCK 在线提交
路径: `BASE/for_HDOCK_submission/`
包含: receptor.pdb, NSQIENL_WT.pdb, NSQIENL_I4N.pdb, README.txt
提交地址: http://hdock.phys.hust.edu.cn/

### C. GROMACS MD
路径: `BASE/GROMACS_input/`
每个肽段有独立目录，含 PDB + md.mdp + README.md

## 七、系统工具

路径: `~/Documents/mimo code/`
| 工具 | 用途 |
|:-----|:-----|
| `analyze.py` | 全自动流水线: 输入CSV→特征+位置重要性+相似度+安全性+Excel |
| `create_task_doc.py` | 任务记录生成: 交互式或命令行参数 |
| `README.md` | 系统说明 |
| `执行任务清单/` | 所有任务docx存档 |

## 八、核心结论摘要

1. **最推荐肽**: NSQIENL (合成优先级0.805, 区分度+0.045)
2. **最佳突变**: I4N (Asn替代Ile, ΔE=-0.17, 互作模式转向氢键)
3. **安全性**: 无毒, 不致敏, NTQxxxNL三肽胃蛋白酶稳定
4. **引物**: Forward=5'-GAATTCAATTCTCAAAATGAAAATCTTGGATCC-3'
5. **NTQxxxNL**: 鱼骨胶原独有motif, 已知抗病毒库中不存在
