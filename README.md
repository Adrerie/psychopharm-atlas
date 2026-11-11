# Psychopharm Atlas

**精神药理图谱 | An evidence-traceable psychopharmacology knowledge base**

Psychopharm Atlas 是一个以精神药理学为核心的开放阅读型知识仓库。主药物条目用于快速回答“它是什么、适应范围是什么、主要长期风险是什么、在什么场景下证据与负担是否相称”。详细 PK/PD、PET、受体占有率或原始试验数据只在确有分析价值时进入独立专题文件或直接链接原始来源。

项目以 WHO ATC/DDD 为基础分类索引，同时保留中国管制状态、法域批准差异、长期风险与按使用场景的证据评分。评分采用多维负担 + 场景适宜度，不生成单一总分，也不构成个体化用药建议。

## 项目文档

- [catalog/index.md](catalog/index.md)：分类目录索引与覆盖进度。
- [catalog/analyses.md](catalog/analyses.md)：25 份问题导向专题的索引与维护规则。
- [catalog/retrieval-log-2026-11.md](catalog/retrieval-log-2026-11.md)：2026-11-11 逐名监管检索记录（CDE 受理、NMPA 数据查询、PMDA、其他法域）。
- [PLAN.md](PLAN.md)：Wave 1–16 的计划、完成与审阅修补记录，以及 2026-11-11 的补证与整理记录。
- [HANDOFF.md](HANDOFF.md)：当前接手状态、尚未解决的来源缺口和继续维护原则。
- [WAVE2-CLOSEOUT.md](WAVE2-CLOSEOUT.md)：已完成的 Wave 2 修补记录。
- [SCORING.md](SCORING.md)：药物负担和按使用场景适宜度的统一评分规则。
- [SOURCES.md](SOURCES.md)：官方数据库、监管资料及文献来源。
- [METHODOLOGY.md](METHODOLOGY.md)：证据核查与分析方法。
- [DISCLAIMER.md](DISCLAIMER.md)：医学用途、准确性、独立性及版权声明。
- [药物条目模板](templates/DRUG_TEMPLATE.md)：精简主条目的标准结构。

## 核心原则

1. **主条目写结论，不重做 Wiki。** 仓库采用“主条目 → 专题分析 → 原始来源”的三层结构：主条目负责快速判断，专题分析解释关键证据链与冲突，完整方法和数据回原始来源。
2. **按场景评分。** 同一药物在不同适应证中的证据与风险收益可完全不同，禁止用一个总分代替。
3. **长期风险优先。** 对精神药物，长期代谢、运动、内分泌、认知、停药及误用问题优先于无决策价值的实验细节。
4. **结论可追溯。** 实质性主张尽量对应监管文件、指南或研究，并保留法域、剂型与证据边界。
5. **机制不等于疗效。** 体外受体亲和力、动物结果和人体临床结局分开呈现。

> 本仓库仅供学习、研究及文献整理，不提供个人诊断、处方或用药指导。阅读前请参阅 [免责声明](DISCLAIMER.md)。

**当前状态（2026-11-11）**：384 份药物档案（核心六组 280、跨组主题 104），状态 **249 reviewed / 128 basic / 7 indexed**。25 份问题导向专题。2026-11-11 对原 132 份 basic 档案完成 CDE 受理品种目录、NMPA 数据查询与日本 PMDA 添付文書的逐名检索，结果与零命中记录并入 [逐名检索记录](catalog/retrieval-log-2026-11.md)。其中 4 份取得日本现行添付文書全文并升级 `reviewed`（溴替唑仑、依替唑仑、氯噁唑仑、匹莫林）。未取得现行文本的 128 份仍标 `basic`，给药方案与核准适应证不按监管级引用。语言审订后的硬指标：破折号 9、正文分号 3、一句多冒号 3、表格单元格 >1 分号 0 处，0 断链、0 BOM／NUL／控制字符。

**阶段记录（截至 2026-11-11）**：Wave 15 在独立分支 `plan/neuropsych-crossgroup-wave15` 完成 50 个跨组候选，按证据定为 40 `reviewed` / 10 `basic`。Wave 16 在 `wave16/basic-upgrade` 对 159 份 `basic` 重做跨法域现行文本检索，27 份升级 `reviewed`，其余保留 `basic` 并完成全库语言审订。2026-11-11 取回 4 份日本现行添付文書升级 `reviewed`，并把原 132 份 basic 的逐名检索记录并入 [catalog/retrieval-log-2026-11.md](catalog/retrieval-log-2026-11.md)。历史批次明细见 [PLAN.md](PLAN.md)，当前数量以 [catalog/index.md](catalog/index.md) 与各档案状态字段为准。

