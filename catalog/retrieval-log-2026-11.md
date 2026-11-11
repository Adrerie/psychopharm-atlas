# 逐名监管检索记录（2026-11-11）

### 4.23 加拿大 DPD 第十一批（2026-11-11）

检索 14 个活性成分，无新增档案。lithium 此前已在第二批写入；pentobarbital 的在售条目为兽用安乐死制剂，不写入；droperidol、iloperidone、metamfetamine、piracetam、quazepam、ramelteon、reboxetine、sulpiride、thiopental、tianeptine、tiapride、valpromide 未捕获到人用 Marketed 示例。

## 5. 未检索的档案

56 份 basic 档案没有可检出的日文名（代码名、中方特有品种与无日本语境条目），PMDA 不支持英文名检索，故未做 PMDA 逐名查询。其余法域仍以四库 0 条为检索事实。

统计与状态见 [目录索引](index.md)，方法与缺口见 [PLAN.md](../PLAN.md)。

## 6. WHO ATC/DDD 索引复核（2026-11-11）

- 范围：384 份药物档案中可解析的 ATC 编码共 369 个唯一编码，逐码打开 `atcddd.fhi.no/atc_ddd_index/?code=<code>` 页面读取 DDD 行。15 份研究候选档案无 ATC 编码，未纳入。
- 结果：369 个编码全部在官方索引中找到对应条目，未发现编码失效或名称不匹配。
- DDD 声明核对：可解析的数值声明与"未列 DDD"声明逐一比对。25 处初筛不一致经逐条人工回读，全部为解析假阳性（多行 DDD 的给药途径格式、相邻药物的 DDD、研究剂量被正则误抓），未发现需要修改的档案。
- 例：buprenorphine `N07BC01` 页面为 1.6 mg 植入、2.1 mg 注射、8 mg 舌下三条，与档案一致；fampridine 页面 20 mg 与同页 amifampridine 40 mg 是两条独立记录，档案已区分。
- 口径：DDD 是群体统计量，不是处方剂量；本页只核对编码与数值是否与官方索引一致，不据此改写剂量建议。

## 7. PubChem／Wikidata 标识回读（2026-11-11）

- 范围：384 份药物档案中可解析的 PubChem CID 308 个与 Wikidata QID 282 个。
- 方法：PubChem PUG REST 按 CID 取 Title 与 IUPACName，Wikidata `wbgetentities` 取英文标签与描述，再与档案 slug 做词元比对，只把不一致项列入人工复核。
- 结果：全部 CID 与 QID 均返回有效实体。初筛 42 个 CID 与 38 个 QID 不一致，逐条回读后确认 8 份档案中的 11 个标识指向错误并已改正。PubChem 侧为 acamprosate 10475069→155434（原为无关核苷衍生物）、imidafenacin 47207931→6433090、nalmefene 439501→5284594（原为 ouabain）、naltrexone 53606→5360515、pregabalin 440545→5486971（原为 α-D-果吡喃糖）、propranolol 4949→4946（原为 propyliodone）。Wikidata 侧为 clonazepam Q409455→Q407988（原为 ibogaine）、pregabalin Q421454→Q412174（原为苏丹 Akasha 神庙）、propranolol Q420021→Q423364（原为 Akkullanu）、doxepin Q416791→Q71704041（cidoxepin 为 E 型单异构体，档案按 E／Z 混合物记录）。doxepin 的 PubChem CID 同步由 667468（Z 型单异构体）改为 3158（doxepin 混合物）。
- 其余初筛差异属于盐型、立体异构体或同义名标签的命名差异（如 acetyl-L-carnitine、DL-amphetamine、thiothixene），不属标识错误，保留原样。
- bentazepam 的 CID 34592 与 fenozolone 的 CID 71682 为无标题的旧记录，两份档案同时列出现行记录 135412795 与 135436543，结构式一致。
- 口径：CID 与 QID 只作实体指针，不引其页面正文结论，本次回读不改变档案中的监管文本、剂量与评分。
