# Wave 17｜Basic 档案清理与证据补全

**分支**：`wave17/basic-cleanup`  
**基线**：Wave 16 成果与最新 `main` 文档清理  
**档案总量**：384  
**基线状态**：252 `reviewed` / 125 `basic` / 7 `indexed`

## 目标

处理仍有研究价值的 38 份 `basic` 档案，尽可能补齐决定性证据，达到标准时再升级 `reviewed`。

Wave 16 的研究处置基线为 10 份「继续研究」、28 份「有限补证」、87 份「仅保留历史档案」。本轮处理前两类。87 份历史档案不作常规返工，仍可保持 `basic`。

执行开始时按文件顶部字段重新核对目标状态。已不再是 `basic` 的文件跳过并记录，不为维持数量替换条目。

## 本轮清单

### A 组：继续研究的临床研发候选（10）

`acp-204`、`ar1001`、`blarcamesine`、`buntanetap`、`deulumateperone`、`hydromethylthionine`、`jnj-2056`、`masitinib`、`zatolmilast`、`zervimesine`。

核对当前研发阶段、试验登记、主要终点与结果、申办方决策及监管状态。研发进展不等于产品获批，也不自动满足 `reviewed`。

### B 组：优先升级候选（10）

`acetylcarnitine`、`aniracetam`、`fluspirilene`、`penfluridol`、`pramiracetam`、`phenibut`、`temgicoluril`、`pinazepam`、`pyritinol`、`piracetam-and-cinnarizine`。

优先核对具体产品与法域的官方注册记录、现行说明书或官方产品信息。固定复方不得借用单方标签。

### C 组：重点证据补充（6）

`nordazepam`、`obidoxime`、`fabomotizole`、`dimdazenil`、`huperzine-a`、`oxiracetam`。

围绕档案 §10 的具体缺口，补充原始来源、现行产品状态或完整监管文本。

### D 组：其余有限补证条目（12）

`bromisoval`、`acetophenazine`、`benzoctamine`、`butaperazine`、`clopenthixol`、`dimetacrine`、`doxefazepam`、`emepronium`、`meclofenoxate`、`melitracen`、`prolintane`、`valnoctamide`。

每份只做一轮针对性核查。没有明确新证据时记录缺口并保留 `basic`。

## 执行与验收

1. 四组一次派发，最多四个互不嵌套的子代理并行。各组只编辑分配的药物文件，主代理处理共享文件与整合。
2. 先读每份档案及 §10，再查看 [逐名检索记录](../../catalog/retrieval-log-2026-11.md)，避免重复无效检索。
3. 优先使用监管机构标签、评估报告、注册库、试验登记原始结果、论文与申办方正式公告。批准结论必须对应法域、产品、剂型和文本版本。数据库零命中不能证明从未获批或已经撤市。
4. `reviewed` 必须满足 [AGENTS.md](../../AGENTS.md) 的完整证据要求。官方历史标签正文可以使用，但须标明「历史标签」、版本日期和产品当前状态。没有标签正文的批准或撤销记录不能单独支撑升级。
5. 不设升级配额。87 份「仅保留历史档案」不返工，不重审现有 252 份 `reviewed` 或 7 份 `indexed`。不新增药物、专题、数据库、爬虫、CI 或自动评分器。
6. 完成后按文件顶部状态字段重算全库数量，更新本计划完成记录与 `catalog/index.md`。只检查本轮改动文件的来源、状态、表格与内部链接。
7. 提交并推送本分支，等待人工审阅，不合并 `main`。

## 完成记录

待执行结束后填写实际升级数量、升级名单、仍为 `basic` 的名单及主要证据缺口。不得预设升级数量。
