# Wave 17｜Basic 档案清理与证据补全

**分支**：`wave17/basic-cleanup`  
**基线**：Wave 16 成果与最新 `main` 文档清理  
**档案总量**：384  
**基线状态**：252 `reviewed` / 125 `basic` / 7 `indexed`

## 目标

处理仍有研究价值的 38 份 `basic` 档案，尽可能补齐决定性证据，达到标准时再升级 `reviewed`。

Wave 16 的研究处置基线在 2026-11-24 执行开始时按档案字段复算为 10 份「继续研究」、50 份「有限补证」、65 份「仅保留历史档案」。原计划所记 28／87 已过期。本轮只处理下面前两类中列明的 38 份，65 份历史档案不作常规返工。

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
5. 不设升级配额。65 份「仅保留历史档案」不返工，不重审现有 252 份 `reviewed` 或 7 份 `indexed`。不新增药物、专题、数据库、爬虫、CI 或自动评分器。
6. 完成后按文件顶部状态字段重算全库数量，更新本计划完成记录与 `catalog/index.md`。只检查本轮改动文件的来源、状态、表格与内部链接。
7. 提交并推送本分支，等待人工审阅，不合并 `main`。

## 完成记录（2026-11-24）

**实际处理**：38 份目标全部完成定向核查并改写，无跳过项。四组并行工作中 A、B、C 组代理在收尾阶段达到轮次上限，B 组尚未落盘的四份由接替代理补完，全部改动由主代理统一复核。没有新增药物、专题、数据库、CI、爬虫或自动评分器。

**实际升级 5 份 `basic` → `reviewed`**：

- `fluspirilene`：荷兰 CBG Imap 2 mg/ml SmPC，RVG 06151，文本末次局部修订 2019-01-08，官方信息库更新 2026-11-18。
- `penfluridol`：荷兰 CBG Acemap 20 mg SmPC 共同版本 006，RVG 129179，首次授权 2023-09-26。
- `phenibut`：拉脱维亚 ZVA Noofen 100 mg 口服粉（17-0230）与共用 SmPC 的 250 mg 片（98-0294），SmPC 日期 2024-10-15，官方产品页当前列示 Rx。
- `temgicoluril`：拉脱维亚 ZVA Adaptol 300 mg 胶囊（03-0001）与 500 mg 片（03-0002），SmPC 日期 2026-08-18，官方产品页当前列示 Rx。
- `obidoxime`：德国 Toxogonin 完整 Package leaflet／SmPC，德国授权号 6102841.00.00，文本修订 2025-12，同时列荷兰 RVG 04562 与瑞士注册号 31514。

**仍为 `basic` 的 33 份**：

- A 组 10 份：`acp-204`、`ar1001`、`blarcamesine`、`buntanetap`、`deulumateperone`、`hydromethylthionine`、`jnj-2056`、`masitinib`、`zatolmilast`、`zervimesine`。
- B 组 6 份：`acetylcarnitine`、`aniracetam`、`pinazepam`、`pramiracetam`、`pyritinol`、`piracetam-and-cinnarizine`。
- C 组 5 份：`nordazepam`、`fabomotizole`、`dimdazenil`、`huperzine-a`、`oxiracetam`。
- D 组 12 份：`bromisoval`、`acetophenazine`、`benzoctamine`、`butaperazine`、`clopenthixol`、`dimetacrine`、`doxefazepam`、`emepronium`、`meclofenoxate`、`melitracen`、`prolintane`、`valnoctamide`。

**主要证据缺口**：

1. A 组均为研发候选，没有任何可引用的人用产品批准或说明书。ClinicalTrials.gov 已补读当前状态与 `resultsSection`，但多项研究仍无张贴结果，或只有申办方公告、会议摘要、媒体报道与POST_HOC 亚组。`ar1001` 的媒体定量读数未采用，只保留复星医药公告的两人群统计结论。
2. B、C、D 组的主要缺口是具体产品的现行或历史官方正文：AIFA 入口 TLS／连接失败，俄罗斯 GRLS 验证码阻断，PMDA 旧文件接口 500，NMPA／CDE 部分入口仍返回 412／202，丹麦 mdat 连接失败。注册记录、价格表、商业转载和单方标签均未替代具体复方或单方说明书。
3. 中国具体产品的现行说明书仍普遍缺失。NMPA 目录登记、CDE 受理记录与医保申报材料只证明相应层级事实，不等于核准适应证、给药方案或当前供应。`pyritinol` 已补入 NMPA 2018 年第 99 号注射剂撤销报道与国药管安〔2000〕513 号再评价通知，但口服产品现行说明书仍缺。
4. 部分历史药物只取得二手生命周期线索，未写“已撤市”或“全球停用”。`acetophenazine` 因 Drugs@FDA 的 TINDAL Discontinued 记录改为`历史停用`，但官方历史标签与停售日期仍缺。

**全库实际统计**：384 份档案，**257 `reviewed` / 120 `basic` / 7 `indexed`**。核心六组 178 reviewed／98 basic／4 indexed；跨组主题 79 reviewed／22 basic／3 indexed。执行前基线为 252 reviewed／125 basic／7 indexed。

**验收**：38 份改动文件的结构、状态行、临床现状、研究处置、A–D 表列数、内部链接与文风红旗已检查。369 个 PMID、2 个 DailyMed setid、64 个 NCT 均存在。URL 审计中的 404／412／202／000 主要为档案已注明的零命中检索端点、官方入口访问限制或提取标点伪报；新增关键官方 PDF 与产品页已单独回读。分支 `wave17/basic-cleanup` 已提交，初次验收不合并 `main`。

## 审阅修补（2026-11-24）

- ACP-204：补入 2026-11-17 CTAD 会议原始演示、实际样本与补充结果。主要终点未达。
- Zatolmilast：补入盐野义 2026-05-12 与 2026-11-18 正式披露，纠正成人及青少年 FXS 主要终点口径并补入 Jordan 综合征结果。
- Bromisoval：补入 Hoei 2024-07 历史标签、持证方 IF 及 PMDA 2025-04-01 过渡期届满记录。直接标签 PDF 已不可用，其他医疗用单方现状待核，维持 basic。历史适应证按场景区分，不作为当前处方依据。
- 三份均维持 basic。原统计 257 reviewed／120 basic／7 indexed 不变。同步修正跨组目录 Obidoxime 状态与专题索引过期链接。
