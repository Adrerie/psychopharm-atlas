# 精神药物建档计划与执行记录

> 当前阶段：**Wave 15 已完成建档与审阅修补，转入交接维护**。本轮工作分支 `plan/neuropsych-crossgroup-wave15`，基础提交 `91702d126c2981d55e7e8de08946b9af3e41e553`；合并后的 `main` 为后续工作唯一基线。Wave 1–15 均为历史完成任务，不重复派发；接手说明见 [HANDOFF.md](HANDOFF.md)。

> Wave 3 历史分支：`feat/reviewed-expansion-wave3`。该轮 24 份档案及后续审阅修补均已完成；主条目为主要交付物，药物利用与滥用证据按需纳入，不设置专题配额。

## Wave 16：基础档案系统性升级与语言审计（2026-11-10）

**分支**：`wave16/basic-upgrade`，基线 `70ec68a`（`main`）。本轮不合并 `main`，不推送。

**背景**：Wave 1–15 完成后仍有 159 份 `basic` 主档案。共同缺口是「给药方案」与「核准适应证」未绑定法域、具体产品与现行监管文本版本。此前各轮遇到的外部来源故障（BDPM 503、emc 429、NMPA 412、CDE 202）不构成永久排除，本轮逐份重做监管检索：能升级的升级，不能升级的留下可复现缺口。

**目标**
1. 159 份 `basic` 全部完成一次跨法域现行监管文本检索，并记录产品、编号、文本版本与核查日期。
2. 取得至少一份可逐节引用现行监管正文的档案，补全给药方案与核准适应证，状态改为 `reviewed`；否则保持 `basic`，把检索范围与缺口写入 §10。
3. 处理交接遗留：Wave 15 的 10 份 `basic`；中国管制字段待核实 10 份；`cinnarizine-and-dimenhydrinate` 的澳大利亚 TGA 文本；历史药品撤销／停供文书（有可核文件者补入）。
4. 语言审计：全部 384 份主档案与 15 份专题按 [STYLE.md](STYLE.md) 审订，保留数字、引用、表格结构、证据边界与章节编号。

**执行方式**（本轮明确授权子代理）
- 8 个升级子代理按批次处理 `drugs/<slug>.md`，批次互不重叠；1 个中国管制复核子代理处理 10 份待核实档案。
- 主代理负责共享文件（AGENTS.md、PLAN.md、README.md、catalog/index.md、catalog/related.md、STYLE.md、HANDOFF.md）、验收、统计与最终语言审计。
- 子代理不得嵌套派生、不得提交／推送／合并、不得新建仓库内文件。
- 语言审计分两段：升级档案按 [STYLE.md](STYLE.md) 随写随改；其余既有档案由主代理另派审计任务，按文件清单互不重叠。

**逐份核查要求**
- 身份与 ATC：按 WHO ATC/DDD 2026 复核编码、盐型、立体异构体与实体边界。
- 现行监管文本：按法域检索并记录产品、剂型、文本版本、核查日期。不得只用通用名，必须同时用商品名、历史别名与本地化拼写（如 flunarizina、biperideno）。重点入口：美国 openFDA/DailyMed、英国 emc/MHRA、法国 BDPM（按商品名前缀）、西班牙 CIMA、加拿大 DPD、澳大利亚 TGA、瑞士 Swissmedic、荷兰 Geneesmiddeleninformatiebank、德国／日本／韩国官方入口、EMA。聚合站只在无法取得一手页面时使用并标注来源层级。
- 中国管制：沿用 [SOURCES.md](SOURCES.md) 现行基准逐项复核；此前待核实的 10 份给出明确结论或保留「待核实」并写明原因。
- 临床证据与评分：按 [SCORING.md](SCORING.md) 重核 A–D 场景与负担维度，不把禁忌、特殊人群、相互作用写成评分行。
- 状态与数量：升级必须有可逐节引用的现行正文；证据不足保留 `basic`；禁止为凑数升级。

**语言口径**：见 [STYLE.md](STYLE.md)。硬指标：破折号连接、分号串句、一句并列名词超过两个、元表述、夸大词、内部流程语言、生造术语。必须保留：数字、剂量、日期、编码、setid/PL/CIS、PMID/DOI、链接、表格结构、章节编号、证据边界、来源节。

**验收**
- 159 份逐份有本轮检索记录与状态结论；总数仍为 384 份，专题仍 15 份。
- 升级档案含现行监管正文引用（法域＋产品＋文本版本）；未升级档案写明缺口。
- 384 份主档案与 15 份专题通过语言审计脚本复测并抽样人工复核。
- `catalog/index.md` 的 reviewed/basic/indexed 统计、README 基线、HANDOFF 缺口清单同步更新。

**交付**：提交到本分支，等待人工审阅，不合并 `main`，不推送。


## Wave 16 完成记录（2026-11-10）

**实际处理**：159 份 `basic` 主档案全部按法域、具体产品与现行监管文本重做检索与改写，覆盖 8 个批次（每批 19–21 份）。**27 份升级为 `reviewed`、132 份保持 `basic`**（逐份把检索范围与缺口写入 §10）；总数 384 份不变（核心六组 280、跨组 104），专题仍 15 份。

**升级名单（27 份）**：acetylleucine、biperiden、bromperidol、chlorprothixene、cinnarizine-and-dimenhydrinate、cinolazepam、cytisinicline、flunarizine、flunitrazepam、ginkgo-folium、hyperici-herba、imidafenacin、levomethadone、levosulpiride、medazepam、melperone、mexazolam、mosapramine、perazine、physostigmine、propiomazine、propiverine、prothipendyl、sertindole、sultopride、tofisopam、vinpocetine。

**取证范围**：新增或补充的现行文本覆盖西班牙 CIMA（Sibelium 55.352、Mictonorm 81879、Serdolect、AKINETON 28994/51224、VINPOCETINA COVEX 等）、日本 PMDA 添付文書（ウリトス、サイレース、バルネチール、クレミン、MELEX、レスミット、ブロムペリドール）、瑞典 FASS（Truxal、Propavan、Buronil）、匈牙利 GRANDAXIN、波兰 RPL Pernazinum、斯洛伐克 Gerodorm、德国 Dominal/Levomethadon/Anticholium、英国 emc（Cytisinicline PL 51228/0001、THR 33336/0003、CIZINATE SmPC 15869）、澳大利亚 TGA（CIZINATE PI CP-2021-PI-02009-1）、法国 BDPM（Tanganil、Tanakan）。`cinnarizine-and-dimenhydrinate` 的两法域文本与 `hexobarbital` 的中国管制结论关闭了 Wave 15 遗留。

**中国管制复核**：159 份逐项复核 2025/2026 三份药用类目录、非药用类 396 项与两批增列；交接时 10 份待核实全部重审——`pimavanserin` 明确不落入四类整类；`pimozide`、`benperidol` 按公告文字落入奥啡类条件（二）但保留「归属待核实」；`hexobarbital` 明确「未发现列入」并辨明同名冲突；`lisdexamfetamine`、`bupropion-and-dextromethorphan` 与三份天然产物保留「待核实」并写明未决条件。

**证据修复**：交叉审计发现升级中压缩掉的 5 条文献引用，已恢复——prothipendyl（14170115、1675298、4263179）、melperone（22356215、81118）、biperiden（42057551）、levosulpiride（36154321）、perazine（6140694）；另修复 11 份文件中的占位符损坏（NUL 字节与丢失 URL），按 HEAD 与正文语境逐行恢复。

**语言审计（[STYLE.md](STYLE.md)）**：全部 384 份主档案与 15 份专题审订。硬指标（基线→本轮结束，按扫描口径统计正文）：破折号 2713→37；分号 20837→1309；3 项以上并列句 3558→1778（4 项以上长枚举经两轮专项改写，剩余多为状态行/引用键与嵌套引用的复杂句）；内部流程语 2796→18；夸大词 1392→674；元表述 7→2；修辞对举（不是…而是／既…又）79+13→0；文档字符数 2641092→2727604（升级新增内容与列表化改写）。保留全部数字、剂量、日期、编码、setid/PL/CIS、PMID/DOI、URL、表格结构、章节编号与证据边界；术语统一为「核准适应证」「半衰期」等；交叉审计按审计前快照逐文件比对，未发现证据丢失（除上述已修复项）。

**第三轮语言审计（2026-11-11，[STYLE.md](STYLE.md) §7 口径）**：384 份主档案与 15 份专题按 §7 逐份复核。基线（本轮开工前 HEAD `85b5842`）→ 结束：破折号 61→9（余下 7 份 9 处均为英文文献题名原文、法语 RCP 引文与表格占位「—」）；正文分号 805→3（引文内 1、反引号 URL 字面量内 2）；一句多冒号 453→3（监管引文「Rare：…」与引用键检索式内）；防御性表述链 195→19（余下经逐条核读为单一条件边界事实的跨句正则命中）；3 项以上并列 1673→1566、4 项以上 155→149（余项按 §7「数据/编号/剂量清单从宽」保留）；表格单元格分号 5612→3248，**单元格 >1 个分号 0 处**；术语变体 0、元表述 0。

**PMDA 补证升级（2026-11-11）**：日本 PMDA 添付文書经站内 XML 取回后，4 份 `basic` 档案升级为 `reviewed`：溴替唑仑（レンドルミンD錠 0.25 mg，2023-01 第 1 版／2025-10 第 2 版）、依替唑仑（エチゾラム錠「アメル」0.25／0.5／1 mg，2024-10 第 1 版／2025-01 第 3 版）、氯噁唑仑（セパゾン錠 1 mg／錠 2 mg／散 1%，2023-07 第 1 版）、匹莫林（ベタナミン錠 10／25／50 mg，2020-08 第 1 版）。四份逐条补入适应证、用法用量、禁忌、相互作用、特殊人群、不良反应与过量处理，并区分日本现行文本与美国历史文本（匹莫林）。状态合计 384 份不变：reviewed 245→249、basic 132→128、indexed 7；语言扫描同步复核：破折号 9、正文分号 3、一句多冒号 3、防御性表述链 19 不变，3 项以上并列 1579→1598（新增为标签不良反应与特殊人群数据清单，按 §7 从宽），4 项以上 149→162，表格单元格分号 3248→3242（4 处 >1 分号的单元格按 §7 归一，总数低于审计结束时），>1 分号 0 处；0 断链、0 BOM／NUL／控制字符。

**检索记录合并（2026-11-11）**：132 份 basic 档案 §10 的 CDE／NMPA／PMDA 零命中检索条与不可达站点描述，合并为 [catalog/retrieval-log-2026-11.md](../catalog/retrieval-log-2026-11.md)；档案只保留已命中的确定事实（CDE 受理号、NMPA 批准文号、PMDA 添付文書编号与 4 份全文记录）。合并后复核：破折号 9、正文分号 3、一句多冒号 3、防御性表述链 19、3 项以上并列 1597、4 项以上 162、表格单元格分号 3242（>1 分号 0 处）；0 断链、0 BOM／NUL／控制字符；状态 reviewed 249／basic 128／indexed 7。

**专题新增（2026-11-11）**：新建 [analysis/benzodiazepine-withdrawal-label-boundaries.md](../analysis/benzodiazepine-withdrawal-label-boundaries.md)，比较苯二氮䓬类停药的三类标签形态（黑框加事件表、黑框加定性清单、仅「依存性（頻度不明）」），把唯一可引的停药期事件率（阿普唑仑 n=641）与日本三份现行文本的缺口并列，并给出不可外推清单。11 份相关主条目 §11 已加入链接，专题总数 15→16。语言扫描：破折号 9、正文分号 3、一句多冒号 3、防御性表述链 19 不变；3 项以上并列 1600、4 项以上 165；0 断链。

**专题新增（2026-11-11，第二篇）**：新建 [analysis/qt-thresholds-label-boundaries.md](../analysis/qt-thresholds-label-boundaries.md)，把 QT 相关的数值分成四种功能（给药前排除、治疗中停止、剂量上限、流程要求），并列西酞普兰、齐拉西酮、氨磺必利、氟哌利多与美索达嗪的 ΔQTc 数值及各自研究条件，说明同一分子在英美文本中"禁忌"与"警告"的差异。10 份主条目 §11 已加入链接，专题总数 16→17。

**专题新增（2026-11-11，第三篇）**：新建 [analysis/anticholinergic-burden-evidence-layers.md](../analysis/anticholinergic-burden-evidence-layers.md)，把"抗胆碱能负担"拆成受体结合、临床表型、标签条款与老年 PIM 名单四层，说明体外弱抗胆碱与 Beers 收录可以同时成立、PIM 占比不是处方不当率，并写入抗胆碱药预防与治疗 EPS 的标签边界。12 份主条目 §11 已加入链接，专题总数 17→18。

**专题新增（2026-11-11，第四篇）**：新建 [analysis/drug-vs-supplement-identity-layers.md](../analysis/drug-vs-supplement-identity-layers.md)，把药品、传统植物药与膳食补充剂三层的注册身份分开，举例褪黑素、石杉碱甲、胞磷胆碱、长春西汀、银杏叶在美欧中三地的不同身份，并列出适应证、剂量、提取物身份、证据与安全性文本五项不可互借。11 份主条目 §11 已加入链接，专题总数 18→19。

**专题新增（2026-11-11，第五篇）**：新建 [analysis/antidepressant-discontinuation-label-boundaries.md](../analysis/antidepressant-discontinuation-label-boundaries.md)，并列 10 份 SSRI／SNRI 标签的停药症状清单与配对数字（帕罗西汀 30%／20%、文拉法辛 31%／17%、艾司西酞普兰 25%／15%、西酞普兰复发预防试验 40%／20%），说明分母与定义不同不能排序，并划出"半衰期决定论"的适用边界（氟西汀长半衰期缓冲、氟伏沙明短半衰期未被标签列为风险因素）。10 份主条目 §11 已加入链接，专题总数 19→20。

**专题新增（2026-11-11，第六篇）**：新建 [analysis/racetams-approval-vs-evidence.md](../analysis/racetams-approval-vs-evidence.md)，把吡拉西坦（英国仅批皮层肌阵挛辅助治疗）、茴拉西坦（意大利批老年注意力与记忆障碍）、奥拉西坦（2026 年韩国 500 例试验阴性）、普拉西坦（10 例富集设计阴性）与丙戊茶碱（Cochrane 有限证据、人用开发停止）分列，说明化学家族、适应证与证据不能合并，并说明 CDE 受理记录不是疗效依据。6 份主条目 §11 已加入链接，专题总数 20→21。

**专题索引（2026-11-11）**：新建 [catalog/analyses.md](../catalog/analyses.md)，把 21 份专题按「剂型、药代与剂量」「停药与戒断」「安全阈值与监测」「证据比较与注册身份」「长期结局」五组列出，含建立日期与所链接主条目数，并写明专题维护规则。21 份专题文末与 README、目录索引、HANDOFF 均已加到索引的链接。

**专题新增（2026-11-11，第七篇）**：新建 [analysis/pim-standards-trigger-and-local-rates.md](../analysis/pim-standards-trigger-and-local-rates.md)，比较 AGS Beers 2023 与 2017 中国 PIM 标准的分级与条目，说明同一药物在两套标准中的不同判定（帕罗西汀 Beers 点名、中国标准未收载；劳拉西泮中国标准点名、Beers 前十未列），并给出浙江单中心 3,155 例队列按两套标准的占比差异，强调占比不是处方不当率。8 份主条目 §11 已加入链接，专题总数 21→22，索引同步。

**basic 状态说明统一（2026-11-11）**：128 份 `basic` 档案原有 85 份在文首写明保持 `basic` 的理由，其余 43 份只在标题或 §10 间接体现。现已在这 43 份的状态行后补入统一条款，写明保持 `basic` 的原因是未取得足以按 `reviewed` 引用的现行监管文本或完整证据体，并指向 §10 与 [逐名检索记录](../catalog/retrieval-log-2026-11.md)。改动只涉及状态行下方的说明句，未改正文数字、评分与证据边界。复测：384 份状态 249／128／7 不变，0 断链，破折号 9、正文分号 3、多冒号 3、防御性表述链 19 与审计结束持平。

**旗舰档案检索表述校正（2026-11-11）**：13 份核心 `reviewed` 档案（quetiapine、clozapine、fluoxetine、alprazolam、methylphenidate、olanzapine、duloxetine、diazepam、atomoxetine、aripiprazole、lithium、bupropion、zolpidem）中“NMPA 返回 412／CDE 返回校验页即不可检索”的旧理由句，改为“2026-11-11 验证入口可按名检索、本条目未重做该药逐名查询”的准确表述，并链接 [逐名检索记录](../catalog/retrieval-log-2026-11.md)。只改检索状态句，未改中国管制归属、批准状态结论或正文数字。其余 `reviewed` 档案的同类旧句保留为历史检索记录，当前口径以检索记录与各档案 §10 为准。复测状态 249／128／7 不变，0 断链。

**检索陈述时间层（2026-11-11）**：167 份档案中"不可脚本检索／不可脚本化／无法脚本检索"的表述统一改写为"在 2026-11-11 之前未能脚本检索"，以标明历史时间层；[SOURCES.md](../SOURCES.md) 新增第 7 节说明两个入口的检索条件变化与各证据层的区别。未改任何数字、结论与评分，状态 249／128／7 不变。

**专题新增（2026-11-11，第八篇）**：新建 [analysis/antipsychotic-metabolic-burden-layers.md](../analysis/antipsychotic-metabolic-burden-layers.md)，并列 9 份抗精神病药的标签体重数据、头对头复方数据与网络荟萃均值差，说明人群、剂量、疗程与指标不同不能排序，并以奥氮平与萨莫多兰复方为例说明体重下降不等于血糖风险同步下降。9 份主条目 §11 已加入链接，专题总数 22→23，索引同步。

**专题新增（2026-11-11，第九篇）**：新建 [analysis/hyponatremia-denominators-and-monitoring.md](../analysis/hyponatremia-denominators-and-monitoring.md)，并列奥卡西平（14 项对照试验 2.5%，38/1524，血钠低于 125 mmol/L）与艾司利卡西平（800／1200 mg 约 1%／1.5%，最低 112 mEq/L）的试验分母，与 SSRI／SNRI 标签中"血钠低于 110 mmol/L 病例"的无分母词句对照，说明两类证据不能排序，并写清老年监测与跌倒归因的边界。8 份主条目 §11 已加入链接，专题总数 23→24，索引同步。

**专题新增（2026-11-11，第十篇）**：新建 [analysis/eps-td-dose-links-and-anticholinergic-boundary.md](../analysis/eps-td-dose-links-and-anticholinergic-boundary.md)，区分急性 EPS 与迟发性运动障碍的时程、剂量关系与处置，并列氟哌啶醇（EPS 报告频繁、网络 OR 4.76）、奋乃静（CATIE 因 EPS 停药比例最高）、三氟拉嗪（≤6 mg/日 EPS 罕见）与氯丙嗪的差异，并写明抗胆碱药只治急性 EPS、不治 TD（三己苯氧啶标签不推荐预防性给药）与缬苯那嗪的 TD 获批位置。9 份主条目 §11 已加入链接，专题总数 24→25，索引同步。

**专题新增（2026-11-11，第十一篇）**：新建 [analysis/seizure-threshold-therapeutic-overdose-withdrawal.md](../analysis/seizure-threshold-therapeutic-overdose-withdrawal.md)，把惊厥风险分成治疗剂量（安非他酮 0.4%／450 mg 以下、450–600 mg 约 10 倍；氯氮平 1 年累积约 5%；马普替林定性排序）、过量（阿莫沙平惊厥与肾衰竭、洛非帕明旧数据方向相反）与撤药／逆转（安非他酮撤药禁忌、氟马西尼促惊厥）三条线，说明不能合成单一排序。7 份主条目 §11 已加入链接，专题总数 25→26，索引同步。

**专题新增（2026-11-11，第十二篇）**：新建 [analysis/cyp-inhibition-magnitude-substrate-dependence.md](../analysis/cyp-inhibition-magnitude-substrate-dependence.md)，并列帕罗西汀对去甲丙米嗪（AUC 约 5 倍）与利培酮（约 4 倍）、氟西汀对三环类（2–10 倍，效应持续 3 周以上）、安非他酮对地昔帕明（AUC 约 5 倍，末次给药后 7 天仍存在）、氟伏沙明对替扎尼定（Cmax 约 12 倍）与雷美替胺（AUC 约 190 倍）、西酞普兰合用 CYP2C19 抑制剂（AUC +43%，剂量帽 20 mg/日）等配对数据，说明倍数由底物比例、抑制强度、基因型与时程共同决定，不能跨底物外推。6 份主条目 §11 已加入链接，专题总数 26→27，索引同步。

**结构与格式清理（2026-11-11）**：对 384 份主档案做一次完整结构检查。修正 doxefazepam 中国管制行多出的空单元格；为 benzgalantamine 与 cariprazine 补上缺失的目录页脚；78 份档案在专题链接与目录页脚之间补空行；13 份档案清理多余空行。结构检查其余项全通过（标题、状态行、11 个章节、表格列数），语言指标与状态计数不变。

**专题新增（2026-11-11，第十三篇）与数字核对**：新建 [analysis/sexual-dysfunction-incidence-and-persistence.md](../analysis/sexual-dysfunction-incidence-and-persistence.md)，并列帕罗西汀（男性射精异常 13%–28% 对 0%–2%）、舍曲林（8% 对 1%）、西酞普兰（6% 对 1%）与艾司西酞普兰的标签比率，说明"停药后持续"的美英分歧（舍曲林四份美国标签均无该表述、英国有）与测量口径差异（西酞普兰标签自认低估、艾司西酞普兰无充分设计研究）。8 份主条目 §11 已加入链接，专题总数 27→28。另对本批 12 份专题的带单位数字逐一回查配套主条目，未发现不可追溯数字，仅 2 处因分隔符排版造成的假阳性（37 ms、46.6 ms）。

**专题新增（2026-11-11，第十四篇）**：新建 [analysis/nms-vs-serotonin-syndrome-label-boundaries.md](../analysis/nms-vs-serotonin-syndrome-label-boundaries.md)，按触发药物类别分开 NMS（多巴胺阻断与撤药，标签含 CK 升高、横纹肌溶解与急性肾衰）与 5-羟色胺综合征（血清素能联用，吗氯贝胺标签列出意识模糊、发热、惊厥、共济失调、反射亢进、肌阵挛与腹泻），说明两张症状清单有重叠但标签不是诊断标准，不能合并成"血清素毒性"类别。9 份主条目 §11 已加入链接，专题总数 28→29，索引同步。

**专题新增（2026-11-11，第十五篇）**：新建 [analysis/falls-fractures-mechanisms-and-label-layers.md](../analysis/falls-fractures-mechanisms-and-label-layers.md)，把跌倒与骨折的关联按镇静、肌松、体位性低血压、抗胆碱能、前庭抑制与低钠分组，并列唑吡坦标签 1.5% 跌倒率（93% 为 70 岁以上）、Z 药骨折 OR 1.63（I²=90%）、美克洛嗪三项队列方向、SSRI 与三环类类级流行病学，说明四层证据不能相加，并记录利培酮专条与米氮平美英文本差异。8 份主条目 §11 已加入链接，专题总数 29→30，索引同步。

**ATC/DDD 官方索引复核（2026-11-11，CDP）**：对 384 份档案中的 369 个唯一 ATC 编码逐码回读 WHO ATC/DDD Index 页面。369 个编码全部找到对应条目；可解析的 DDD 数值与"未列 DDD"声明逐一比对，25 处初筛差异经人工回读均为解析假阳性（多行给药途径、相邻药物 DDD、研究剂量），未修改任何档案数值。方法与结果写入 [catalog/retrieval-log-2026-11.md](../catalog/retrieval-log-2026-11.md) 第 6 节。

**审计后补录（2026-11-11 晚间）**：132 份 basic 的 CDE／NMPA／PMDA 检索记录补入 §10，均为检索事实与原库链接，未改动既有数字、剂量、日期与证据边界。按同一扫描口径复核：破折号 9、正文分号 3、一句多冒号 3、防御性表述链 19 与审计结束持平；3 项以上并列 1566→1579（增量来自新增检索记录的并列清单，按 §7 数据与编号清单从宽），4 项以上 149 不变；表格单元格分号 3248 不变；399 份 0 BOM、0 NUL、0 控制字符，相对链接 0 处断开；状态 reviewed 245／basic 132／indexed 7。PMDA 检索覆盖 76 份 basic 档案（按 Wikidata 日文名与线索名检索），命中现行添付文書者 4 份（ブロチゾラム 17、エチゾラム 14、クロキサゾラム 1、ペモリン 1），バルビタール 10 件与アリルイソプロピルアセチル尿素 1 件经核对为子串／配合剂命中，不作单方条目认定。

**审计自身的回退与修复**：批次 3 一度把顿号批量改成逗号以压低并列计数（顿号 −525），已按快照全部回退（顿号恢复至快照水平、5 处监管引文逐字恢复），并列指标如实保留 >0；撤销把句子拆成半句列表的机械列表化，新增「列表项后紧跟散文」断句 0 处；重复免责声明 306 处合并为单次表述；修复 4 处引用键损坏（brexanolone `N06AX29`、buprenorphine `N02AE`、diamorphine `N02AA01`、remternetug `term` 曾被控制字符加数字替换）、diamorphine 来源清单与缺口段被拆散的恢复、sertraline 与 hydroxyzine 两处内容丢失的恢复。保留全部数字、剂量、日期、编码、setid/PL/CIS、PMID/DOI、URL、表格行数、章节编号、状态行与证据边界。终检：399 份文档 0 BOM、0 NUL、0 控制字符、末尾换行齐全；384 份状态 reviewed 245／basic 132／indexed 7；相对链接 0 处断开。

**执行方式**：8 个升级子代理、多个审计/改写子代理并行，批次文件互不重叠；主代理负责共享文件、统计、标题与状态行收尾及最终验收。子代理未提交、未推送、未合并 `main`。

**仍开放**：NMPA 的 412 与 CDE 的 202 仍不可脚本检索，132 份 `basic` 的中国上市与核准适应证继续按待核实记录；部分历史药物（terodiline、emepronium、obidoxime 等）在任何检索法域均无现行产品文本；德国、意大利、丹麦等官方入口仍不可达。本轮未新增专题、未扩写计划外药物。

## Wave 15：50 条跨组神经精神与神经药物建档（2026-11-05）

**分支**：`plan/neuropsych-crossgroup-wave15`。基于 Wave 14 审阅修补合并后的 `main`，基线 `91702d126c2981d55e7e8de08946b9af3e41e553`。

**目标**：一次推进 50 个跨组候选。以主药物档案为交付主体，按证据实际情况定为 `reviewed`、`basic` 或 `indexed`，不预设升级数量。允许五个互不重叠的子代理并行完成五组；不拆成多轮人工审批，不为每个药物预建专题。

### 候选清单

A. 下尿路药物与抗胆碱负担（13）
`emepronium`、`flavoxate`、`oxybutynin`、`terodiline`、`propiverine`、`tolterodine`、`solifenacin`、`trospium`、`darifenacin`、`fesoterodine`、`imidafenacin`、`mirabegron`、`vibegron`

B. 前庭与眩晕治疗（7）
`betahistine`、`cinnarizine`、`flunarizine`、`acetylleucine`、`meclizine`、`dimenhydrinate`、`cinnarizine-and-dimenhydrinate`

C. 急性中毒与解毒药（10）
`pralidoxime`、`sodium-thiosulfate`、`sodium-nitrite`、`dimercaprol`、`obidoxime`、`naloxone`、`physostigmine`、`acetylcysteine`、`flumazenil`、`fomepizole`

D. 帕金森病与多巴胺能药物（10）
`trihexyphenidyl`、`biperiden`、`levodopa`、`amantadine`、`bromocriptine`、`ropinirole`、`pramipexole`、`selegiline`、`rasagiline`、`safinamide`

E. 神经退行性、运动与神经肌肉疾病药物（10）
`riluzole`、`sodium-oxybate`、`amifampridine`、`tetrabenazine`、`fampridine`、`pitolisant`、`valbenazine`、`edaravone`、`deutetrabenazine`、`trofinetide`

### 候选实体边界

- 初筛中的 `meladrazine` 不纳入本轮候选：FDA Substance Registration System 将该名称映射至 hydramitrazine，和本轮选定的下尿路／前庭主题不匹配（[FDA UNII](https://precision.fda.gov/uniisearch/srs/unii/2V6Z0JG2X0)）。
- 初筛中的 `desfesoterodine` 不单独建档：PubChem 将其描述为 tolterodine 的代谢物，本轮不把代谢物重复计作独立上市药物（[PubChem](https://pubchem.ncbi.nlm.nih.gov/compound/9819382)）。
- 以上两项由 `meclizine` 与 `dimenhydrinate` 替换。两者用于前庭症状／晕动病相关场景，但 WHO ATC 归入 R06A 抗组胺药组，不得为贴合 N07CA 而错误分类；具体产品与现行文本仍须逐项核验（[WHO ATC R06AA](https://atcddd.fhi.no/atc_ddd_index/?code=R06AA)、[DailyMed meclizine](https://www.dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=598eb392-1dfe-c08c-e063-6394a90a4c7d)）。
### 执行分工

1. **Agent A**：A 组 13 条；**Agent B**：B 组 7 条；**Agent C**：C 组 10 条；**Agent D**：D 组 10 条；**Agent E**：E 组 10 条。每个子代理只处理分配给自己的 `drugs/<slug>.md`，不得编辑共享文件，不得嵌套派生子代理。
2. 主代理负责核对身份与重复项、处理跨组目录 `catalog/related.md`、更新 `catalog/index.md`、`README.md`、`PLAN.md` 与必要的 `AGENTS.md`，并统一检查引用、链接、状态与文件数量。
3. 如发现候选实际为别名、代谢物、未指明成分的类别码或已存在实体，不得创建重复档案。按同一主题替换为一个有明确实体身份的候选，维持 50 个独立候选；在执行记录中简要说明替换原因。

### 必须遵守的核查要求

- **身份与分类**：逐项确认 INN／通用名、盐型、立体异构体、代谢物、研发代号与产品边界；以 WHO ATC/DDD Index 2026 核对官方 ATC 编码与名称。没有适用 ATC 编码时如实说明，不得猜码。`meclizine` 与 `dimenhydrinate` 按各自 R06A 分类记录，不得为凑主题改列 N07CA。`cinnarizine-and-dimenhydrinate` 必须按具体固定复方及完整成分建档，不建立抽象的“cinnarizine combinations”类别档案。
- **A 组**：区分 antimuscarinic 与 β3-adrenoceptor agonist。重点核对中枢穿透、抗胆碱负担、认知结局、老年人跌倒／谵妄风险、尿潴留及心血管风险；不得假定所有膀胱药都具有相同中枢作用。`terodiline` 等历史药物须区分正式撤市／撤销决定、持证人停销与当前供应状态。
- **B 组**：区分 vertigo、motion sickness、Ménière’s disease 等具体场景及急性症状控制与长期治疗。对抗组胺药和抗胆碱药核对镇静、认知、跌倒与 vestibular compensation；不要把不同前庭疾病或不同药物的证据合并。
- **C 组**：按中毒物质、毒理机制、适用时窗、给药途径与具体解毒方案分别核查。急诊解毒用途与长期或精神科超适应证研究分开记录；不得将一种中毒的解毒证据外推到另一种中毒。没有合理的长期用药场景时，不为 A–D 表制造占位行。
- **D 组**：区分 Parkinson’s disease 的运动症状治疗、其他批准用途与超适应证精神科使用。重点核对 impulse-control disorders、幻觉／精神病性症状、冲动行为、嗜睡／睡眠发作、运动并发症与停药风险；不得从多巴胺机制推导抗抑郁或抗精神病疗效。
- **E 组**：分别处理 ALS、narcolepsy、Lambert–Eaton myasthenic syndrome、multiple sclerosis、hyperkinetic movement disorders 与 Rett syndrome。严格区分疾病、产品、盐型与治疗目标；`amifampridine` 与 `fampridine`、`tetrabenazine` 与 `deutetrabenazine`／`valbenazine` 不得互相继承适应证或剂量。
- **监管状态**：按“法域＋具体产品＋剂型＋文本版本”核查现行标签与历史决定。数据库零命中只写检索事实，不推断“从未获批／从未上市”；批准、撤销、持证人停销和商业供应分别记录。
- **中国管制**：50 条逐项复核四份现行目录及 2026-07-01 生效的 16 种非药用类增列附表。名称未命中不自动排除整类列管；结构定义、盐型、异构体和例外按官方原文判断。不得仅沿用既有条目的阴性结果。
- **临床证据与评分**：适应证按法域分列；A–D 只评有临床决策价值的真实使用场景。证据不足写 `N/A`／“待核实”，不强行评分；没有合理使用场景的历史候选或失败项目不设占位行。风险评分与疗效场景评分不得合并为总分。
- **药物利用与专题**：仅在存在可靠且与该药相关的数据时纳入，注明地区、年份、人群与分母；不为每个条目强制搜集滥用率或处方量。只有满足 `AGENTS.md` 既有问题导向标准时才新增专题，不设专题配额。

### 交付与验收

- 50 个候选均完成实体核对并建立独立档案；如发生替换，执行记录列明原候选、替代项与理由。
- 更新 `catalog/related.md`：复用已有的 emepronium、trospium、naloxone、physostigmine、flumazenil 待建档行，不重复插入；其余核实后的实体按官方 ATC 位置补入。固定复方必须对应具体产品。更新各组分布与已建档状态。
- 更新 `catalog/index.md` 的跨组档案数量、状态统计与 Wave 15 执行记录；核心六组统计不因跨组扩展而改变。
- 更新 `README.md` 当前计划与基线统计；在本节末尾记录实际建档数、`reviewed/basic/indexed` 数量、替换项、未解决缺口及是否新增专题。
- 仅做必要的 Markdown、链接、重复档案与数量核对；不新增 CI、数据库、爬虫、自动评分器、空白模板或其他基础设施。完成后提交并推送本分支，等待人工审阅，不自行合并 `main`。

## Wave 15 完成记录（2026-11-06）

**实际建档数**：50 条候选全部完成实体核对并各自建立独立档案，仓库总数由 334 份增至 384 份（跨组主题档案 54 → 104，核心六组 280 份不变）。

**状态分布**：**40 份 `reviewed`、10 份 `basic`、0 份 `indexed`**，未强制升级。
- `basic` 的 10 份及原因：`emepronium`、`terodiline`、`propiverine`、`imidafenacin`、`biperiden`、`obidoxime`、`physostigmine`、`acetylleucine`、`flunarizine`、`cinnarizine-and-dimenhydrinate` —— 共同原因是本轮未取得任何法域的现行监管说明书正文（DailyMed／emc／BDPM 检索为 0 条或站点拦截），"给药方案"与"核准适应证"两项核心模块无法绑定法域＋产品＋文本版本；`cinnarizine-and-dimenhydrinate` 另因具体产品的现行监管文本仅取得转载口径。
- `reviewed` 的 40 份均至少有一份可逐节引用的现行正文（美国 DailyMed SPL／英国 emc SmPC／欧盟 EPAR 之一）或等效一手监管文本，且中国管制字段逐项核查完成。

**替换项**：
1. `meladrazine` → 不纳入。FDA Substance Registration System 将该名称映射至 hydramitrazine，与本轮下尿路／前庭主题不符；官方 ATC `G04BD03` 条目保留为分类事实记录，不建档。
2. `desfesoterodine` → 不单独建档。官方与 PubChem 口径均为 tolterodine 的活性代谢物，官方 `G04BD13`（DDD 3.5 mg）保留为分类记录。
3. 替换为 `meclizine` 与 `dimenhydrinate`。两者用于晕动病／前庭症状场景，但 WHO ATC 分别归 `R06AE05`（官方条目名 meclozine）与 `R06AA11`，档案按官方编码记录，未为贴合 N07CA 主题改写分类。

**候选实体边界的处理**：
- `acetylleucine` 与官方 `N07XX27` levacetylleucine 为不同实体，聚合库曾把两者混映射，档案按 WHO 官方行分别记录。
- `cinnarizine-and-dimenhydrinate` 按具体固定复方（Cizinate 20/40 mg）建档，未建立抽象的 "cinnarizine combinations" 类别档案；官方 `N07CA52` 与 `R06AA61` 两个复方类别在目录中标为类别记录。
- `levodopa` 档案只评价该分子本身：现行美国单方产品为吸入制剂，持续的口服替代治疗由含脱羧酶抑制剂的固定复方承载，复方的批准与方案不计入单方评分；`safinamide` 同理按标签口径限定为左旋多巴／卡比多巴背景上的添加治疗。
- `amifampridine`／`fampridine`、`tetrabenazine`／`deutetrabenazine`／`valbenazine` 三者适应证、剂量与禁忌互不继承。
- `terodiline` 与 `emepronium` 等历史药物只记录检索缺口，未写成"已撤市／从未获批"。

**目录与统计更新**：`catalog/related.md` 复用 5 条既有待建档行（emepronium、trospium、naloxone、physostigmine、flumazenil），另按官方 ATC 位置插入 45 行，选录总数 46 → 91，已建档 39 → 89，未建档 2（`N07BC51` 复方类别、`N06DA53` 暂不建档）；分布表补入 G04BD、N04AA/BA/BB/BC/BD、N07CA、N07XX、R06AA/AE、V03AB 各亚组计数。`catalog/index.md` 与 `README.md` 的基线改为 218 reviewed / 7 indexed / 159 basic。

**中国管制**：50 条逐项复核 2025 年版麻醉药品目录（32 项）、2025 年版精神药品目录（第一类 18 项＋第二类 78 项）、2026 年第 58 号增列 3 项、2025 年版非药用类目录（396 项）及 2026-07-01 生效的 16 种非药用类增列附表。唯一逐项命中为 `sodium oxybate`——归第一类精神药品第 6 项 γ-羟丁酸，并按目录总注 1（盐与单方制剂）处理钠盐归属；`naloxone` 仅在第二类第 74 项"丁丙诺啡和纳洛酮复方口服固体制剂"中以复方形式出现，不构成单方列管。四类整类范围按公告列举的母体名称逐字判读，未以药理族属或骨架名称推定。

**未解决的共同缺口**：
1. 中国 NMPA 对本机恒返回 HTTP 412、CDE 目录接口返回 202 校验页，50 份档案的中国上市与核准适应证全部标注待核实；未使用商业药品库补足。
2. 英国 emc 的脚本端检索在本轮多数请求中返回 429／反爬页，现行正文仅按已验证的产品编号读取；欧盟、日本、韩国、澳大利亚等法域未逐国核对。
3. PubMed 与 Europe PMC 在部分时段返回 500／503，个别档案的研究性用途只保留检索事实与题名级引用，未抽取数值。
4. `trofinetide` 的审批路径（是否加速批准及确认性试验状态）未取得可核验的监管决定原文，DailyMed 正文无该字段、Drugs@FDA 提交事项为空，档案写为待核实。

**专题与基础设施**：本轮未新增 `analysis/` 专题（仍为 15 份），分歧均可在主条目 §2.2、§5 与 §10 就近并列；未新增数据库、CI、爬虫、自动评分器或空白模板。

**执行方式的如实记录**：五个子代理按 A–E 分组并行，其中两组在长时间无响应后被中止，未完成的部分由主线程按同一核查标准补写并统一复核；中途一次主线程简报对 `trofinetide` 黑框提示有误，经与现行标签逐字比对后更正（该标签 §4 禁忌为 None，无黑框，腹泻／体重下降／呕吐载于 §5.1–§5.3）。

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

**仍开放缺口**：35 份中国注册待核实；英国 emc、德／意／瑞士／比利时／日本官方库多数未取回；`gedocarnil` 无任何本药特异文献（四个研发代号检索亦 0 命中）；`etallobarbital` 同样零文献；`pirisudanol` 两份老年抑郁实践报告只到题录、未取得原文；`scopolamine` 与 `valerianae-radix` 已取得本轮用于升级的产品文本；其他法域或剂型的产品文本仍待补。本轮未重写 Wave 1–9、未扩写计划外档案、未新增专题；审阅修补与合并状态以 [PR #13](https://github.com/Adrerie/psychopharm-atlas/pull/13) 为准。

## Wave 11 焦虑障碍相关药物覆盖扩展计划（2026-10-28）

**目标与基线**：本轮从“清理既有 indexed 档案”转向按临床问题补全跨组覆盖。当前主分支基线为 **280 份核心 ATC 组档案，149 reviewed / 4 indexed / 127 basic**，另有 15 份专题；`catalog/related.md` 有 42 个尚未建档的跨组选录。本轮只处理以下 7 份档案，不把它扩展成通用焦虑治疗指南，也不假定所列药物在所有法域均获批用于焦虑。

### 本轮清单

**新建 4 份跨组档案**：
- `pregabalin`（普瑞巴林，ATC `N03AX16`）：重点核对部分法域的广泛性焦虑障碍适应证及其与癫痫、神经病理性疼痛用途的边界。
- `clonazepam`（氯硝西泮，ATC `N03AE01`）：区分部分法域的惊恐障碍适应证与其他法域的癫痫用途，并核实管制等级、依赖和停药风险。
- `gabapentin`（加巴喷丁，ATC `N03AX12`）：焦虑用途按超适应证证据核对，不能从神经病理性疼痛或癫痫标签推导焦虑适应证。
- `propranolol`（普萘洛尔，ATC `C07AA05`）：只重点处理表现焦虑／情境性焦虑的证据与实际使用边界，不将其描述为广泛性焦虑障碍的常规治疗。

**补证 3 份既有 `basic` 档案**：
- `opipramol`（`N06AA05`）：重点寻找德国、波兰等相关法域的现行官方产品文本。
- `tofisopam`（`N05BA23`）：重点寻找匈牙利等实际使用法域的官方产品文本。
- `fabomotizole`（`N05BX04`）：重点核对俄罗斯官方注册与说明书来源。

`lavandulae-aetheroleum` 已为 `reviewed`，本轮不返工。不得因主题相关性把其他已处理档案重新纳入。

### 一次执行要求

1. 主代理阅读 `AGENTS.md`、`SCORING.md`、`SOURCES.md`、`METHODOLOGY.md`、`DISCLAIMER.md` 与喹硫平样板。允许 **2 个非嵌套子代理**一次并行执行：A 组新建 4 份档案，B 组补证 3 份既有档案。子代理只编辑分配的药物文件；主代理负责跨组索引、共享文件、实体与状态复核。无需中途审批或额外分阶段计划。
2. 新建档案先核对官方 ATC、药物实体、盐型与制剂，尤其确认跨组条目未与现有药物或固定复方重复。中国管制字段按现行官方目录核查。新条目放入 `catalog/related.md`，不将 N03／C07 药物误并入核心 N05／N06 子目录。
3. 对所有药物按具体产品、法域、剂型和文本版本核对现行标签。优先官方说明书与监管决定，其次指南、高质量系统综述及药物特异原始研究。分别记录批准适应证与超适应证证据，写清人群、比较组、终点和随访；没有证据就记录缺口。
4. `pregabalin` 的焦虑适应证按法域逐项核实；`clonazepam` 的惊恐障碍与癫痫用途分开；`propranolol` 限于表现／情境性焦虑的具体证据；`gabapentin` 不得把有限或混合的超适应证研究写成已核准用途。不得将某一地区的标签外推为全球批准。
5. `opipramol`、`tofisopam`、`fabomotizole` 优先补取相关法域的官方注册与说明书正文。官方入口不可用时，记录实际检索缺口；不得把二手数据库、历史论文或其他国家标签伪装成现行官方文本。
6. 维持当前状态门槛：`reviewed` 必须满足仓库定义，并有足以支撑监管结论的可核来源；Wave 9／10 使用的说明书审阅门槛继续适用。没有完整现行产品正文时，不得仅凭章节齐全或研究数量将条目升为 `reviewed`。A–D 只保留有本药特异证据且有当前临床决策价值的场景；负担维度证据不足写 `N/A`。不强求任何固定的升级数量。
7. 不为凑齐数量新增专题。只有出现重要证据冲突、独立临床问题或主条目无法简洁解释的结论时，才新增问题导向专题。
8. 完成后更新 `catalog/related.md`，加入 4 个新跨组条目并调整分组计数；更新 `catalog/index.md`，明确区分核心六组 280 份与跨组主题档案，并按全部实际药物文件重算状态数；同步更新 `README.md` 和本计划的完成记录。核心 294 个 ATC 编码及核心 280 份档案的统计口径不变，跨组档案单独统计。核对本轮文件的相对链接、官方来源和状态字段，提交并推送 `plan/anxiety-coverage-wave11`，**等待审阅，不合并 `main`**。

**不做**：不重新审阅全部 280 份核心档案；不重做已为 `reviewed` 的薰衣草油；不将表现焦虑等具体用途泛化成所有焦虑障碍；不强制升级状态；不新增数据库、爬虫、CI、自动评分器或专题配额。

## Wave 11 完成记录（2026-10-28）

**状态**：7 份全部处理完毕——新建 4 份跨组档案均 `reviewed`（加巴喷丁、普瑞巴林、氯硝西泮、普萘洛尔），补证 3 份为 `opipramol` 保持 `reviewed`、`tofisopam` 维持 `basic`、`fabomotizole` 维持 `basic`。仓库合计 **154 reviewed / 4 indexed / 126 basic**，共 **284 份档案**（核心六组 280 份：150 reviewed／4 indexed／126 basic；跨组主题 4 份全部 reviewed），`analysis/` 仍 15 份。

**分类校正**：计划所列 `N03AX16`（普瑞巴林）与 `N03AX12`（加巴喷丁）是改版前旧码。WHO 2026 的 `N03AX` 亚组页原文明写 "Gabapentin and pregabalin are classified in N02BF Gabapentinoids"，两份档案按现行码 `N02BF02`（DDD 0.3 g O）与 `N02BF01`（DDD 1.8 g O）归类，并把旧码写作归属变更史；`clonazepam` `N03AE01`（DDD 8 mg O、8 mg P）与 `propranolol` `C07AA05`（DDD 0.16 g O、0.16 g P）与计划一致。`catalog/related.md` 相应新增 4 行、加入 `N02BF`／`N03AE`／`C07AA` 三行分布计数（42→46），并改写原先"两个亚组页面未出现加巴喷丁与普瑞巴林"的待核实备注。

**主要来源**：美国 openFDA／DailyMed 现行标签逐节引用（普瑞巴林胶囊 2 份、加巴喷丁 3 份、氯硝西泮片 3 份含黑框、普萘洛尔片 4 份与缓释胶囊 1 份）；波兰官方注册库 ChPL（Pramolan 50 mg，记录 ID 5470，许可号 R/2058；制造商页列 2019-06 版）与德国 2022 年版 Fachinformation（opipramol，现行性未确认）；匈牙利 OGYÉI 药品数据记录（GRANDAXIN 50 mg，OGYI-T-3475/01，正文核对日 2024-04-10）与日本添付文書引用条目（tofisopam）；WHO ATC/DDD Index 2026 逐码回查；DEA《Alphabetic Order of Controlled Substances》（pregabalin 2782；gabapentin 与 propranolol 按名未命中，与标签"Not a scheduled drug"及 §9 无受控条目一致）；中国 2025 年第 55 号公告目录附件与 2026 年第 58 号增列按官方 `.doc`／`.docx` 附件字节级检索。

**中国管制结论**：氯硝西泮**命中**《药用类精神药品目录（2025年版）》第二类第 17 项（CAS 1622-61-3）；普瑞巴林、加巴喷丁、普萘洛尔在两份目录中**按中文名与英文名均未命中**，四类整类结构定义不适用；非药用类 396 项原始附件返回 HTTP 521，各档案均写明"未逐名核对"，不作整体排除。方法回测：地西泮解析为第二类第 24 项，与仓库 `diazepam` 档案一致。

**整合与验收（主代理）**：① 我此前对 `reposal`／商品名类错误保持警惕，本轮把 gabapentin 与 pregabalin 的 α2δ 同类关系写成"位点相同但分子不同、剂量效力不互换"；② 氯硝西泮标签原文的"疗程中疗效可减弱"与惊恐障碍条目分别落到 §INDICATIONS 与 §5，网络荟萃（`PMID:38014714`）标为间接比较，故该场景 C+ 而非 B；③ 普萘洛尔四份美国正文均无焦虑适应证，表现焦虑按超适应证处理并只用本药特异小样本研究支撑，非医嘱使用（`PMID:41787430` 横断面自报）留在 §7 不作滥用率；④ 我自己写的两份档案最初把"不设行"当作 A–D 等级填入表格，已改为表后说明段；⑤ `tofisopam` 与 `fabomotizole` 的官方入口仍未完整取回（OGYÉI 全域 TLS 中断；ГРЛС 检索页只返回跳转壳），两者均维持 `basic`；`tofisopam` 已压至去空白 15,171 字符，低于 15,174 上限。`opipramol` 的波兰官方注册记录与 ChPL 已由网页端复核，许可号校正为 R/2058；第 10 项修订日期为空白，制造商页列 2019-06 版，德国 2022 年文本的现行性仍未确认，故德国文本只作补充比较来源。

**仍开放缺口**：普萘洛尔与普瑞巴林的**欧盟／英国／澳大利亚现行正文未取回**，故 GAD 与血管性用途的跨法域批准状态未定；婴儿血管瘤用普萘洛尔口服溶液为单独产品，本轮未取正文；`fabomotizole` 的 ГРЛС 注册号与说明书全文未取得；`tofisopam` 匈牙利正文仍待独立复核；其档案已精简至去空白 15,171 字符，符合 15,174 上限；`opipramol` 德国 2022 年文本的后续更新状态仍未确认，波兰 ChPL 第 10 项修订日期为空白；7 份档案的中国上市与核准适应证仍待核实；本轮未重写 Wave 1–10、未扩写计划外档案、未新增专题；Wave 11 的合并状态以 Git 历史为准。

## Wave 12 跨组情绪稳定剂相关抗癫痫药建档计划（2026-10-28）

**状态：已完成（见文末“Wave 12 完成记录”）。** 六份全部建立，均为 `reviewed`；本轮未合并 `main`。

**目标与基线**：沿用 Wave 11 的跨组建档方式，从 `catalog/related.md` 现有选录中完成一组精神科相关抗癫痫药。当前 `main` 有 **284 份药物档案**（154 reviewed / 4 indexed / 126 basic），其中核心六组 280 份、跨组主题 4 份；`catalog/related.md` 共 46 条选录，4 条已建档、42 条待建档。本轮只新建以下 6 份跨组档案，核心六组 280 份统计不变。

### 本轮清单

- **A 组，羧酰胺衍生物**：`carbamazepine`（N03AF01）、`oxcarbazepine`（N03AF02）、`eslicarbazepine`（N03AF04）。
- **B 组，脂肪酸衍生物及其他抗癫痫药**：`valproic-acid`（N03AG01）、`valpromide`（N03AG02）、`lamotrigine`（N03AX09）。

六种药物均已存在于跨组选录，不新增重复条目。完成后将 `related.md` 的已建档数由 4 更新为 10、待建档数由 42 更新为 36。若六份新档案全部建立，`drugs/` 总数应为 290，其中核心六组 280 份、跨组主题 10 份。状态统计必须根据最终文件顶部的真实状态重算，不预设六份均为 reviewed。

### 一次执行要求

1. 一次完成六份新档案，不拆成逐组审批阶段。主代理先阅读 `AGENTS.md`、`SOURCES.md`、`METHODOLOGY.md`、`SCORING.md`、`DISCLAIMER.md` 与喹硫平样板。允许两个非嵌套子代理并行，各处理 A 或 B 组的三份药物文件。子代理不得编辑共享文件；主代理负责实体核对、交叉矛盾修复、目录与状态整合。
2. 每份先核实 WHO ATC/DDD Index 2026 的身份与编码，再按具体产品、法域、剂型和版本核对官方标签或说明书。优先使用 FDA/DailyMed、英国 emc、法国 BDPM、EMA 及相关国家监管机构。记录能确认的法域与版本，不要求每种药覆盖所有国家。数据库零命中、接口失败或只取得历史文本均写成具体证据缺口，不推断为未批准或已撤市。
3. **严格区分癫痫与精神科用途**。卡马西平分别核对癫痫和双相障碍相关批准用途及维持治疗证据；奥卡西平的精神科用途必须按其自身证据标注，不能继承卡马西平结论；艾司利卡西平不得仅凭同属羧酰胺类推断情绪稳定疗效。丙戊酸、丙戊酸钠、双丙戊酸等盐型与具体制剂按各自标签记录；`valpromide` 是独立实体，不继承丙戊酸的批准状态或疗效结论。拉莫三嗪必须区分双相障碍维持治疗与急性发作治疗的证据和标签范围。
4. 重点核对能改变临床判断的风险：卡马西平的严重皮肤反应、血液学风险与酶诱导相互作用；奥卡西平的低钠血症与皮肤／超敏反应；艾司利卡西平的低钠血症、神经系统不良反应与相互作用；丙戊酸类的生殖毒性、肝毒性、胰腺炎及高氨血症；拉莫三嗪的严重皮疹、滴定要求与丙戊酸等相互作用。具体表述以匹配的现行产品标签为准，不将类效应冒充每一产品的标签原文。
5. 中国管制字段按现行官方目录逐药核对；中国上市与核准适应证只有在可靠官方来源可核实时才写为已确认。不要重做全库管制审计，也不要用商业数据库填补 NMPA/CDE 官方入口缺口。
6. 严格沿用既有评分规则。A–D 只保留有本药特异证据且具有当前临床决策价值的场景。未获批本身、缺少证据、特殊人群、相互作用或禁忌不得单独构成评分行。证据不足时写 `N/A` 或“待核实”，不得为完成批次强行升级状态。只有满足 `AGENTS.md` 的全部状态门槛时才标为 `reviewed`。
7. 不设专题配额。只有发现重要证据冲突或一个无法在主条目内简洁解释、且确有独立决策价值的问题时，才新增问题导向专题。主条目保持快速判断导向，完整剂量方案与次要试验细节留在原始来源或必要的正文段落。
8. 完成后更新六份条目、`catalog/related.md`、`catalog/index.md`、`README.md`、`PLAN.md`，并按需要对 `AGENTS.md` 做最小修订。目录只把现有六条状态改为已建档，不增加重复条目；跨组选录总数仍为 46。重新计算总档案数、核心／跨组数量及 reviewed/indexed/basic 计数。检查本轮改动文件的来源、相对链接、表格和状态字段，提交并推送本分支，交由审阅，不自行合并 `main`。

**不做**：不重审既有 284 份档案；不把六种药物强行升为 reviewed；不重做中国全库管制审计；不新增数据库、爬虫、CI、自动评分器或多阶段审批；不扩写清单外药物；不为每种药物新增专题。

## Wave 12 完成记录（2026-10-28）

**状态与计数**：六份全部建立且均为 `reviewed`；`drugs/` 共 290 份（核心六组 280 份＋跨组主题 10 份），按各档案顶部状态字段汇总为 **160 reviewed / 4 indexed / 126 basic**；`analysis/` 仍 15 份，本轮未新增专题。`catalog/related.md` 只把原有六条状态改为已建档，选录总数仍 46（已建档 10、待建档 36）。

**执行方式**：两个非嵌套子代理并行（A 组羧酰胺三份、B 组丙戊酸系与拉莫三嗪三份）。两组各出现一次中断，由主代理按原分工接管补齐；共享文件、事实复算与提交由主代理完成。

**主要锚点**：美国 DailyMed 具体 setid＋生效日——卡马西平片 `047bc284…`（生效 2025-02-18，文内 Revised January 2024, V-08）、奥卡西平口服混悬液 `03bec567…`（生效 2024-11-18；另核普通片 `8841174a…` 与缓释片 `21caded0…`，两份均为 2026 年新提交、openFDA 尚未收录）、艾司利卡西平醋酸盐片 `190fccbc…`（生效 2025-01-30；另核原研 APTIOM `3d0c9554…`）、丙戊酸口服溶液 `1286ab49…`（生效 2024-05-27；另核胶囊 `7d4df6ad…` 与 divalproex／丙戊酸钠注射剂作为对照实体）、拉莫三嗪口崩片 `003663e5…`（生效 2026-04-22；另核 LAMICTAL `d7e3572d…` 与 LAMICTAL XR `3e2c9a35…`）。法国公开药物数据库——TRILEPTAL 600 mg（CIS 64876757，ANSM 标注 2026-02-16）、ESLICARBAZEPINE ARROW 800 mg（CIS 63927729，§10 字段 2022-12-28）、DEPAMIDE 300 mg（CIS 63737879，2025-10-30）。英国 emc——Tegretol 100 mg 片 SmPC（产品 1040，PL 00101/0461，§10 修订 2026-04-20）。WHO ATC/DDD Index 2026 逐码回查：`N03AF01` 1 g 口服／直肠、`N03AF02` 1 g 口服、`N03AF04` 0.8 g 口服、`N03AG01` 1.5 g 口服／胃肠外／直肠、`N03AG02` 1.5 g 口服、`N03AX09` 0.3 g 口服；`N03A` 亚组页原文注明本组 DDD 基于联合治疗口径。

**实体与用途分离结论**：卡马西平美国普通片标签收载癫痫与三叉神经痛，独立产品 EQUETRO 缓释胶囊另批准成人 Bipolar I disorder 急性躁狂或混合发作；英国与法国文本各自收载其他心境用途；奥卡西平与艾司利卡西平在所引美法正文中均无精神科与疼痛适应证，其双相与神经病理性疼痛的随机证据为阴性或效力不足，按 SCORING 记为 C−／D 而不写成获批用途；丙戊酸实体的两份美国正文 §INDICATIONS 只有癫痫，急性躁狂与偏头痛预防属 divalproex sodium 产品的批准，且所引丙戊酸溶液 §6.2 原文明写该实体未就躁狂评价过安全性与疗效；丙戊酰胺按法国独立正文建档，唯一适应证为成人躁狂发作（限锂禁忌或不耐受），§4.1 第二句“发作后可考虑续用”是续用条款而非维持治疗适应证，癫痫未被该正文收载；拉莫三嗪双相只写 I 型维持治疗，标签 Limitations of Use 原文不推荐用于急性躁狂或混合发作，LAMICTAL XR 正文则完全没有精神科条目。

**中国维度**：六份按 2025 年第 55 号公告两份目录附件与 2026 年第 58 号增列逐名检索均未命中（同一方法把地西泮解析为第二类第 24 项作方法回测）；非药用类 2025 年版目录原始附件对本机返回 HTTP 521，未逐名核对，故不写整体排除；NMPA 412／CDE 202 仍不可脚本访问，六份的中国上市与核准适应证一律写“待核实”。美国 DEA 字母清单按名检索对六名均未收录。

**整合修正**：艾司利卡西平档案不使用未能验证的研发代号 SR-12948，代谢通路改由标签 §12.3 的暴露构成（eslicarbazepine 91%、(R)-licarbazepine 5%、oxcarbazepine 1%）与 `PMID:25489632` 支撑；奥卡西平的卡马西平交叉超敏率统一为标签原文的 25%–30%；丙戊酰胺的不良反应频次按法语原文 Très fréquent／Fréquent／Peu fréquent 校正（“出血事件”改为正文的贫血与血小板减少），并补入 §4.4 的抗癫痫药类别自杀警示；拉莫三嗪与丙戊酸的相互作用按方向分列，并写明标签对本药影响丙戊酸浓度的结论相互矛盾（健康志愿者平均降 25%、癫痫患者试验无变化）；六份的说明书引用一律改为具体 setid／CIS 页面＋生效或更新日期，不再以检索 URL 充当批准依据（丙戊酰胺的 openFDA 404 查询作为检索事实保留）。

**仍开放缺口**：六份均无中国现行产品文本；英国 emc 对奥卡西平与艾司利卡西平本轮未取回正文，EMA、日本、德国、澳大利亚正文未逐份取得；卡马西平与奥卡西平治疗三叉神经痛及双相的原始随机试验原文未取得，相应等级建立在标签条款加综述或阴性试验之上；丙戊酰胺治疗躁狂的随机试验原文与意大利、西班牙、比利时正文未取得（AIFA 检索地址与 CIMA api.json 端点对本机返回 404）；拉莫三嗪与丙戊酸系的欧盟／英国正文未取回。本轮未重写前十轮档案、未扩写清单外药物、未合并 `main`。


## Wave 12 审阅修补与合并记录（2026-11-02）

Wave 12 六份档案经审阅后完成定点修补，未重做研究，也未改变核心 ATC 目录统计。

1. **卡马西平**：补入美国 EQUETRO 缓释胶囊独立标签（DailyMed setid `be478f3c-40f6-47cc-8ab9-f420a9372b1c`，NDA 021710；文内 Revised 10/2022，SPL 生效及 DailyMed Updated 2025-08-19）。该产品 §1.1 批准成人 Bipolar I disorder 的急性躁狂或混合发作，§14.1 提供两项 3 周随机双盲安慰剂对照试验（n=94、n=120，YMRS 主要终点 P=0.033、P<0.0001）。与普通片标签分开记录，急性躁狂／混合发作场景由 C− 调整为 B。
2. **奥卡西平**：周围神经病理性疼痛评分行不再混入三叉神经痛替换用药。补充 2019 年 European Academy of Neurology guideline 的独立边界：对三叉神经痛的长期使用建议基于 very low-quality evidence 与临床经验，未发现完整发表的随机试验，仅有一项小型比较试验；不把指南建议写成标签批准，也不继承卡马西平的评分。
3. **艾司利卡西平**：将双相急性躁狂与复发预防拆为两行，均为 D。急性期 BIA-2093-203 的 YMRS 主要终点未显著优于安慰剂（n=160，较高剂量组 P=0.0523），BIA-2093-204 因提前终止而无确定结论（n=38）；复发预防 BIA-2093-205 的主要终点亦未达显著（n=85，P=0.250）。
4. **丙戊酰胺**：长期风险负担由 4 调整为 5，依据为现行法国正文记载的严重肝损害、胰腺炎、凝血与血小板异常、神经系统长期风险及生殖／发育毒性；二线定位与年度专科复评不再用来抵消药物本身风险。成人停药负担改为 N/A，因为现行正文没有成人停药症状证据；新生儿宫内暴露后戒断综合征移回特殊人群解释，不计入成人停药评分。
5. **目录与规范**：修复 Wave 11 四条跨组记录缺失的状态列分隔符；更新卡马西平、奥卡西平与丙戊酸的目录说明；在 `AGENTS.md` 补充同一成分不同产品标签必须分别检索，以及成人停药负担不得由新生儿戒断结局代替的规则。

**验收范围**：仅复核上述四份受影响药物档案、`catalog/related.md`、`AGENTS.md` 与本计划；核对标签与研究来源、评分行、表格列数、相对链接和原有状态统计。六份 Wave 12 档案仍为 `reviewed`；药物档案总数仍为 290（核心六组 280、跨组主题 10），状态仍为 160 reviewed / 4 indexed / 126 basic；跨组选录仍为 46 条（已建档 10、待建档 36）；专题仍为 15 份。未扩写清单外档案，未重做全库管制审计。



## Wave 13 计划：N07B 物质使用障碍药物（2026-11-02）

**状态：已完成（见文末“Wave 13 完成记录”）。**

**分支**：`plan/substance-use-treatment-wave13`，从 Wave 12 修补合并后的 `main` 创建。

**目标与基线**：当前 `drugs/` 共 290 份（核心六组 280、跨组主题 10），状态为 160 reviewed / 4 indexed / 126 basic；`catalog/related.md` 共 46 条选录，已建档 10 条、待建档 36 条。本轮只处理现有 N07B 选录中的 15 个明确药物实体，不新增重复选录。若 15 份均建立，药物档案总数将为 305、跨组主题为 25、待建档选录为 21；最终状态计数必须按文件顶部字段重新统计，不预设均为 `reviewed`。

### 本轮清单

- **A 组，N07BA 戒烟药物（3）**：`nicotine`（N07BA01）、`varenicline`（N07BA03）、`cytisinicline`（N07BA04）。
- **B 组，N07BB 酒精依赖药物（6）**：`disulfiram`（N07BB01）、`calcium-carbimide`（N07BB02）、`acamprosate`（N07BB03）、`naltrexone`（N07BB04）、`nalmefene`（N07BB05）、`ondelopran`（N07BB06）。
- **C 组，N07BC 阿片依赖药物（6）**：`buprenorphine`（N07BC01）、`methadone`（N07BC02）、`levacetylmethadol`（N07BC03）、`lofexidine`（N07BC04）、`levomethadone`（N07BC05）、`diamorphine`（N07BC06）。

**不纳入本轮**：`N07BA02` bupropion 已有核心档案 [`drugs/bupropion.md`](drugs/bupropion.md)，不重复建档；如需比较戒烟用途，引用该档案并单独核对 bupropion 的戒烟证据。`N07BC51`（buprenorphine, combinations）只是未指明配对成分的 ATC 复方分类，不建立成分不明确的档案；naloxone 属 `V03AB15`，是阿片过量逆转药，不属于本轮 N07B 清单，留待独立主题处理。药用 nicotine 只讨论戒烟治疗，不讨论烟草消费或非药用尼古丁产品。

### 一次执行要求

1. 一次完成 15 份档案，不拆成逐组审批阶段。允许三个非嵌套子代理并行，各负责 A、B、C 一组；主代理负责实体核对、来源交叉检查、评分一致性、共享目录与状态统计。子代理不得编辑 `AGENTS.md`、`PLAN.md`、`README.md`、`catalog/index.md` 或 `catalog/related.md`。
2. 每种药先核实 WHO ATC/DDD Index 2026 的身份与编码，再按具体产品、法域、剂型和版本核对现行监管标签或说明书。优先使用 FDA/DailyMed、英国 emc、EMA、法国 BDPM 及其他国家药监机构；研究证据使用原始 RCT、系统综述与相关指南。分别记录文内 Revised、SPL 生效日与数据库发布日。检索零命中、历史文本或接口失败只能写具体缺口，不推断为未批准、已撤市或不存在。
3. **戒烟药物**：区分 nicotine replacement therapy 的具体剂型与产品、varenicline、cytisinicline 的受体作用和临床证据。核实 cytisinicline 与 cytisine 的名称、实体及监管关系，不因名称相近直接合并。尼古丁不同剂型的标签、给药方式与使用限制分别核对。
4. **酒精依赖药物**：区分 disulfiram／calcium carbimide 的厌恶性威慑治疗、acamprosate 的维持戒酒用途，以及 naltrexone 与 nalmefene 在减少饮酒、降低渴求或复发预防方面的具体证据；逐药核对适应证、人群选择、肝肾限制及与阿片类药物的相互作用，不预设二者的标签与疗效相同。对 ondelopran 优先确认其当前研发、批准与上市状态，不得仅凭 ATC 编码将其写成已上市药物。
5. **阿片依赖药物**：区分 buprenorphine、methadone、levomethadone、diamorphine 的 OUD 维持或监督治疗用途，与 lofexidine 的戒断症状管理；单独核实 naltrexone 在 OUD 复发预防中的口服或长效制剂证据与批准范围，不将其与酒精依赖用途合并评分；核实 levacetylmethadol 的历史批准、停销与当前可及状态。必须区分 OUD 标签与疼痛标签，区分不同剂型、途径和产品；不得把一种药的管制级别外推给同类药或其他法域。
6. 中国管制字段按现行官方目录逐药核对；中国上市与核准适应证只有在可靠官方来源可核实时才写为已确认。美国 DEA、英国 Misuse of Drugs Regulations、欧盟成员国及其他法域的管制结论按各自官方目录记录，不将不同国家的分类互换。不要重做全库管制审计。
7. 严格沿用既有评分规则。A–D 只保留有本药特异证据且具有当前临床决策价值的场景。戒烟、戒酒、减少饮酒、OUD 维持治疗、戒断症状缓解等场景分开评分。未获批本身、缺少证据、管制身份或 ATC 归属不得单独构成评分行；证据不足时写 `N/A` 或“待核实”，不得为完成批次强行升级状态。
8. 不设专题配额。只有发现重要证据冲突或一个无法在主条目内简洁解释、且确有独立决策价值的问题时，才新增问题导向专题。主条目保持快速判断导向，完整给药方案与次要试验细节留在原始来源或必要的正文段落。
9. 完成后更新本轮实际建立的药物档案、`catalog/related.md`、`catalog/index.md`、`README.md`、`PLAN.md`，并按需要对 `AGENTS.md` 做最小修订。目录只更新现有 15 条状态，不增加重复条目；选录总数仍为 46。重新计算总档案数、核心／跨组数量及 reviewed/indexed/basic 计数。检查来源、产品边界、相对链接、表格、状态字段与目录数量，提交并推送本分支，交由审阅，不自行合并 `main`。

**不做**：不重审既有 290 份档案；不建立 `N07BC51` 未指明成分的复方档案；不纳入 naloxone 或其他清单外药物；不重做中国全库管制审计；不强制将 15 份全部标为 `reviewed`；不新增数据库、爬虫、CI、自动评分器或多阶段审批；不新增专题配额。


## Wave 13 完成记录（2026-11-03）

**结果与计数**：本轮新建 15 份跨组档案，按实际证据定级为 **10 份 `reviewed`、4 份 `basic`、1 份 `indexed`**，未强制升级。`drugs/` 由 290 份增至 **305 份**（核心六组 280 份不变，跨组主题 10 份增至 25 份）；全库状态 **170 `reviewed`／5 `indexed`／130 `basic`**。`catalog/related.md` 选录总数仍为 46 条，已建档由 10 条增至 25 条，未建档 21 条（其中 20 条为待建档候选，`N07BC51` 属未指明全部成分的 ATC 复方类别、仅分类记录）。`analysis/` 仍为 15 份，本轮未新增专题。达到 `reviewed` 的 10 份：尼古丁、伐尼克兰、双硫仑、阿坎酸、纳曲酮、纳美芬、丁丙诺啡、美沙酮、洛非西定、二乙酰吗啡；保持 `basic` 的 4 份：cytisinicline、calcium carbimide、levacetylmethadol、levomethadone；`indexed` 1 份：ondelopran。

**执行方式**：按 PLAN 授权启用三个互不嵌套子代理并行，A 组 3 份、B 组 6 份、C 组 6 份；主代理负责全部共享文件、实体与来源复核、评分口径统一、验收与提交。首次派发的 A 组代理在写盘前耗尽轮次，改以“先把美国标签正文批量落盘、再限时取证”的方式复派后完成。本轮美国标签正文共取回 46 份现行文本，档案实际引用 32 个 setid，逐一回查 DailyMed 存在；emc 产品 13 个逐一回查标题正确；PMID 54 个经 eutils 批量校验全部命中且题名相符；外部链接 129 条逐条复检，仅 fda.gov／federalregister.gov 的文档页对本机脚本请求返回反爬拦截（改用 govinfo 全文或站内标题检索，并已在档案内注明）。

**分类与取证锚点**：WHO ATC/DDD Index 2026（页面脚注 Last updated 2026-01-20）除逐码核对外，把 `N07B` 组注与三个亚组注原文写入各档案——维持治疗归 `N07B`、脱毒用药归 `V03A`、bupropion 归 `N06A`、naltrexone 虽也用于阿片依赖仍归 `N07BB`、≤0.4 mg 丁丙诺啡制剂归 `N02AE`、与纳洛酮复方归 `N07BC51`、用于阿片依赖的吗啡归 `N02AA01`、nalmefene 的 DDD 18 mg 按“治疗日推荐剂量”设定。本轮有 DDD 者 10 个，cytisinicline、calcium carbimide、ondelopran、levacetylmethadol、diamorphine 五个编码在索引中无 DDD，按缺口写而不补数。美国 DailyMed 对 carbimide、ondelopran、levomethadyl、diamorphine、levomethadone 返回 0 条、openFDA 按通用名对本轮全部名称返回 404，均写作检索事实而非“未批准”。

**中国管制**：本轮把核查从“药用类两份目录＋58 号增列”扩到**《非药用类麻醉药品和精神药品目录》完整 396 项逐名核对**。公安部原始附件对本机仍返回 HTTP 521，改由政府门户转载的同一公告附件取回全文并转录目录注 1（盐类、立体异构体及其盐类）与注 2（305–396 项另含酯、醚及其盐类与立体异构体）。结果命中三份：美沙酮为《药用类麻醉药品目录（2025 年版）》第 17 项（`17 美沙酮* Methadone 76-99-3`，星号按注 3 表示我国生产及使用）；丁丙诺啡按制剂分三档——第一类第 4 项（`52485-79-7`）、第二类第 7 项透皮贴剂、第二类第 74 项丁丙诺啡和纳洛酮复方口服固体制剂，其分档依据是精神药品目录注 1 的“除非另有规定”；海洛因（二乙酰吗啡）为《非药用类目录》第 347 项（`561-27-3`）。levomethadone 与 levacetylmethadol 只能靠扩展条款归口（前者经美沙酮条目注 2 的立体异构体条款，后者经非药用类第 311 项阿醋美沙朵注 1 的立体异构体条款，两条均以 CAS／InChIKey／PubChem 同义名段支撑并写为“可覆盖的边界情形”，不作已列管断言）；305–396 项的酯醚规则未被外推到 1–304 项或任何整类。其余十二份逐名未命中。四个整类的判据统一按公告列举的母体书写——**并纠正了多份档案把奥啡类写成“吗啡烷／蒂巴因骨架”的误记，公告的两种母体是溴啡与螺溴啡**。中国上市与核准适应证仍全部待核实（NMPA 恒 HTTP 412、CDE 目录集恒 202 校验页）。

**实体与阶段分界**：戒烟一侧把尼古丁的五种剂型按产品分别引用（咀嚼胶、含片、贴剂为面向消费者的现行标签，其中含片挂 NDA 022360、贴剂引用 NDA 020076 与 ANDA 074612，而本轮所引咀嚼胶条目未挂申请号，故“OTC 销售”不等于同一注册路径；鼻喷与吸入剂为处方文本），并把伐尼克兰的戒烟片与 TYRVAYA 干眼症鼻喷写成两个产品两个治疗目标；cytisinicline 与 cytisine 的同一性以 PubChem 两名同指 CID 10235 与 ORCA 论文口径为据，但监管状态按“cytisine 名义产品”与“cytisinicline 名义申请”分别记录，美国无正文（NDA 经 2026-06-22 CRL、缺陷为第三方设施 cGMP 与最终标签，属申请人自述）故保持 `basic`。酒精一侧把双硫仑与卡巴米得钙按两个实体分列、纳曲酮与纳美芬不预设相同：纳曲酮的酒精依赖与阿片使用障碍复发预防、口服与长效注射各自成行；纳美芬把欧盟／日本的“减少饮酒量＋持续心理社会支持”与美国的阿片过量逆转产品（OPVEE 鼻喷、注射剂）按不同治疗目标与不同 ATC 归属分写。阿片一侧把 OUD 维持、戒断症状管理、疼痛与过量逆转逐支文本分开，固定复方不计入单方评分，`N07BC51` 不建档，同名 ETHIQA XR 的 DailyMed 条目经核为动物用药文本（“Not for use in humans”）而排除；levomethadone 作为美沙酮左旋异构体不继承美沙酮的批准与评分；levacetylmethadol 按 ATC 收录、曾批准、当前不可得与研究状态四段分列。

**评分层**：各档案的 A–D 行均绑定本药特异证据与法域措辞；“未收载＋缺证据”不作评分行——nalmefene 的“戒酒维持”与“OUD 复发预防”两行、lofexidine 的维持治疗与渴求结局、levomethadone 的镇痛用途均改为表后说明。滥用／误用维度只有 varenicline 记 1 分，依据是其标签人体滥用潜力研究在 1 mg 未产生显著正性主观效应、3 mg 一致产生不适体验；尼古丁记 3 分依据标签自述的强化效应通路与鼻喷超疗程／依赖转移的定量记录；纳曲酮、纳美芬、双硫仑、阿坎酸、丁丙诺啡、美沙酮、左美沙酮按各自标签与列管事实分别定档；cytisinicline、calcium carbimide、ondelopran、lofexidine、levacetylmethadol 因缺本药特异人体强化效应或误用资料记 `N/A`，未以“未列管”推定低风险。停药负担只评价患者自身，洛非西定与卡巴米得钙按缺口记 `N/A`。中国“非适应证／潜在不适当处方风险” 15 份一律 `N/A`：未取到以这些药逐名对应的中国处方偏离、PIM 判定或药物利用证据。

**主代理整合修正**：① 奥啡类结构判据按公告母体重写（尼古丁、伐尼克兰、cytisinicline、双硫仑、阿坎酸、纳曲酮、纳美芬、丁丙诺啡共 8 份），并把纳曲酮与纳美芬由误设的“边界·待核实”改为“按定义不落入”；② nalmefene 表内两条 `不评分` 占位移出 A–D 表，其历史产品 Revex 的批准与撤出改引联邦公报一手认定通知（82 FR 51282，FR Doc 2017-23952：NDA 20-459 初始批准 1995-04-17，Baxter 2009-06-05 函告生产与分销于 2008-05-21 停止且理由为商业，FDA 认定非因安全或疗效撤出销售）；③ **calcium carbimide 原写“本实体无可归属随机试验”不成立**，按通用名与历史商品名检索补入其自身证据（1989 年 128 例随机双盲安慰剂对照交叉试验未把药与安慰剂分开、78% 患者自认全程服活性药；同试验医学检查端；1992 年复饮预防情境随机试验仅呈未达显著趋势；2006 年九年在队列为适应证混杂的非随机比较），并据此定三个负担维度与一个 C 级场景；④ **ondelopran 原记“PubChem 无 CID、四整类无法判定”有误**，按 CID 10457387（同义名段含 Odelepran [USAN]、LY2196044、CAS 676501-25-0、UNII 4VZT670SD9）补齐结构判据，并补入其 II 期随机双盲试验（375 例，主要终点大量饮酒日变化 −43.02% 对 −38.72%、P=0.12 未分离，两个次要终点与预设基因亚组提示信号）与生理药剂吸收建模研究，新增一行 C− 场景；⑤ cytisinicline 的监管时间线改挂申请人公告原始页面并明示“FDA 不公布 CRL 原文”，2006 年系统评述改用可校验的 PMID 链接；⑥ 尼古丁的“OTC 专论”表述按各条目申请号实况改写；⑦ lofexidine 场景格内的合用时点细节移回 §8；⑧ levomethadyl 的立体异构体链条补入 PubChem 同义名与两组 CAS 对照；⑨ diamorphine 把“重度疼痛”与“急性肺水肿呼吸困难”两个证据结构不同的收载用途拆成两行；⑩ naltrexone 场景格内的试验例数移出。

**仍开放的来源缺口**：15 份的中国上市与核准适应证全部待核实；本轮未取得任何欧盟成员国、瑞士、德国、荷兰、俄罗斯、日本、加拿大的现行说明书正文（纳美芬与丁丙诺啡、美沙酮、阿坎酸、双硫仑以英国 emc 现行 SmPC 为跨法域锚点，EMA 的 Orlaam 页与 Selincro EPAR 可访问但未按成员国逐份核对）；cytisinicline 的保加利亚／波兰等现行注册条目未从各国药监库核到；ondelopran 的 III 期结果未张贴、后续申报法域未知；calcium carbimide 的加拿大历史 Temposil 产品记录已由 Health Canada DPD 确认，但当前上市与欧洲现行注册仍未核；levomethadone 与 diamorphine 的瑞士、德国、荷兰处方文本以 BAG／BfArM 法规页为主而未取产品正文；levacetylmethadol 与 levomethadone、ondelopran 无现行说明书正文，状态据此保持。历史批准细节（如 1993 年 ORLAAM 与 1995 年 REVEX 的立项文件）以联邦公报原文为据，未回 Orange Book 历史卷逐字段复核。

**未做事项**：未重审既有 290 份档案；未建立 `N07BC51` 复方档案；未纳入 naloxone 或其他清单外药物；未重做中国全库管制审计（仅新增本批 15 份的逐名核对与转载附件入口）；未强制把 15 份标为 `reviewed`；未新增数据库、爬虫、CI、自动评分器或多阶段审批；未新增专题；未合并 `main`，等待人工审阅。
## Wave 13 审阅修补记录（2026-11-04）

1. **卡巴米得钙实体与商品名**：删除错误的 Alcover 归属（EMA 明确 Alcover 175 mg/ml 为 sodium oxybate），删除未获可靠来源支持的 Carbidix 商品名；补入 Health Canada DPD 的 TEMPOSIL TAB 50MG 历史记录（DIN 00014958，原始上市日 1959-12-31，1999-04-12 Cancelled Post Market）与 FDA SRS 的 citrated calcium cyanamide／Temposil 同义名映射。原始产品说明书未取得，故不推断精确盐型、剂型互换或当前可获得性，档案保持 `basic`。卡巴米得钙的 A–D 表移除历史用途占位行，历史试验留在正文。
2. **场景评分收口**：cytisinicline 的美国固定剂量三期方案与 ondelopran 的研究阶段用途移出 A–D 表；disulfiram 的无支持减量场景移除；acamprosate 的减少饮酒场景依据直接阴性 RCT 调整为 D，复发后继续用药合并至戒酒维持行；lofexidine 的纳曲酮相互作用移回 §8；diamorphine 的误用与过量风险移回 §7。上述修改不删除研究结果或风险资料。
3. **尼古丁与交叉引用**：删除“合并吸烟必然产生高于单独吸烟的尼古丁峰浓度”这一缺乏直接 PK 支撑的断言，保留标签对持续吸烟与尼古丁过量症状的谨慎提示；修复 naltrexone 与 nalmefene 关于奥啡类结构归属的两处过时交叉引用。
4. **目录与规则**：`catalog/related.md` 核查日期更新至 2026-11-04，并明确剩余 20 条为具体药物候选、`N07BC51` 为分类记录；`catalog/index.md` 状态统计日期更新至 2026-11-04。`SOURCES.md` 补入 Health Canada DPD 与 FDA SRS。`AGENTS.md` 不作重复修改，其现有规则已明确 A–D 仅评价有当前临床决策价值的临床场景，研究阶段、相互作用与误用风险不单独占用评分行。
5. **验收**：本次只修补 Wave 13 的 10 份药物档案与共享来源、目录和计划文件；未新建药物档案或专题。全库仍为 305 份，状态仍为 170 `reviewed`／5 `indexed`／130 `basic`；跨组主题仍为 25 份。后续按更新后的文件内容复核内部链接、表格结构、场景评分与统计后合并 `main`。
## Wave 14 计划：N06D 与 Alzheimer’s disease 候选药物（2026-11-04）

**分支**：`plan/dementia-drugs-wave14`，从 Wave 13 审阅修补合并后的 `main`（`87f1c9133c30b57db13333dfef289b7c18e2a91c`）创建。

**目标与基线**：本轮扩展为 **30 条候选**，由 15 条 WHO ATC N06D 候选与 15 条非 N06D 的 Alzheimer’s disease／相关神经精神症状候选组成。当前 `drugs/` 共 305 份（核心六组 280、跨组主题 25），状态为 170 `reviewed`／5 `indexed`／130 `basic`。若 30 条全部核实为互不重复的独立药物实体或具体固定复方并建立档案，总数上限为 335，跨组主题上限为 55；**这只是理论上限，不得为了达到数字而把 ATC 分类、未确认的组合、同义名或没有独立实体的研发代号强行建档**。

本轮前 15 条来自 WHO ATC/DDD Index 2026 的 N06D；后 15 条是补充的 AD 药物研发与区域性用药候选，不属于 N06D 官方清单，也不应伪造 ATC 编码。当前 `catalog/related.md` 的 46 条 WHO 选录不因这 15 条补充候选而改变；只有完成实体核实并实际建档后，才按项目目录规则记录其跨组归属。

### 本轮 30 条候选

**A 组：胆碱酯酶抑制剂（6）**

- `tacrine`（N06DA01）
- `donepezil`（N06DA02）
- `rivastigmine`（N06DA03）
- `galantamine`（N06DA04）
- `ipidacrine`（N06DA05）
- `benzgalantamine`（N06DA06）

**B 组：其他 N06D 症状治疗、植物药、复方与研发候选（6）**

- `donepezil and memantine`（N06DA52）
- `donepezil, memantine and Ginkgo folium`（N06DA53）
- `memantine`（N06DX01）
- `Ginkgo folium`（N06DX02）
- `blarcamesine`（N06DX06）
- `hydromethylthionine`（N06DX07）

**C 组：抗淀粉样蛋白与相关疾病修饰候选（6）**

- `aducanumab`（N06DX03）
- `lecanemab`（N06DX04）
- `donanemab`（N06DX05）
- `remternetug`
- `valiltramiprosate`（ALZ-801）
- `gantenerumab`

**D 组：区域性用药与非淀粉样蛋白疾病修饰候选（6）**

- `huperzine A`
- `sodium oligomannate`（GV-971）
- `AR1001`
- `buntanetap`
- `masitinib`
- `zervimesine`（CT1812）

**E 组：认知／神经精神症状及其他研发候选（6）**

- `ACP-204`
- `ITI-1284`（deulumateperone）
- `zatolmilast`
- `MK-1167`
- `JNJ-2056`（ACI-35.030）
- `simufilam`

候选清单是本轮预审范围，不预设所有项目在 2026-11-04 仍处于活跃研发阶段。研发阶段、试验状态、监管状态与商业供应必须逐项以当前可核实来源确认。

### 一次执行要求

1. 一次完成全部 30 条候选的核查，不拆成需要人工逐阶段确认的子计划。允许五个互不嵌套的子代理并行，分别负责 A、B、C、D、E 组；主代理负责实体边界、交叉核查、共享目录、评分一致性和最终验收。子代理只编辑分配给自己的药物档案，不编辑 `AGENTS.md`、`PLAN.md`、`README.md`、`catalog/index.md` 或 `catalog/related.md`。
2. N06D 项先核实 WHO ATC/DDD Index 2026 的名称、编码和分类注，再核对具体药物实体、盐型、剂型、产品、法域与当前上市状态。**ATC 收录不等于批准、上市或临床有效**；历史批准、现行批准、商业供应与研发阶段分别记录。监管数据库零命中或网页不可访问只记录为检索缺口，不推断未批准或已撤市。
3. **胆碱酯酶抑制剂**：分别核实 tacrine 的历史批准与撤市／供应状态及肝毒性；donepezil、rivastigmine、galantamine 的具体法域、剂型和适应证；ipidacrine、benzgalantamine 的实体身份、研发或上市状态与可核实产品。不得把整个药理类别的证据或标签互相外推。
4. **Memantine、Ginkgo 与 ATC 复方**：memantine 单方与固定复方分开建档和评分。N06DA52、N06DA53 必须核实是否存在可识别的具体产品、确切成分、配比、剂型及监管文本；若只能确认 ATC 分类而不能确认具体产品，不创建虚构的固定复方档案，保留分类记录并说明缺口。Ginkgo folium 是多组分植物药，必须明确所评估的标准化提取物或具体产品，区分药品、传统植物药、补充剂、叶粉与不同提取物，不跨产品继承疗效或批准结论。
5. **抗淀粉样蛋白候选**：逐产品核实 aducanumab、lecanemab、donanemab、remternetug、gantenerumab 的研发／批准／商业供应状态与法域差异；区分抗体与 valiltramiprosate 这类小分子／前药候选。重点记录疾病阶段、患者筛选、生物标志物确认、ARIA-E／ARIA-H、MRI 监测及 APOE ε4 相关风险。区分临床量表变化、疾病进程终点与生物标志物变化，不把机制或影像学变化直接写成已证实的临床获益。失败或停止开发的项目保留历史证据，不设置当前临床使用场景评分。
6. **区域性药物与非淀粉样蛋白候选**：huperzine A 与 sodium oligomannate 必须核对中国具体注册产品、现行说明书、批准范围和商业供应；不得由中国市场记录推断其他法域批准。AR1001、buntanetap、masitinib、zervimesine 必须核实研发代号、试验登记、主要终点、结果发布日期、当前试验状态及申办方后续决策；综述或商业 pipeline 数据只作候选发现入口，不替代试验登记与原始结果。
7. **神经精神症状候选**：ACP-204 与 ITI-1284 需明确其研究目标是 AD 相关 psychosis／其他 neuropsychiatric symptoms，而不是认知增强或疾病修饰。Zatolmilast、MK-1167、JNJ-2056 分别核实机制、试验人群、主要终点和当前研发状态；不因其进入 AD 试验就推断已具有临床疗效。
8. **Simufilam 与历史失败项目**：核对 RETHINK-ALZ、REFOCUS-ALZ 的共同主要终点、次要终点、结果发布日期、试验提前终止及申办方项目后续决定；区分 ClinicalTrials.gov 的记录状态、试验实际完成情况与研发项目是否继续。阴性或未达主要终点的结果应明确记录，不用事后亚组或探索性结果覆盖主要结论。
9. 中国管制字段按现行官方目录逐项核对名称、别名和可适用的整类定义；其他法域按本药实际监管文本核对。不要重做全库管制审计，也不要由抗体类别、ATC 归属或药理机制推断管制状态。
10. 严格沿用现有评分规则。A–D 只评价有本药特异证据且具有当前临床决策价值的临床场景；研究方案、单纯机制、ATC 分类、未批准状态、相互作用、特殊人群和风险来源不单独占用场景评分。药物负担各维度按本药证据评分，缺证据写 `N/A`，不得以类别印象填分。没有当前临床使用场景的研发或失败项目不设置 A–D 行；不得为完成批次强制升级 `reviewed`。
11. 项目中已存在的 `caffeine`、`escitalopram`、`xanomeline-and-trospium` 等档案不重复建档；如其 AD 试验对本轮有意义，只作交叉引用。研发代号与通用名、前药与活性成分、固定复方与单方必须先做重复检查。
12. 不设专题配额。只有发现重要证据冲突或一个无法在主条目内简洁解释、且确有独立决策价值的问题，才新增问题导向专题。主条目保持快速判断导向，完整试验设计与次要数值留在原始来源或必要的正文段落。
13. 完成后更新实际建立的药物档案、`catalog/related.md`、`catalog/index.md`、`README.md`、`PLAN.md`，并按需要对 `AGENTS.md` 做最小修订。核对总档案数、核心／跨组数量与 `reviewed/indexed/basic` 计数；检查产品身份、来源、内部链接、表格和状态字段。提交并推送本分支，交由审阅，不自行合并 `main`。

**候选发现与核查入口**

- Cummings JL et al. *Alzheimer's disease drug development pipeline: 2026*. Alzheimer's & Dementia: Translational Research & Clinical Interventions. DOI: [10.1002/trc2.70251](https://doi.org/10.1002/trc2.70251)。该综述以 2026-01-01 为 pipeline 截点，作为候选发现与研究阶段交叉核对入口，不代替当前试验登记或监管文本。
- [ClinicalTrials.gov](https://clinicaltrials.gov/)：核对试验注册、状态、终点、结果与更新时间。
- [FDA Drugs@FDA](https://www.accessdata.fda.gov/scripts/cder/daf/)、[DailyMed](https://dailymed.nlm.nih.gov/dailymed/)：核对美国批准与现行标签。
- [国家药品监督管理局 NMPA](https://www.nmpa.gov.cn/)：核对中国区域性产品注册与批准信息。
- [Alzheimer's disease pipeline tracker（November 2026）](https://cnspulse.com/indication/alzheimers-disease/)：仅作补充候选发现入口，所有阶段和状态必须回到临床试验登记、申办方公告或监管文件核实。

**不做**：不重审既有 305 份档案；不处理剩余 G04BD 与 V03AB 候选；不把 `N07BC51` 分类记录变成药物档案；不强制创建全部 30 个候选文件；不强制升级状态；不新增数据库、爬虫、CI、自动评分器或多阶段审批；不新增专题配额；不合并 `main`。
## Wave 14 完成记录（2026-11-05）

**分支与状态**：`plan/dementia-drugs-wave14`，自 Wave 13 合并后的 `main`（`87f1c9133c30b57db13333dfef289b7c18e2a91c`）创建；完成后推送本分支等待人工审阅，未合并 `main`。

**结果统计**：30 条候选实际建档 **29 份**——8 份 `reviewed`（donepezil、rivastigmine、galantamine、benzgalantamine、donepezil-and-memantine、memantine、lecanemab、donanemab）、2 份 `indexed`（ipidacrine、remternetug）、19 份 `basic`；**`N06DA53`（donepezil, memantine and Ginkgo folium）不建档**（见下方裁决记录）。全库 334 份（核心六组 280＋跨组主题 54），状态 **178 reviewed／7 indexed／149 basic**（核心 150/4/126 未变，跨组 28/3/23）。未新增专题（`analysis/` 仍 15 份）。

**主代理预检与取证**（先于子代理完成）：WHO ATC 2026 的 N06DA／N06DX 全部候选码逐页回读（含 DDD 逐行核对；`N06DX30 combinations` 为分类条目不入候选）；DailyMed／openFDA／PubChem／emc／ClinicalTrials.gov v2 的身份与状态锚点（ZUNVEYL、NAMZARIC、LEQEMBI、KISUNLA 等 setid；**AR1001 的 PubChem 同名碰撞**——字符串解析为 N-methylbenzylamine，CID 7669——被识别并在档案中显式甄别）；中国四份现行管制目录及 2026-07-01 增列 16 种附表对 30 条候选按英文名、中文译名、研发代号与已核同义名逐名扫描**全部未命中**（16 种附表转录见 SOURCES.md）；Cummings 2026 pipeline 全文取回并逐字核对可引用表述（158 药／192 试验、DTT 73%、"no DTTs approved for preclinical AD…"等）；联邦公报一手文本（**78 FR 43210**：Cognex／NDA 020070 依 21 CFR 314.150(c) 持证人请求撤销、公告 2013-07-19、生效 2013-08-19；**89 FR 14869**：ADUHELM 专利期审查期认定含加速批准表述）；10 项试验的登记张贴结果逐项核对（RETHINK-ALZ、REFOCUS-ALZ、GRADUATE、buntanetap 两项、gantenerumab 两条、LUCIDITY、ACI-35.030 Ib/IIa 等）。

**执行实况**：五个子代理并行（A 胆碱酯酶抑制剂 6、B 其他 N06D 与复方 5＋1 条不建档、C 抗淀粉样蛋白 6、D 区域性用药 6、E 神经精神与研发候选 6）。A、B、C 组如期交付；**D 组与 E 组先后触及子代理轮次上限**——D 组未落盘任何文件、复派一次后仍未落盘，E 组交付 3／6；D 组六份与 E 组剩余三份（mk-1167、jnj-2056、simufilam）由主代理接管完成。E 组已交付的三份经验收保留。

**主代理在验收中的修正**：① C 组四份 §2.1 的"待核实"改 `N/A`（缺证据写 N/A 的口径）；② A 组六份中国管制行名由"中国上市与管制"改为仓库统一的"中国管制状态"，行内"上述现行目录"展开为四份目录枚举；③ donepezil／rivastigmine／galantamine／ipidacrine 的英国 emc 检索缺口补入复核事实（浏览器 UA 下分别返回 21／34／11／0 条结果），防止"无结果"被误读为"英国无产品"；④ valiltramiprosate 的 PubChem property URL 由省略号占位改为可解析 URL；⑤ 清除主代理自身补丁引入的内部工作措辞（"主代理复核"→"独立复核"）。

**本轮裁决记录**：`N06DA53` 三成分复方无可识别具体产品（DailyMed／emc／ClinicalTrials／Drugs@FDA 均无），只保留目录分类行；`tacrine` 美国状态按"持证人请求撤销（314.150(c)）＋实际退市年代待核实"分层；`aducanumab` 保持 `basic`（FDA 撤回清单列明加速批准适应证于 2024-11-01 撤回；Biogen 2024-01-31 已公告停止开发与商业化；两项事件分开记录，缺现行文本不升级）；甘露特钠按"附条件批准→确认性 III 期搁置→注册证到期→媒体据未见批准证明文件解读为未获再注册，官方文书待核实"分层且不设 A–D 行；`buntanetap` 的 PDD III 期与 AD 试验分列、POST_HOC 亚组不得覆盖主要终点；`simufilam` 两项 III 期共同主要终点阴性按登记张贴 P 值记录（RETHINK-ALZ：ADAS-Cog12 p=0.5335/0.5836、ADCS-ADL p=0.0763/0.1530；REFOCUS-ALZ：0.4308、0.4034）；`zervimesine` 已张贴 II 期的"主要"条目只有安全性计数，疗效方向不作表述。

**验收方式**：仓库外脚本对 29 份档案做结构与体例检查（H1／状态条／免责声明／11 节／2.1 六维／2.2 四列／密度带／内部链接／工作流措辞泄漏），全部通过；来源审计并发验证全部 PMID（37）、DailyMed setid（15）、NCT（96）与外链（133），除已在档案内如实标注的 404／403 检索缺口外无失效引用。跨组重复检查：30 条候选与既有 305 份无同名或同实体档案；`tacrine` 的唯一子串命中 `dimetacrine.md`、`deulumateperone` 对照 `lumateperone.md`、`benzgalantamine` 对照 `galantamine.md`、`AR1001` 同名碰撞均已按实体边界写入档案。

**仍开放的证据缺口**：29 份的中国上市与核准适应证全部未取得（NMPA 412／CDE 202）；石杉碱甲与甘露特钠的中国产品文本只有门户与转载层；文献接口本轮多次 500／503，C 组六份与 D／E 多份未列 PMID（已在各档案记录）；blarcamesine 欧盟审评正文、hydromethylthionine MHRA 结论、tacrine 其他法域文本未取得；buntanetap／AR1001 等已完成试验的张贴数值未逐条读取。


## Wave 14 审阅修补记录（2026-11-05）

**审阅结论**：主体档案与结构验收通过，按审阅意见完成定点修补，不重做 29 份档案。

**实际修补**：① Aducanumab 补入 FDA 加速批准撤回清单（BLA 761178，2024-11-01）与 Biogen 2024-01-31 一手停研公告，区分企业停研与 FDA 撤回，不把撤回原因写成未经证实的法律路径；② Galantamine 删除重度 AD 与皮疹两个不构成独立临床使用场景的评分行；benzgalantamine 删除重度 AD 续用评分行；③ Ginkgo folium 按产品与人群收窄评分：EGb 761 240 mg/day 在德国 2026 S3 指南所列轻中度 AD／伴非精神病性行为症状的血管性痴呆场景保留 C，MCI 调整为 D，卒中后认知障碍不再与指南场景合并；Cochrane 2026 对痴呆的低确定性小到中度获益不支持把所有痴呆场景一律降为 D；④ Gantenerumab、ACP-204、AR1001、Blarcamesine、Buntanetap、Deulumateperone、Hydromethylthionine、JNJ-2056、Masitinib、MK-1167、Remternetug、Simufilam、Valiltramiprosate、Zatolmilast 与 Zervimesine 等研究候选的全球性“从未获批／无任何法域批准”改为可复现的检索事实与状态待核实；⑤ 甘露特钠的再注册结论改为媒体层解读，官方文书未取得，现行注册状态待核实；⑥ Lecanemab 中国管制行补入奥啡类；⑦ SOURCES.md 纳入 2026-07-01 增列 16 种完整逐名核查清单，29 个候选的名称、代号与已核同义名逐项对照均未命中；ipidacrine.md 对该附表的检索缺口据此关闭；⑧ AGENTS.md 修正标点并增加否定性批准状态的证据规则。

**复核结果**：29 份档案数量与状态不变（8 `reviewed`、2 `indexed`、19 `basic`）；未新增药物文件或专题；所有修补均为局部证据边界与评分修正。

## Wave 15 审阅修补与交接记录（2026-11-10）

**审阅范围**：50 份本轮档案与 `AGENTS.md`、`PLAN.md`、`README.md`、`catalog/index.md`、`catalog/related.md`。不对既有 334 份药物重新评估。

**实质修补**：按 `AGENTS.md` 和 `SCORING.md` 的规则，删除 89 条仅凭禁忌证、特殊人群、相互作用、监测、机制推测、无对照证据或固定复方外推形成的独立 A–D 评分行，保留可核实的实际治疗场景。高风险禁忌仍保留在 §6–§9 与相关主适应证的限制说明中，删除独立评分不代表降低或否定风险。更正 naloxone 妊娠期紧急逆转的错误风险暗示，flumazenil 对 benzodiazepine 抗惊厥保护的拮抗表述，levodopa 单方与固定复方边界；betahistine 按 Cochrane 2023 公开摘要的低确定性证据下调场景等级，flunarizine 的 PMID:42572044 从错误的 RCT 定性改为回顾性两中心队列并加入随机证据综述；trofinetide 主场景反映效应量有限与胃肠道负担。amifampridine 成人与已批准的 ≥6 岁儿童 LEMS 场景分别陈述。E 组 9 份重复 §2.2 标题已清理。

**结构复核**：50 份均含 1–10 主要章节、唯一 §2.2 标题和引用键；全部内部 Markdown 文件链接可解析，无 A–D 表格字段结构错误。`terodiline` 与 `obidoxime` 无可评分的当前治疗场景，保持无评分行而非填充占位。原有 40 `reviewed`、10 `basic`、0 `indexed` 状态保持不变。

**目录复核**：修正 `catalog/index.md` 遗留的 334／54／46／39／7 旧统计，并把 `ipidacrine` 与 `remternetug` 补入七份 `indexed` 名单。`catalog/related.md` 对 aducanumab 的 FDA 撤回日期与企业停售分别注明。最终总数 **384 份**，其中核心六组 **280**、跨组 **104**；**218 reviewed／7 indexed／159 basic**；跨组选录 **91**，已建档 **89**，未建档的 **2 条均为未落地具体产品的 ATC 复方类别**；专题仍为 15 份。

**移交边界**：中国 NMPA 412 与 CDE 202 拦截、部分欧洲／亚洲官方标签未取得、个别历史药物批准及撤回文书未核实，均不视为已解决；以 [HANDOFF.md](HANDOFF.md) 所列范围作为下一接手方起点，不自动启动新波次。

## Wave 16 标识回读与体例收尾（2026-11-11）

**标识回读**：对 384 份档案可解析的 308 个 PubChem CID 与 282 个 Wikidata QID 逐条回读官方接口，全部返回有效实体。初筛 42 个 CID 与 38 个 QID 与档案 slug 不一致，人工复核后改正 8 份档案中的 11 个错误标识，涉及 acamprosate、imidafenacin、nalmefene、naltrexone、pregabalin、propranolol 的 CID 与 clonazepam、pregabalin、propranolol、doxepin 的 QID，doxepin 同时改为混合物记录 CID 3158。其余差异属于盐型、立体异构体与同义名标签，不属标识错误。原始回读与逐条判定见 [逐名监管检索记录](catalog/retrieval-log-2026-11.md)。

**体例收尾**：清空全部散文分号（3→0）与单句多冒号（3→0），修正 tacrine 一处内联代码跨入中文文本的断行错误。破折号残留 9 处均为英文原文标题、表格占位符或法文引文，不作改动。

**验证**：`audit2_scan.py` 记录 semi_prose 0、colon_multi 0；`qc_final.py` 0 问题、0 断链；`full_struct_qa.py` 仅 gedocarnil 的章节计数提示保持原状，属索引状态档案的既有结构。

## Wave 16 中国 NMPA 注册补检索（2026-11-11）

**检索**：对 234 份 `reviewed` 档案按中文名逐名重查 NMPA 境内生产药品库，53 份命中，写入批准文号、产品名与企业示例，完整结果见 [逐名监管检索记录](catalog/retrieval-log-2026-11.md)。初筛另有两处命中经人工排除，hydroxyzine 的返回实为去氯羟嗪，caffeine 的返回均为复方制剂。零命中档案不改正文。

**边界**：注册条目只证明批件存在，不证明核准适应证文本。各档案原有"待核实"段落按其检索日期保留，新事实标注 2026-11-11。

**未完成**：境外生产药品（国药准字 HJ）类别在当日稍后尝试时 NMPA 返回空响应，属站点限流，未取得结果，不据此推断未上市。

## Wave 16 中国 CDE 受理补检索（2026-11-11）

**检索**：对 179 份无 NMPA 境内批准记录的 `reviewed` 档案按中文名查 CDE 受理品种目录，89 份命中，写入最近受理号、申请类型与承办日期，完整表见 [逐名监管检索记录](catalog/retrieval-log-2026-11.md)。7 份已有受理记录的档案不重复写入。初筛另有 7 处命中因产品名指向其他药物或复方而排除。

**边界**：受理只证明申报被受理，不证明批准，不改写适应证或评分。

**境外生产药品补检索（同日）**：对 179 份无境内批准记录的档案查 NMPA 境外生产药品库，8 份命中并写入 HJ 批准文号示例（duloxetine、escitalopram、esketamine、fluoxetine、fluvoxamine、ginkgo-folium、haloperidol、milnacipran）。trospium 的命中实为异丙托溴铵，已排除。
**名称补检索（同日）**：对 15 份标题未带可解析中文名的档案按常用译名补查 CDE 受理品种目录，5 份命中并写入最近受理号，涉及 pralidoxime、iloperidone、etifoxine、fampridine 与 bupropion／dextromethorphan 复方。这批档案的 NMPA 境内生产药品补查于当日再次遇到站点限流，未取得结果，不写入档案。
**空响应档案重试（同日）**：首批 234 份中有 131 份接口响应为空，本次重试 80 份，41 份命中并写入批准文号示例（表见 [逐名监管检索记录](catalog/retrieval-log-2026-11.md)）。promazine（返回二氧丙嗪）与 pentobarbital（返回异戊巴比妥复方）排除。重试期间站点再次限流，剩余 53 份未取得结果，留待下次。
**日本 PMDA 补检索（同日）**：按日文名检索 PMDA 添付文書等情報検索并取回现行 XML，8 份档案写入收载适应症与剂量要点，涉及 fluvoxamine、milnacipran、mirtazapine、sertraline、paroxetine、escitalopram、donepezil 与 memantine。blonanserin 与 perospirone 检索到标签，但仓库无对应档案，未写入。
**日本 PMDA 第二批（同日）**：再检索 10 个日文名并解析现行 XML，写入 mosapramine、quazepam、triazolam、zolpidem、sulpiride、sultopride、tofisopam、clotiazepam、bromazepam 与 flunitrazepam 的收载适应症与剂量要点。其中 tofisopam 的日本适应症为自主神经症状而非焦虑障碍，zolpidem 明确除外精神分裂症与躁郁症伴发失眠，两处均按原文写入。
**空响应档案补齐（同日）**：待补的 53 份在后续窗口补得 52 份，22 份命中并写入批准文号示例，tetrabenazine（返回氘丁苯那嗪）与 trospium（返回异丙托溴铵复方）排除。pramipexole 当日未取得结果。
**日本 PMDA 第三批（同日）**：再检索 10 个日文名，9 份写入收载适应症与剂量要点（amitriptyline、imipramine、clomipramine、amoxapine、maprotiline、chlorpromazine、levomepromazine、alprazolam、diazepam）。haloperidol 解析到的是癸酸酯肌注标签，未写入。alprazolam 的日本适应症限于心身症，不含广泛性焦虑障碍与惊恐障碍，按原文记录。
**日本 PMDA 第四批（同日）**：再检索 10 个日文名，9 份写入收载适应症与剂量要点（ramelteon、suvorexant、lemborexant、galantamine、rivastigmine、carbamazepine、valproic-acid、lithium、lamotrigine）。gabapentin 解析到的是加巴喷丁恩那卡比（前药）的 RLS 标签，未写入。ramelteon 在日本只收载入睡困难改善，rivastigmine 解析到贴剂标签，按原文记录。另补入 pramipexole 的 NMPA 境内批准文号（50 条）。
**日本 PMDA 第五批（同日）**：再检索 10 个日文名，10 份写入收载适应症与剂量要点（quetiapine、olanzapine、risperidone、aripiprazole、paliperidone、lurasidone、brexpiprazole、trazodone、venlafaxine、duloxetine）。quetiapine 解析到的标签只收载精神分裂症，paliperidone 解析到长效注射剂标签，均按原文记录。
**日本 PMDA 第六批（同日）**：再检索 10 个日文名，9 份写入收载适应症与剂量要点（lorazepam、clonazepam、estazolam、nitrazepam、disulfiram、zotepine、periciazine、bromperidol、tiapride）。clonazepam 的日本标签只收载癫痫类发作、无惊恐障碍，按原文记录。mexazolam 的解析遇到连接中断，未写入。
**mexazolam 重试**：PMDA 连接中断后补查成功，按 2024-02 修订标签写入神经症与心身症适应症、成人 1.5–3 mg/日分 3 次、老年上限 1.5 mg/日。
**日本 PMDA 第七批（同日）**：再检索 10 个日文名，9 份写入收载适应症与剂量要点（biperiden、trihexyphenidyl、amantadine、bromocriptine、pramipexole、ropinirole、selegiline、rasagiline、betahistine）。biperiden 解析到的是注射剂标签，levodopa 解析到的是持续皮下输注制剂标签，后者未写入。amantadine 的日本标签另收载脑梗塞后遗症意欲低下与甲型流感，bromocriptine 的日本标签以高催乳素相关适应症为主，均按原文记录。
**日本 PMDA 第八批（同日）**：再检索 10 个日文名，7 份写入收载适应症与剂量要点（acamprosate、varenicline、methylphenidate、atomoxetine、lisdexamfetamine、mianserin、droperidol），prochlorperazine 与 hydroxyzine 经重试补入，nicotine 命中维生素类制剂未写入。methylphenidate 解析到的是发作性睡病标签，droperidol 解析到的是麻醉用途标签，均按原文记录。
**日本 PMDA 第九批（同日）**：再检索 10 个日文名，4 份写入收载适应症与剂量要点（dimenhydrinate、caffeine、naloxone、flumazenil），midazolam 经重试补入儿童麻醉前口服制剂标签。flunarizine、cinnarizine、meclizine、naltrexone 在该检索口径下为 0 结果，scopolamine 命中丁溴东莨菪碱，均未写入。
**日本 PMDA 第十批（同日）**：再检索 10 个日文名，6 份写入收载适应症与剂量要点（clobazam、vortioxetine、daridorexant、potassium-clorazepate、thiopental、pentobarbital）。agomelatine、desvenlafaxine、cariprazine、bupropion 在该检索口径下为 0 结果。thiopental 的日本标签收载精神科电休克治疗的麻醉与麻醉面谈，按原文记录。
**境外生产药品补检索（同日）**：对 109 份已有境内批准记录的已审阅档案查境外生产药品库，69 份取得响应，31 份命中并写入 HJ 批准文号示例（表见 [逐名监管检索记录](catalog/retrieval-log-2026-11.md)）。其余 40 份当日再次遇到限流，未取得结果。
**PMDA 制剂分型补检索（同日）**：haloperidol 与 paliperidone 的首条结果分别为癸酸酯肌注与长效注射剂标签，追加解析同次检索的其余 XML，补入口服片剂标签（haloperidol 0.75–2.25 mg/日起始、维持 3–6 mg/日；paliperidone 口服缓释片 6 mg 每日 1 次、上限 12 mg/日），两份档案同时标注两种制剂。NMPA 境外生产药品剩余 40 份当日仍受限流，未取得结果。
**制剂分型与境外库续查（同日）**：追加解析 PMDA 同次检索的其余 XML，补入 biperiden 口服片、methylphenidate 缓释片（ADHD）、midazolam 注射剂与癫痫持续状态制剂的标签事实。NMPA 境外库剩余 40 份补得 20 份，7 份命中并写入 HJ 批准文号，naloxone 命中羟考酮纳洛酮复方排除。
**境外库续查收尾**：剩余 40 份最终补得 27 份，12 份命中并写入 HJ 批准文号示例（含 venlafaxine、vinpocetine、ziprasidone、zolpidem、zopiclone），其余 13 份当日限流未取得结果。
**加拿大 DPD 补检索（同日）**：对 24 个活性成分检索 Health Canada Drug Product Database，19 份有 Marketed 状态产品并写入 DIN、企业与商品名示例，涉及 chlorpromazine、haloperidol、clozapine、quetiapine、paliperidone、asenapine、clonazepam、lorazepam、moclobemide 等。olanzapine、risperidone、trifluoperazine 的已捕获行未见 Marketed 示例，未写入。
**加拿大 DPD 第二批（同日）**：对 25 个活性成分检索 Health Canada DPD，24 份有 Marketed 状态产品并写入档案，涉及抗抑郁药、心境稳定剂、ADHD 药物与痴呆药物。acamprosate 与 varenicline 未捕获结果行，trifluoperazine 的 41 条记录未见 Marketed 条目，均未写入。
**澳大利亚 TGA 与 NMPA 境外库收尾（同日）**：按药名检索 TGA 网站并解析 ARTG 条目，18 份档案写入首个非撤销条目（含 ARTG ID 与商品名）。NMPA 境外库最后 13 份全部取得响应，4 份命中并写入 HJ 批准文号（rasagiline、risperidone、ropinirole、selegiline），109 份的境外库查询完成。
**TGA 与加拿大 DPD 第二批（同日）**：澳大利亚 TGA 第二批 16 份档案写入 ARTG 条目（citalopram、escitalopram、paroxetine、duloxetine、desvenlafaxine、vortioxetine、agomelatine、cariprazine、brexpiprazole、ziprasidone、lisdexamfetamine、galantamine、rivastigmine、naltrexone、buspirone 等）。加拿大 DPD 第三批 19 份写入 Marketed 产品示例（cariprazine、brexpiprazole、ziprasidone、flupentixol、zuclopenthixol、pimozide、desvenlafaxine、vortioxetine、levomilnacipran、vilazodone、tranylcypromine、buspirone、hydroxyzine、propranolol、buprenorphine、solriamfetol、pitolisant、lemborexant、daridorexant）。propranolol 与 buprenorphine 的示例分别改为单方人用产品。
**TGA 与加拿大 DPD 第三轮（同日）**：澳大利亚 TGA 第三批 11 份档案写入 ARTG 条目（trazodone、nortriptyline、clomipramine、doxepin、gabapentin、pregabalin、melatonin、deutetrabenazine、tetrabenazine、acetylcysteine、methadone）。加拿大 DPD 第四批 14 份写入 Marketed 产品示例（trazodone、nortriptyline、desipramine、imipramine、clomipramine、doxepin、gabapentin、pregabalin、rivastigmine、melatonin、tetrabenazine、naloxone、acetylcysteine、methadone）。melatonin 的加拿大示例改为 SLENYTO，避免兽用植入剂。
**EMA EPAR 补检索（同日）**：按 EPAR 直接地址读取 18 份欧盟集中上市许可的适应证摘要并写入档案，涉及 agomelatine、vortioxetine、cariprazine、lurasidone、brexpiprazole、aripiprazole、asenapine、paliperidone、olanzapine、duloxetine、esketamine、pitolisant、solriamfetol、daridorexant、nalmefene、tasimelteon、deutetrabenazine 与 melatonin。seroquel、risperdal、leponex、pristiq、dayvigo、strattera、elvanse、provigil 的 EPAR 地址未命中。
**EMA EPAR 第二批（同日）**：补查 lyrica 与 champix 的 EPAR，pregabalin 与 varenicline 两份档案写入欧盟适应证（pregabalin 为周围与中枢神经病理性疼痛、部分性发作添加治疗与广泛性焦虑障碍；varenicline 为成人戒烟）。zyban、strattera、elvanse、provigil、seroquel、risperdal、leponex、pristiq、dayvigo、invega-sustenna 的地址未命中，EMA 站内搜索返回安全验证页，未继续强求。
**TGA 与加拿大 DPD 第四轮（同日）**：澳大利亚 TGA 第四批写入 prochlorperazine、dimenhydrinate、temazepam、amoxapine、phenelzine、suvorexant 的 ARTG 条目；加拿大 DPD 第五批写入 prochlorperazine、trimipramine、dimenhydrinate、scopolamine、triazolam、temazepam 的 Marketed 产品示例。
**TGA 与加拿大 DPD 第五轮（同日）**：澳大利亚 TGA 第五批写入 moclobemide、propranolol、buprenorphine、modafinil、armodafinil、lemborexant、clobazam 的 ARTG 条目；加拿大 DPD 第六批写入 clobazam、riluzole、edaravone、betahistine、flunarizine 的 Marketed 产品示例。
**TGA 与加拿大 DPD 第六轮（同日）**：澳大利亚 TGA 第六批写入 alprazolam、diazepam、midazolam、oxcarbazepine、lecanemab、donanemab、amantadine、levodopa、pramipexole、ropinirole、rasagiline、safinamide 的 ARTG 条目；加拿大 DPD 第七批写入 17 份 Marketed 产品示例，含 alprazolam、bromazepam、diazepam、flurazepam、midazolam、oxcarbazepine、lecanemab、donanemab、trihexyphenidyl、amantadine、levodopa、bromocriptine、pramipexole、ropinirole、selegiline、rasagiline、safinamide。
**TGA 与加拿大 DPD 第七轮（同日）**：澳大利亚 TGA 第七批写入 dexmedetomidine、fomepizole、mirabegron、oxybutynin、sodium-oxybate、sodium-thiosulfate、solifenacin、esketamine 的 ARTG 条目；加拿大 DPD 第八批写入 12 份 Marketed 产品示例，含 darifenacin、dexmedetomidine、fesoterodine、fomepizole、mirabegron、oxybutynin、sodium oxybate（XYREM）、sodium thiosulfate、solifenacin、tolterodine（DETROL）、trospium、milnacipran（FETZIMA）。兽医产品已排除。
**TGA 与加拿大 DPD 第八轮（同日）**：TGA 第八批写入 amifampridine（RUZURGI）与 amisulpride（AMISULPRIDE SCP）的 ARTG 条目。加拿大 DPD 第九批在站点限速下仅完成 12/20 个活性成分，写入 amifampridine（FIRDAPSE）与 chloral hydrate（CHLORAL HYDRATE SYRUP ODAN）；其余 8 个留待下次。
**TGA 与加拿大 DPD 第九轮（同日）**：澳大利亚 TGA 第九批写入 eszopiclone、fampridine、flumazenil 与 ginkgo 的 ARTG 条目；加拿大 DPD 第十批写入 dexamfetamine（APO-DEXTROAMPHETAMINE）、eszopiclone（LUNESTA）、fampridine（FAMPYRA）与 flumazenil 注射剂的 Marketed 产品示例。eslicarbazepine 连接超时、flavoxate 未完成，留待下次。
**TGA 与加拿大 DPD 第十轮（同日）**：TGA 第十批写入 droperidol（DROPERIDOL MEDSURGE）、reboxetine（EDRONAX）与 thiopental（OMEGAPHARM THIOPENTAL SODIUM）的 ARTG 条目。加拿大第十一批无新增：lithium 此前已写入，pentobarbital 的在售条目为兽用制剂。
**TGA 与加拿大 DPD 第十一轮（同日）**：TGA 第十一批 14 个药名全部未解析到 ARTG 条目；加拿大第十二批仅 nitrazepam（MOGADON）命中并写入，其余未捕获人用示例，lofexidine 与 opipramol 未完成。
**EMA 第 30 条转介补读（同日）**：EPAR 地址未命中的 quetiapine 与 risperidone，改从 EMA 第 30 条转介文件读取统一适应证并写入档案。另评估 medicines.ie（basic 档案药物多未在爱尔兰授权）与俄罗斯 ГРЛС（图形验证码阻断）两个来源，本轮未取得数据。
**TGA 与加拿大 DPD 第十二轮（同日）**：TGA 第十二批仅 dosulepin（DOSULEPIN VIATRIS）写入 ARTG 条目；加拿大第十三批 10 个活性成分均未捕获人用 Marketed 示例。
**爱尔兰 HPRA SmPC 补检索（同日）**：通过 medicines.ie 对 16 个药名检索并读取首个 SmPC 的 4.1 适应证，flupentixol（Depixol）、zuclopenthixol（Clopixol）与 sulpiride（Dolmatil）写入爱尔兰适应证。clopenthixol 命中 Clopixol（活性成分为 zuclopenthixol）、perazine 命中 Stelazine（活性成分为 trifluoperazine），两处按错配排除。
**爱尔兰 HPRA SmPC 第二、三批（同日）**：medicines.ie 浏览器端间歇返回空页，改直接 HTTP 抓取，并从 SPC 页面内嵌 PDF 提取 4.1 节原文。23 份档案写入爱尔兰适应证，覆盖抗抑郁药、催眠药、抗焦虑药与抗精神病药。amitriptyline、clomipramine、imipramine、fluoxetine、buspirone、hydroxyzine、propranolol、diazepam、clonazepam、dosulepin、opipramol 在该目录检索为 0 条，未写入。carbamazepine 与 valproate 的 PDF 未抽到 4.1 正文，留待重试。
**basic 档案现行标签可得性复核（2026-11-12）**：128 份 `basic` 逐份向 medicines.ie 与 DailyMed 现行 SPL 接口检索，另取 11 个日文名查 PMDA 现行添付文書索引。仅得兽用标签、膳食补充剂标签、停售产品标签与实体错配，未取得可用的人用现行标签；按现行证据规则不得升级 `reviewed`，状态维持 `basic`，检索事实记入 [逐名检索记录](catalog/retrieval-log-2026-11.md) §4.31。
**历史标签规则修订与三份升级（2026-11-12）**：经确认修订证据口径，AGENTS.md 与 STYLE.md 允许已撤市产品的官方历史标签正文支撑 `reviewed`，须逐处标注「历史标签」、版本日期与产品状态。secobarbital（美国 SECONAL SODIUM，2007 存档 SPL）、niaprazine（法国 NOPRON RCP，2005-10-24 版）、brexanolone（美国 ZULRESSO，2024-07-19 存档版本）三份升级为 `reviewed`，并补入适应证、给药、禁忌与警示条款。状态合计 `reviewed` 249→252、`basic` 128→125。检索细节见 [逐名检索记录](catalog/retrieval-log-2026-11.md) §4.32。
