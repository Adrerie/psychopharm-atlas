# 精神药物建档计划与执行记录

> 当前任务：**Wave 10 一次性建档，35 份尚未深入处理的 `indexed` 药物**。工作分支 `plan/reviewed-expansion-wave10`，基于 Wave 9 经审阅修补、通过 [PR #12](https://github.com/Adrerie/psychopharm-atlas/pull/12) 合并的 `main`。**以本文件末尾的 Wave 10 计划为唯一任务清单**，Wave 1–9 均是历史完成记录，不重复派发。

> Wave 3 历史分支：`feat/reviewed-expansion-wave3`。该轮 24 份档案及后续审阅修补均已完成；主条目为主要交付物，药物利用与滥用证据按需纳入，不设置专题配额。

## Wave 3 历史药物清单（24 份）

- **三环类抗抑郁药**：`clomipramine`、`imipramine`、`nortriptyline`、`doxepin`
- **第一代抗精神病药**：`chlorpromazine`、`fluphenazine`、`perphenazine`、`zuclopenthixol`
- **苯二氮䓬类与镇静药**：`clobazam`、`midazolam`、`temazepam`、`flunitrazepam`
- **失眠治疗药物**：`daridorexant`、`ramelteon`、`zaleplon`、`tasimelteon`
- **MAOI 与其他抗抑郁药**：`moclobemide`、`phenelzine`、`tranylcypromine`、`tianeptine`
- **其他有代表性的临床药物**：`dexmethylphenidate`、`viloxazine`、`pimavanserin`、`zuranolone`

## Wave 3 历史执行要求

1. 一次任务处理以上全部 24 份，不等待逐组确认。逐药核对身份、法域与剂型、主要适应证和疗效、长期与短期风险、停药／依赖／误用、重要相互作用、特殊人群及证据边界。
2. **主档案优先**：保持快速判断页的篇幅和信息密度。只有符合 `AGENTS.md` 中现有条件、且确有独立解释价值时才新增专题，不为本轮设专题配额。
3. 对滥用或处方适当性有实际意义的药物，查找可用的处方／调剂、药物利用、全国调查、毒物中心、急诊、药物警戒或高质量研究。社交媒体只用于发现使用动机和假设，不以发帖量估计发生率。
4. 使用量、生产配额、分销量、处方张数、患者人数和非医疗使用报告不是同一指标。记录地区、年份、研究人群和分母；没有可比的分母时不计算发生率。总量大不自动等于滥用或过度处方，off-label 也不自动等于不合理使用。
5. 相关数据若找不到或口径不可靠，简洁记录证据缺口并继续其他条目。不得为填评分而推断；沿用现有评分，不新增维度或自动公式。
6. 中国上市／核准适应证只有在可靠官方来源可核实时才更新。已有管制字段按药物特异的官方证据核对；不借此重做全部 280 份管制审计。
7. 完成后更新 `catalog/index.md` 的实际数量和状态。只有达到 `reviewed` 定义的条目才升级，其余保留 `indexed/basic` 并注明缺口。检查实际修改文件的引用、表格与链接，提交并推送本分支，报告结果。

## Wave 3 历史范围限制

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
- **`zaleplon` 的 20 mg 上限**依据是试验集合中“多数受试者为 20 mg”，不是上市后安全阈值。
- **`phenelzine` 与 `moclobemide` 的多文本差异**：苯乙肼两份美国现行标签的起病时程与术前洗脱条款措辞不同，且美国标签无手术条款；吗氯贝胺两份英国 SmPC 的适应证集合与驾驶条款互异。法国 MOCLAMINE RCP 已补入，适应证仅为重性抑郁发作、不含社交恐惧；“法国无记录”已不是待办事项。
- **`viloxazine` 与 `tianeptine` 的文本层单一性**：前者只有 Qelbree 一份 SPL 且 `openfda` 索引块为空、
  全文无“药物滥用与依赖”章节；后者监管文本只有法国。两份条目的结论范围都受此限制。
- 本轮**未建立试点、独立阶段、数据库、爬虫、自动评分器或 CI**，**未启用子代理**，**未扩写计划外药物**，
  **未重审既有 45 份档案**，**未合并 `main`**。

## 审阅后修补计划（2026-10-21）

只处理本次审阅指出的问题，不重开 Wave 3 研究。

1. 按更新后的 `AGENTS.md` 与 `SCORING.md` 清理本批 24 份档案的 A–D 表。只保留主要获批适应证、有证据的常见超适应证用途及有实际决策价值的临床场景。特殊人群、相互作用、禁忌证、服药时点、吸烟影响、尿液筛查与非医疗使用等不单独评分，必要信息移至现有章节；固定复方不得进入单方表，`待核实` 不得作为等级。保留证据，不重写整份条目。
2. 补入并核对法国官方 RCP。吗氯贝胺使用 [MOCLAMINE 150 mg RCP（CIS 62439997，文本更新于 2024-08-05）](https://base-donnees-publique.medicaments.gouv.fr/medicament/62439997/extrait)；多塞平使用 [QUITAXON 10 mg RCP](https://base-donnees-publique.medicaments.gouv.fr/medicament/63046819/extrait) 与 [QUITAXON 50 mg RCP](https://base-donnees-publique.medicaments.gouv.fr/medicament/63940790/extrait)。更新对应条目的法国法域状态、适应证和确有来源支持的剂量／限制，加入来源链接；不得把法国抗抑郁制剂的适应证外推到美国低剂量失眠制剂，也不得把一个法域的文本外推到其他法域。
3. 只检查本次改动的条目、`AGENTS.md` 与本计划，确认来源链接可用、无残留的替马西泮分级冲突、无吗氯贝胺“法国无记录”的旧结论、无无效 A–D 占位行。保留现有档案状态与目录计数，除非证据确实要求调整；氟硝西泮仍为 `basic`。提交并推送当前分支，不合并 `main`。

不做全库复审，不新增脚本、子代理、验证框架或 CI，不建立新计划文件。

## 审阅后修补结果（2026-10-21）

三项均已完成，逐批独立提交，未合并 `main`。

1. **A–D 表清理（24 份全部）**：本批场景表行数由 200 余行降到 **89 行**。撤销评分的行类是年龄、妊娠与哺乳、肝肾功能、
   呼吸共病、合用药物与禁忌、监测要求、给药时点与进食、吸烟、尿液药物筛查、物质滥用史与非医疗使用；被点名的
   `tianeptine` **妊娠与哺乳行把"待核实"当等级**，该行删除后缺口仍留在 §10。保留的内容是获批适应证、
   有证据的超适应证用途、剂型修正场景，以及会改变治疗选择的用途（如喹硫平样板中的失眠与非适应证精神病）。
   属主已做的四处直接修补（替马西泮分级、氟硝西泮取证范围、奋乃静复方行、柔速瑞尿筛行）全部保留、未被覆盖。
   搬移用两道审计回查：数值 token 存活审计与定性短语存活审计，共发现 **15 处**证据缺口并已回补到
   §4／§5／§6／§8／§9（含扎来普隆肝硬化清除数据、氯巴占妊娠结局、雷诺替明呼吸共病研究与生殖毒性数值、
   苯乙肼围术期与饮食清单、反苯环丙胺血压监测措辞、匹莫范色林动物暴露比与起效尺度、珠氯噻醇 Cochrane
   辅助用药数据）。指向已删场景行的"§2.2 第 N 行"引用改为指向章节。
2. **法国官方 RCP 补全**：吗氯贝胺取 **MOCLAMINE 150 mg**（CIS 62439997，titulaire Biocodex，授权状态 Valide，
   国家程序，Liste I，首次授权 1990-09-12，30 片规格商业化申报 1994-07-19，ANSM 文本更新 2024-08-05），
   §4.1 只有重性抑郁发作、**不含社交恐惧**；多塞平取 **QUITAXON 10 mg**（CIS 63046819，文本更新 2019-04-11）与
   **QUITAXON 50 mg**（CIS 63940790，文本更新 2020-12-22），titulaire Provepharm，两份 §4.1 同样只有重性抑郁发作，
   **法国无低剂量失眠规格**。上一轮"法国 BDPM 0 条"的成因已查明：字母序接口 `startBy=` 按**商品名前缀**匹配，
   所以 `MOCLOBEMIDE`／`DOXEPINE` 零命中不能证明无法国产品。英法文本的禁忌分层（法国 §4.3 设"相对禁忌"一档、
   未列 linezolid）、换药间隔（15 天对 14 天）、哺乳与驾驶口径均并列照录、不折中；法国抗抑郁适应证没有外推到
   美国 3／6 mg 失眠产品，反之亦然。
3. **验收**：此前三条法国链接虽返回 HTTP 200，但两条未落到目标药品正文。二次审阅已将三条统一为官方药品提取页，验收需核对药品名与规格，不能仅凭 HTTP 200 判定链接有效；此前“0 坏链”结果未识别内容错链；
   替马西泮不再存在分级冲突表述（`catalog/index.md` 的旧"两来源不一致"记法已同步为一致）；
   吗氯贝胺"法国无记录"的旧结论在条目与目录两处均已更正；场景行规则曾通过脚本逐行复核，但后续人工审阅仍发现少量语义问题，包括无独立证据的场景占位、不同适应证合并评分与过长依据，见下方二次审阅修补。
   档案状态与目录计数不变：**68 份 `reviewed` / 211 份 `indexed` / 1 份 `basic`（`flunitrazepam`）**。

仍然开放的缺口：中国 NMPA 与 CDE 入口依旧不可脚本检索，24 份的中国上市与核准适应证仍为待核实；
两份法国 RCP 的 §10"文本更新日期"字段本身写"[à compléter ultérieurement par le titulaire]"，
本批引用的日期是页面标注的 ANSM 更新日期；`doxepin` 三法域哺乳口径强度不同、`moclobemide` 英法禁忌分层不同，
均按文本并列；上一轮记下的 `zaleplon` 20 mg 上限、`viloxazine` 单一 SPL、`tianeptine` 文本层限于法国等缺口不变。


## 二次审阅后修补（2026-10-21）

### 已直接修复

- 将 MOCLAMINE 与两种 QUITAXON 规格的链接改为官方药品提取页，并修正“法国无记录须补 RCP”的过期待办。
- 更新 `AGENTS.md`，明确 A–D 表按单一、可评估的临床场景评分；不以未获批或缺少标签单独构成评分行；不机械合并不同适应证；历史用途若无当前决策价值则留在正文。
- 从 `midazolam.md` 删除“产科操作辅助与新生儿”警示性评分行。相关风险仍保留在 §9，§6 的交叉引用同步改为 §9。
- 从 `imipramine.md` 删除仅用于记录“惊恐与焦虑未获批”且缺少药物特异证据的评分行，并在 §10 保留适应证边界。
- 从 `tianeptine.md` 删除仅用于记录“社交恐惧／焦虑未获批”且缺少支持证据的评分行，并在 §10 保留法国 RCP 的适应证边界。

### 本轮修补范围（已完成）

1. `chlorpromazine.md`：将恶心与呕吐、顽固性呃逆拆为独立场景；删除缺乏药物特异证据支持的老年低剂量镇静／助眠评分，并在 §10 保留风险与证据边界；补充精神病性用途的风险收益依据，压缩儿科评分行并将剂量细节移至 §4。
2. `flunitrazepam.md`：继续不提供 A–D 评分；将 §10 的表述从“无现行监管文本”改为“未取得可核对的现行产品说明书／监管标签”，保留列管状态与上市状态的区别。
3. `imipramine.md`：分别标注 Cochrane 各终点的样本量，区分 4 项试验、347 名儿童的每周尿床夜数结果与 12 项试验、831 名儿童的连续 14 晚干燥结果；补充高异质性及报警器比较的样本量。
4. `perphenazine.md`：在 CATIE 结果中明确奋乃静比较的 Hochberg 校正阈值 p≤0.017，以及齐拉西酮比较的阈值 p≤0.013，避免按未校正的 0.05 阈值解释。
5. `PLAN.md`：修正评分表章节引用，记录本轮实际修补与最终验收。仅核对相关条目、`AGENTS.md`、`PLAN.md` 和受影响的交叉引用，不做全库复审，不新增脚本、CI、子代理或验证框架；完成最终核对后按用户最新指示合并 `main`。

### 本轮完成记录（2026-10-21）

- `chlorpromazine.md`：删除“术前不安与焦虑的缓解；急性间歇性卟啉症；破伤风辅助”合并评分行，这三项美国标签适应证只作为监管事实留在 §1 与 §4，不参与评分的理由与“促进低体温”的双重解释写入 §10 第 1 项；没有机械拆成三行。止吐与顽固性呃逆拆为两个场景，Beers 的短期止吐例外不外推至止呃；儿童 Reye 综合征相关警告仍置于 §7。§4 改为按三组用途并列美国 9 项适应证，并把两国剂量区间与标签自设上限集中于此；§1 的“英国仅 1 项”与 §4 的“两组用途”口径矛盾一并消除。
- `flunitrazepam.md`：§2.2 不再给 A–D 等级，改为写明“五法域均未取得可核对的现行产品说明书／监管标签，因此无法核对场景的获批状态、剂量—效应关系与禁忌分母”；术前用药、短期催眠与酒精戒断谵妄静脉给药三项研究的设计与数值（`PMID:2895705`、`PMID:8500918`、`PMID:8214408`）整体保留在 §5 新增的历史证据条目中，§10 第 6 项改为“历史用途不等于现行核准，且不为其评分”。未添加占位行。
- 过长单元格压缩：`doxepin.md` 睡眠维持行 481→225 字符、抗抑郁行 271→130（获批试验构成与逐组数值移入 §5，三法域抗抑郁剂量体系移入 §4）；`imipramine.md` 遗尿行 394→167（Cochrane 完整数值移入 §5，逐年龄滴定、“>75 mg 不增效”与两倍该剂量的 ECG 改变移入 §5 与 §9，成人抑郁剂量梯度移入 §4）；`perphenazine.md` 精神分裂症行 385→212（CATIE 逐组停药率与 p 值移入 §5，标签给药方案移入 §4）。压缩只做位置迁移，数值与限定短语逐条比对确认未丢失；顺带修正 `imipramine.md` §5 中“约五分之二达到连续 14 晚干燥”与该试验自身数字（78% 未达到）不符的表述，按原文口径写明 22% 对 5%。
- 未改动项：`lemborexant.md`（322／289／270 字符）、`agomelatine.md`（313）、`modafinil.md`（293／287）等 260–322 字符的单元格经逐一阅读后保留原文。它们的长度来自决定该分数的对比性事实（主观与客观终点不可合并、差异化主张只存在于标签之外、与同类药方向相反等），不属于“完整剂量方案或试验细节”，压缩会丢失决策依据。
- 核对范围与结果：只核对上述 5 份实际修改文件。结构完整性、§2.2 评分单元格长度、条目总长区间、全库状态计数（68 reviewed／211 indexed／1 basic，共 280 份，`analysis/` 15 份）与相对链接（0 处失效）均通过；本轮未新增或改写任何 URL，官方链接与上一轮已核对的版本逐字相同，故未重跑在线取回（当前环境无网络）。`AGENTS.md` 的规则已覆盖本轮问题，无需再改。


## 三次审阅后修补与最终验收（2026-10-21）

- `imipramine.md`：§5 分别标注每周尿床夜数（4 项试验、347 名儿童）与连续 14 晚干燥（12 项试验、831 名儿童）的证据分母；将随访结局写为“仍尿床”，并注明该终点的高异质性与报警器比较的样本量。
- `perphenazine.md`：§2.2 与 §5 统一注明 CATIE 的多重比较校正阈值，避免将 p=0.021 或 p=0.028 直接按 0.05 判为显著。
- `chlorpromazine.md`：拆分止吐与顽固性呃逆；从 A–D 表移除缺乏药物特异疗效／使用证据的老年低剂量镇静／助眠场景；重写精神病性用途评分理由，压缩儿科场景依据并将具体剂量移至 §4；在 §10 保留未评分的理由与风险边界。
- `flunitrazepam.md`：将证据边界准确限定为本轮未取得现行产品说明书／监管标签，不再将其概括为没有现行监管文本。
- 验收：核对修改文件的章节引用、评分表结构、关键样本量、统计阈值与相对链接；本轮未修改药物目录计数或新增条目。通过差异复核后创建合并请求并合并至 `main`。


## Wave 4 批量建档计划（2026-10-21）

**状态：已完成（见文末"Wave 4 完成记录"）。** 分支：`plan/reviewed-expansion-wave4`。派发时基线为 68 份 `reviewed`、211 份 `indexed`、1 份 `basic`。本轮只处理以下 24 份，不扩写计划外药物，不重审全库。

### 本轮药物与子代理分工

使用最多 4 个并行子代理，每个负责 6 份互不重叠的主条目。子代理可读取既有相关条目作交叉核对，但只编辑自己分配的 `drugs/*.md` 文件。

- **代理 A：抗精神病药（6）**：`prochlorperazine`、`trifluoperazine`、`flupentixol`、`sulpiride`、`asenapine`、`lumateperone`。
- **代理 B：抗抑郁药（6）**：`desvenlafaxine`、`vilazodone`、`levomilnacipran`、`nefazodone`、`milnacipran`、`mianserin`。
- **代理 C：催眠与镇静药（6）**：`triazolam`、`flurazepam`、`nitrazepam`、`estazolam`、`melatonin`、`remimazolam`。
- **代理 D：抗焦虑、促醒与其他精神活性药物（6）**：`hydroxyzine`、`etifoxine`、`meprobamate`、`armodafinil`、`amfetamine`、`phenibut`。

### 执行要求

1. 一次派发完成上述 24 份，不设置逐组人工确认门槛。主代理先阅读本文件、`AGENTS.md`、`SOURCES.md`、`METHODOLOGY.md`、`SCORING.md`、`DISCLAIMER.md`，并参考 `drugs/quetiapine.md` 的快速判断结构。
2. 每份至少核对药物身份、法域与剂型、主要适应证、关键疗效证据、长期和短期风险、停药／依赖／误用、重要相互作用、必要特殊人群、中国管制状态及证据边界。监管事实优先使用现行官方标签与说明书，明确产品、法域、剂型、文本版本或生效日期。可用时核对美国 FDA／DailyMed、英国 emc SmPC、法国官方 RCP；不要求每个药物强行覆盖全部法域。
3. 中国管制状态使用药物特异的官方目录与原文核对。不得把 ATC 分类、结构相似、未命中或其他法域的列管状态当作中国结论；确实无法确认时保留“待核实”并说明缺口。本轮不重做全部 280 份药物的管制审计，也不把 NMPA／CDE 当前的检索障碍用商业数据库替代。
4. 严格沿用现有评分规范。A–D 只评价有证据且有实际决策价值的临床场景；不把年龄、妊娠、相互作用、禁忌或非医疗使用单独评分。未获批本身不构成评分理由；证据不足时使用 `N/A` 或“待核实”，不得为了完成批次数量强行升级 `reviewed`。
5. 对确有意义的药物利用、处方、滥用或误用问题，寻找口径明确的可靠证据，注明地区、年份、人群与分母。数据不可比或不存在时记录缺口，不凑指标、不用社交媒体提及量推算发生率。
6. 主条目保持快速判断导向，信息密度接近喹硫平样板。将完整试验设计、次要数值与复杂争议压回现有章节或原始来源链接；仅在存在明确独立问题时新增专题，不设专题配额。
7. **代理分工**：每个子代理只修改自己分配的 6 份药物文件，不编辑 `AGENTS.md`、`PLAN.md`、`catalog/index.md` 或其他代理的文件；不得嵌套派生子代理，不单独提交或合并 `main`。每个代理返回修改文件、主要来源与版本、关键结论、尚未解决的缺口。主代理负责统一评分口径、解决跨文件矛盾、更新共享文件并提交。
8. 汇总后只检查本轮 24 份文件及必要的共享文件。核对来源与相对链接、章节引用、Markdown 表格、评分行语义、关键数字是否有原始来源支持，以及状态是否符合 `reviewed/basic/indexed` 定义。使用轻量人工核对即可，不新增脚本、CI、数据库或自动评分器。
9. 仅在所有子代理结果完成整合后，更新 `catalog/index.md` 的实际状态与计数，并更新本计划的完成记录。提交并推送当前分支，报告实际完成数、仍为 `indexed/basic` 的条目和证据缺口。等待人工审阅，不合并 `main`。

### 不做

不重审既有 68 份 `reviewed` 档案，不重新执行全库管制审计，不批量爬取社交媒体，不新增统一评分维度、自动评分、CI、数据库、长期爬虫、批量空模板或独立研究阶段。子代理仅用于上述明确分工的并行工作，不改变证据标准，也不取代主代理的整合审阅。

## Wave 4 完成记录（2026-10-21）

**状态：已完成并推送当前分支；人工审阅修正已纳入分支，合并状态以 Git 历史为准。** 实际计数：**23 份 `reviewed` ＋ 1 份 `basic`（`phenibut`）**，无计划外条目；全库现为 91 份 `reviewed`、187 份 `indexed`、2 份 `basic`（共 280 份）。

**分工与执行实况**：4 个子代理各 6 份的分工按文件互不重叠执行，但 3 个代理在 150 轮上限处中止、1 个代理命中模型服务限额，剩余条目（`lumateperone`、`remimazolam` 的英国 50 mg 产品、`asenapine`／`trifluoperazine` 的收尾压缩）由主代理直接取证与写作。共享文件（`AGENTS.md`、`PLAN.md`、`catalog/index.md`）与跨文件口径统一全部由主代理完成，子代理未提交、未合并。

**主要来源**：美国 DailyMed 现行处方资料（set_id＋生效日，17 份）与 openFDA `drug/label.json`；英国 emc SmPC（产品号＋PL／PLGB＋§10 修订日，11 份）；法国 BDPM 公开药品库（CIS＋ANSM 文本日期，4 份）；WHO ATC/DDD Index 2026；Beers 2023 与中国 2017 年老年人 PIM 标准全文；中国 2025 年版麻精目录与 2026 年第 58 号增列公告；PubMed／Europe PMC 的药物特异试验与综述。取不到的法域一律写成检索事实（openFDA 404、emc 0 命中、BDPM 按商品名前缀匹配），不写成"未获批"。

**整合阶段修正**（全部由主代理执行并逐条复核）：
1. **占位与"未获批即差评"**：删除羟嗪的 `—` 占位行与失眠 `C−` 行、甲丙氨酯的"惊恐障碍长期控制 D"与"与阿片／酒精／镇静剂合用 D"两行，相关事实退回 §7／§8，并在 §10 说明为何不构成评分场景。
2. **交叉引用脆弱**：5 处"§2.2 第 N 行"式指称改为按场景名指称（三氟拉嗪、氟哌噻吨类条目与舒必利、瑞马唑仑）。
3. **监管标识错误**：去甲文拉法辛申报号 NDA021549→**NDA021992**（持有方 Wyeth Pharmaceuticals LLC，活性成分为琥珀酸一水物，删去"富马酸盐当量"表述）；米那普仑 NDA021549→**NDA022256** 并补全原品牌 setid。
4. **剂型措辞**：苯丙胺的混合盐（MAS）不再写作"复方盐"；复方词在本轮所有 2.1／2.2 段落清零。
5. **中国 PIM 口径统一**：三唑仑与硝西泮由 3 分改为 `N/A`，理由与既有口径一致——标准的逐名条款与风险等级不等于当地处方偏离数据；艾司唑仑保留 4 分，其依据是三项中国医院处方数据集（PIP 患病率、AAPC 趋势、深圳失眠队列）而非标准本身。
6. **瑞马唑仑补全**：主代理取回英国 Byfavo 50 mg（emc 15066，PLGB 59768/0002，全麻诱导与维持）与欧洲关键试验（CNS7056-022、ONO-2745-05），条目改为"同分子两产品两适应证"写法，并把两法域冲突值按原文并列（终端半衰期 37–53 分钟／7–11 分钟；哺乳建议 5 小时挤弃／24 小时停哺）。

**验收方式**：只检查本轮 24 份文件与两个共享文件；逐项核对表结构（§2.1 六维、§2.2 四列与 A–D 档位）、评分单元格长度与占位符、相对链接与 §11 的官方 URL 是否可达、信息密度（去空白字符数落在喹硫平样板的 0.6–1.45 倍带内）、状态定义是否被夸大。**DailyMed 的 `services/v2/spls/<setid>.json` 元数据接口对多份现行 setid 恒返回 HTTP 415，链接核验以 `drugInfo.cfm?setid=` 页面为准**，否则会产生假阳性失效链接。未新增脚本、CI、数据库或自动评分器（核对脚本一律放在仓库之外）。

**仍开放的证据缺口**：24 份的中国上市剂型与核准适应证全部未取得（NMPA 恒 412、CDE 恒 202 校验页），管制字段沿用 2026-10-06 审计结果、本轮未重跑全库结构核查；多份美国现行文本为旧格式（无 §14 对照试验章节、无结构化滥用／管制章节），因此普樂明、三氟拉嗪、甲丙氨酯、奈法唑酮、艾司唑仑等条目的疗效叙述停在标签与机制层面；卢美哌隆的 concentration-QTc 数值在 openFDA 文本字段中被截断，只记为缺口；`phenibut` 与 `flunitrazepam` 无任何法域现行说明书可引，保持 `basic`；欧盟其他成员国文本未逐一体检，英国结论不外推为"欧盟状态"。


## Wave 5 批量建档计划（2026-10-22）

**状态：已完成（见文末“Wave 5 完成记录”。）** 分支：`plan/reviewed-expansion-wave5`；派发时基线为已合并 Wave 4 的 `main`：**91 reviewed / 187 indexed / 2 basic**，共 280 份。Wave 5 一次处理下列 **24 份**尚为 `indexed` 的档案。下列分组只为文件归属与并行取证，不设分组验收门槛，也不预设升级数额。

### 任务清单与子代理归属

最多并行 4 个子代理，每组 6 份、路径互不重叠：

- **A｜抗精神病药及其新型复方（6）**：`iloperidone`、`pimozide`、`droperidol`、`loxapine`、`olanzapine-and-samidorphan`、`xanomeline-and-trospium`。
- **B｜抗抑郁药及其新型复方（6）**：`citalopram`、`reboxetine`、`brexanolone`、`gepirone`、`desipramine`、`bupropion-and-dextromethorphan`。
- **C｜巴比妥类、麻醉与镇静药（6）**：`pentobarbital`、`secobarbital`、`methohexital`、`thiopental`、`dexmedetomidine`、`chloral-hydrate`。
- **D｜抗焦虑、兴奋与认知相关药（6）**：`potassium-clorazepate`、`etizolam`、`metamfetamine`、`caffeine`、`dexmethylphenidate-and-serdexmethylphenidate`、`piracetam`。

### 一次性执行要求

1. 主代理读取 `AGENTS.md`、本计划、`SOURCES.md`、`METHODOLOGY.md`、`SCORING.md`、`DISCLAIMER.md` 及喹硫平样板后，一次派发全部四组。子代理**只修改**所分配的 `drugs/*.md`，不得编辑共享文件、互相覆盖、嵌套派发或合并 `main`。主代理处理整合与任何中断后未完成的条目。
2. 每份保持快速判断页：确认身份与 ATC、中国管制状态、可核实的法域与具体产品／剂型／版本、适应证、机制、关键人体疗效证据、长期及短期风险、停药／依赖／误用、重要相互作用、必要特殊人群和证据边界。优先核现行官方说明书，其次指南、系统综述与有必要的原始试验；不强制凑齐美英法三地来源。
3. **四份固定复方分别作为独立产品**，不得把其中单一成分的适应证、剂量、临床试验或负担评分直接搬来使用。注意产品与活性成分层级。对于 `brexanolone`、`gepirone`、`etizolam` 等可能存在产品可得性或监管来源限制的档案，核对版本及产品现状；检索零命中只记录检索事实，不能推断未批准、撤市或无监管文件。
4. 区分镇静麻醉的**给药途径和场所**，以及药物本体与特定剂型风险。对 `metamfetamine`、`caffeine` 等须分开临床制剂、剂量情境与非医疗使用，不以总体滥用或公众消费资料代替具体适应证证据；不提供个人给药或调药指示。
5. 仍依 `SCORING.md` 分开给出多维风险评分与有临床决策意义的 A–D 场景评分。年龄、妊娠、合用禁忌、单纯未获批、非医疗使用或研究过但无实际临床价值的用途，不单独凑评分行。证据不足为 `N/A` 或待核实，不强行升 `reviewed`。
6. 重要处方规模、误用或潜在不适当使用数据按药物特异性选取，注明地区、时间、人群、分母及证据性质。现行中国核准说明书不可取得时保留缺口，不用商业摘要替代；仅复核本轮条目的中国管制字段，不重做全库审计。
7. 无独立研究问题时不新增专题；只有主条目确实无法简洁承载的重要证据冲突时才新增少量问题导向专题。原则上不复制试验方案、不堆砌 PK/PD 参数和长表格。
8. 四组结果完成后由主代理统一核对**本轮变更文件**的事实、法域/剂型、评分依据、引用链接、相对路径和表格；统计真实的 `reviewed/basic/indexed` 数量，更新 `catalog/index.md`、`README.md` 与本计划的完成记录。若代理中断，先收回其已完成内容，由主代理补齐或如实标缺口，不制造完成记录。提交并推送此分支，等待人工审阅，**不自行合并 `main`**。

### 不做

不额外划分试点与多阶段审批，不新增 CI、数据库、爬虫、自动评分器、哈希流程、批量空模板或独立验证框架；不扩写计划外的 256 份档案，不重审前四轮的 91 份 `reviewed`、不重新打开两份 `basic` 的旧证据缺口。单份资料不足时保持原状态，继续完成其他档案。


## Wave 5 完成记录（2026-10-22）

**状态**：计划列出的 24 份全部处理完毕，21 份达到 `reviewed`，3 份保持 `basic`（`brexanolone`、`secobarbital`、`etizolam`）。仓库实际计数为 **112 reviewed / 163 indexed / 5 basic**，共 280 份；`analysis/` 仍为 15 份，本 Wave 未新增专题。

**分工与执行实况**：四组子代理并行、每组 6 份且路径互不重叠。A 组（抗精神病药与两份新型复方）与 B 组（抗抑郁药与一份新型复方）各自完成 6 份；C 组（巴比妥类、麻醉与镇静药）在完成 5 份后触及子代理轮次上限，第 6 份 `chloral-hydrate` 由主代理按已抓取的英国 SmPC 与历史 SPL 写成；D 组（抗焦虑、兴奋与认知相关药）在完成 3 份后因模型响应中断，补做代理完成剩余 3 份（`etizolam`、`caffeine`、`piracetam`），其中 `caffeine` 由主代理压回信息密度带。共享文件（`AGENTS.md`、`PLAN.md`、`README.md`、`catalog/index.md`）与跨文件口径全部由主代理处理，子代理未提交、未合并。

**主要来源与版本口径**：监管事实一律按“产品＋法域＋文本版本”引用。美国 17 份条目有可引的现行文本，取 DailyMed setid＋生效或发布日（如 LYBALVI setid `32ffddd1-…` 生效 2026-01-31、COBENFY setid `8f0e73bf-…` 生效 2026-01-16、AUVELITY setid `dcefda7c-…`、AZSTARYS setid `00b5e716-…` 生效 2026-05-11、EXXUA setid `0c78edd8-…` 生效 2026-07-14）；英国以 emc 产品号＋PL＋SmPC 修订日引用，**本轮 8 份条目以英国现行文本为核心或补充**：`reboxetine`（Edronax，emc 1578，修订 2025-04）、`citalopram`（Cipramil 片 992 与滴剂 1392，修订 2023-11）、`pimozide`（Orap，emc 6911，修订 2016-07-01）、`droperidol`（emc 7310，修订 2024-10-08）、`thiopental`（emc 665 修订 2023-12-18；emc 9376 修订 2024-02-12）、`chloral-hydrate`（emc 8136 修订 2025-10-31；emc 13223 修订 2026-08-17）、`piracetam`（Nootropil，emc 101129／101131，修订 2025-07）、`dexmedetomidine`（Dexdor emc 4783；Kalceks emc 13154，修订 2026-05-12）。**法国 BDPM 本轮对首页、`/medicaments?search=` 与字母序接口恒返回 HTTP 503，24 份均无法国文本**，一律写成检索事实。`PMID` 与 `NCT` 按原文标注地区、年份、人群与分母。

**本轮写准的法域与产品反差**：`pimozide` 在美英两侧的收载用途几乎互换（美国两份现行仿制文本只有妥瑞氏障碍且非一线，英国 Orap 只有慢性精神分裂症与其他精神病、含 12 岁以上，且不收载妥瑞氏）；`chloral hydrate` 在美国的唯一 DailyMed 记录是 HPUS 口径的顺势疗法产品（CHLORALUM 3X，2011），不能充当给药方案，其现行锚点是英国两份口服溶液 SmPC；`piracetam` 的核准用途只有成人皮层起源肌阵挛且要求与其他抗肌阵挛治疗联用；`caffeine` 按产品分成 NICU 制剂、OTC 提神与 `US-BNZ`（Marketing Status: unapproved drug other，页面附 FDA 未经判定声明）三种语境，出院后延长疗程一行依据 MoCHA 的阴性结果；`pentobarbital` 的人用评分排除同名的兽用 pentobarbital＋phenytoin 安乐死产品；`loxapine` 的吸入粉雾剂（ADASUVE，DailyMed v9，2026-10-05）与口服胶囊分行，吸入剂的支气管痉挛与 REMS 场所条件只作剂型修正项；`droperidol` 的美国最大初始量 2.5 mg 与英国的 1.25 mg 封顶、以及英国独有的 PCA 场景并列不综合。

**整合阶段的六处修正（主代理）**：① 派发时英国 emc 抓取尚未完成，主代理把英国现行文本并入 `pimozide` 与 `droperidol`（适应证、剂量台阶、禁忌清单、撤药与过量条款、定量药代），并把四组的“未取回”表述改成实测检索事实（emc 0 命中：iloperidone、loxapine、Lybalvi 与 olanzapine and samidorphan、Cobenfy 与 xanomeline、gepirone、desipramine、pentobarbital、secobarbital、methohexital、clorazepate、methamphetamine、brexanolone 与 Zulresso、Azstarys）；② `brexanolone` 的 §2.2 改为“不给 A–D 等级”——其说明书虽仍可按 setid 浏览（版本 11，2024-07-19）但已退出现行索引、openFDA 404、英国 0 命中，美国 FDA 批准撤销事实已于审阅后补入（2025-04-14 生效），历史试验仍保留 §5，不把存档说明书当作现行获批文本；③ 逐份复核 A–D 场景表，确保无年龄组、妊娠哺乳、肝肾功能、禁忌人群、监测要求或“未获批”凑成的评分行，`metamfetamine` 因现行三份仿制文本只收载 ADHD 而把发作性睡病与外源性肥胖留在检索缺口、不设行；④ 滥用维度只有 `citalopram` 记 1 分，依据是标签原句“动物研究提示西酞普兰的滥用可能性低”，其余按本药特异的人体或自身给药证据（`secobarbital`、`methohexital`、`caffeine`）或 `N/A` 处理，停药与滥用全程分开；⑤ 中国维度 24 份一律 `N/A`（2017 版中国标准与 AGS Beers 2023 全文按药逐字核对，只有类别条款或完全未收录，无当地处方偏离数据），中国管制字段沿用 2026-10-06 审计且层级结论未改（含 `pimozide` 的“疑似落入奥啡类·待核实”、`bupropion-and-dextromethorphan` 的“待核实”、`potassium-clorazepate` 的非药用类第 288 项经目录注 1 的盐型覆盖论证、`dexmethylphenidate-and-serdexmethylphenidate` 依赖哌甲酯第 11 项备注的复方归属）；⑥ 把 `dexmedetomidine` 与 `caffeine` 压回 15,174 的去空白上限以内，删的是次要数值与跨节重复，未删任何结论。

**验收方式**：只检查本轮 24 份文件与 `catalog/index.md`、`README.md` 及本计划——表结构（§2.1 六维、§2.2 四列与 A–D 档位）、评分行语义与占位行、§2.2 依据单元格长度、相对链接与官方 URL 可达性、去空白字符密度带、状态定义是否被夸大。**链接可达性以 DailyMed `drugInfo.cfm?setid=` 页面与 openFDA 查询返回为准：已退出现行索引的存档标签其 `spls/<setid>.xml` 返回 404 而页面仍可浏览，故 XML 404 只说明版本退出现行接口，不能判成死链；`services/v2/spls/<setid>.json` 对有效 setid 也常返回 415。** 核对脚本一律放在仓库之外，未新增脚本、CI、数据库或自动评分器。

**仍开放的证据缺口**：24 份的中国上市剂型与核准适应证全部未取得（NMPA 恒返回 412 拦截页、CDE 恒返回 202 脚本校验页），管制字段沿用 2026-10-06 审计、本轮未重跑全库结构核查；法国本轮无文本；多份美国现行文本为旧格式（`desipramine`、`pimozide`、`droperidol`、`loxapine` 口服、`metamfetamine` 仿制片、`potassium-clorazepate` 仿制片无 §14 定量对照与结构化滥用章节），相应疗效叙述停在标签层；`citalopram` 的英国 10／40 mg 片文本未逐份读取；`reboxetine` 的 §4.8 频率档在纯文本化时被压平，已在条目 §10 标注；`piracetam` 的两规格文本只全读了 1200 mg 一份；`thiopental` 与 `chloral-hydrate` 的其他欧盟成员国文本未核；emc 按 chloral 检索的第三条命中（Welldorm Elixir，4687）本轮未读取；`etizolam` 与 `brexanolone` 的任何法域现行说明书仍为空缺，故保持 `basic`。本 Wave 未扩写计划外药物、未重审前四轮档案、未合并 `main`。


## Wave 5 审阅后定点修补与验收（2026-10-23）

本节只记录对本轮 24 份档案的定点修补，不重新研究既有 Waves，不改变数量与评级状态。

- `brexanolone.md`：补入 FDA 2025-03-14 正式撤销公告（90 FR 12162，NDA 211371，**2025-04-14 生效**），原因是持证方报告产品停止销售并申请撤销；据此修正美国监管状态、§2.2 评分边界、§4 和 §10，保留 `basic`，不凭撤销推断疗效或安全性失败，英法中仍为未核实。
- `citalopram.md`：修正氢溴酸盐分子式为 `C₂₀H₂₂BrFN₂O`（或游离碱 `C₂₀H₂₁FN₂O·HBr`），不再重复计算 HBr。
- `bupropion-and-dextromethorphan.md`：将“右美沙芬氢溴酸铵”改为“氢溴酸右美沙芬”；删除基于同一 MDD 试验第 1–2 周次要终点的独立 B− 评分行，结果仍在 §5，批准的 AD 激越场景保留。
- `gepirone.md`：撤销把性功能不良反应差异设为独立 C+ 场景的做法，将厂方相关事后合并分析及局限保留在 §5／§10；原 MDD 适应证不变。
- `xanomeline-and-trospium.md`：删除未经适当跨试验比较支持的“与其他抗精神病药效应量级相当”，仅保留两项本复方对安慰剂的 PANSS 结果。
- `pentobarbital.md`、`methohexital.md`、`thiopental.md`、`potassium-clorazepate.md`：A–D 表只保留用途、临床证据与主要负担；详细滴定、年龄剂量、给药浓度与速率移入既有 §4，原关键数字和法域限定保留，不创造新场景或新评分。
- `piracetam.md`：统一取证深度声明，1200 mg 英国 SmPC 完整读取，800 mg 规格核对产品身份与版本，不再声称两规格逐节一致。
- `catalog/index.md`、`README.md` 与本文件同步监管状态、核查结论及准确计数。验收仅针对本轮改动文档：检查上述陈述与内容一致、A–D 表格与等级、链接与相对路径、24 份状态数量不变、`main` 合并前没有其他计划外改动。新证据来自 FDA 正式撤销公告与 DailyMed 分子式页面；其余为文档内部校准。

保留的取证缺口不因本次修补关闭：中国核准信息、英国／法国部分产品说明书，以及 800 mg 吡拉西坦全文等；不新增脚本、CI、数据库或专题。合并结果以 PR 和 Git 历史为准。


## Wave 6 批量建档计划（2026-10-23）

**当前状态：已完成并经审阅定点修补（见文末记录）。** 分支：`plan/reviewed-expansion-wave6`，基于 Wave 5 已合并的 `main`（PR #8）。执行前基线：**112 reviewed / 163 indexed / 5 basic**，共 280 份档案与 15 份专题。本轮一次性处理下列 **32 份尚为 `indexed` 的条目**，仅按文件归属分四组，不以完成篇数或升级数额作为质量指标。

### 四组文件清单（每组 8 份）

- **A｜抗精神病药，主要为旧药与地区性制剂**：`levomepromazine`、`thioridazine`、`chlorprothixene`、`tiotixene`、`periciazine`、`molindone`、`sertindole`、`tiapride`。
- **B｜三环抗抑郁药及 MAOI 等**：`trimipramine`、`amoxapine`、`maprotiline`、`dosulepin`、`isocarboxazid`、`protriptyline`、`lofepramine`、`opipramol`。
- **C｜苯二氮䓬类、催眠药和其他镇静药**：`lormetazepam`、`brotizolam`、`quazepam`、`nimetazepam`、`dimdazenil`、`clomethiazole`、`paraldehyde`、`amobarbital`。
- **D｜抗焦虑、促醒与认知相关药及一份固定复方**：`prazepam`、`tofisopam`、`fabomotizole`、`pemoline`、`adrafinil`、`citicoline`、`oxiracetam`、`piracetam-and-cinnarizine`。

### 执行与验收

1. 主代理先读 `AGENTS.md`、`SCORING.md`、`SOURCES.md`、`METHODOLOGY.md`、`DISCLAIMER.md` 和喹硫平样板，**一次派发四组**。允许最多四个并行子代理，一组一个，**只改本组列出的八个药物文件**；不得交叉编辑、嵌套派发或动共享文档。主代理负责统稿、接管中断任务、共享文档与提交。不要拆成待人工审批的阶段。
2. 每份主条目继续坚持**档案优先、简短且可溯源**：核对 WHO ATC 与药物身份、中国管制、具体产品／法域／途径／版本与注册状态，整理有实际意义的获批和有据可评的使用场景、关键疗效证据、短长期风险、停药／依赖／误用、主要相互作用和证据边界。监管来源先于指南、综述或原始研究，不能拿其他国家、单方、相似药或历史说明书填补现行产品信息。
3. **本轮特别留意实体与法规边界**：`tiotixene` 的命名与美国产品称谓、`periciazine` 的地区名称、`dosulepin` 的 dothiepin 别名及 `opipramol` 的类别定位须以原始资料核实；`dimdazenil` 的中国具体产品信息、`pemoline` 等药的批准或撤销历史、`adrafinil` 的药物与非药物销售语境，均要区分已证实注册事实、历史使用与现行核准。**`piracetam-and-cinnarizine` 是独立固定复方**，不得复制吡拉西坦单方的适应证、试验、剂量或评分。
4. **分数跟随证据而非档案篇幅**：六维负担与 A–D 场景按 `SCORING.md`；仅评有现行临床决策价值的适应证或用途，特殊人群、禁忌、非医疗使用、停药方案和监测条件不另凑场景。A–D 依据只保留决定性事实，具体给药操作和次要试验数据留原始来源。缺证据写 `N/A` 或保留状态，不为追求 32 份 reviewed 硬凑结论。
5. 对历史或地区性产品，优先检查**能够取得的官方注册资料、现行产品文件及正式撤销公告**。openFDA／DailyMed／emc／NMPA 检索零结果只作为检索事实，官方无法取得就清楚标缺口；不把一地的状态推广到另一地。实际读取的产品版本与规格范围如实记录，不声称没有做过的逐页比对。
6. 只有能回答独立、重要证据冲突时才新建专题，不设置专题数配额。若有可靠的药物特异使用／误用数据，应说明地区、年份、分母及原始指标，不能拿类级用量或网络讨论推本药发生率。主代理复核本轮改动的事实、评分表、关键链接与相对路径，按真实状态更新 `catalog/index.md`、`README.md` 和本计划的完成记录。提交并推送当前分支，**等待审阅，不合并 `main`**。

**不做**：不扩写其余 248 份档案，不重开前五轮的 112 份 reviewed 或既有 5 份 basic，不追加数据库、爬虫、自动评分器、CI、独立试点、多轮验收流程或配额制专题。资料受限的单药简要记录缺口后继续，不让整个任务被一个旧药阻塞。


## Wave 6 完成记录（2026-10-23）

**状态**：32 份全部处理完毕，**18 份达到 `reviewed`**、**14 份保持 `basic`**；仓库实际计数 **130 reviewed / 131 indexed / 19 basic**，共 280 份；`analysis/` 仍 15 份，本轮未新增专题。

**分工与执行实况**：四组各 8 份并行；B 组与 D 组全部完成；A 组与 C 组在写完各 8 份后触及子代理轮次上限而停止（文件均已落盘并经骨架、表头、页脚核验，无半成品）。主代理负责共享文件、剂量位置修正与 tiotixene 状态补充。

**主要来源与版本口径**：美国只有 8 个分子有可引现行标签（amoxapine、isocarboxazid、molindone、protriptyline、quazepam、thioridazine、tiotixene／thiothixene、trimipramine）；英国 emc 现行 SmPC 支撑 8 份条目；法国 BDPM 本轮可用，15 份条目引用法国 RCP；citicoline 用西班牙 CIMA（Somazina）；sertindole 用 EMA 第 36 条转介；dimdazenil 用 NMPA 2023-11 批准公告转载；pemoline 的 2005 年停售用 NMPA《药物警戒快讯》转载的 FDA 公告。

**官方撤销／认定记录的核验（本轮重点）**：NAVANE 胶囊（NDA 016584）**2024-06-03 公告撤销、2024-07-03 生效**（89 FR 47566）＋2017 年“并非因安全或疗效撤出”认定（82 FR 43388）；Surmontil（NDA 016792）与 Vivactil（NDA 016012）**2025-08-04 公告撤销、2025-09-03 生效**（90 FR 36440）＋各自的认定文件；Mellaril（NDA 11-808）2007-11-07 撤销（72 FR 62858，2007-12-07 生效）；Asendin（NDA 18-021）2003-08-18 撤销（68 FR 49481）；Centrax 在 1994-03-02（94-4660）与 1996-03-27（61 FR 13506）两批撤销中均被列入；CYLERT（NDA 016832／017703）**2021-04-12 FDA 因肝毒性要求企业申请撤销、2021-09-02 Abbott 提交申请、2023-05-23 正式撤销**（88 FR 33148）；MOBAN 2013-11-06“并非因安全或疗效撤出”认定（78 FR 66742）；brotizolam 的 WHO ECDD 1994 建议与 1995 年美国 Schedule IV 公告（FR 95-1553）。**区分公告日与生效日，以及企业因停销申请撤销和 FDA 基于明确肝毒性要求申请撤销两种程序；撤销本身不单独作为 D 分依据，匹莫林另有独立的安全性与风险收益认定。**

**中国事实**：7 份命中管制目录（lormetazepam 二类41、brotizolam 二类6、nimetazepam 二类49、dimdazenil 二类25、amobarbital 二类3、prazepam 二类62、pemoline 非药用类302），其余 25 份为“未发现列入”；dimdazenil 是唯一以中国批准为主轴的条目（2023-11 批准，说明书未取得）。

**整合修正**：① periciazine、quazepam 的 A–D 单元格剂量细节移入 §4；② tiotixene §1 补入 NAVANE 2024 撤销与“现行文本为仿制标签”；③ 逐份复核 A–D 表，确认无年龄组、妊娠、禁忌人群、监测要求或撤销本身凑成的评分行；④ 滥用维度、停药维度与中国 PIM 维度按既有口径处理（无本药特异证据即 `N/A`）。

**验收方式**：只核本轮 32 份与 `catalog/index.md`、`README.md`、本计划；表结构、评分语义、剂量位置、相对链接、官方 URL 可达性与去空白字符密度带；核对脚本在仓库外运行，未新增 CI、数据库或自动评分器。

**仍开放的证据缺口**：32 份的中国上市与核准适应证全部未取得（NMPA 412／CDE 202）；opipramol、lofepramine 片剂、fabomotizole、tofisopam、oxiracetam、paraldehyde、amobarbital 无现行产品文本；dimdazenil 说明书、adrafinil 的法国撤市官方文件、brotizolam 与 nimetazepam 的原产国文本未取得；citicoline 只读西班牙一份；法国 RCP 不外推至其他国家。本 Wave 未扩写其余档案、未重审前五轮 reviewed、未合并 `main`。


## Wave 6 审阅定点修补记录（2026-10-23）

仅修补本轮审阅所涉及的临床证据、监管生效日期和评分语义，**不重做 32 份全文、不改变状态数字**。

- **正式生效日期**：`tiotixene` 的 NAVANE 胶囊 NDA 016584 于 2024-06-03 **公告**撤销、**2024-07-03 生效**。NAVANE 口服浓缩液 NDA 016758、注射液 NDA 016904 与 `maprotiline` 的 LUDIOMIL NDA 017543 均列入 2009-05-19 公告、**2009-06-18 生效**的 74 FR 23407。`trimipramine` 的 SURMONTIL 与 `protriptyline` 的 VIVACTIL 于 2025-08-04 公告、**2025-09-03 生效**（90 FR 36440）。原有“公告当天已撤销”改为区分两个日期，认定文件与仿制药现行标签继续分开陈述。
- **`opipramol` 原始试验补证**：增加 `PMID:11199949` 的 307 例 GAD 随机双盲三臂安慰剂对照试验（28 天，HAM-A 主要终点 p<0.05，总体改善 63%／64%／47%，分别对应本药／阿普唑仑／安慰剂）。修正 §2.2、§5、§10 与来源，GAD 场景由 C 重新评为 B−，并明确无长期及等效性证据。由于德国现行产品标签仍未取得，档案**保持 `basic`**。
- **评分行去重**：`levomepromazine`、`tiotixene`、`molindone` 删除仅据“痴呆相关精神病未获批＋抗精神病药类级黑框风险”建立的 D 行，把高影响警告保留在 §6／§9。`isocarboxazid` 删除“作为初始抗抑郁药 D”这一二次场景，把美国标签“不宜初始使用”作为治疗抵抗性抑郁行的限制。对 `thioridazine` 等有药物特异临床证据的 D 行不作机械删除。
- **风险来源与结构**：`pemoline` 澄清 FDA 于 2021 年主动要求 Abbott 因肝毒性提出撤销申请，不再概括为普通企业停售撤销；`chlorprothixene`、`sertindole` 的独立 `## 待核实` 标题降为 §10 内部小标题，内容未删。

复核范围限定为上述修改过的药物条目、共享文档与计划内 32 份的状态／评分表结构；验收保持 **130 reviewed / 131 indexed / 19 basic（280 总数）**，专题分析 15 份。`main` 的合并由独立 PR 完成后再核对 Git 历史。


## Wave 7 批量建档计划（2026-10-23）

**状态：已完成（见文末“Wave 7 完成记录”。）** 工作分支：`plan/reviewed-expansion-wave7`，基于已合并 PR #9 的 `main`。起点为 **130 reviewed / 131 indexed / 19 basic**，280 份档案与 15 份专题分析。本轮已确认下列 **32 份全部处于 `indexed`**。目标是补齐抗焦虑药、相关草药、部分历史抗抑郁药以及地区性抗精神病／镇静药的档案，不按类别机械推断用途，不预设升级 `reviewed` 的数量。

### 文件与并行分组（4 × 8，彼此不重叠）

- **A｜苯二氮䓬类抗焦虑药及活性代谢物**：`medazepam`、`ketazolam`、`nordazepam`、`ethyl-loflazepate`、`clotiazepam`、`cloxazolam`、`mexazolam`、`fludiazepam`。
- **B｜其他抗焦虑药与补充类型**：`halazepam`、`camazepam`、`bentazepam`、`captodiame`、`benzoctamine`、`lavandulae-aetheroleum`、`emylcamate`、`mephenoxalone`。
- **C｜三环类、早期抗抑郁药及植物／前体成分**：`imipramine-oxide`、`dibenzepin`、`melitracen`、`amineptine`、`nomifensine`、`zimeldine`、`hyperici-herba`、`tryptophan`。
- **D｜地区性抗精神病药与镇静药**：`cyamemazine`、`pipamperone`、`melperone`、`benperidol`、`penfluridol`、`zotepine`、`clotiapine`、`propiomazine`。

### 本轮执行口径

1. 主代理先阅读 `AGENTS.md`、本计划、`SCORING.md`、`SOURCES.md`、`METHODOLOGY.md`、`DISCLAIMER.md` 与喹硫平样板。**一次派发四组，允许最多 4 个并行子代理**，一代理一组，仅修改自己分组的 8 个 `drugs/*.md`。子代理不得更改共享文档、交叉编辑、嵌套委派或合并；主代理处理共享文档、失败接管、整体验收与提交。**不拆成逐阶段审批流程。**
2. 主条目仍是**快速判断档案**：按药物实体核对 ATC、名称／盐型／代谢物、中国管制与核准注册信息、现行标签（可取得时注明**产品＋法域＋剂型＋版本**）、批准适应证、主要机制、关键药物特异临床结果、长期和短期风险、停药依赖、误用及重要相互作用。风险评分和 A–D 使用场景只按 `SCORING.md` 证据层级评价，每行保留 1–3 个决定性事实，详细给药步骤与次要试验数值留正文或原始来源。
3. **取证优先找有具体产品的法域**，不限美英法：如德国、奥地利、法国、西班牙、瑞士、日本等有可信官方产品注册与说明书资料才引用，且只代表所核对的国家与剂型。不得将数据库零命中理解为未批准、从未上市或撤销。撤销公告必须区分**公告日、生效日、企业停销与监管安全原因**。找不到现行产品说明书时保留 `basic` 或 `indexed` 并明确缺口，继续下一药，不用其他分子说明书补齐。
4. **本轮特别需要区分实体层级**：`nordazepam` 同时可作为其他苯二氮䓬药的活性代谢物，不能借母药适应证与评分；`melitracen` 单方不得直接沿用与氟哌噻吨的固定组合证据；`lavandulae-aetheroleum` 的标准化口服薰衣草油药品与普通精油／芳疗商品分开；`hyperici-herba` 的药典植物原料、标准化提取物、不同剂型及保健品不能互相替代；`tryptophan` 的药品与膳食／补充剂语境分开。高风险的历史抗抑郁药（`amineptine`、`nomifensine`、`zimeldine`）如有停售、撤销或药物警戒事实，按具体官方决定与生效时间记录，勿将停销等同于 D 级疗效判断。
5. **避免 Wave 6 的两类返工**：涉及实际治疗价值的 A–D 场景，在下结论“无药物特异 RCT”之前核对原始试验检索，不要只引二次综述；不能仅凭未获批或类别黑框设 D 行。若存在真实的药物特异阴性试验或药物风险收益监管认定，仍应如实陈述且可以形成有依据的场景评分。证据不足不强行给等级，不以同类药物、代谢物、植物成分的研究替代本药产品研究。
6. 无独立重要争议需要解释时**不新增专题**。主代理按四组实际完成情况复查六维评分表、A–D 场景语义、关键原始引用和相对链接，将 `catalog/index.md`、`README.md` 与本计划的最终**真实**状态和未解决缺口一次更新。提交并推送本分支，**等待审阅，不得合并 `main`**。

**不做**：不回头重写 Waves 1–6 或现有 `basic`，不扩写其余 99 份未列入的 `indexed`，不新增数据库、自动评分器、CI、长期爬虫、结构性迁移或配额型专题，不以字数和表格复杂度代替证据质量。


## Wave 7 完成记录（2026-10-24）

**状态**：32 份全部处理，**11 份达到 `reviewed`**、**18 份 `basic`**、**3 份保留 `indexed`**（fludiazepam、emylcamate、mephenoxalone：有完整骨架但无现行产品文本、无可评分临床内容）。仓库实际计数 **141 reviewed / 102 indexed / 37 basic**，共 280 份；`analysis/` 仍 15 份、本轮未新增专题。

**执行实况**：四组各 8 份并行；A 组在写完 8 份后触及子代理轮次上限停止（文件完整），其余三组正常完成。主代理负责共享文件、两处剂量位置修正、日期统一与实体错误核验。

**主要来源**：法国 BDPM（TERCIAN、DIPIPERON、VICTAN、VERATRAN 的现行 RCP）；西班牙 CIMA（medazepam、ketazolam、Tiadipona、薰衣草油、clotiapine 的 Ficha técnica）；英国 emc（benperidol、贯叶连翘 THR 33336/0003、色氨酸 Optimax PLGB 17509/0093）；美国 openFDA 只有色氨酸与贯叶连翘的补充剂标签，未被当作药品证据。

**关键修正与发现**：① **BDPM 的 DEFANYL 实为 amoxapine**，不能作 imipramine oxide 的现行锚点；② **西班牙 mexazolam／melitracen 的命中分别是复方或非单方**，melitracen 的记录为 Deanxit（美利曲辛＋氟哌噻吨），不能当单方证据；③ `nordazepam` 作为活性代谢物单独建档；`lavandulae-aetheroleum` 分开标准化药品／精油／化妆品；`hyperici-herba` 分开英国 THR／德国标准化提取物／法国顺势疗法稀释液／美国补充剂标签；`tryptophan` 分开英国药品与补充剂；④ 历史撤市按日期与性质记录：amineptine（法国 1999-01）、nomifensine（1986）、zimeldine（1983）、zotepine（英国曾有上市线索，现行产品状态及撤销决定未核实），均不作 D 分；⑤ 按属主 Wave 6 要求先查原始试验：ethyl-loflazepate 1989 年日本双盲试验、pipamperone 1975 年交叉试验与 2011 年增效试验、薰衣草油与贯叶连翘的随机试验与 Cochrane 汇总；⑥ 痴呆相关行为与“初始治疗线数”均未设 A–D 行。

**验收方式**：只核本轮 32 份与 `catalog/index.md`、`README.md`、本计划；表结构、评分语义、剂量位置、相对链接、官方 URL 可达性与密度带；脚本在仓库外运行，未新增 CI、数据库或自动评分器。

**仍开放的证据缺口**：32 份的中国上市与核准适应证全部未取得（NMPA 412／CDE 202）；德国（melperone、benperidol、dibenzepin）、日本（cloxazolam、mexazolam、fludiazepam、clotiapine）、瑞典（propiomazine）、比利时／荷兰（penfluridol）的现行文本未取得；zotepine 仅读取 KEGG MEDICUS 的 2026-10 日本转录版而未核对 PMDA PDF；EMA／HMPC 的贯叶连翘专论访问返回服务器错误；美国 1989 年色氨酸 EMS 召回与法国 amineptine 1999 年官方公报原件未取得；西班牙薰衣草油 Lasea／Revisea 两条 CIMA 记录均属药品（分别按植物药／传统植物药注册），不得与普通化妆品或精油商品混同。本 Wave 未扩写其余 99 份 `indexed`、未重审前六轮 reviewed、未合并 `main`。


### Wave 7 审阅修补记录（2026-10-24）

本轮只做定点修补，不重新派发 32 份，不改变 11 reviewed / 18 basic / 3 indexed 的状态。

- `hyperici-herba`：Cochrane 2008 与 SSRI 的 12 项比较属于**直接随机头对头试验**。汇总 RR 1.00（95% CI 0.90–1.11）不等于已严格证明等效／非劣，提取物和受试人群差异须保留。
- `tryptophan`：Cochrane 2002 共 64 人的两项试验分别针对色氨酸和 5-HTP，合并 OR 不能充当色氨酸单药效应量或 Optimax 辅助治疗证据。删除单药抑郁治疗 C 行，保留英国标签辅助治疗 C+ 行并说明缺少直接试验。
- `clotiapine`：西班牙说明书收载急性及慢性治疗，但现有对照研究不能证明长期复发预防。合并为一个 C+ 场景，维持剂量信息仍放 §4。
- `zotepine`：阴性症状小样本试验留 §5，移除同一适应证内重复的独立 C+ 行。明确日文说明书来自 KEGG MEDICUS 转录、未逐页核对 PMDA 官方原件。英国正式撤销公告及现行法律状态未核实。
- 共享来源事实：THR 33336/0003 是**贯叶连翘**而非薰衣草油。西班牙 Lasea／Revisea 两款均有 CIMA 药品记录，普通精油／化妆品不得继承其药品适应证。

状态仍为 **141 reviewed / 102 indexed / 37 basic**（280 份），专题 15 份。实际合并状态以 PR 为准。


## Wave 8 批量建档计划（2026-10-24）

**状态：已完成（见文末“Wave 8 完成记录”。）** 基线为已合并 Wave 7 PR #10 的 `main`：**141 reviewed / 102 indexed / 37 basic**，共 280 份档案与 15 份专题。下列 **32 个文件已在 `main` 逐份确认存在且状态均为 `indexed`**，无前七轮的重复任务。目的是补齐跨治疗组的临床档案，保持真实取证结果而非规定必须升级几份。

### 一次派发的四组清单（每组 8 份）

- **A｜抗精神病药、长效制剂及历史撤市药**：`promazine`、`perazine`、`pipotiazine`、`bromperidol`、`fluspirilene`、`remoxipride`、`levosulpiride`、`mesoridazine`。
- **B｜苯二氮䓬类、镇静催眠及历史高风险药**：`loprazolam`、`cinolazepam`、`triclofos`、`niaprazine`、`valnoctamide`、`methaqualone`、`glutethimide`、`adinazolam`。
- **C｜早期与地区性抗抑郁药、MAOI**：`iprindole`、`butriptyline`、`toloxatone`、`nialamide`、`iproniazide`、`quinupramine`、`bifemelane`、`medifoxamine`。
- **D｜认知／神经功能相关药与补充剂边界**：`meclofenoxate`、`pyritinol`、`aniracetam`、`acetylcarnitine`、`idebenone`、`pramiracetam`、`vinpocetine`、`propentofylline`。

### 执行要求与重点核查

1. 主代理先阅读 `AGENTS.md`、`SCORING.md`、`SOURCES.md`、`METHODOLOGY.md`、`DISCLAIMER.md` 和喹硫平样板。**一次性派发全部四组，允许最多 4 个并行子代理**，每个代理只编辑分配组的 8 份药物文件。不得交叉改文件或嵌套派发。共享文件（`PLAN.md`、`README.md`、`catalog/index.md`、`AGENTS.md`）仅由主代理更新与提交。不拆成需要人工确认的多阶段任务。
2. 主条目优先回答身份与 ATC、**现行具体产品／法域／剂型／标签版本**、中国管制与注册核实结果、获批用途与有实际价值的使用场景、关键本药特异临床结果、短期／长期风险、停药依赖／误用、重要相互作用及证据缺口。来源按监管文件 → 指南与高质量系统综述 → 原始临床研究处理。没有官方产品文本时坦陈缺口，可保持 `basic` 或 `indexed`，不得用同类药、商品名片段、旧论文或他国标签冒充现行批准。正式撤销要区分公告日、生效日、停售、撤销及安全原因。
3. **A 组重点**：`pipotiazine`、`fluspirilene` 区分长效注射与单方的剂型特有负担；`levosulpiride` 的胃肠动力用途与精神科用途按具体获批法域和剂量分别写，不能混用；`remoxipride`、`mesoridazine` 的历史安全问题与各国产品法律状态用官方公告核对，不因停销本身生成 D 行。
4. **B 组重点**：`triclofos`、`niaprazine` 特别核对儿童用途、年龄和产品剂型，不把老年／儿童当独立评分行；`methaqualone`、`glutethimide`、`adinazolam` 区分历史医学使用、列管、非医疗误用与现行批准，不以同类别的依赖性替代本药人体资料；`valnoctamide` 须区分历史制剂、临床研究与相关化合物（如 valproate）。
5. **C 组重点**：地区性 MAOI 与三环类必须先确认单方实体和现行具体说明书。对 `iproniazide`、`medifoxamine` 等历史风险或撤市，核实事实发生日期与正式来源，不能只凭二手综述宣称某法域已撤销。抗抑郁疗效与安全性按本药研究评价，不借相邻药物及复方的证据。
6. **D 组重点**：严格区分**药品与膳食补充剂／保健品／兽药制剂**。对 `idebenone`、`vinpocetine`、`acetylcarnitine`、`propentofylline` 等，核对产品、批准法域、适应证及其现时状态，不从某一法域或某一用途推导全球精神科疗效。对认知、痴呆、卒中及其他神经疾病研究，需区分独立药物特异随机试验、不同疾病人群及长期硬终点。**Meta-analysis（荟萃分析）合并多个分子时，不得把合并效应量当作单一分子的定量疗效，直接头对头与间接比较必须分清。**
7. A–D 仅评价获批或有当前决策意义、具本药特异证据的实际场景。年龄组、禁忌、停药、监测、普通剂量变化、纯粹“未获批”与临床症状亚型，不为凑分独立成行。评分单元格只写 1–3 个关键依据。对“维持治疗”“复发预防”“非劣／等效”等结论须核对真实研究设计和终点，**标签允许长期用药不等于有随机复发预防证据**。资料不足记 `N/A` 或不设场景，不强求 32 份都达 `reviewed`。
8. 仅当证据冲突超出主条目可解释范围时新增专题，不设数量配额。主代理结束时复核 32 份的结构、证据、主要链接、A–D 语义及相对路径，按真实结果更新 `catalog/index.md`、`README.md` 和本计划完成记录，提交并推送 `plan/reviewed-expansion-wave8`，**等待审阅，不合并 `main`**。缺口记录后继续，不因单药无法取证而中断全部任务。

**不做**：不重写 Waves 1–7、不返工既有 `basic`、不扩写计划之外的 70 份 `indexed`、不引入 CI、爬虫、数据库、自动评分器、分阶段审批、字数配额或无独立必要的专题；不把数据库检索零命中写成从未批准或已撤市。

## Wave 8 完成记录（2026-10-24）

**状态**：32 份全部处理，**6 份达到 `reviewed`**（promazine、pipotiazine、triclofos 等以现行英国或法国文本为锚点）、**26 份保持 `basic`**（无现行产品文本，缺口逐份写明）；仓库实际计数 **147 reviewed / 70 indexed / 63 basic**，共 280 份；`analysis/` 仍 15 份。

**主要来源**：法国 BDPM 的 PIPORTIL 片与 L4 长效注射、MARSILID 片、RAXONE 片；英国 emc 的 promazine 糖浆 SmPC；Cochrane 与原始试验（triclofos 2025 双盲试验、pipotiazine 1970 年代试验等）；美国 openFDA 仅 acetylcarnitine 补充剂标签；西班牙 CIMA 0 条。

**关键更正**：mesoridazine 的“2004 年 QT 撤市”缺官方公告支撑。FDA **2018-02-22** 正式公告、**2018-03-26** 生效撤销 **三项 SERENTIL NDA（片剂 016774、注射剂 016775、口服浓缩液 016997）**；**2021-04-01**“非因安全或疗效撤出销售”认定**仅针对片剂**，不能外推其他剂型；pipotiazine 两规格均标“已或即将不再上市”，L4 记 2025-08-30 停止商业化声明，但 RCP 仍有效。`fluspirilene` 中国字段维持“待核实（疑似奥啡类）”。

**整合修正**：pipotiazine 的等效措辞改为“未见差异（未做等效性检验）”；triclofos 的试验给药量移出 A–D 单元格。

**仍开放缺口**：32 份中国上市与核准适应证全部未取得（NMPA 412／CDE 202）；多数条目缺核准剂量与禁忌文本；意大利、日本、德国、瑞典等原产国文本未逐份取得；mesoridazine 已定位 2018 年正式撤销公告，但“2004 年 QT 撤市”的原始出处仍未定位，三个剂型的完整历史说明书未取得。本 Wave 未重写前七轮、未扩写其他 indexed、未合并 `main`。


### Wave 8 审阅定点修补（2026-10-24）

- `mesoridazine`：2018 年 FDA 正式撤销公告同时列出片、注射、口服浓缩液的三项 NDA，补齐剂型、批准号与 **2018-03-26 生效日**；2021 年非因安全／疗效撤出销售的认定仅对应**片剂**，不能移至其他剂型。
- `levosulpiride`：把 `PMID:8891846` 错称“单组研究”纠正为**四臂随机双盲、45 中心、1,298 人**的对照研究，保留年代、量表与跨成分网络荟萃节点不能拆分的限制；其三项评分场景名称移出具体剂量。
- `pipotiazine`、`loprazolam`：将评分表中的试验或标签详细剂量退回正文已有 §4／§5，保留场景依据。
- `pramiracetam`：10 人阿尔茨海默病阴性探索性试验仍详载 §5／§10，因缺现行获批和当前决策价值依据，不为历史研究单设 D 场景。
- 同步 README、目录索引与本计划的 **147 reviewed / 70 indexed / 63 basic** 口径。**不改本轮状态数量与 15 份专题**；待 PR 审阅合并后才进入主分支。


## Wave 9 批量建档计划（2026-10-24）

**状态：已完成（见文末“Wave 9 完成记录”。）** 分支 `plan/reviewed-expansion-wave9` 基于已合并 [PR #11](https://github.com/Adrerie/psychopharm-atlas/pull/11) 的 `main`。基线为 **147 reviewed / 70 indexed / 63 basic**，总计 280 份药物档案与 15 份专题。本轮 32 份已在 `main` 逐份确认全部为 `indexed`，无重复，也不重复 Wave 7 已评估却仍处于 `indexed` 的 fludiazepam、emylcamate、mephenoxalone。**一次派发、四组各 8 份，按实际证据决定最终状态**。

### 任务清单

- **A｜地区性抗精神病药及早期神经阻滞剂（8）**：`acetophenazine`、`butaperazine`、`clopenthixol`、`dixyrazine`、`moperone`、`mosapramine`、`sultopride`、`thioproperazine`。
- **B｜历史镇静催眠、苯二氮䓬及氨基甲酸酯／巴比妥类（8）**：`doxefazepam`、`ethchlorvynol`、`methyprylon`、`methylpentynol`、`bromisoval`、`carbromal`、`allobarbital`、`hexobarbital`。
- **C｜早期抗抑郁药、MAOI 与血清素前体（8）**：`alaproclate`、`etoperidone`、`iproclozide`、`minaprine`、`nizofenone`、`oxaflozane`、`oxitriptan`、`pivagabine`。
- **D｜历史促醒／兴奋剂与认知研究药（8）**：`fenetylline`、`fencamfamin`、`fenozolone`、`fipexide`、`pipradrol`、`prolintane`、`deanol`、`linopirdine`。

### 一次执行要求

1. 主代理阅读 `AGENTS.md`、`SCORING.md`、`SOURCES.md`、`METHODOLOGY.md`、`DISCLAIMER.md` 和喹硫平样板。**可以同时派发最多四个子代理**，A/B/C/D 每组一个，每个代理仅修改所分配的 8 份 `drugs/*.md`；无交叉编辑、无嵌套派发。主代理独自处理共享文档、复查与提交。**不分阶段申请审批，能一次完成的一次完成**。
2. 以药物档案为主，快速核对**本药实体、ATC、盐型及代谢物、现行产品的国家／剂型／说明书版本、核准适应证、中国管制、关键疗效研究、风险、停药与误用、重要相互作用和缺口**。优先官方产品说明书／药监决定，其次指南、系统综述和药物特异原始试验。需要判断临床价值时核对试验人群、对照设计与主要终点。**未取得现行产品文本时如实保持 `basic` 或 `indexed`**，不得从药名、商品名、临床研究所在国家或数据库零命中推断获批、当前在售或撤市。
3. **A 组**核对德国、法国、意大利及日本等地区性单方产品，与同名代谢物／复方分开。对于运动障碍、QT、镇静与高催乳素风险，类别警告和本药特异试验分别标注，只有类级黑框或未获批不能自动生成独立 D 场景。
4. **B 组**重点分清各巴比妥类与替代镇静药的**单一成分、剂型、历史批准、撤销记录、当今管制**。同类依赖风险不能直接当成本药误用率，撤销／停产必须有本法域的公告和**生效日期**。仅有历史题录者不要凑满评分，不对儿童、老人或其他特殊人群单独设场景。
5. **C 组**重点核对试验与上市阶段区别、不可逆／可逆 MAO 抑制的证据来源、严重肝损伤与撤市记录，尤其 `oxitriptan`（5-HTP）**不是** L-tryptophan。不可把既有 `tryptophan` 条目中两种前体合并后的 OR 直接分配给任一物质。
6. **D 组**重点区分历史合法 fenetylline 药品与如今被称为“Captagon”的不同成分及非法压片制剂，**街头名称不等于原药分子身份**，不借用混合片检测结果判断本药强化效应、剂量或市场使用率。其余历史兴奋剂、认知研究药同样区分药品、研究化合物、补充剂、列管与现实非医疗使用；不借其他刺激剂疗效给 A–D 分。
7. 评分遵守 `SCORING.md`：仅为**实际获批或有当前决策价值且药物特异证据足够**的场景给 A–D，负担六维不足写 `N/A`，研究阴性如属历史且无当前决策价值则保留正文不强制设 D 行。**随机直接对照 ≠ 间接网络比较，差异不显著 ≠ 已证明等效，现行标签的维持用量 ≠ 随机复发预防证据。** A–D 单元格只保留关键事实，剂量细节放 §4、试验数值放 §5。不得强求完成后 `reviewed` 数量或配额型专题。
8. 最后仅核对本轮 32 份档案、相对链接和共享索引，按真实结果更新 `catalog/index.md`、`README.md`、本文件的完成记录。必要时主代理精简修订 `AGENTS.md`。提交、推送 `plan/reviewed-expansion-wave9`，**等待我方审阅，不得合并 `main`**。单药取不到来源时记录缺口并继续下一项。

**不做**：不返工 Waves 1–8，不追求剩余 38 份 `indexed` 的同步完成，不新增 CI、数据库、爬虫、自动评分程序、复杂批次验收机制或无实际争议价值的专题。不把 32 份都升到 `reviewed` 作为完成标准。

## Wave 9 完成记录（2026-10-25）

**状态**：32 份全部处理完毕，**0 份达到 `reviewed`**、**32 份达到 `basic`**（ethchlorvynol、methyprylon 虽取得 FDA 历史 NDA 与撤销公告，但无说明书正文，复核后改回 `basic`）；仓库实际计数 **147 reviewed / 38 indexed / 95 basic**，共 280 份档案，`analysis/` 仍 15 份。

**主要来源**：美国 FDA 撤销公告 `2012-6591`（77 FR 16039；公告 2012-03-19、生效 2012-04-18；NDA 010021 PLACIDYL 胶囊）与 `96-7309`（61 FR 13506；公告 1996-03-27、生效 1996-04-26；NDA 9-660 Noludar 片），两者均记载持证人告知不再销售并申请撤回，**公告未独立认定撤出销售不是由安全或有效性原因引起**，也没有现行产品说明书正文；DEA《Alphabetic Order of Controlled Substances》用于联邦列管层级核对；WHO ATC/DDD Index 2026 逐个回查 32 个编码（15 份无 DDD）；其余为本药特异的原始试验与系统综述（PubMed）。法国 BDPM、西班牙 CIMA、英国 emc 对多数条目 0 命中，只按检索缺口记录。

**实体与事实校正（主代理复核）**：thiopropazate／Dartal（N05AB05）与 thioproperazine 分离，剔除误挂的舞蹈症／迟发性运动障碍试验；法国 CLOPIXOL 各规格实为 zuclopenthixol（N05AF05），故 clopenthixol 在法无现行产品；SEROTONINUM BOIRON 为顺势稀释制剂，不作 iproclozide 批准证据；Tenuate 归属 diethylpropion；carphenazine／Proketazine ≠ butaperazine；oxitriptan（5-HTP）与 L-tryptophan 分开，Cochrane 跨物质合并 OR 不归给本药；carbromal 代谢物不写成 bromisoval；“Avertin”属 tribromoethanol；Reposal 非 allobarbital 复方；“Captagon”街头压片化验不用于 fenetylline；prolintane→propylamphetamine 标为未证实；deanol 注明 2022 年实测对象为 centrophenoxine。

**整合修正**：C 组 7 份与 methyprylon 的 A–D 表把 `待核实`／`不评分` 当作等级——按 AGENTS.md 改为表后显式“不评分”说明；未定维度统一 `N/A`；alaproclate、etoperidone、pivagabine 删除写入正文的内部检索措辞；ethchlorvynol、methyprylon、pipradrol、fencamfamin、fenetylline 增加 DEA 字母表交叉核对并注明 CFR 段落号未能独立复核到段落一级。

**仍开放缺口**：32 份中国上市与核准适应证未取得（NMPA 412／CDE 202）；minaprine、iproclozide、fencamfamin、fipexide 的退出决定只有二手转述，正式文件未定位；mosapramine 无日文官方文本；丹麦 mdat.dk、意大利 AIFA、英国 emc 列表未能取回；ethchlorvynol 特征性宿醉与嗅味觉描述无单方出处；hexobarbital、allobarbital、doxefazepam、methylpentynol、bromisoval 无对照疗效原文。本轮未重写前八轮、未扩写计划外 `indexed`、未新增专题、未合并 `main`。


### Wave 9 审阅修补记录（2026-10-26）

- **跨药物实体修正**：`butaperazine` 混入的 Moditen-Retard／Moditen-Depot 实为**氟奋乃静／氟奋乃静癸酸酯**；撤销它在本药中的长效注射剂型、维持／复发预防 C− 场景、长期风险支持、研究链接及门诊用法的错误归属（FDA GSRS UNII FMU62K1L3C；PubMed 899478、1979463）。本药口服研究与 Repoise／Tyrylen 别名保留。
- `clopenthixol`：Deanxit 正式产品为 **flupentixol＋melitracen**，并非 flupentixol＋clopenthixol，按西班牙 AEMPS CIMA 产品说明纠正复方边界。
- `ethchlorvynol`、`methyprylon`：历史批准与正式撤准记录不等于已核齐现行／历史说明书的适应证、警告、禁忌、相互作用与监测要求，均改为 **`basic`**。持有人“产品不再销售、申请撤销”的 FDA 公告不得写成 FDA 已独立作出“非因安全或有效性撤出销售”的判断。
- 删除 `sultopride`、`fipexide` 对没有当前决策价值的历史剂量／历史认知用途单列的 D 级行，并将其本药特异 PET、QTc、暴发性肝衰与药物热资料保留在 §2.1／§5–§7；同理移除 `pipradrol`、`prolintane` 对历史用法的独立 C− 行，保留人体原始研究。
- 清理 `fencamfamin`、`deanol` A–D 单元格的 Markdown 加粗符号；全部本轮档案最终共 **147 reviewed / 38 indexed / 95 basic**（280 份），`analysis/` 15 份。

经本次审阅修复后才允许合并，**本记录不等于已合并**。


## Wave 10 最后一批未深入建档药物计划（2026-10-26）

**状态：已完成（见文末“Wave 10 完成记录”。）** 基线为 Wave 9 PR #12 已合并的 `main`，**147 reviewed / 38 indexed / 95 basic**，280 份档案、15 份专题。经目录与 280 份文件交叉核对，38 份 `indexed` 中有 **35 份从未经过前九轮的深入建档**，本轮将它们**一次性派发**。另外三份 `fludiazepam`、`emylcamate`、`mephenoxalone` 已在 Wave 7 核查过且明确记载资料不足，**本次不返工**，除非得到新的权威来源，允许长期保留 `indexed`。**目标是完成档案事实核查，不是清零 indexed 数量或强制提升 reviewed。**

### 分组与文件清单（35 份）

- **A｜早期抗精神病／多巴胺拮抗相关药（8 份）**：`acepromazine`、`chlorproethazine`、`fluanisone`、`oxypertine`、`prothipendyl`、`thiopropazate`、`trifluperidol`、`triflupromazine`。
- **B｜巴比妥类催眠药与历史剂型（10 份）**：`aprobarbital`、`barbital`、`butobarbital`、`cyclobarbital`、`etallobarbital`、`heptabarbital`、`proxibarbal`、`talbutal`、`vinbarbital`、`vinylbital`。
- **C｜其他早期镇静催眠／抗焦虑制剂（9 份）**：`acetylglycinamide-chloral-hydrate`、`apronal`、`bromides`、`chloralodol`、`dichloralphenazone`、`hexapropymate`、`mebutamate`、`pinazepam`、`pyrithyldione`。
- **D｜早期认知研究药、植物药与特殊用途制剂（8 份）**：`dimetacrine`、`gedocarnil`、`pirisudanol`、`reposal`、`scopolamine`、`temgicoluril`、`valerianae-radix`、`veralipride`。

### 一次执行要求

1. 主代理先阅读 `AGENTS.md`、`SCORING.md`、`SOURCES.md`、`METHODOLOGY.md`、`DISCLAIMER.md` 和喹硫平样板。允许 **4 个非嵌套并行子代理**按 A/B/C/D 分别处理 **8／10／9／8 份**，只修改各自分配的 `drugs/*.md`。主代理负责证据复核、共享文档、整合、提交与推送。**一次派发即可，不设中途审批或人为分阶段计划**。
2. 档案优先。按药物实体核对 WHO ATC、盐／酯／异构体与复方归属、真实监管产品／法域／剂型／说明书版本、中国药物管制、核准用途、本药特异关键临床研究、短期／长期风险、相互作用、停药与误用。先官方说明书／公告，再高质量综述与原始试验；无来源不补结论。**撤准公告、生效日期、停销请求与 FDA 独立非安全／疗效认定分开。**
3. **A 组的特殊边界**：`acepromazine` 必须区分**人用与兽用制剂**，兽药的标签与剂量不得直接变成人体适应证。`thiopropazate`（Dartal）与 `thioproperazine` 是不同药，优先检索商品名、MeSH 及原始受试物质，避免 Wave 9 跨药污染。历史 `trifluperidol`／`triflupromazine` 与近似拼写同系抗精神病药的试验不能混用。
4. **B、C 组的特殊边界**：所有巴比妥类的**单方与复方、不同盐和口服／注射**分别核准。类别层面依赖、呼吸抑制和列管法律条款不能冒充本药特异发生率。历史撤市需要正式决定，不把数据库零命中视为撤销。`bromides` 是含多种盐的分类名称，**必须明确研究对象是哪种溴盐**，各盐剂量与风险不可混算。`acetylglycinamide-chloral-hydrate`、`dichloralphenazone`、`chloralodol` 与水合氯醛的药物身份及水解关系须按来源区分，不把母体或固定复方的批准与试验当作单方事实。
5. **D 组的特殊边界**：`valerianae-radix` 要区分**药用缬草根、特定标准化提取物、传统草药注册及普通营养补充品**。`scopolamine` 区分给药途径与实际批准用途，不把晕动症或麻醉用药直接写成精神科适应证。`reposal` 先确认具体活性成分及商品名归属，不继承 allobarbital 旧记录。`veralipride` 的更年期用途、锥体外系风险与监管退出，应优先查 EMA／国家主管机构的正式文件，**公告和生效日期分别记录**。
6. A–D 只设**确有当前临床决策价值且有本药特异证据**的场景。无现行说明书或仅有历史人体试验，可以保持 `basic` 乃至 `indexed`，不因篇幅、目录零命中或仅有 NDA 撤销公告升为 `reviewed`。负担六维无法量化写 `N/A`。严重历史危害进入 §5–§7，**不强行建立历史用途 D 行**。不得以其他分子、同一商品名的假冒产品、不同盐或交叉荟萃合并效应量支撑当前分子评分。数值、剂量与试验详述留正文，A–D 单元格保持简短、纯等级。
7. 主代理收尾复核本轮所有文件的章节、六维表、场景等级、关键来源与相对链接，**按真实结果**更新 `catalog/index.md`、`README.md`、`PLAN.md` 的完成记录，必要时仅做极短 `AGENTS.md` 修订。提交并推送 `plan/reviewed-expansion-wave10`，**不合并 `main`，交由我方审阅**。单药官方资料打不开即记录缺口、继续其他药物，不增加额外机制、长期爬虫或审批环节。

**不做**：不重复 Wave 1–9 已处理药物，不人为压成恰好 32 份，不因最后一批而强制将 35 份全部升 `reviewed`，不新增无必要的专题、CI、数据库、评分程序或人工多阶段流程。

## Wave 10 完成记录（2026-10-28）

**状态**：35 份全部处理完毕，**2 份 `reviewed`、32 份 `basic`、1 份如实保留 `indexed`（`gedocarnil`）**；仓库实际计数 **149 reviewed / 4 indexed / 127 basic**，共 280 份档案，`analysis/` 仍 15 份。派发为 A(8)／B(10)／C(9)／D(8) 四个非嵌套子代理，其中 A、B、D 三组代理先后因中断与轮次上限停止，剩余 **A 组 4 份与 D 组 6 份由主代理接管完成**。

**`reviewed` 只有两份的依据**：Wave 9 审阅后门槛为“必须有可逐节引用的说明书正文（适应证＋警告＋禁忌＋相互作用＋监测）”。`scopolamine` 取到美国现行贴剂标签（DailyMed setid b877a694-a1d0-4280-937a-a06820b12a88，NDA 017874）与法国现行注射剂 RCP（BDPM CIS 64665646，AMM「Valide」），两条锚定均由主代理在本机重新取回确认；`valerianae-radix` 取到西班牙 AEMPS 注册 72461 的现行 ficha técnica（文本修订 2016-09，§4.1 为传统草药注册口径）与 EU 草药专论。其余 32 份没有这样的正文，注册命中要么为 0、要么属别的分子或动物用药，因此一律 `basic` 或 `indexed`，未把结构齐全当作升级理由。

**主要来源**：WHO ATC/DDD Index 2026（35 码逐个回查，12 份无 DDD）；PubChem／RxNorm 的 CAS 与同义词表；DEA《Alphabetic Order of Controlled Substances》PDF 实测行；美国 DailyMed（带 `/dailymed/` 前缀的检索接口）与 openFDA；法国 BDPM 前缀精确匹配接口；西班牙 CIMA REST；药物特异的原始试验与综述（PubMed）。中国 NMPA／CDE 恒不可脚本访问，上市与核准适应证全部“待核实”。

**关键归属结论**：`acepromazine` 的现行 FDA 产品全为动物用药（PROMACE，NADA 117-532），兽用标签不转写为人用适应证；`fluanisone` 的芬太尼复方（Hypnorm 类）条款不计入单方，且复方中芬太尼的中国列管与本药分述；`reposal` 按 CAS 3625-25-0／N05CA12 独立成药，文献检索排除了“甲己巴比妥商品名”与“allobarbital 复方”两种误归属；`apronal` 是单一尿素化合物（CAS 528-92-7），与环巴比妥复方分开；`bromides` 为盐类集合名，禁止跨盐换算；`pinazepam`（CAS 52463-83-9）与 `propazepam` 在“Domar”归属上存在 DEA 与 PubChem 冲突，已按 CAS 锚定并记录冲突；巴比妥同族按 CAS 逐项分离，`proxibarbal` 的 Ipronal 线索与 carbromal 制剂碰撞需按 CAS 判读；`pirisudanol` 的 Stivane 与 Nadex 归并同一物质，维基别名 NEX431 无权威佐证不作依据。

**整合修正**：A–D 表内被当作等级的 `待核实`／`不评分` 改为表后显式说明；未定维度统一 `N/A`；单元格清除剂量、试验数值与 Markdown 加粗；氯醛释放类不继承 `chloral-hydrate` 条目的批准与试验；类别证据与本药特异证据分开标注；联邦列管以 DEA 实测行为准并注明 2100 为类别码。

**仍开放缺口**：35 份中国注册待核实；英国 emc、德／意／瑞士／比利时／日本官方库多数未取回；`gedocarnil` 无任何本药特异文献（四个研发代号检索亦 0 命中）；`etallobarbital` 同样零文献；`pirisudanol` 两份老年抑郁实践报告只到题录、未取得原文；`scopolamine`、`valerianae-radix` 的产品文本待补。本轮未重写 Wave 1–9、未扩写计划外档案、未新增专题、未合并 `main`。
