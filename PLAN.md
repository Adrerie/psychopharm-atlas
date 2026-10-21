# Wave 3 批量建档计划

> 分支：`feat/reviewed-expansion-wave3`。一次派发完成本计划列出的 24 份药物档案。主条目是主要交付物，药物利用与滥用证据直接纳入相关档案，不另设独立试点或分阶段门槛。

## 本轮药物（24 份）

- **三环类抗抑郁药**：`clomipramine`、`imipramine`、`nortriptyline`、`doxepin`
- **第一代抗精神病药**：`chlorpromazine`、`fluphenazine`、`perphenazine`、`zuclopenthixol`
- **苯二氮䓬类与镇静药**：`clobazam`、`midazolam`、`temazepam`、`flunitrazepam`
- **失眠治疗药物**：`daridorexant`、`ramelteon`、`zaleplon`、`tasimelteon`
- **MAOI 与其他抗抑郁药**：`moclobemide`、`phenelzine`、`tranylcypromine`、`tianeptine`
- **其他有代表性的临床药物**：`dexmethylphenidate`、`viloxazine`、`pimavanserin`、`zuranolone`

## 执行要求

1. 一次任务处理以上全部 24 份，不等待逐组确认。逐药核对身份、法域与剂型、主要适应证和疗效、长期与短期风险、停药／依赖／误用、重要相互作用、特殊人群及证据边界。
2. **主档案优先**：保持快速判断页的篇幅和信息密度。只有符合 `AGENTS.md` 中现有条件、且确有独立解释价值时才新增专题，不为本轮设专题配额。
3. 对滥用或处方适当性有实际意义的药物，查找可用的处方／调剂、药物利用、全国调查、毒物中心、急诊、药物警戒或高质量研究。社交媒体只用于发现使用动机和假设，不以发帖量估计发生率。
4. 使用量、生产配额、分销量、处方张数、患者人数和非医疗使用报告不是同一指标。记录地区、年份、研究人群和分母；没有可比的分母时不计算发生率。总量大不自动等于滥用或过度处方，off-label 也不自动等于不合理使用。
5. 相关数据若找不到或口径不可靠，简洁记录证据缺口并继续其他条目。不得为填评分而推断；沿用现有评分，不新增维度或自动公式。
6. 中国上市／核准适应证只有在可靠官方来源可核实时才更新。已有管制字段按药物特异的官方证据核对；不借此重做全部 280 份管制审计。
7. 完成后更新 `catalog/index.md` 的实际数量和状态。只有达到 `reviewed` 定义的条目才升级，其余保留 `indexed/basic` 并注明缺口。检查实际修改文件的引用、表格与链接，提交并推送本分支，报告结果。

## 不做

不建立独立研究阶段、试点阶段或多重审批门槛；不批量爬取社交媒体，不建数据库、评分器或 CI，不启用子代理，不全量重审既有 45 份档案，不扩写计划外药物，不为每种药新增专题。完成后等待人工审阅，不自行合并 `main`。


## 完成结果（2026-10-21）

PLAN 列出的 24 份全部处理完毕，逐批独立提交并推送到 `feat/reviewed-expansion-wave3`。

- **达到 `reviewed` 的 23 份**：
  - Batch A 三环类：`clomipramine`、`imipramine`、`nortriptyline`、`doxepin`
  - Batch B 第一代抗精神病药：`chlorpromazine`、`fluphenazine`、`perphenazine`、`zuclopenthixol`
  - Batch C 苯二氮䓬类：`clobazam`、`midazolam`、`temazepam`
  - Batch D 失眠治疗药物：`daridorexant`、`ramelteon`、`zaleplon`、`tasimelteon`
  - Batch E MAOI 与其他抗抑郁药：`moclobemide`、`phenelzine`、`tranylcypromine`、`tianeptine`
  - Batch F 其他代表性药物：`dexmethylphenidate`、`viloxazine`、`pimavanserin`、`zuranolone`
- **保持 `basic` 的 1 份**：`flunitrazepam`——美国无处方资料、英国 emc 与法国 BDPM 均 0 条，
  本轮检索的五个法域均未找到可引用的现行说明书文本，“给药方案”与“核准适应证”两项核心模块无法填写，
  因此不升级为 `reviewed`，条目内以文首状态说明与 §10 记录该取证缺口。
- **未新增专题文件**：本批所有分歧（法域文本互异、评分口径冲突、单一法域证据）均可在主条目
  §2.2 与 §10 就近并列，未出现需要跨文件承载的独立研究问题；按 PLAN 第 2 条不设专题配额。

### 评分口径的三项落实

1. **滥用／误用潜力**：9 份记 `N/A`（`clomipramine`、`imipramine`、`nortriptyline`、`fluphenazine`、
   `zuclopenthixol`、`moclobemide`、`phenelzine`、`viloxazine`、`pimavanserin`），理由是这三类情形
   ——未受管制、标签无相关章节、无觅药报告——按 SCORING.md **不能单独证明 1 分**。5 份的 1 分
   （`doxepin`、`chlorpromazine`、`perphenazine`、`ramelteon`、`tasimelteon`）全部落在标签对本药的
   **主动阴性定性**或**人体实验室阴性试验**上。
2. **中国 PIM 维度**：24 份一律 `N/A`。两套老年标准给出的只是条款与风险等级，不含逐药的当地处方
   偏离数据；被逐名点名（如 `zaleplon` 被 2017 年中国标准表 2 第 22 项收录）、只有类别条款
   （`temazepam`、`clobazam`、`midazolam`）或完全未收录（MAOI 整类、ADHD 用药整类）三种状态均已
   逐项写入依据行，但不据此评分。`pimavanserin` 在 Beers 中被点名两次：一次随抗精神病药类别清单，
   一次作为帕金森病行的**例外**，两者都不构成不适当处方证据。
3. **药物利用与误用证据的口径**：`tianeptine` 的美国数据来自毒物暴露通报（分母不是处方人群，且该药
   未获美国批准）、法国数据来自全国调配序列（4.5 M 人群、410,525 名患者、处方频率排名第 6、
   医生购物指数（DSI）2.0%，不是患者比例或总体滥用率）；`viloxazine` 的 FAERS 信号（546 份首要可疑报告、自杀观念 EBGM 29.51）
   按自发报告系统对待，不换算发生率；`pimavanserin` 的真实世界综述为厂方作者撰写，只用于说明
   此类数据存在。未以社交媒体提及量推算任何发生率。

### 仍开放、需在下一轮处理前知晓的事项

- **中国上市与核准适应证 24 份全部未取得**（NMPA 拦截、CDE 脚本校验页）；管制字段沿用 2026-10-06
  审计，未重做全量核查。`pimavanserin` 因芬太尼类整类结构范围边界未决，管制字段仍为“待核实”。
- **`temazepam` 的美国管制分级已修正**：美国现行标签与 DEA 字母序清单均列 Schedule IV（代码 2925）；原“II 级冲突”是清单读取错误，已在条目中更正。
- **`zaleplon` 的 20 mg 上限**依据是试验集合中“多数受试者为 20 mg”，不是上市后安全阈值。
- **`phenelzine` 与 `moclobemide` 的多文本差异**：苯乙肼两份美国现行标签的起病时程与术前洗脱条款措辞不同，且美国标签无手术条款；吗氯贝胺两份英国 SmPC 的适应证集合与驾驶条款互异。原“法国 BDPM 无吗氯贝胺记录”已被官方数据库的 MOCLAMINE 150 mg 记录推翻，须补入法国 RCP 后再更新结论。
- **`viloxazine` 与 `tianeptine` 的文本层单一性**：前者只有 Qelbree 一份 SPL 且 `openfda` 索引块为空、
  全文无“药物滥用与依赖”章节；后者监管文本只有法国。两份条目的结论范围都受此限制。
- 本轮**未建立试点、独立阶段、数据库、爬虫、自动评分器或 CI**，**未启用子代理**，**未扩写计划外药物**，
  **未重审既有 45 份档案**，**未合并 `main`**。

## 审阅后修补计划（2026-10-21）

只处理本次审阅指出的问题，不重开 Wave 3 研究。

1. 按更新后的 `AGENTS.md` 与 `SCORING.md` 清理本批 24 份档案的 A–D 表。只保留主要获批适应证、有证据的常见超适应证用途及有实际决策价值的临床场景。特殊人群、相互作用、禁忌证、服药时点、吸烟影响、尿液筛查与非医疗使用等不单独评分，必要信息移至现有章节；固定复方不得进入单方表，`待核实` 不得作为等级。保留证据，不重写整份条目。
2. 补入并核对法国官方 RCP。吗氯贝胺使用 [MOCLAMINE 150 mg RCP（CIS 62439997，文本更新于 2024-08-05）](https://m.base-donnees-publique.medicaments.gouv.fr/rcp-62439997-1)；多塞平使用 [QUITAXON 10 mg RCP](https://m.base-donnees-publique.medicaments.gouv.fr/rcp-63046819-4) 与 [QUITAXON 50 mg RCP](https://m.base-donnees-publique.medicaments.gouv.fr/rcp-63940790-7)。更新对应条目的法国法域状态、适应证和确有来源支持的剂量／限制，加入来源链接；不得把法国抗抑郁制剂的适应证外推到美国低剂量失眠制剂，也不得把一个法域的文本外推到其他法域。
3. 只检查本次改动的条目、`AGENTS.md` 与本计划，确认来源链接可用、无残留的替马西泮分级冲突、无吗氯贝胺“法国无记录”的旧结论、无无效 A–D 占位行。保留现有档案状态与目录计数，除非证据确实要求调整；氟硝西泮仍为 `basic`。提交并推送当前分支，不合并 `main`。

不做全库复审，不新增脚本、子代理、验证框架或 CI，不建立新计划文件。
