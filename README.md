# Psychopharm Atlas

**精神药理图谱 | An evidence-traceable psychopharmacology knowledge base**

Psychopharm Atlas 是一个以精神药理学为核心的开放阅读型知识仓库。主药物条目用于快速回答“它是什么、适应范围是什么、主要长期风险是什么、在什么场景下证据与负担是否相称”；详细 PK/PD、PET、受体占有率或原始试验数据只在确有分析价值时进入独立专题文件或直接链接原始来源。

项目以 WHO ATC/DDD 为基础分类索引，同时保留中国管制状态、法域批准差异、长期风险与按使用场景的证据评分。评分采用多维负担 + 场景适宜度，不生成单一总分，也不构成个体化用药建议。

## 项目文档

- [catalog/index.md](catalog/index.md)：分类目录索引与覆盖进度。
- [PLAN.md](PLAN.md)：Wave 1–15 的计划、完成与审阅修补记录。
- [HANDOFF.md](HANDOFF.md)：Wave 15 收尾后的接手状态、尚未解决的来源缺口和继续维护原则。
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

**历史阶段记录（截至 Wave 9，非当前统计）**：首轮目录与身份建档已完成。WHO ATC/DDD Index 2026 六个治疗组共 294 个五级编码已核对，核心六组 280 份档案与 25 份跨组主题档案均已建立，总计 305 份；中国管制字段已填写 305/305，自 Wave 13 起《非药用类麻醉药品和精神药品目录》完整 396 项已逐名核对（公安部原附件对本机仍返回 HTTP 521，改用政府门户转载的同一公告附件）。[喹硫平](drugs/quetiapine.md) 已完成“精简主条目 + 场景评分 + 必要专题分析”样板验证；Wave 1 把 12 个代表性药物（Batch A 氯氮平、氟西汀、阿普唑仑、哌甲酯；Batch B 奥氮平、度洛西汀、地西泮、托莫西汀；Batch C 阿立哌唑、锂盐、丁氨苯丙酮、唑吡坦）推进到 `reviewed`；[Wave 2 收尾记录](WAVE2-CLOSEOUT.md) 中记录的 8 组 32 份档案（Batch A 舍曲林、艾司西酞普兰、帕罗西汀、氟伏沙明；Batch B 文拉法辛、米氮平、曲唑酮、沃替西汀；Batch C 利培酮、帕利哌酮、氟哌啶醇、氨磺必利；Batch D 鲁拉西酮、齐拉西酮、卡利拉嗪、布瑞哌唑；Batch E 劳拉西泮、奥沙西泮、氯氮䓬、溴西泮；Batch F 艾司佐匹克隆、佐匹克隆、苏沃雷生、莱博雷生；Batch G 赖右苯丙胺、右苯丙胺、莫达非尼、索安非托；Batch H 阿戈美拉汀、艾司氯胺酮、阿米替林、丁螺环酮）已全部按批次逐药核查并**全部达到 `reviewed`（无一降为 basic）**。截至 Wave 9 审阅修补，reviewed 共 **147 份**，另有 **38 份**为 `indexed`、**95 份**为 `basic`（历史批次记录见 [目录索引](catalog/index.md)，当前状态以各药物档案顶部的状态字段为准）；[`analysis/`](analysis) 共 15 份问题导向专题（Wave 2 期间新增 9 份），配额制未使用、每份专题均对应一个具体的跨文件研究问题。未新增数据库、CI、评分程序或爬虫。仍存的共同缺口：中国 NMPA 与 CDE 官方入口在本轮全部返回拦截或脚本校验页，因此全部 147 份 reviewed 档案的中国上市与核准适应证均明确标注为待核实，未使用商业药品库补足；除美国 DailyMed／openFDA、英国 emc 与个别法域（溴西泮取法国 BDPM）外，其余法域未逐国核对；英国《2001 年药物滥用法规》附表归属、部分美国产品的审批日期与 EMA 中央文件仍未取得，相关条目内已逐项标注。[Wave 3](PLAN.md) 已一次处理 PLAN 列出的 24 份档案：23 份达到 `reviewed`（核查 2026-10-21），唯一保持 `basic` 的是 `flunitrazepam`——本轮未能取回任何法域的现行监管说明书文本；本 Wave 未新增专题文件，药物利用、处方规模与非医疗使用证据只在相关条目内纳入并注明地区、年份、人群与分母。[Wave 4](PLAN.md) 另处理 24 份：23 份达到 `reviewed`、`phenibut` 因三法域均无现行说明书可引保持 `basic`；监管事实一律按"产品＋法域＋文本版本"引用（美国 17 份取 DailyMed set_id＋生效日，英国 11 份取 emc 产品号＋PL＋文本修订日，法国 4 份取 BDPM CIS），取不到的法域写成检索事实而非"未获批"。[Wave 5](PLAN.md) 再处理 24 份：21 份达到 `reviewed`（核查 2026-10-22），`brexanolone`、`secobarbital` 与 `etizolam` 保持 `basic`，其中 ZULRESSO 的美国批准已由 FDA 正式公告确认于 2025-04-14 撤销，另外两份及 brexanolone 的其他法域仍缺可核对现行说明书；本轮法国 BDPM 全程返回 HTTP 503，无法国文本，英国 emc 现行 SmPC 成为 8 份条目的核心或补充锚点（含把 pimozide 的美英收载用途差异、chloral hydrate 的唯一美国记录实为顺势疗法产品这两项反差写进条目）；四份固定复方只用复方自身文本评分。[Wave 6](PLAN.md) 再处理 32 份旧药与地区性产品：18 份达到 `reviewed`、14 份保持 `basic`；审阅已定点修正监管公告日与撤销生效日、补入 opipramol 的 GAD 随机试验并去掉四处不合适的独立评分行；本轮把“官方批准／撤销记录”与“说明书索引”分开核对，NAVANE（2024）、Surmontil／Vivactil（2025）、Mellaril（2007）、CYLERT（2023 撤销、2005 停售）等撤销记录与美国“并非因安全或疗效撤出”的认定逐项分列；sertindole 以 EMA 第 36 条转介为轴、dimdazenil 以 2023 年中国批准公告为轴，均诚实标注说明书缺口。[Wave 7](PLAN.md) 处理 32 份抗焦虑药、植物药、早期抗抑郁药与地区性抗精神病药：11 份达到 `reviewed`、18 份 `basic`、3 份保留 `indexed`；法国 RCP 与西班牙 Ficha técnica 是主要锚点，并纠正两处实体错配（Defanyl 实为 amoxapine、西班牙 melitracen 记录为 Deanxit 复方）。[Wave 14](PLAN.md) 一次处理 N06D 与阿尔茨海默病相关候选 30 条：实际建档 29 份（8 份 `reviewed`、19 份 `basic`、2 份 `indexed`），`N06DA53`（多奈哌齐＋美金刚＋银杏叶）经检索未证实任何具体产品而**暂不建档**，只保留目录分类记录；本轮把“ATC 收录≠产品”、失败／暂停项目不设场景评分、AD 精神病症状治疗与疾病修饰候选分列、登记库张贴条目的终点性质核对作为硬要求。

**当前计划**：[Wave 15](PLAN.md) 已在独立分支 `plan/neuropsych-crossgroup-wave15` 一次完成 50 个跨组候选（下尿路与抗胆碱负担 13、前庭与眩晕 7、急性中毒与解毒 10、帕金森病与多巴胺能药物 10、神经退行性与神经肌肉疾病药物 10），按实际证据定级为 **40 份 `reviewed`、10 份 `basic`**，未强制升级；候选身份边界处理上，`meladrazine`（FDA SRS 将其映射至 hydramitrazine）与 `desfesoterodine`（官方描述为 tolterodine 代谢物）不纳入，改由 `meclizine` 与 `dimenhydrinate` 替换，两者按官方 `R06A` 抗组胺编码记录而非前庭主题编码。本轮未新增专题文件（`analysis/` 仍为 15 份），未新增数据库、CI、爬虫或评分程序。当前基线为 **218 reviewed / 7 indexed / 159 basic**（384 份药物档案：核心六组 280 份＋跨组主题 104 份）；跨组选录 91 条中已建档 89 条、未建档 2 条（`N07BC51` 复方类别、`N06DA53` 暂不建档）。50 条中国管制字段逐项复核四份现行目录与 2026-07-01 生效的 16 种非药用类增列附表，仅 sodium oxybate 命中第一类精神药品第 6 项 γ-羟丁酸；共同缺口仍是 NMPA HTTP 412／CDE 202 拦截，故中国上市与核准适应证全部标注待核实。Wave 15 已通过审阅修补与结构核对，下一阶段以合并后的 `main` 为基线，交接说明见 [HANDOFF.md](HANDOFF.md)，计划与完成记录见 [PLAN.md](PLAN.md)。

**Wave 16（2026-11-10，分支 `wave16/basic-upgrade`）**：Wave 15 收尾后剩余的 159 份 `basic` 全部按法域、具体产品与现行监管文本重做检索，其中 **27 份升级为 `reviewed`**（acetylleucine、biperiden、bromperidol、chlorprothixene、cinnarizine-and-dimenhydrinate、cinolazepam、cytisinicline、flunarizine、flunitrazepam、ginkgo-folium、hyperici-herba、imidafenacin、levomethadone、levosulpiride、medazepam、melperone、mexazolam、mosapramine、perazine、physostigmine、propiomazine、propiverine、prothipendyl、sertindole、sultopride、tofisopam、vinpocetine），其余保持 `basic` 并把检索范围与缺口写入各档案 §10。现基线为 **245 reviewed / 7 indexed / 132 basic**（384 份：核心六组 280＋跨组 104），专题仍 15 份。本轮同时按 [STYLE.md](STYLE.md) 完成全库语言审订，并修复了升级过程中被压缩的 5 条文献引用。中国 NMPA／CDE 入口仍返回 412／202，中国上市与核准适应证继续按待核实记录。
