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
  在没有任何法域现行说明书可引的情况下，“给药方案”与“核准适应证”两项核心模块无法填写，
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
   药物使用异常率 2.0%）；`viloxazine` 的 FAERS 信号（546 份首要可疑报告、自杀观念 EBGM 29.51）
   按自发报告系统对待，不换算发生率；`pimavanserin` 的真实世界综述为厂方作者撰写，只用于说明
   此类数据存在。未以社交媒体提及量推算任何发生率。

### 仍开放、需在下一轮处理前知晓的事项

- **中国上市与核准适应证 24 份全部未取得**（NMPA 拦截、CDE 脚本校验页）；管制字段沿用 2026-10-06
  审计，未重做全量核查。`pimavanserin` 因芬太尼类整类结构范围边界未决，管制字段仍为“待核实”。
- **`temazepam` 的两个一手来源不一致**：30 份现行美国标签一律写 Schedule IV，`DEA-α` 列为 II 类
  （代码 2925）。条目并列照录，未裁决。
- **`zaleplon` 的 20 mg 上限**依据是试验集合中“多数受试者为 20 mg”，不是上市后安全阈值。
- **`phenelzine` 与 `moclobemide` 的多文本冲突**：苯乙肼两份美国现行标签的起病时程与术前洗脱条款措辞
  不同、且美国标签无任何手术条款；吗氯贝胺同一分子的两份英国 SmPC 适应证集合与驾驶条款互异，
  该药在美法两国均无监管记录。
- **`viloxazine` 与 `tianeptine` 的文本层单一性**：前者只有 Qelbree 一份 SPL 且 `openfda` 索引块为空、
  全文无“药物滥用与依赖”章节；后者监管文本只有法国。两份条目的结论范围都受此限制。
- 本轮**未建立试点、独立阶段、数据库、爬虫、自动评分器或 CI**，**未启用子代理**，**未扩写计划外药物**，
  **未重审既有 45 份档案**，**未合并 `main`**。
