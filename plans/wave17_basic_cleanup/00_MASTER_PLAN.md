# Wave 17｜Basic 档案清理与证据补全

**分支**：`wave17/basic-cleanup`  
**基线**：Wave 16 分支 `2e412478b761ed7d3b715ba52aa1e6310ec348ac`，并入最新 `main` 文档清理  
**档案总量**：384  
**基线状态**：252 `reviewed` / 125 `basic` / 7 `indexed`

## 目标与范围

本轮集中处理仍有研究价值的 38 份 `basic` 档案，尽可能补齐决定性证据，并在确实达到仓库标准时升级为 `reviewed`。

Wave 16 的研究处置基线为 10 份「继续研究」、28 份「有限补证」、87 份「仅保留历史档案」。本轮覆盖前两类共 38 份。87 份历史档案不作常规返工，仍可保持 `basic`。研究处置标签不代表档案证据已经完整。

执行开始时先按药物文件顶部字段重新核对 38 个目标的状态和研究处置。若某文件已不再是 `basic`，跳过并记录实际情况，不为维持计划数量替换药物。

## 本轮清单

### A 组：继续研究的临床研发候选（10）

- `acp-204.md`
- `ar1001.md`
- `blarcamesine.md`
- `buntanetap.md`
- `deulumateperone.md`
- `hydromethylthionine.md`
- `jnj-2056.md`
- `masitinib.md`
- `zatolmilast.md`
- `zervimesine.md`

核对当前研发阶段、试验登记状态、主要终点与结果、申办方后续决策及监管状态。优先读取试验登记原始结果、论文和申办方正式公告。临床研发仍在继续不等于产品获批，也不自动满足 `reviewed`。

### B 组：优先升级候选（10）

- `acetylcarnitine.md`
- `aniracetam.md`
- `fluspirilene.md`
- `penfluridol.md`
- `pramiracetam.md`
- `phenibut.md`
- `temgicoluril.md`
- `pinazepam.md`
- `pyritinol.md`
- `piracetam-and-cinnarizine.md`

优先核对具体产品与法域的官方注册记录、现行说明书或官方产品信息。产品层证据必须与档案中的实体、剂型和适应证一致。固定复方不得借用单方标签。

### C 组：重点证据补充（6）

- `nordazepam.md`
- `obidoxime.md`
- `fabomotizole.md`
- `dimdazenil.md`
- `huperzine-a.md`
- `oxiracetam.md`

围绕各档案 §10 已记录的缺口，定向补充原始来源、现行产品状态或完整监管文本。不得把同类药、代谢物、补充剂或不同提取物的证据移植到当前实体。

### D 组：其余有限补证条目（12）

- `bromisoval.md`
- `acetophenazine.md`
- `benzoctamine.md`
- `butaperazine.md`
- `clopenthixol.md`
- `dimetacrine.md`
- `doxefazepam.md`
- `emepronium.md`
- `meclofenoxate.md`
- `melitracen.md`
- `prolintane.md`
- `valnoctamide.md`

每份只做一轮有针对性的官方或专业来源核查。没有明确新证据时记录具体缺口并保留 `basic`，不开展无止境的跨国检索。

## 执行要求

1. 四组一次派发，允许最多四个互不嵌套的子代理并行。每组只编辑分配的药物文件。主代理负责共享文件、交叉核查与最终整合。
2. 每份档案先读现有正文与 §10，查看 [逐名检索记录](../../catalog/retrieval-log-2026-11.md) 中已经完成的检索，避免重复无效查询。
3. 优先使用监管机构现行标签、评估报告、注册库与试验登记原始结果，其次使用指南、原始研究和高质量系统综述。商业数据库与聚合站只用于发现线索，不能替代监管原文。
4. 所有批准结论必须绑定法域、具体产品、剂型与文本版本。区分批准、现行供应、历史撤销和临床试验状态。数据库零命中不能证明从未获批或已经撤市。
5. 已撤市产品的官方历史标签正文可以支撑 `reviewed`，但必须标注「历史标签」、文本版本日期与产品当前状态。只有批准或撤销记录而没有说明书正文，不足以替代标签证据。
6. `reviewed` 仍须满足 [AGENTS.md](../../AGENTS.md) 的完整证据要求，包括基本信息、适应范围、管制状态、关键临床证据、主要风险、重要相互作用与证据边界。不得因篇幅增加、研究阶段推进或计划目标而强行升级。
7. 不重审现有 252 份 `reviewed`，不处理 7 份 `indexed`，不常规返工 87 份「仅保留历史档案」。只有发现会改变具体安全、管制或实体判断的新证据时，才报告并申请扩大范围。
8. 不新增药物档案，不设专题配额。只有出现无法在主条目内清楚解释且有独立决策价值的重大证据冲突时，才考虑专题文件。
9. 不新增数据库、爬虫、CI、自动评分器、批量脚本或额外审批阶段。单份来源受阻时记录缺口并继续其他档案。
10. 完成后按实际文件状态重算全库 `reviewed/basic/indexed`，更新本文件的完成记录与 `catalog/index.md`。检查本轮改动文件的引用、内部链接、表格、状态行与证据边界。
11. 提交并推送本分支，等待人工审阅，不合并 `main`。

## 完成记录

待本轮执行结束后填写实际完成数量、升级名单、仍为 `basic` 的名单及其主要证据缺口。不得预设升级数量。
