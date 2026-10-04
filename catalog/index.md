# 精神药物分类目录索引

> 分类基准：WHO ATC/DDD Index 2026 ｜ 核查日期：2026-10-04  
> 首轮已完成公开数据导入、分类目录构建与身份建档；剩余分类、身份和结构问题见 [修补计划](../PLAN.md)。作用机制、获批适应证与安全性分析尚未录入。

## 1. 总体结果

| 环节 | 数量 | 说明 |
| --- | --- | --- |
| 官方目标五级条目 | 294 | 六个治疗亚组逐条核对 |
| 官方不同五级 ATC 编码 | 294 | 同名不意味着同一制剂，所有编码单独保留 |
| 已建立 Markdown 文件 | 292 | 一项目录占位未建档，两条同名 ATC 分类暂共用一份索引页 |
| 公开来源以 ATC 编码命中 | 260（88.4%） | Wikidata P267 携带官方编码 |
| 公开来源仅以名称命中 | 14 | 条目未携带对应 ATC 编码 |
| 公开来源零命中 | 20 | 档案身份仅由官方索引确认 |
| 有中文标签 | 192 | 取自 Wikidata 标签，非监管核准名称 |
| 有英文维基百科条目 | 264 | 仅作指针，未复制正文 |
| 官方索引列出 DDD | 200 | 其余条目官方未给出 DDD |

按名称初分：单方 275（其中植物药/多组分制剂 3）、复方类编码 18、目录占位编码 1。复方类编码中既有成分明确的固定复方，也有未指定全部成分的 ATC 分类，仍需逐项复核；292 个文件目前均为 `indexed`，不代表完成了临床分析。

## 2. 分组核对进度

| 组 | 官方名称 | 官方条目 | 档案 | ATC 命中 | 命中率 | 名称命中 | 零命中 | 中文名 | 维基条目 | 有 DDD |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [N05A](N05A.md) | ANTIPSYCHOTICS | 70 | 70 | 67 | 95.7% | 1 | 2 | 36 | 67 | 61 |
| [N05B](N05B.md) | ANXIOLYTICS | 39 | 39 | 35 | 89.7% | 1 | 3 | 23 | 36 | 24 |
| [N05C](N05C.md) | HYPNOTICS AND SEDATIVES | 76 | 75 | 60 | 78.9% | 7 | 9 | 54 | 65 | 49 |
| [N06A](N06A.md) | ANTIDEPRESSANTS | 68 | 68 | 63 | 92.6% | 4 | 1 | 52 | 62 | 49 |
| [N06B](N06B.md) | PSYCHOSTIMULANTS, AGENTS USED FOR ADHD AND NOOTROPICS | 38 | 38 | 35 | 92.1% | 1 | 2 | 27 | 34 | 17 |
| [N06C](N06C.md) | PSYCHOLEPTICS AND PSYCHOANALEPTICS IN COMBINATION | 3 | 3 | 0 | 0.0% | 0 | 3 | 0 | 0 | 0 |
| 合计 | — | 294 | 292 | 260 | 88.4% | 14 | 20 | 192 | 264 | 200 |

分组档案数之和为 293，实际 Markdown 文件为 292：`N05BC51` 与 `N05CX01` 分属不同治疗亚组，当前仅因名称相同而共用一份**临时分类索引页**。这不是对两者完整成分或实际制剂身份的归并结论。

官方结构核对：三级治疗组清单（N05 → N05A/N05B/N05C；N06 → N06A/N06B/N06C/N06D）与逐页抓取结果一致；四级亚组与五级条目共抓取 43 个页面，条目行与页面编码链接逐一比对，无解析缺漏。N06D（抗痴呆药）按计划归入[跨组清单](related.md)，不计入核心目录。

## 3. 数据来源与获取方式

**WHO ATC/DDD Index 2026**（官方免费在线索引，https://atcddd.fhi.no/atc_ddd_index/）：
抓取 43 个页面，取得 294 个五级条目、36 个四级亚组名称；索引页面标注的最后更新时间为 2026-01-20。完整电子表格须向权利方订购，本轮未使用，因此差异核查基于公开浏览页面。

**Wikidata**（结构化数据 CC0，https://query.wikidata.org/sparql）：
第一趟按四级亚组分片查询 P267，共 37 个分片，返回 278 条编码绑定、266 个条目；第二趟取回这些条目的全部 ATC 编码、中文语言标签、P279 上位类与英文维基条目指针，共 266 个条目；第三趟对官方有、ATC 编码未命中的 32 个名称使用维基数据实体检索（索引覆盖标签与别名），其中 8 个取得唯一匹配并取回详情，5 个因同名候选过多而未链接。
查询条件：`?item wdt:P267 ?atk FILTER STRSTARTS(?atk, <亚组>)`；标识符属性经逐项核对后使用：P267 ATC 编码、P662 PubChem CID、P486 MeSH 描述符、P715 DrugBank ID（P661 为 ChemSpider、P627 为 IUCN 分类单元，未采用）。抓取时间：2026-10-03T16:15:18Z。

**English Wikipedia**（en.wikipedia.org 类别页面）：
读取 11 个药物类别页面，共 1740 条条目名，用于独立覆盖比对；解析到 5 条重定向页，对名称变体的补充有限。条目正文属 CC BY-SA 4.0，本项目未复制。

**RxNorm：未获取。** *Current Prescribable Content* 下载和 API 在本机环境下均返回 HTTP 403，具体原因尚未确定。NLM [官方文件页面](https://www.nlm.nih.gov/research/umls/licensedcontent/rxnormfiles.html) 说明该子集无需许可证，[Prescribable RxNorm API](https://lhncbc.nlm.nih.gov/RxNav/APIs/PrescribableAPIs.html) 亦不要求许可证；不能仅凭本机 403 认定必须申请 API key。完整 RxNorm 发布包可能涉及 UMLS 账户及来源许可。本轮未完成 RxNorm 名称归一，暂以已有 Wikidata、PubChem CID 与 MeSH 标识符辅助核查。

**PubChem PUG REST：** 已验证可用（无凭据要求），本轮仅用于确认标识符可达性，未逐药抓取化合物记录；化学名与同义名以 Wikidata 别名为来源。

## 4. 归并与去重规则

- 以官方名称、ATC 编码和经核实的具体成分识别条目。不同 ATC 编码即使名称相同也先分别保留；`N05BC51` 与 `N05CX01` 目前共用临时索引页，待按类别拆分，不能假定为同一固定复方。
- 商品名与系统命名仅作别名，不单独建档。
- 已确认完整成分的固定复方单列；未指明全部成分的 ATC 复方类别仅建立分类记录，不将其当作确定配方或具体上市产品。
- 官方索引中的 `barbiturates in combination with other drugs`（`N05CB02`）为目录占位条目而非具体药物，列入目录但不建档。
- 植物药/多组分制剂 3 条（`Lavandulae aetheroleum`、`Valerianae radix`、`Hyperici herba`）保留条目并标注其为多组分制剂，不按单一分子处理。
- 名称链接的证据等级低于 ATC 编码链接，档案中逐条记录 `strongest_link`；同名候选过多时不建立链接，仅标记歧义。

## 5. 已知缺口

1. **N06C 无公开结构化覆盖**：3 个复方条目（`N06CA01`–`N06CA03`）在 Wikidata 中既无 ATC 编码也无名称命中，目录完整，身份只能依赖官方索引。
2. **20 个官方条目公开来源零命中**，其中 5 个存在同名歧义（brexanolone、esketamine、lemborexant、levomilnacipran、solriamfetol），尚未逐一人工判定。
3. **Wikidata 编码滞后于官方索引**：`suvorexant` 在维基数据中标为 `N05CM19`，官方 2026 索引为 `N05CJ01`；`N05CJ02` lemborexant、`N05CJ03` daridorexant 等较新条目缺少 ATC 声明。此外维基数据把若干三级/四级**类别**当作带 P267 的条目：`N05AN`、`N05BA`、`N05BC`、`N05CD`、`N05CH`、`N05CM19`、`N06AB`、`N06AF`。这些差异说明公开来源不能替代官方索引。
4. **中文名覆盖 192/292**：其余条目无中文标签，且现有标签非监管核准名称，须以 NMPA 等官方入口核实。
5. **92 个档案无官方 DDD**，官方索引未给出统计剂量。
6. **获批用途与安全性全部待核实**：本轮未逐药核对监管资料（Drugs@FDA、DailyMed、EMA、NMPA），也未录入任何机制或警告结论。
7. **跨组清单未建档**：43 个条目仅记录编码与理由。
8. **别名冲突待核实**：已从 `lorazepam` 正式别名栏删除 `Lormetazepam`、`Methyllorazepam` 和 `N-Methyllorazepam`，并保留纠错说明。其余 `levosulpiride`↔`sulpiride`、`eszopiclone`↔`zopiclone`、`escitalopram`↔`citalopram`、`armodafinil`↔`modafinil` 可能涉及对映体与外消旋体关系，须分别核对，不得仅凭部分名称重合归并。
9. **RxNorm 仍未接入**（见上），名称归一尚有缺口；此外，通用名中文标签和复方类别仍需审核。

## 6. 目录

| 文件 | 内容 |
| --- | --- |
| [N05A.md](N05A.md) | ANTIPSYCHOTICS，70 个档案 |
| [N05B.md](N05B.md) | ANXIOLYTICS，39 个档案 |
| [N05C.md](N05C.md) | HYPNOTICS AND SEDATIVES，75 个档案 |
| [N06A.md](N06A.md) | ANTIDEPRESSANTS，68 个档案 |
| [N06B.md](N06B.md) | PSYCHOSTIMULANTS, AGENTS USED FOR ADHD AND NOOTROPICS，38 个档案 |
| [N06C.md](N06C.md) | PSYCHOLEPTICS AND PSYCHOANALEPTICS IN COMBINATION，3 个档案 |
| [related.md](related.md) | 跨组选录 43 条，均未建档 |

药物档案共 292 个文件，位于 [`drugs/`](../drugs/)，文件名取英文通用名小写并以连字符分隔。

> 本目录不声称对任何治疗组以外的范围完整；只有在目标范围与官方基准逐项核对后，才对该范围声明完整。

