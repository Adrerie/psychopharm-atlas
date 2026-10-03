# 精神药物分类目录索引

> 分类基准：WHO ATC/DDD Index 2026 ｜ 核查日期：2026-10-04  
> 本轮范围：公开数据导入、分类目录构建与短篇建档（[计划](../PLAN.md) 阶段一、二）。作用机制、获批适应证与安全性分析属阶段三，本轮未录入。

## 1. 总体结果

| 环节 | 数量 | 说明 |
| --- | --- | --- |
| 官方目标五级条目 | 294 | 六个治疗亚组逐条核对 |
| 去重后唯一条目 | 293 | 合并 1 组同名条目 |
| 已建立短篇档案 | 292 | 目录占位条目未建档 |
| 公开来源以 ATC 编码命中 | 260（88.4%） | Wikidata P267 携带官方编码 |
| 公开来源仅以名称命中 | 14 | 条目未携带对应 ATC 编码 |
| 公开来源零命中 | 20 | 档案身份仅由官方索引确认 |
| 有中文标签 | 192 | 取自 Wikidata 标签，非监管核准名称 |
| 有英文维基百科条目 | 264 | 仅作指针，未复制正文 |
| 官方索引列出 DDD | 200 | 其余条目官方未给出 DDD |

条目类型分布：单方 275（其中植物药/多组分制剂 3）、固定复方 17、目录占位条目 1。档案状态一律为 `indexed`（仅核实身份与分类）。

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

分组行按“条目所属组”计数，跨组归并的条目在两组各计一次，因此分组档案数之和（293）比唯一档案数（292）多 1。

官方结构核对：三级治疗组清单（N05 → N05A/N05B/N05C；N06 → N06A/N06B/N06C/N06D）与逐页抓取结果一致；四级亚组与五级条目共抓取 43 个页面，条目行与页面编码链接逐一比对，无解析缺漏。N06D（抗痴呆药）按计划归入[跨组清单](related.md)，不计入核心目录。

## 3. 数据来源与获取方式

**WHO ATC/DDD Index 2026**（官方免费在线索引，https://atcddd.fhi.no/atc_ddd_index/）：
抓取 43 个页面，取得 294 个五级条目、36 个四级亚组名称；索引页面标注的最后更新时间为 2026-01-20。完整电子表格须向权利方订购，本轮未使用，因此差异核查基于公开浏览页面。

**Wikidata**（结构化数据 CC0，https://query.wikidata.org/sparql）：
第一趟按四级亚组分片查询 P267，共 37 个分片，返回 278 条编码绑定、266 个条目；第二趟取回这些条目的全部 ATC 编码、中文语言标签、P279 上位类与英文维基条目指针，共 266 个条目；第三趟对官方有、ATC 编码未命中的 32 个名称使用维基数据实体检索（索引覆盖标签与别名），其中 8 个取得唯一匹配并取回详情，5 个因同名候选过多而未链接。
查询条件：`?item wdt:P267 ?atk FILTER STRSTARTS(?atk, <亚组>)`；标识符属性经逐项核对后使用：P267 ATC 编码、P662 PubChem CID、P486 MeSH 描述符、P715 DrugBank ID（P661 为 ChemSpider、P627 为 IUCN 分类单元，未采用）。抓取时间：2026-10-03T16:15:18Z。

**English Wikipedia**（en.wikipedia.org 类别页面）：
读取 11 个药物类别页面，共 1740 条条目名，用于独立覆盖比对；解析到 5 条重定向页，对名称变体的补充有限。条目正文属 CC BY-SA 4.0，本项目未复制。

**RxNorm：未获取。** *Current Prescribable Content* 子集与 RxNorm API 在本机环境下均返回 403，须 UMLS/UTS 账号与 API key；本轮未申请凭据，因此**没有**执行 RxNorm 名称归一，计划中的该项交叉核对尚未履行。替代做法是使用 Wikidata 携带的 PubChem CID、MeSH 描述符与 DrugBank ID 做标识符交叉核对。

**PubChem PUG REST：** 已验证可用（无凭据要求），本轮仅用于确认标识符可达性，未逐药抓取化合物记录；化学名与同义名以 Wikidata 别名为来源。

## 4. 归并与去重规则

- 以官方通用名与有效成分为唯一条目；同一成分的多个 ATC 编码并入同一档案（本轮归并 1 组：`N05BC51` 与 `N05CX01` 的 meprobamate, combinations）。
- 商品名与系统命名仅作别名，不单独建档。
- 固定复方单列，绝不并入其单方条目；即使复方与成分共享维基数据条目也不归并。
- 官方索引中的 `barbiturates in combination with other drugs`（`N05CB02`）为目录占位条目而非具体药物，列入目录但不建档。
- 植物药/多组分制剂 3 条（`Lavandulae aetheroleum`、`Valerianae radix`、`Hyperici herba`）保留条目并标注其为多组分制剂，不按单一分子处理。
- 名称链接的证据等级低于 ATC 编码链接，档案中逐条记录 `strongest_link`；同名候选过多时不建立链接，仅标记歧义。

## 5. 已知缺口

1. **N06C 无公开结构化覆盖**：3 个复方条目（`N06CA01`–`N06CA03`）在 Wikidata 中既无 ATC 编码也无名称命中，目录完整，身份只能依赖官方索引。
2. **20 个官方条目公开来源零命中**，其中 5 个存在同名歧义（brexanolone、esketamine、lemborexant、levomilnacipran、solriamfetol），尚未逐一人工判定。
3. **Wikidata 编码滞后于官方索引**：`suvorexant` 在维基数据中标为 `N05CM19`，官方 2026 索引为 `N05CJ01`；`N05CJ02` lemborexant、`N05CJ03` daridorexant 等较新条目缺少 ATC 声明。此外维基数据把若干三级/四级**类别**当作带 P267 的条目：`N05AN`、`N05BA`、`N05BC`、`N05CD`、`N05CH`、`N05CM19`、`N06AB`、`N06AF`。这些差异说明公开来源不能替代官方索引。
4. **中文名覆盖 192/293**：其余条目无中文标签，且现有标签非监管核准名称，须以 NMPA 等官方入口核实。
5. **93 个档案无官方 DDD**，官方索引未给出统计剂量。
6. **获批用途与安全性全部待核实**：本轮未逐药核对监管资料（Drugs@FDA、DailyMed、EMA、NMPA），也未录入任何机制或警告结论。
7. **跨组清单未建档**：43 个条目仅记录编码与理由。
8. **Wikidata 别名与目录内其他条目同名 5 处**，已在相应档案中作冲突提示而不作归并：`levosulpiride`↔`sulpiride`、`lorazepam`↔`lormetazepam`、`eszopiclone`↔`zopiclone`、`escitalopram`↔`citalopram`、`armodafinil`↔`modafinil`。其中 armodafinil、escitalopram、eszopiclone、levosulpiride 的取值符合对映体命名习惯；`lorazepam` 条目携带 `Lormetazepam` 别名，与 `N05CD06` lormetazepam 同名，疑为来源库错误挂接，须核实后再处理。
9. **RxNorm 未接入**（见上），名称归一尚有缺口。

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

