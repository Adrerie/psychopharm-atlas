# 接手说明 | Psychopharm Atlas · Wave 16 收尾（2026-11-10）

本文件只汇总**接手所需事实与未决问题**，不启动新任务，也不增加新流程。后续维护以 GitHub `main` 为唯一基线，先读 [AGENTS.md](AGENTS.md)、[SCORING.md](SCORING.md)、[SOURCES.md](SOURCES.md)、[PLAN.md](PLAN.md)。

## 当前完成度

- 药物主档案：**384** 份（核心六组 280，跨组 104）。状态 **249 reviewed / 7 indexed / 128 basic**。
- 跨组选录目录：**91** 条，其中 **89** 条已建档。余下 `N07BC51` 和 `N06DA53` 仅为尚无可核验具体产品的复方分类记录，**不计为缺失药品**。
- 专题分析：`analysis/` **29** 份，采用问题导向，未设配额。索引见 [catalog/analyses.md](catalog/analyses.md)（按问题类型分组，含建立日期与主条目数）。2026-11-11 新增 [benzodiazepine-withdrawal-label-boundaries.md](analysis/benzodiazepine-withdrawal-label-boundaries.md)（苯二氮䓬类停药）、[qt-thresholds-label-boundaries.md](analysis/qt-thresholds-label-boundaries.md)（QT 阈值与监测流程）、[anticholinergic-burden-evidence-layers.md](analysis/anticholinergic-burden-evidence-layers.md)（抗胆碱能负担的四层证据）、[drug-vs-supplement-identity-layers.md](analysis/drug-vs-supplement-identity-layers.md)（药品与膳食补充剂的注册层边界）、[antidepressant-discontinuation-label-boundaries.md](analysis/antidepressant-discontinuation-label-boundaries.md)（抗抑郁药停药症状与发生率边界）、[racetams-approval-vs-evidence.md](analysis/racetams-approval-vs-evidence.md)（拉西坦类促智药的批准与证据边界）、[pim-standards-trigger-and-local-rates.md](analysis/pim-standards-trigger-and-local-rates.md)（老年 PIM 标准的分级与本地占比边界）、[antipsychotic-metabolic-burden-layers.md](analysis/antipsychotic-metabolic-burden-layers.md)（抗精神病药代谢负担的三层证据边界）、[hyponatremia-denominators-and-monitoring.md](analysis/hyponatremia-denominators-and-monitoring.md)（低钠血症的分母与监测边界）、[eps-td-dose-links-and-anticholinergic-boundary.md](analysis/eps-td-dose-links-and-anticholinergic-boundary.md)（EPS 与迟发性运动障碍）、[seizure-threshold-therapeutic-overdose-withdrawal.md](analysis/seizure-threshold-therapeutic-overdose-withdrawal.md)（惊厥阈值的三条情境线）、[cyp-inhibition-magnitude-substrate-dependence.md](analysis/cyp-inhibition-magnitude-substrate-dependence.md)（CYP 抑制倍数与底物依赖）、[sexual-dysfunction-incidence-and-persistence.md](analysis/sexual-dysfunction-incidence-and-persistence.md)（性功能障碍的发生率与持续边界）、[nms-vs-serotonin-syndrome-label-boundaries.md](analysis/nms-vs-serotonin-syndrome-label-boundaries.md)（NMS 与 5-羟色胺综合征的标签边界）。
- Wave 15：50 份（A 下尿路 13，B 前庭 7，C 解毒 10，D 帕金森及多巴胺 10，E 其他神经疾病 10）。**40 reviewed / 10 basic / 0 indexed**。已完成逐组评分修补、结构及内部链接检查，结果记于 [PLAN.md](PLAN.md)。
- Wave 16：159 份 `basic` 全部重做跨法域现行监管文本检索，**27 份升级 reviewed**、132 份保持 basic（缺口逐份写入 §10）。同时完成全库语言审订并修复 5 条被压缩的文献引用。完成记录见 [PLAN.md](PLAN.md)。
- 2026-11-11 补证：日本 PMDA 现行添付文書取回 4 份并升级 `reviewed`（brotizolam、etizolam、cloxazolam、pemoline），132 份 basic 的 CDE／NMPA／PMDA 检索记录并入 [catalog/retrieval-log-2026-11.md](catalog/retrieval-log-2026-11.md)，档案正文只保留命中事实。

## 对接时必须保留的判断边界

1. **监管批准、现行药品说明书、ATC 编码、商业供应和临床证据分开处理**。数据库零命中不可推出“从未批准”“已撤市”。`reviewed` 不是只要写了大量文献就能升级，必须满足 [AGENTS.md](AGENTS.md) 证据要求。
2. **A–D 仅针对有实际决策价值、能够被药物特异证据支持的治疗场景**。禁忌、妊娠、肝肾功能、药物相互作用、监测步骤、缺乏研究等一般记录在安全／特殊人群／证据边界，不机械单独评分。有确切已发表负面干预证据的临床使用场景可按证据评价。
3. **固定复方与单方隔离**。例：levodopa 单方吸入 INBRIJA 的正式适应证是已用 carbidopa/levodopa 者的间歇性 OFF 发作，长期口服固定复方不得当成单方临床评分依据。
4. **重大急救事实不得被评分误导**。naloxone 在妊娠期母体阿片过量时仍应及时用于救命逆转。flumazenil 可以拮抗 benzodiazepine 的抗惊厥保护，可能诱发惊厥。sodium oxybate（GHB 钠盐）在中国第一类精神药品目录范围内。
5. **证据等级例子**：betahistine 的 Ménière 病长期疗效由 2023 Cochrane 综述判为很不确定，不把 SmPC 适应证等同于高质量确证。2026 年 `PMID:42572044` flunarizine/cinnarizine 比较为回顾性队列，非 RCT。trofinetide 的 Rett 综合征获益有统计学意义，但效应幅度和腹泻负担须同时呈现。

## 尚未消除的证据缺口

- NMPA 数据查询与 CDE 受理品种目录 2026-11-11 可经浏览器逐名检索，132 份 basic 已全部检索（命中清单见 [catalog/retrieval-log-2026-11.md](catalog/retrieval-log-2026-11.md)）。检索记录与批准文本是两件事，许多药物的**中国上市状态及核准适应证仍待官方说明书核实**。中国**列管**核对与中国**批准**是两项独立工作。
- Wave 15 遗留的 10 份 `basic` 在 Wave 16 已重审：`propiverine`、`imidafenacin`、`biperiden`、`physostigmine`、`acetylleucine`、`flunarizine`、`cinnarizine-and-dimenhydrinate` 取得现行文本后升级为 `reviewed`。`emepronium`、`terodiline`、`obidoxime` 仍无任何法域现行监管正文，保持 `basic`。
- 现存的 128 份 `basic` 中，多数在任何检索法域均无现行产品文本（历史药物或地区性产品），检索范围与缺口已逐份写入各档案 §10 或检索记录。这些档案的给药方案与核准适应证仍不能按监管级引用。
- `cinnarizine-and-dimenhydrinate` 的澳大利亚 TGA 产品信息（CP-2021-PI-02009-1，修订 2025-12-23）与英国 SmPC（emc 15869，PL 25298/0366）已在 Wave 16 取得并写入，档案升级为 `reviewed`。欧洲大陆其他法域文本仍未逐国核对。
- 个别历史药品的正式撤销／停供文件、部分非英美法域产品文本、部分研究全文与中国具体产品数据仍缺，逐条以原档案 §10 的事实层级为准。

## 推荐的继续方式

先在 `main` 检查实际 HEAD 和 [catalog/index.md](catalog/index.md) 的数量。**不要重跑 Wave 1–15，也不要强制增加专题或创建空档案。** 新任务在独立分支一次派发，必要时并行处理互不重叠的药物文件，最后统一核对身份、来源、A–D 语义、链接及目录。涉及监管更新时优先官方一手文件，无法访问则保留确切缺口。新一轮的具体名单与范围留待接手方另行确定。
