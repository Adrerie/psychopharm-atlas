# 精神药物分类目录索引

> 基准 WHO ATC/DDD Index 2026 ｜ 目录核查 2026-10-04 ｜ 首轮导入与身份纠错已完成；280 份档案均已填写中国麻醉药品／精神药品管制字段，逐项目录已核对；对具有可核对单一结构的候选已完成四类整类列管的 RDKit 标准结构复核（2026-10-07），无法执行结构核查的条目已转为待核实；单药样板（快速判断页＋场景评分＋一个专题分析）见 [喹硫平](../drugs/quetiapine.md) 与 [PLAN.md](../PLAN.md)

## 1. 数量口径

编码数、文件数与完成分析数分别统计，不互相代替。

| 口径 | 数量 | 含义 |
| --- | --- | --- |
| 官方五级 ATC 编码 | 294 | 六个治疗组逐条核对的基准 |
| 建立的药物档案 | 280 | 单方与成分明确的固定复方 |
| 其中成分明确的固定复方 | 5 | 官方条目点名全部成分 |
| ATC 复方类别（不建档） | 13 | 官方条目未指明全部成分，仅分类记录 |
| 目录占位编码（不建档） | 1 | 非具体药物 |
| 完成机制与临床分析 | 25 | 喹硫平（精简主条目 [`drugs/quetiapine.md`](../drugs/quetiapine.md) ＋ 专题分析 [`analysis/quetiapine-dose-pk-pd.md`](../analysis/quetiapine-dose-pk-pd.md)）＋ Wave 1 Batch A 四份：[氯氮平](../drugs/clozapine.md)、[氟西汀](../drugs/fluoxetine.md)、[阿普唑仑](../drugs/alprazolam.md)、[哌甲酯](../drugs/methylphenidate.md)＋ Batch B 四份：[奥氮平](../drugs/olanzapine.md)、[度洛西汀](../drugs/duloxetine.md)、[地西泮](../drugs/diazepam.md)、[托莫西汀](../drugs/atomoxetine.md)＋ Batch C 四份：[阿立哌唑](../drugs/aripiprazole.md)、[锂盐](../drugs/lithium.md)、[丁氨苯丙酮](../drugs/bupropion.md)、[唑吡坦](../drugs/zolpidem.md)；均为状态 `reviewed`，核查 2026-10-07 ＋ Wave 2 Batch A 四份：[舍曲林](../drugs/sertraline.md)、[艾司西酞普兰](../drugs/escitalopram.md)、[帕罗西汀](../drugs/paroxetine.md)、[氟伏沙明](../drugs/fluvoxamine.md)＋ Batch B 四份：[文拉法辛](../drugs/venlafaxine.md)、[米氮平](../drugs/mirtazapine.md)、[曲唑酮](../drugs/trazodone.md)、[沃替西汀](../drugs/vortioxetine.md)＋ Batch C 四份：[利培酮](../drugs/risperidone.md)、[帕利哌酮](../drugs/paliperidone.md)、[氟哌啶醇](../drugs/haloperidol.md)、[氨磺必利](../drugs/amisulpride.md)（状态均为 `reviewed`，核查 2026-10-08） |
| 中国管制字段已填写 | 280 | 已确认逐项目录命中 67；203 份经启发式预筛与 RDKit 标准结构复核一致排除四类整类范围；待核实 10（身份／适用范围 3＋整类结构范围边界 4＋无单一结构式可核查 3） |
| 跨组选录条目 | 42 | 见 related.md，均未建档 |

除上述 25 份为 `reviewed` 外，其余 255 份档案状态仍为 `indexed`（仅核实身份与分类）。

## 2. 身份来源覆盖

Wikidata 以 ATC 编码（P267）命中 260 条（88.4%），以名称命中 13 条，名称检索多候选而无独立物质条目 1 条（brexanolone），Wikidata 未能匹配 20 条。**此处的 20 条仅表示 Wikidata 交叉链接缺口，不代表其他公开来源或 RxNorm 均未命中。**

| 组 | 官方名称 | 编码 | 档案 | 复方类别 | ATC 命中 | 名称命中 | Wikidata 零命中 | 中文标签 | 有 DDD |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [N05A](N05A.md) | ANTIPSYCHOTICS | 70 | 70 | 0 | 67 | 1 | 2 | 36 | 61 |
| [N05B](N05B.md) | ANXIOLYTICS | 39 | 36 | 3 | 35 | 1 | 3 | 23 | 24 |
| [N05C](N05C.md) | HYPNOTICS AND SEDATIVES | 76 | 68 | 7 | 60 | 7 | 9 | 55 | 49 |
| [N06A](N06A.md) | ANTIDEPRESSANTS | 68 | 68 | 0 | 63 | 3 | 1 | 54 | 49 |
| [N06B](N06B.md) | PSYCHOSTIMULANTS, AGENTS USED FOR ADHD AND NOOTROPICS | 38 | 38 | 0 | 35 | 1 | 2 | 28 | 17 |
| [N06C](N06C.md) | PSYCHOLEPTICS AND PSYCHOANALEPTICS IN COMBINATION | 3 | 0 | 3 | 0 | 0 | 3 | 0 | 0 |
| 合计 | — | 294 | 280 | 13 | 260 | 13 | 20 | 196 | 200 |

官方结构核对与首轮一致：三级治疗组清单（N05 → N05A/N05B/N05C；N06 → N06A/N06B/N06C/N06D）与抓取结果一致，43 个页面的五级条目行与页面编码链接逐一比对无缺漏。N06D 归入[跨组清单](related.md)。

## 3. 本轮修补内容

1. **取消按名称归并**。`N05BC51` 与 `N05CX01` 名称相同但分属抗焦虑药复方与镇静催眠药复方两个亚组，现各自保留一行分类记录，不再共用档案；同名、同一主要成分或多个 ATC 编码均不足以证明两者是同一制剂。
2. **复方对象分级**。5 条成分明确的固定复方保留档案；13 条形如 `X, combinations`、`combinations of X` 或 `X and psycholeptics` 的条目属未指明全部成分的 ATC 分类，改为目录内分类记录并从 `drugs/` 移除；`N05CB02` 仍为目录占位编码。
3. **同名歧义处理**。按实体类型（P31）剔除文章后，`esketamine`、`lemborexant`、`levomilnacipran`、`solriamfetol` 已链接到相应物质条目。依据 [DailyMed 的 ZULRESSO 标签第 11 节](https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=b40f3b2a-1859-4ed6-8551-444300806d13)，`brexanolone` 在化学上与内源性 allopregnanolone 相同，因此档案链接 [allopregnanolone（Q2482223）](https://www.wikidata.org/wiki/Q2482223) 作为化学关联，不将其视作独立药品制剂记录。
4. **别名与中文标签**。`(+)-Zopiclone`、`(+)-citalopram`、`(-)-modafinil`、`(-)-sulpiride` 已依据对应 [PubChem](https://pubchem.ncbi.nlm.nih.gov/) 物质记录恢复为有来源的对映体别名，且注明其与外消旋体的区别；`lorazepam` 的错误别名清理及 MeSH 依据保留。中文标签覆盖 196/280，均标明 Wikidata 语言变体，不视作监管核准名称。
5. **档案精简**。压缩重复声明与清一色的待核实章节，系统命名改为节选并注明条数；保留编码、类型、核实过的别名、标识符、官方 DDD 原文、来源与纠错说明。

## 4. 数据来源

**WHO ATC/DDD Index 2026**（https://atcddd.fhi.no/atc_ddd_index/）：43 个页面，294 个五级编码与 37 个亚组名称，页面标注更新时间 2026-01-20。完整电子表格须向权利方订购，未使用。

**Wikidata**（CC0）：37 个亚组分片查询 P267 得 278 条绑定 / 266 个条目；第二趟取回条目全部 ATC、中文标签、P279 与英文维基指针；第三趟对官方有而编码未命中的 32 个名称改用实体检索。属性经逐项核对：P267 ATC、P662 PubChem CID、P486 MeSH 描述符、P715 DrugBank ID（P661 为 ChemSpider、P668 为 GeneReviews、P627 为 IUCN，未采用）。

**RxNorm**：改用 NLM 公共 REST 接口 `rxnav.nlm.nih.gov`（无需凭据）后，275 个单一成分官方名中 222 个解析到 RXCUI，抓取时间 2026-10-04。其中 24 个名称的 RxNorm 首选名与官方名不同（如 amfetamine→amphetamine、dosulepin→dothiepin、clomethiazole→chlormethiazole、potassium clorazepate→clorazepate dipotassium），属美/国际命名差异；53 个未解析，多为未在美国上市或已撤市的品种。此前经 `lhncbc.nlm.nih.gov` 的 API 与 *Current Prescribable Content* 下载仍返回 HTTP 403，原因未定；不能据此推断必须申请密钥，完整的 RxNorm 发布包另涉 UMLS 账户与来源许可。

**English Wikipedia**：11 个类别页面 1740 条条目名用于覆盖比对，重定向仅 5 条，名称变体补充有限；正文属 CC BY-SA 4.0，未复制。

**PubChem / MeSH / DrugBank**：标识符取自 Wikidata 声明并保留原链接；PubChem PUG REST 可用，DrugBank 页面对自动请求返回 403（其链接经 301 跳转仍有效）。

## 5. 剩余问题

1. `brexanolone`（`N06AX29`）与内源性 allopregnanolone 的**化学同一性已由 DailyMed 药品标签确认**，现关联 Wikidata Q2482223；Wikidata 仍无独立的 brexanolone 物质/产品条目，具体制剂、监管状态和适用地区待后续分析。
2. **20 条官方编码在本轮 Wikidata 交叉核对中未命中**；其中多项是泛指复方分类。RxNorm 已独立匹配部分名称，不能据此称为全部公开来源零命中；未匹配的身份信息和监管状态留待逐项核实。
3. **13 条 ATC 复方类别无具体成分**，`N06CA01`–`N06CA03` 等以类别词（psycholeptics）作为配对成分，须取得具体制剂组成证据后才能建立复方档案。
4. **中文标签 196 条全部未经监管核对**，其余 84 条无中文标签；须以 NMPA 等官方入口逐条确认。
5. **Wikidata 分类滞后**：`suvorexant` 条目仍标 `N05CM19`（官方 `N05CJ01`），`esketamine` 物质条目只带 `N01AX14`；维基数据另有把三/四级类别当作带 P267 条目的情形（`N05AN`、`N05BA`、`N05BC`、`N05CD`、`N05CH`、`N06AB`、`N06AF`）。
6. **80 份档案无官方 DDD**（官方索引未给出统计剂量）。
7. **中国管制字段已覆盖 280/280；四类整类列管的结构阴性结果已经 RDKit 标准工具复核，10 份保留待核实。** 逐项目录已确认命中 67 份，并保留盐、立体异构体、原料药／注射剂、单方制剂等原文范围。203 份在逐项列名与芬太尼类、合成大麻素类、尼秦类、奥啡类四个整类的官方结构定义上均不落入（启发式预筛与 RDKit 子结构复核结论一致，规则先用母体和已知整类成员验证），写“未发现列入上述现行目录（核查至 2026-10-06）”；该表述仍不含处方、携带、进出口等其他限制。待核实 10 份分三类：身份／适用范围问题 3 份——`hexobarbital`、`lisdexamfetamine`、`bupropion and dextromethorphan`；整类结构范围边界 4 份——`pimozide`、`benperidol` 的母核与奥啡类母体溴啡一致、`fluspirilene` 的母核与母体螺溴啡一致，RDKit 复核同样命中，三者差异恰落在公告条件（二）（五）列举的哌啶氮取代基替换上，而该整类载于《非药用类麻醉药品和精神药品目录》并另设“发现医药等合法用途予以调整”条款，未检索到针对这些药物的公开调整、豁免或具体监管认定，实际归属待主管部门确认；`pimavanserin` 属芬太尼类结构定义的真正边界案例（哌啶氮甲基替换符合条件（四），但芳基经亚甲基连接、丙酰基换为脲羰基，两项差异均不在公告列举范围内）；无单一结构式可核查 3 份——`Valerianae radix`、`Hyperici herba`、`Lavandulae aetheroleum` 为多组分天然产物，结构核查无法执行。结构核查方法与限制见 [SOURCES.md](../SOURCES.md#整类列管的结构定义结构核查基准)。本轮不涉及易制毒化学品、兴奋剂目录、地方性规定与进出口规则。
8. **除喹硫平、Wave 1 的十二份（Batch A 氯氮平、氟西汀、阿普唑仑、哌甲酯；Batch B 奥氮平、度洛西汀、地西泮、托莫西汀；Batch C 阿立哌唑、锂盐、丁氨苯丙酮、唑吡坦）与 Wave 2 的十二份（Batch A 舍曲林、艾司西酞普兰、帕罗西汀、氟伏沙明；Batch B 文拉法辛、米氮平、曲唑酮、沃替西汀；Batch C 利培酮、帕利哌酮、氟哌啶醇、氨磺必利）外的 255 份档案未录入机制、获批用途与安全警告**，未逐药核对 Drugs@FDA、DailyMed、EMA、NMPA 资料。喹硫平条目改用美国 DailyMed 标签与英国 emc 药品数据库的 SmPC 完成核查；国家药监局药品审评中心《2023年度药品审评报告》（2024-02）附件 5 已确认南通联亚药业股份有限公司的富马酸喹硫平缓释片为首次批准上市并纳入优先审评审批程序，但该名单不含批准文号、规格与适应证，这些字段仍待核准说明书（NMPA 数据查询与 CDE 目录集入口返回脚本／处理中校验页），本轮对 EMA 的 seroquel、qsmia 等条目及产品信息 PDF 直接查询均返回 404，未能定位该分子的中央评估文件，因此欧盟其他成员国的国家批准文本未核对（该分子的获批状态按地区与剂型分列，见 [喹硫平 §4 与证据边界 §10](../drugs/quetiapine.md)）。Batch A 四份同样以美国现行标签（DailyMed set_id＋生效日）与英国 emc SmPC 为监管事实主干，并按需补 NICE 指南与系统综述；**四份的中国批准信息全部未取得**（NMPA 恒返回 HTTP 412、CDE 返回 202 脚本校验页），因此各条目把中国上市状态与核准适应证明确标为待核实，未使用商业药品库补足；氯氮平与氟西汀的欧盟集中授权检索为否定命中，成员国国家许可未逐国核对。 Batch B 四份沿用同一取证顺序（美国现行标签 set_id＋生效日 → 英国 emc SmPC／NICE → 系统综述），其中国行批准状态：地西泮已取得英国 SmPC（PL 06464/1400，文本修订 2025-11-11，含与美国口服标签不等价的禁忌表）与英国管制定级，奥氮平、度洛西汀、托莫西汀同样取自 emc；**四份的中国批准信息仍全部未取得**（NMPA HTTP 412、CDE 202 脚本校验页），均标为待核实而不用商业库补足。Batch C 四份沿用同一取证顺序，并已完成英国文本核对：阿立哌唑取自 emc Abilify SmPC（英国无抑郁辅助、孤独症与 Tourette 适应证），锂取自 Priadel 400 SmPC 与 NICE CG185（英国适应证比美国更宽、但**不推荐儿童**且把哺乳列为禁忌，与美国"不推荐"相反），丁氨苯丙酮取自 Zyban SmPC（2026-08-28 修订，英国仍有效）；美国 ZYBAN 品牌虽在 Drugs@FDA 记为 Discontinued，但当前仍有安非他酮 SR 仿制产品以戒烟为获批适应证，品牌状态与活性成分产品线已在条目内分开说明，唑吡坦取自 emc 3975 SmPC（英国把阻塞性睡眠呼吸暂停、重症肌无力与重度肝损列为禁忌，美国仅为警示；英国限疗程≤4 周含减停，美国无周数上限）。**四份的中国批准信息同样未取得**（NMPA HTTP 412、CDE 脚本校验页；丁氨苯丙酮连中国上市状态都未能确认）。Wave 2 Batch A（SSRI 对照，核查 2026-10-08）四份均已改为 `reviewed`：舍曲林取自美国片剂现行标签（setid 42120ff8-b353-4632-9ea9-54de9a698724，生效 2025-10-14）与英国 emc 文本；艾司西酞普兰取自原研（setid 13bb8267-1cab-43e5-acae-55a4d957630a）与仿制（setid 9ddd1f24-3ebd-4307-bb23-6acd742cd140）两条美国产品线加英国 emc 101944（PL 49445/0353，修订 2025-06-13）——同分子不同持有人的 GAD 年龄口径不同，QT 处理也不同（美国 §5 无 QT 警告、英国 §4.3 把已知 QT 延长与先天性长 QT 列为禁忌）；帕罗西汀取自速释／控释／低剂量潮热三条美国产品线加旧式仍现行标签与英国 Seroxat emc 7593（PL 10592/0001，修订 2025-04-04）——PMDD 只属控释线、潮热线把妊娠写成禁忌；氟伏沙明取自美国速释与缓释两条线加英国 Faverin emc 1169（PL 46302/0034，修订 2026-02），其美国 §1 只有强迫症而无抑郁，英国 §4.1 同时含抑郁发作与强迫症。**四份的中国批准信息同样全部未取得**（NMPA 恒 HTTP 412、CDE 返回脚本校验页），均未使用商业药品库补足；中国管制字段沿用 2026-10-06 的既有核查结果，本轮未重新审计。四份均未新增专题分析：批次内需要并列的冲突（儿童青少年荟萃两套结论、美英禁忌与洗脱期差异、原研与仿制适应证口径不同）都在主条目 §2.2 与 §10 内就近呈现，另建文件只会把同一证据拆散。Wave 2 Batch B（其他常见抗抑郁药，核查 2026-10-08）四份均改为 `reviewed`：文拉法辛取自美国三条现行产品线——缓释胶囊（ANDA212277，setid c41d847b-88ba-49a5-9d73-269ac4caa4ed，生效 2026-09-03）、速释片（ANDA078932，setid e14bfb9f-3bd2-4419-9294-9c286e79730a，生效 2026-08-28，旧式章节）与缓释片（ANDA209193，setid 38431a76-6185-4c17-994f-8278b6cd7510，生效 2026-09-18）——**三线适应证集合互不覆盖**（胶囊 MDD／GAD／SAD／PD、速释片仅 MDD、缓释片仅 MDD／SAD），英国取 emc 1219 Efexor XL（PL 46302/0280，修订 10/2025）与 emc 764 速释片（PL 14017/0121，修订 2025-12-10），英国抑郁最大剂量 375 mg 高于美国缓释胶囊的 225 mg，且英国 §4.4 给出停药期不良事件 31% 对安慰剂 17%、§4.6 提出 PPHN"不能排除"而美国三线标签均无 PPHN 条目；米氮平取自美国 REMERON／REMERONSolTab（NDA020415／NDA021208，setid 98ad1917-a094-44f5-a28f-a64a8cfcd887，生效 2025-08-06）与英国 emc 100723（PL 49445/0214，修订 2026-03-13），美国标签**没有 §9 滥用与依赖章节**，英国 §4.8 脚注写明"减量一般不减少嗜睡／镇静但可能危及抗抑郁疗效"；曲唑酮取自美国片剂（ANDA072193，setid a57da4f8-151d-4a74-8710-6158d1da3852，生效 2026-09-03）与 RALDESY 口服溶液（NDA218637，setid 34708cc1-b0b2-4fd0-b9f3-7f008b457fc9，生效 2026-09-01）加英国三份 emc SmPC（4975／13126／12505），**本轮核对的 102 份美国曲唑酮片标签 §1 中 "insomnia" 命中为 0**，而三种英国产品 §4.1 措辞互不相同；沃替西汀取自美国 Trintellix（NDA204447，setid 1a5b68e2-14d0-419d-9ec6-1ca97145e838，生效 2025-03-05）与英国 emc 10441 Brintellix（PLGB 00458/0296 等，修订 05/2026），两侧 MAOI 洗脱期不一致（美国停本药后 21 天、英国 14 天），哺乳口径相反（美国"无人乳数据"、英国"RID 估计低于 2%"），美国无骨折条目而英国按 SSRI／TCA 类别信号记载。**四份的中国批准信息同样全部未取得**（NMPA 恒 HTTP 412、CDE 返回脚本校验页），均未使用商业药品库补足；中国管制字段沿用 2026-10-06 的既有核查结果。Batch B 新增 1 份专题（[`trazodone-insomnia-offlabel.md`](../analysis/trazodone-insomnia-offlabel.md)）：只有曲唑酮存在"批准状态、处方行为与指南立场三层互相冲突、且荟萃与 PSG 结局方向不一致"的独立研究问题，其余三份的分歧均可在主条目 §2.2／§10 就近呈现，故未机械配平文件数。Wave 2 Batch C（典型与非典型抗精神病药对照，核查 2026-10-08）四份均改为 `reviewed`：利培酮取自美国七条现行产品线中的六条代表——口服常释（NDA020272／020588／021444，setid 7e117c7e-02fc-4343-92a1-230061dfc5e0，生效 2026-05-28）、仿制口服溶液（ANDA078452，setid c4582bdf-5eda-438c-98b4-0517500501e8）、CONSTA（NDA021346，setid bb34ee82-d2c2-43b8-ba21-2825c0954691）、RYKINDO（NDA212849，山东绿叶，setid 58534c96-96f5-4c2e-a061-92d4506aee91）、UZEDY（setid 734eb776-4be0-4808-834b-0d8b0f9e021e）与 PERSERIS（setid a4f21b1a-5691-4b14-a56d-651962d06f39）——**PERSERIS 只有成人精神分裂症，其余长效线含双相 I 维持而无急性躁狂**；英国取 emc 11872（PL 04416/0663，Sandoz）、6936（Rosemont，修订 2025-09-09）、1690（PL 00242/0375，Janssen-Cilag）与 13777（OKEDI，Orion／Rovi），英国 §4.1 批准**痴呆持续性攻击与 5 岁起品行障碍攻击各≤6 周**，而美国黑框写"未批准用于痴呆相关精神病"。帕利哌酮取自美国五条产品线（INVEGA NDA021999 setid 7b8e5b26-b9e4-4704-921b-3c3c0d159916；SUSTENNA NDA022264 setid 1af14e42-951d-414d-8564-5d5fce138554；TRINZA 与 HAFYERA 同 NDA207946，setid c39e65d7-fa44-4e4c-8b12-a654d3ed0eae 与 6cd61892-d2cb-434d-83ed-5c1b2c4e7a0b；ERZOFRI NDA216352，山东绿叶，setid 492bf9dd-868e-421a-92db-8cca8973aac1）与英国 Xeplion（emc 7652，PLGB 00242/0711，修订 2023-08-09）——**TRINZA／HAFYERA 只有精神分裂症且以先前长效充分治疗为启用前提，英国适应证只写"稳定后的维持治疗"**；美国以棕榈酸盐计数、英国以碱基计数（英国 §2 自给 234 mg 盐＝150 mg 碱基），SUSTENNA 与 ERZOFRI 的启动方案不同（234 mg＋第 8 天 156 mg、5 周后维持 对 351 mg 单针、4 周后维持）。氟哌啶醇取自美国三份（片剂 Mylan setid c559b0b0-4087-d12a-e718-c18ccb6811e6，生效 2025-01-15；注射液 HealthFirst setid beb6d1cf-98db-d0a5-e053-2995a90ace90；癸酸酯 Zydus setid 6d2d7612-ad47-4ee7-a42c-945c976d947b，生效 2026-07-10）加口服溶液（Lannett setid 3e44fed0-6132-4881-a9cd-af6156c7af9c），英国取 emc 10907（PL39307/0025，Syri，修订 2022-12-16）、100592（PLGB 56809/0003，Galvany，修订 2025-03-24）、15245（HALDOL Decanoate，Essential Pharma，修订 2023-09-12）与 9868（200 微克/mL 儿童低浓度口服液）——**美国口服允许"部分病例可需 100 mg/日"，英国封顶 20 mg/日；英国把已知 QTc 延长与先天性长 QT 列为禁忌、把帕金森病＋路易体痴呆＋进行性核上性麻痹三项同时列为禁忌，美国片剂只列帕金森病**；美国写"未批准静脉给药"，英国写"推荐仅供肌内，若静脉给药必须持续 ECG 监测"；美国片／注射／口服液为旧式无编号章节且**四类标签均无滥用与管制章节**，故条目未写"非管制"。氨磺必利取自美国 BARHEMSYS（NDA209510，Acacia Pharma，setid ab23bc6e-b6a8-165f-e053-2a95a90ab144，生效 2026-06-17）与英国 14 份口服 SmPC 中核对的两份代表（emc 548 的 50 mg 片、emc 101726）——**同分子在两法域几乎无适应证交集：美国只有术后恶心呕吐的预防与治疗（5 mg／10 mg 单次静脉，且 §10 加注"未批准口服给药"），英国只有精神分裂症并给 50–300 mg/日的阴性症状剂量带**；美国给出定量 QT（5 mg ΔΔQTcF 5.0 ms、40 mg 23.4 ms），英国不给数值而改为给药前排除四项风险因素＋禁忌级合并用药清单（催乳素依赖性肿瘤、嗜铬细胞瘤、15 岁以下、左旋多巴与致 TdP 药物）。**四份的中国批准信息同样全部未取得**（NMPA 恒 HTTP 412、CDE 返回脚本校验页），均未使用商业药品库补足；中国管制字段沿用 2026-10-06 的既有核查结果。Batch C 新增 1 份专题（[`paliperidone-prolactin-evidence.md`](../analysis/paliperidone-prolactin-evidence.md)）：该页只回答"帕利哌酮与利培酮的催乳素抬升孰高"，因为美国标签（写"与利培酮相似"）、两代网络荟萃（均把帕利哌酮列为网络极值、摘要未给利培酮数值）与中国上海住院队列（利培酮 HR 2.70 对帕利哌酮 1.84，氨磺必利 2.76 居首）三层方向不一致且结局定义不同，主条目一行无法承载；利培酮、氟哌啶醇与氨磺必利的分歧继续在主条目 §2.2／§10 就近呈现。另需记入本批的取证事实：2026-10-08 经 Europe PMC 取回 PMID:40830714（*CNS Drugs* 2025;39(12):1317-1330，上海住院 EMR 2007–2019，6,489 名精神分裂症患者，NCT04002258）的九药催乳素升高风险比，为本目录首个中国人群实测安全性锚点，已写入帕利哌酮与氨磺必利条目并建页；Leucht 2013 与 Huhn 2019 的网络数值本轮按摘要原文复核（帕利哌酮 SMD 0.50、催乳素 +48.51 ng/mL；氟哌啶醇 EPS OR 4.76 与全因停药 OR 0.80 为网络最差；氨磺必利阳性症状 −0.69 为网络最佳）。本 Wave 已为 5 份主条目各建 1 个问题导向专题（[`lithium-long-term-outcomes.md`](../analysis/lithium-long-term-outcomes.md)、[`diazepam-formulation-pk.md`](../analysis/diazepam-formulation-pk.md)、[`zolpidem-next-day-impairment.md`](../analysis/zolpidem-next-day-impairment.md)、[`aripiprazole-formulation-pd-safety.md`](../analysis/aripiprazole-formulation-pd-safety.md)、[`bupropion-pk-risk.md`](../analysis/bupropion-pk-risk.md)），内容是上一轮压缩时删掉的证据而非主条目扩写；未新增数据库、CI、评分程序或爬虫。
9. **跨组 42 条选录未建档**；所有选录编码均取自官方抓取，「收录依据」列只陈述官方分类位置与选录动机，涉及的适应证、受体机制、上市与管制状态、研发阶段一律标注待核实。nalmefene 的欧盟获批用途与心理社会支持要求依据 EMA 产品资料页面，μ/δ 受体拮抗和 κ 受体部分激动的体外结果依据 [EMA 正式产品说明书第 5.1 节](https://www.ema.europa.eu/en/documents/product-information/selincro-epar-product-information_en.pdf)；其余临床与机制结论尚待逐药核实。加巴喷丁、普瑞巴林的官方归属尚待核实。
10. 未发现同一 Wikidata 物质条目对应多个官方编码的情形.

## 6. 目录

- [N05A.md](N05A.md)｜ANTIPSYCHOTICS｜编码 70，档案 70，复方类别 0
- [N05B.md](N05B.md)｜ANXIOLYTICS｜编码 39，档案 36，复方类别 3
- [N05C.md](N05C.md)｜HYPNOTICS AND SEDATIVES｜编码 76，档案 68，复方类别 7
- [N06A.md](N06A.md)｜ANTIDEPRESSANTS｜编码 68，档案 68，复方类别 0
- [N06B.md](N06B.md)｜PSYCHOSTIMULANTS, AGENTS USED FOR ADHD AND NOOTROPICS｜编码 38，档案 38，复方类别 0
- [N06C.md](N06C.md)｜PSYCHOLEPTICS AND PSYCHOANALEPTICS IN COMBINATION｜编码 3，档案 0，复方类别 3
- [related.md](related.md)｜跨组选录 42 条，均未建档

`drugs/` 共 280 份档案。建档数量不等于完成分析的数量。

