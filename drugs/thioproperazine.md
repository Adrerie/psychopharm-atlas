# thioproperazine｜中文名待核实（骨架未收录中文标签，本条不自行拟定译名）

> 状态：`basic` ｜ 最后核查：2026-10-25（身份 2026-10-04，中国管制 2026-10-06）｜ ATC：`N05AB08`（WHO ATC/DDD Index 2026）
> 仅供学习研究，不构成用药指导。详见 [免责声明](../DISCLAIMER.md)。

**引用键**：`OPENFDA`＝美国 openFDA 检索（2026-10-25）：`/drug/label.json` 按 `openfda.generic_name`、`openfda.active_ingredient`、`openfda.brand_name`＝"thioproperazine／majeptil／mustine／mustio"，`/drug/ndc.json` 与 `/drug/drugsfda.json` 按通用名，**均返回 HTTP 404 NOT_FOUND**；`DAILYMED`＝DailyMed v2 `spls.json?drug_name=thioproperazine`，本轮经页面抓取确认 **`total_elements＝0`**；`FR-BDPM`＝法国公共药品数据库字母序接口 `startBy＝MUST／THIO`（**`MUST` 0 行**；`THIO`／`THIO` 前缀 21 行全部为 thiocolchicoside／thiopental／thiotepa 等，无本药）；`ES-CIMA`＝西班牙 Aemps CIMA REST `nombre＝thioproperazine／tioperozina`（`totalFilas＝0`）；`UK-EMC`＝英国 emc 检索页（客户端渲染，本轮未取得产品清单）；`KEGG-D01447`／`KEGG-D08585`＝KEGG DRUG 条目（Thioproperazine mesilate，JAN；INN 见 D08585；属收载／转录页，**不是监管原件**）；`PUBCHEM-ID`＝PubChem 按名称检索的 CID、分子式、系统名与同义词名单（**本条用它核实了两个致命同音陷阱**，见下）；`PMID:……`＝PubMed。**核心缺口**：本轮未取得任何法域的现行或历史官方说明书／监管文本，故保持 `basic`。

## 1. 基本信息

| 项目 | 内容 |
| --- | --- |
| 类型／药理类别 | 单方，**哌嗪侧链吩噻嗪**（ATC 亚组 N05AB）。PubChem CID 9429：分子式 **C22H30N4O2S2**，系统名 **N,N-二甲基-10-[3-(4-甲基哌嗪-1-基)丙基]-10H-吩噻嗪-2-磺酰胺**——即 2 位是**磺酰胺基**、侧链末端为 **N-甲基哌嗪**（`PUBCHEM-ID`）；KEGG 归入 `Dopamine antagonist／D2-receptor antagonist`（`KEGG-D08585`）。同一 CID 的登记同义词含 **RP 7843**、SKF 5883、Vontil、Cephalmin、Sulfenazin（`PUBCHEM-ID`）；其中 "RP 7843" 与 1959 年法国早期论文的命名一致（"le 7843 R.P."／"un nouveau neuroleptique majeur, le 7843 RP"，见 1962 年那篇致死反应报告的引用文献，`PMID:13861687` 的参考列表） |
| **陷阱一：thiopropazate ≠ thioproperazine** | **这是本条目最重要的一条。** 运动障碍文献里常用的名拼写 "thiopropazate（Dartal）" 经 PubChem 名称解析对应 **CID 6762、分子式 C23H28ClN3O2S、ATC `N05AB05`、系统名"2-[4-[3-(2-氯吩噻嗪-10-基)丙基]哌嗪-1-基]乙酸乙酯"（同义词含 Dartal 与 "perphenazine acetate"）**（`PUBCHEM-ID`）——它是**奋乃静的乙酸酯、含 2-氯**，与本药（2-磺酰胺、无氯）是**不同分子**。因此：舞蹈症与迟发性运动障碍的几项经典双盲研究（`PMID:4130307`、`PMID:381595`、`PMID:4214673`、`PMID:329332`）以及大鼠应激性溃疡研究（`PMID:573317`）**均属 thiopropazate，本条一律不采作本药证据**（§10 第 3 项）。以通用名在 PubMed 检索时这些记录会一并命中，必须按拼写与 ATC 排除 |
| **陷阱二："mustine" 不是本药商品名** | 取证单把本药的法国产品记为"Mustine"。本轮检索显示 **"mustine"在本库语境中指氮芥类细胞毒药 mechlorethamine（chlormethine）**：同一检索会命中"Mechlorethamine"（`PMID:37094062`）、"-mustine"词干辨析（`PMID:22428186`）、mustine 凝胶治疗蕈样肉芽肿（`PMID:41299164`、`PMID:37262305`）、mustine 外用治疗朗格汉斯细胞组织细胞增生症（`PMID:10833183`）等；法国 BDPM 的 `MUST` 前缀检索 **0 行**，CIMA 检索 "mustina" 命中的是 bendamustine 类（`ES-CIMA`）。**因此本条不写"Mustine／Mustio"为本药商品名**，该归属待核实；可核的本药商品名是文献标题中的 **Majeptil**（`PMID:13864564`、`PMID:4385802`） |
| 主要剂型与给药途径 | **本轮无官方文本**。文献中出现的是口服给药（`PMID:19230` 的双盲比较、`PMID:13864564` 等），以及"3 支／日"式急性给药的表述线索不足。WHO 2026 索引列 **DDD 75 mg 口服、20 mg 非口服**。**取证单称法国有"长效注射"产品：本轮未取得任何支持本药存在长效（癸酸酯类）注射剂型的证据**（`thioproperazine AND depot` 的 PubMed 题录检索为 **0 条**）；非口服 DDD 只说明存在非口服途径的统计口径，**不等于长效制剂**，故本条不写长效注射的剂型风险、不设剂型场景（§10 第 4 项） |
| 主要活性代谢物 | 未取得本药人体代谢物鉴定数据 |
| 关键药代摘要 | 未取得人体 Tmax、半衰期、生物利用度或蛋白结合数据。可核的只有动物与离体实验的时间过程：大鼠纹状体切片研究中，急性注射后 **2.5 h 多巴胺合成显著加速、24 h 回到对照水平**，11 天重复给药后 2.5 h 仍升高但弱于急性、24 h 则显著低于对照（`PMID:240136`）——**这是动物脑片的时程，不是人体药动学** |
| 中国管制状态 | **未发现列入上述现行目录（核查至 2026-10-06）**：逐项核对 2025 年版《药用类麻醉药品目录》《药用类精神药品目录》、2026 年第 58 号药用类精神药品增列、2025 年版《非药用类麻醉药品和精神药品目录》与 2026-07-01 生效的 16 种非药用类增列，均未命中"thioproperazine"；再按公告结构定义核查四个整类范围——芬太尼类（母体芬太尼，条件一至四）、合成大麻素类（目录结构式图所列母核通式与 R1–R5、X、Y、Z 定义）、尼秦类（母体依托尼秦，条件一至四）、奥啡类（母体溴啡条件一至三、母体螺溴啡条件四至六）；结构核查以 PubChem 收录的分子式与结构式做预筛，预筛阳性与边界案例逐项人工回看公告条件，本药不落入其中任何一类的母核或所列替代条件。此表述不等于"非管制"，也不表示不存在处方、携带、进出口或其他法律限制（[核查基准](../SOURCES.md#中国麻醉药品和精神药品管制)） |
| 主要法域批准状态 | **本轮未取得任何法域的现行文本或撤销／退市记录**。美国 openFDA 三类检索 NOT_FOUND、DailyMed `total_elements＝0`、法国 BDPM 与西班牙 CIMA 0 条、英国 emc 未取回清单——均为检索事实，**不推断未获批或已撤市**。文献显示本药曾以 **Majeptil** 之名在美国与加拿大用于临床研究与治疗（1962–1977，`PMID:13864564`、`PMID:14153363`、`PMID:19230`、`PMID:4385802`、`PMID:6129273`），并有 1959 年法国 7843 R.P. 的早期论文（引用见 `PMID:13861687`）；KEGG 另有 **Thioproperazine mesilate（JAN）**（`KEGG-D01447`）。**中国**：上市与核准适应证待核实 |
| 身份与统计 | WHO ATC `N05AB08`；DDD **75 mg 口服／20 mg 非口服**；[ATC/DDD Index](https://atcddd.fhi.no/atc_ddd_index/?code=N05AB08)；KEGG DRUG [D08585](https://www.kegg.jp/entry/D08585)（INN）与 [D01447](https://www.kegg.jp/entry/D01447)（甲磺酸盐，JAN）；PubChem [CID 9429](https://pubchem.ncbi.nlm.nih.gov/compound/9429)（CAS 316-81-4）；对照分子 [CID 6762 thiopropazate／N05AB05](https://pubchem.ncbi.nlm.nih.gov/compound/6762)；Wikidata [Q2622839](https://www.wikidata.org/wiki/Q2622839)；DrugBank [DB01622](https://www.drugbank.ca/r/DB01622)；RxNorm [RXCUI 10498](https://rxnav.nlm.nih.gov/REST/rxcui/10498.json)（RxNorm 另有独立概念 thiopropazate `RXCUI 38133`，二者不可合并） |

## 2. 评分

规则见 [SCORING.md](../SCORING.md)。基线按**口服全身用药**评。本条的评分纪律：凡文献写 "thiopropazate／Dartal" 的结果全部排除；凡"抗精神病药通常怎样"的类别表述只标注为类别证据，不用于给分。

### 2.1 药物负担（1–5，越高越重）

| 维度 | 评分 | 依据 |
| --- | ---: | --- |
| 长期风险负担 | 3 | ① **内分泌／催乳素**：本药致泌乳的个案报告（1964，`PMID:14194225`）＋大鼠催乳素与血镁变化的给药研究（`PMID:2873785`）＋小鼠着床抑制实验中"催乳素与本药"共同作为干预（`PMID:6127981`）；② **一例用药期间死亡**的病例报告（1962，BMJ，开放获取于 PMC，本轮**未取得正文细节**，故不写死因与时间线，`PMID:13861687`）；③ 一例 Tourette 综合征患者"用药一年多耐受良好"的个案（`PMID:6120723`）。评 3 的理由是"有药物特异的长期相关事件，但全部为个案／动物、无分母"；迟发性运动障碍、代谢与心电均无本药数据 |
| 短期耐受负担 | 3 | ① 一项**双盲对照**（本药 vs 舒托必利，BPRS 与 7 条目量表）记录"观察到的副作用**没有差异**，尤其是锥体外系效应"（`PMID:19230`）——这是本药唯一的双盲耐受性对照描述，但它是相对于另一分子的比较，不能换算成本药的发生率；② 动物行为学中本药在**产生实验性紧张症、对抗苯丙胺行为与抗阿扑吗啡致吐**这几项上**强于氯丙嗪**（`PMID:14190465`），提示纹状体多巴胺阻断负荷高；③ 同时本药在降压、抑制呼吸、降温与镇痛上弱于氯丙嗪（同文）。评 3 而非更高：没有人体频率数据 |
| 相互作用／监测负担 | 2 | 药物特异的相互作用线索主要是**抗胆碱能／抗帕金森药的效应修饰**：东莨菪碱、苯托品或异丙嗪类（promethazine）可显著削弱本药对抗苯丙胺行为改变的作用并消除其紧张症状态，但**不削弱其抗阿扑吗啡致吐作用**（动物，`PMID:14190465`）。未取得本药的人体 CYP、蛋白结合或心电监测研究，故不给更高分 |
| 停药负担 | N/A | 未检得本药特异的撤药症状报告或随机停药研究 |
| 滥用／误用潜力 | N/A | 未检得本药的人体强化效应、自身给药或带分母的非医疗使用证据；未列管、数据库无记录均不能单独支撑 1 分（按 SCORING） |
| 非适应证／潜在不适当处方风险（中国） | N/A | 本药在中国无上市与处方数据；本轮**未逐条复核** 2017 版中国老年 PIM 标准表 1 与 AGS Beers 2023，只按"抗精神病药"类别条款理解；没有当地处方偏离数据即记 `N/A` |

总体解释：本药的信号偏"**高多巴胺阻断负荷＋催乳素相关事件＋无人体量化数据**"。它能给到 3 分的三个维度里，最强的也只到"个案与动物层面的方向性"；所有发生率、剂量—反应与长期监测都是空白。因此本档读作的正确方式是"高 EPS／催乳素倾向的历史磺酰胺类哌嗪吩噻嗪，量化证据缺失"，而不是"已被证明危险"。

### 2.2 按使用场景适宜度（A–D）

| 使用场景 | 法域／获批状态 | 适宜度 | 一句话依据（含主要限制） |
| --- | --- | ---: | --- |
| 慢性精神分裂症的精神病性症状控制（口服） | 本轮无可核批准文本；美国与加拿大历史文献以 Majeptil 之名给药（§1） | C- | 本药特异的临床证据是两项 1960 年代精神科研究报告（`PMID:13864564`、`PMID:14153363`，本轮**只取得题录**，无样本量、量表与效应量），以及一项与舒托必利的**双盲头对头比较**：总体量表均数差异显著偏向舒托必利、逐条目差异不显著、副作用（含 EPS）两组无差异（`PMID:19230`；量表与细节见 §5）。限制：无可核现代随机对照、无现行文本，且上述比较不构成对本药疗效的阴性判定 |

**不设为场景的内容**：① **舞蹈症／迟发性运动障碍／运动障碍症状控制**——本药只有 1968 年一篇罗马尼亚语"本药（Majeptil）治疗舞蹈综合征"的题录（`PMID:4385802`），而该适应证上被反复引用的双盲安慰剂对照与 6 个月盲评研究全部属于**另一分子 thiopropazate（Dartal，N05AB05）**，不能移用（§10 第 3 项）；② **溃疡性结肠炎与 Tourette 综合征**——分别为 3 例与 1 例的开放个案，作者自己声明"需对照试验确证"（`PMID:6129273`、`PMID:6120723`），留在 §5；③ **与本药无关的"mustine（氮芥）化疗止吐"文献**（如 1969 年"mustine 恶心"的止吐研究）不得作为本药止吐场景的证据（§10 第 2 项）；④ 与左旋promazine 的**固定复方**评价（`PMID:4398781`）属复方对象；⑤ 年龄、妊娠、肝肾功能与监测要求写入 §9；⑥ "现行数据库无产品"不作为档位理由。

## 3. 主要作用

本药的药理描述主要来自动物研究：**与氯丙嗪同批比较**时，本药在降压、拮抗肾上腺素（猫）、抑制呼吸（兔）、降温与镇痛、降低最小麻醉剂量（小鼠）以及对抗色胺致惊厥（大鼠）等方面**均弱于氯丙嗪**，在减少小鼠自发活动上二者大致相当；但在**保护群居小鼠对抗苯丙胺急性毒性、防止苯丙胺所致大鼠行为紊乱、产生实验性紧张症、以及对抗犬的阿扑吗啡致吐**上**强于氯丙嗪**（`PMID:14190465`）。同文还显示东莨菪碱、苯托品或 promethazine 明显削弱其抗苯丙胺行为效应并消除紧张症，而不削弱抗阿扑吗啡致吐作用——这提示其行为效应与紧张症高度依赖胆碱能张力。另有本药作为**神经阻滞剂受体的探针配体**的成套研究（离体Ⅰ、在体Ⅱ，1980，`PMID:6109531`、`PMID:6109532`），以及离体大鼠纹状体多巴胺合成与释放的急性／亚急性时程（`PMID:240136`）、中脑皮质多巴胺系统的合成调控（`PMID:238717`）与去皮质猫活动节律（`PMID:35804`）等动物工作。

本轮未取得本药的受体 Ki 数值、人体 D2 占有率或内分泌剂量—曲线；因此不写"受体谱"，也不把奋乃静、三氟拉嗪或 prochlorperazine 的数值移过来。

## 4. 适应范围

**现行核准适应证：待核实。** 未取得法国、美国、加拿大或任何法域的说明书／监管决定文本，因此不写核准措辞、剂量、禁忌与监测条款。

**文献中出现过的用途（非核准表述）**：慢性精神分裂症与精神病性症状（`PMID:13864564`、`PMID:14153363`、`PMID:19230`）；舞蹈综合征（`PMID:4385802`，题录）；溃疡性结肠炎（3 例开放个案，`PMID:6129273`）；Gilles de la Tourette 综合征（1 例个案，`PMID:6120723`）；以及作为神经阻滞剂受体探针的工具性使用（`PMID:6109531`、`PMID:6109532`）。

**剂量**：**不写处方建议**。可核的用药量信息极少，双盲比较研究的具体剂量本轮未取得；WHO DDD 75 mg 口服／20 mg 非口服只是统计口径（且非口服 DDD 不表示存在长效制剂，§10 第 4 项）。

**中国**：上市剂型与核准适应证待核实。

## 5. 实际效果与局限

- **临床研究报告（题录级）**：1962 年"本药（Majeptil）的临床研究"（`PMID:13864564`）与 1964 年"本药在慢性精神分裂症中的应用"（`PMID:14153363`）。本轮**未取得摘要、设计细节、量表与结果数值**，故不写"有效"或效应量，只确认这两项人体研究存在。
- **与舒托必利的双盲比较（1977）**：用法是 BPRS 与一条目简表（激越—妄想—思维散漫—焦虑—攻击—幻觉—孤独）；**总体分差异显著、偏向舒托必利，但逐条目差异不显著；副作用（尤其锥体外系）未见组间差异**（`PMID:19230`）。解读边界：这是**两药头对头的相对差异**，不构成"本药无效"或"舒托必利对所有症状更优"的结论，也不能外推给其他分子（另见 [sultopride](sultopride.md) 中同一条研究的另一侧）。
- **运动障碍**：本药（Majeptil）治疗舞蹈综合征的 1968 年罗马尼亚语研究只有题录（`PMID:4385802`）。**必须排除的相邻文献**：舞蹈症的双盲安慰剂对照试验（`PMID:4130307`）、迟发性运动障碍 6 个月盲评电影胶片研究（`PMID:381595`）、与本药无关的口服运动障碍双盲比较（`PMID:4214673`）、以及 1977 年未对照的持续性运动障碍研究（`PMID:329332`）——这些的受试药均为 **thiopropazate（Dartal，N05AB05）**，另一分子。
- **个案（非疗效证据）**：3 例溃疡性结肠炎患者"临床、影像、内镜、组织与生化指标显著改善"，作者明确写"这是初步观察、需要对照试验确证"，并推测与本药进入某些脑多巴胺区的中枢机制有关（`PMID:6129273`）；1 例 Tourette 综合征患者本药"完全抑制症状"并耐受一年多（`PMID:6120723`）。
- **复方评价（不计入单方）**：1970 年对本药与左旋promazine（levopromazine）**复方**的评价只有题录（`PMID:4398781`），复方的效应与禁忌不得转记给单方。
- **非临床与体外**：本药在约 200 种两亲性阳离子药物的**体外抗克氏锥虫**筛查中属最强一档（≤1 mM 浓度即有活性，`PMID:3926530`）；小鼠着床与胚胎转移实验（`PMID:6127981`、`PMID:4156437`）。这些不构成任何人体适应证。
- **总体局限**：本药的可核人体证据是"两项题录级研究＋一项双盲对照的相对比较＋两三个案"，**没有可引用的效应量、发生率或长期随访**。

## 6. 长期风险

- **内分泌**：本药致泌乳的个案（`PMID:14194225`）；大鼠血浆催乳素与血镁的给药后变化（`PMID:2873785`）。未检得本药的月经紊乱、溢乳率、男性乳房发育或骨健康数据。
- **运动系统**：动物层面的高紧张症与抗苯丙胺效应提示锥体外系负荷高（`PMID:14190465`）；双盲比较中本药的 EPS 与舒托必利无显著差异（`PMID:19230`）；**迟发性运动障碍在本药无发生率数据**（相关 TD 研究属于 thiopropazate，排除）。
- **严重事件**：1962 年一例"对本药的致死反应"病例报告（`PMID:13861687`）——本轮**未取得正文**，因此不写剂量、时间线、尸检所见或归因；个案不构成本药的风险率。
- **不借类别**：QT 延长、粒细胞缺乏、NMS、老年痴呆人群死亡与脑血管事件升高均属**类别层面的警示**，本药未被单独研究；本条把它们标注为"类别证据、本药未测定"，不列发生率。

## 7. 短期风险、停药与误用

**短期**：没有本药的人体频率数据；双盲比较提示 EPS 与其他哌嗪类吩噻嗪／苯甲酰胺相当（`PMID:19230`），动物研究提示镇静与降压弱于氯丙嗪而紧张症更强（`PMID:14190465`）。**抗胆碱能药（东莨菪碱、苯托品、promethazine）会削弱本药的行为效应并消除紧张症**（动物，`PMID:14190465`）——这既是效应修饰，也是"合用抗帕金森药可能改变本药表现"的唯一线索。**驾驶与操作机器**：无资料。**停药**：无撤药研究，记 `N/A`。**误用**：无药物特异证据，记 `N/A`。**过量**：未检得本药中毒病例系列或处理方案（1969 年"mustine 恶心的新止吐药"一文属于氮芥语境，与本药过量无关，见 §10 第 2 项）。

## 8. 重要相互作用

本轮未取得本药的人体药动学相互作用研究。可列的本药特异事实只有：① **抗胆碱能／抗帕金森药的效应修饰**（动物；`PMID:14190465`）；② **多巴胺能药物的方向性拮抗**——本药与阿扑吗啡在纹状体多巴胺合成与行为层面互为拮抗（`PMID:238717`、`PMID:14190465`）；③ 与**溴麦角环肽（bromocriptine）**在大鼠催乳素与血镁反应上互为激动／拮抗对照（`PMID:2873785`）；④ 复方语境下的左旋promazine（`PMID:4398781`）不作单方相互作用。锂、其他延长 QT 的药物、CYP 抑制剂等类别清单在本条**不列**，理由是没有本药数据支持。

## 9. 特殊人群

**无文本，不写禁忌与剂量调整**。可核信息全部为个案级：Tourette 综合征成年女性 1 例（`PMID:6120723`）、溃疡性结肠炎 3 例（`PMID:6129273`）、泌乳个案 1 例（`PMID:14194225`）、致死反应个案 1 例（`PMID:13861687`）。生殖与发育方面只有小鼠实验（着床抑制与胚胎转移，`PMID:6127981`、`PMID:4156437`）——动物数据，不作人体结论。老年、儿童、妊娠哺乳与肝肾功能均无本药资料；此空白不是"无注意事项"。

## 10. 证据边界

1. **没有任何官方文本**：美国 openFDA 三类检索 NOT_FOUND、DailyMed `total_elements＝0`、法国 BDPM `MUST` 前缀 0 行（`THI`／`THIO` 前缀 21 行均他药）、西班牙 CIMA 0 条、英国 emc 清单未取回。零命中只写检索事实。要升 `reviewed`，需要法国／美国／加拿大的历史说明书或带规格、公告日与生效日的退市／撤销公告（Majeptil 由哪家持证、哪个规格、哪一天退出，本轮均未核）。
2. **"mustine" 词义冲突未解**：取证单把法国产品名写作 Mustine，但本轮所有含 "mustine" 的可核记录都指向**氮芥类细胞毒药 mechlorethamine**（`PMID:37094062`、`PMID:22428186`、`PMID:41299164`、`PMID:10833183`、`PMID:4898162`），BDPM 与 CIMA 也没有本药的对应条目。**本条不使用该商品名**；若将来核实本药法国产品名为 "Mustio" 之类，须以官方页面（CIS 号＋规格）重新落地。
3. **thiopropazate（Dartal，N05AB05）是另一个分子**：其 PubChem CID 6762、分子式 C23H28ClN3O2S、同义词含 "perphenazine acetate"（`PUBCHEM-ID`），RxNorm 亦有独立概念 `RXCUI 38133`。舞蹈症与 TD 的双盲证据属于它，**不得移给本药**（§2.2、§5）。
4. **长效注射剂型未获证据**：`thioproperazine AND depot` 的 PubMed 题录检索为 0 条；WHO 的"非口服 DDD 20 mg"只是途径统计口径。本条因此不写注射／长效风险，也不设剂型场景。
5. **多数人体研究只有题录**：`PMID:13864564`、`PMID:14153363`、`PMID:4385802`、`PMID:4398781`、`PMID:13861687`（正文未解析）本轮未取得可引用数值，因此本档没有效应量；这是"未测"，不是"阴性"。
6. **个案不可换算为发生率**：致死反应与泌乳各 1 例（`PMID:13861687`、`PMID:14194225`），没有分母。
7. **DDD 75 mg 口服／20 mg 非口服是统计指标**，不用于个体剂量或利用度推算。
8. **中国字段**：沿用 2026-10-06 的目录核查结论与"不等于非管制"的限定；中国注册状态因 NMPA／CDE 入口不可脚本检索而待核实。

## 11. 深入分析与来源

本条目不建专题文件：真正值得专题化的问题是"运动障碍治疗文献中 thioproperazine 与 thiopropazate 的名称混淆如何影响历史结论的归属"——但回答它只需要本条 §1／§10 的命名核对，不需要另开文件；若将来取得法国或北美的历史标签，再考虑把"高 EPS／高催乳素倾向是否曾被写入监管文本"升级为专题。

**监管与检索记录**：[openFDA 标签检索（NOT_FOUND）](https://api.fda.gov/drug/label.json?search=openfda.generic_name:%22thioproperazine%22&limit=5)；[openFDA drugs@fda 申请检索（NOT_FOUND）](https://api.fda.gov/drug/drugsfda.json?search=openfda.generic_name:%22thioproperazine%22&limit=1)；[DailyMed 按药名检索（total_elements＝0）](https://dailymed.nlm.nih.gov/dailymed/services/v2/spls.json?drug_name=thioproperazine)；[法国 BDPM 字母序检索 MUST（0 行）](https://base-donnees-publique.medicaments.gouv.fr/api/recherche/alphabetique?startBy=MUST&page=1&limit=20)；[法国 BDPM 字母序检索 THIO](https://base-donnees-publique.medicaments.gouv.fr/api/recherche/alphabetique?startBy=THIO&page=1&limit=20)；[西班牙 CIMA 检索入口](https://www.aemps.gob.es/cima/publico/home.html)；[英国 emc 检索页](https://www.medicines.org.uk/emc/search?s=thioproperazine)；[KEGG DRUG D08585／D01447（转录／收载页）](https://www.kegg.jp/entry/D01447)；[NMPA 政务服务窗口](https://www.nmpa.gov.cn/zwfwqjd/index.html?type=pc) 与 [CDE 上市药品目录集](https://www.cde.org.cn/hzmp/)（均不可脚本检索）。

**研究**：[本药（Majeptil）的临床研究（题录，PMID:13864564）](https://pubmed.ncbi.nlm.nih.gov/13864564/)；[慢性精神分裂症中的本药（题录，PMID:14153363）](https://pubmed.ncbi.nlm.nih.gov/14153363/)；[本药与舒托必利的双盲比较（PMID:19230）](https://pubmed.ncbi.nlm.nih.gov/19230/)；[本药致泌乳个案（PMID:14194225）](https://pubmed.ncbi.nlm.nih.gov/14194225/)；[对本药的致死反应（个案，PMID:13861687）](https://pubmed.ncbi.nlm.nih.gov/13861687/)；[本药药理性质与抗帕金森药的修饰（PMID:14190465）](https://pubmed.ncbi.nlm.nih.gov/14190465/)；[作为神经阻滞剂受体配体Ⅰ离体（PMID:6109531）](https://pubmed.ncbi.nlm.nih.gov/6109531/)；[Ⅱ在体（PMID:6109532）](https://pubmed.ncbi.nlm.nih.gov/6109532/)；[大鼠纹状体多巴胺合成与释放的急／亚急性效应（PMID:240136）](https://pubmed.ncbi.nlm.nih.gov/240136/)；[中脑皮质多巴胺系统（PMID:238717）](https://pubmed.ncbi.nlm.nih.gov/238717/)；[去皮质猫活动节律（PMID:35804）](https://pubmed.ncbi.nlm.nih.gov/35804/)；[大鼠催乳素与血镁（PMID:2873785）](https://pubmed.ncbi.nlm.nih.gov/2873785/)；[溃疡性结肠炎 3 例（PMID:6129273）](https://pubmed.ncbi.nlm.nih.gov/6129273/)；[Tourette 综合征个案（PMID:6120723）](https://pubmed.ncbi.nlm.nih.gov/6120723/)；[舞蹈综合征（题录，PMID:4385802）](https://pubmed.ncbi.nlm.nih.gov/4385802/)；[与本药—左旋promazine 复方评价（题录，PMID:4398781）](https://pubmed.ncbi.nlm.nih.gov/4398781/)；[体外抗克氏锥虫（PMID:3926530）](https://pubmed.ncbi.nlm.nih.gov/3926530/)。**以下为 thiopropazate（另一分子，N05AB05），列出仅作排除**：[舞蹈症双盲安慰剂对照（PMID:4130307）](https://pubmed.ncbi.nlm.nih.gov/4130307/)；[迟发性运动障碍 6 个月盲评（PMID:381595）](https://pubmed.ncbi.nlm.nih.gov/381595/)；[口服运动障碍双盲比较（PMID:4214673）](https://pubmed.ncbi.nlm.nih.gov/4214673/)；[持续性运动障碍未对照研究（PMID:329332）](https://pubmed.ncbi.nlm.nih.gov/329332/)。

**分类与身份**：[WHO ATC/DDD Index `N05AB08`](https://atcddd.fhi.no/atc_ddd_index/?code=N05AB08)；[WHO ATC/DDD Index `N05AB05`（thiopropazate，须区分）](https://atcddd.fhi.no/atc_ddd_index/?code=N05AB05)；[PubChem CID 9429（thioproperazine，含 RP 7843 等同义词）](https://pubchem.ncbi.nlm.nih.gov/compound/9429)；[PubChem CID 6762（thiopropazate／Dartal）](https://pubchem.ncbi.nlm.nih.gov/compound/6762)；[RxNorm RXCUI 10498](https://rxnav.nlm.nih.gov/REST/rxcui/10498.json)；[RxNorm RXCUI 38133（thiopropazate）](https://rxnav.nlm.nih.gov/REST/rxcui/38133.json)；[Wikidata Q2622839](https://www.wikidata.org/wiki/Q2622839)；[DrugBank DB01622](https://www.drugbank.ca/r/DB01622)；English Wikipedia（标题指针，未复制正文）：[Thioproperazine](https://en.wikipedia.org/wiki/Thioproperazine)。

统计与缺口见 [目录索引](../catalog/index.md)。
