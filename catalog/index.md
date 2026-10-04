# 精神药物分类目录索引

> 基准 WHO ATC/DDD Index 2026 ｜ 核查 2026-10-04 ｜ 首轮导入与身份纠错已完成；少量收尾见 [PLAN.md](../PLAN.md)

## 1. 数量口径

编码数、文件数与完成分析数分别统计，不互相代替。

| 口径 | 数量 | 含义 |
| --- | --- | --- |
| 官方五级 ATC 编码 | 294 | 六个治疗组逐条核对的基准 |
| 建立的药物档案 | 280 | 单方与成分明确的固定复方 |
| 其中成分明确的固定复方 | 5 | 官方条目点名全部成分 |
| ATC 复方类别（不建档） | 13 | 官方条目未指明全部成分，仅分类记录 |
| 目录占位编码（不建档） | 1 | 非具体药物 |
| 完成机制与临床分析 | 0 | 本轮未开展 |
| 跨组选录条目 | 42 | 见 related.md，均未建档 |

档案状态一律 `indexed`（仅核实身份与分类）。

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
7. **机制、获批用途与安全警告全部未录入**，未逐药核对 Drugs@FDA、DailyMed、EMA、NMPA 资料。
8. **跨组 42 条选录未建档**；所有选录编码均取自官方抓取，「收录依据」列只陈述官方分类位置与选录动机，涉及的适应证、受体机制、上市与管制状态、研发阶段一律标注待核实。唯一的例外性陈述是 nalmefene 的欧盟批准用途与「须配合持续心理社会支持」条件，已核对 EMA 产品资料页面；该页面不含受体亚型作用，故 `μ/δ 拮抗、κ 部分激动` 仍列为待核实。加巴喷丁、普瑞巴林的官方归属尚待核实。
9. 未发现同一 Wikidata 物质条目对应多个官方编码的情形。

## 6. 目录

- [N05A.md](N05A.md)｜ANTIPSYCHOTICS｜编码 70，档案 70，复方类别 0
- [N05B.md](N05B.md)｜ANXIOLYTICS｜编码 39，档案 36，复方类别 3
- [N05C.md](N05C.md)｜HYPNOTICS AND SEDATIVES｜编码 76，档案 68，复方类别 7
- [N06A.md](N06A.md)｜ANTIDEPRESSANTS｜编码 68，档案 68，复方类别 0
- [N06B.md](N06B.md)｜PSYCHOSTIMULANTS, AGENTS USED FOR ADHD AND NOOTROPICS｜编码 38，档案 38，复方类别 0
- [N06C.md](N06C.md)｜PSYCHOLEPTICS AND PSYCHOANALEPTICS IN COMBINATION｜编码 3，档案 0，复方类别 3
- [related.md](related.md)｜跨组选录 42 条，均未建档

`drugs/` 共 280 份档案。建档数量不等于完成分析的数量。

