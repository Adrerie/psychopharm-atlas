# moperone｜中文名待核实（骨架未收录中文标签，本条不自行拟定译名）

> 状态：`basic` ｜ 最后核查：2026-10-25（身份 2026-10-04，中国管制 2026-10-06）｜ ATC：`N05AD04`（WHO ATC/DDD Index 2026）
> 仅供学习研究，不构成用药指导。详见 [免责声明](../DISCLAIMER.md)。

**引用键**：`OPENFDA`＝美国 openFDA 检索（2026-10-25）：`/drug/label.json` 按 `openfda.generic_name`、`openfda.active_ingredient`、`openfda.brand_name`＝"moperone／dosen／listom／luvatren"，`/drug/ndc.json` 与 `/drug/drugsfda.json` 按通用名，**均返回 HTTP 404 NOT_FOUND**；`US-DAILYMED`＝DailyMed v2 `spls.json?drug_name=moperone`（本轮脚本访问返回 JS 验证页，未取得 `total_elements`）；`FR-BDPM`＝法国公共药品数据库字母序接口 `startBy＝MOPER／MOP`（`MOPER` 0 行；`MOP` 前缀 3 行均为 Mopral 类质子泵抑制剂）；`ES-CIMA`＝西班牙 Aemps CIMA REST `nombre＝moperone／moperona`（`totalFilas＝0`）；`UK-EMC`＝英国 emc 检索页（客户端渲染，本轮未取得产品清单）；`KEGG-D02623`／`KEGG-D01105`＝KEGG DRUG 条目（Moperone INN 与 Moperone hydrochloride JAN，后者商品名标注 Luvatren；属收载／转录页，**不是监管原件**）；`PUBCHEM-ID`＝PubChem 名称检索的分子式与系统名；`PMID:……`＝PubMed。**核心缺口**：本轮未取得任何法域的现行或历史官方说明书／监管文本；取证单提到的比利时 Dosen 与意大利 Listom **均无可核证据**（§10 第 3 项），故保持 `basic`。

## 1. 基本信息

| 项目 | 内容 |
| --- | --- |
| 类型／药理类别 | 单方，**丁酰苯类（butyrophenone）衍生物**（ATC 亚组 N05AD）。KEGG 把它归入"Dopamine antagonist／Dopamine D2-receptor antagonist"与"Butyrophenone derivative"药物组（`KEGG-D02623`）。PubChem 系统名 **1-(4-氟苯基)-4-[4-羟基-4-(4-甲基苯基)哌啶-1-基]丁-1-酮**、分子式 C22H26FNO2（`PUBCHEM-ID`）：即与氟哌啶醇同属"4-羟基-4-芳基哌啶丁酮"骨架，差别在芳基端（本药为 4-甲基苯基＋4-氟苯甲酰，氟哌啶醇为 4-氯苯基＋4-氯苯甲酰）。**骨架相似不等于数据可互借**（见下行与 §6） |
| 与同类分子的区分 | 本药与 **haloperidol、droperidol、benperidol（仓库已有条目）、fluanisone、pipamperone、benzperidol、trifluperidol、clofluperol、lenperone、floropipamide** 都是不同的分子。1969 年大鼠分布研究把 haloperidol、trifluperidol、moperone、clofluperol 并列比较（`PMID:5818759`），1984 年眼压研究把本药与 haloperidol、trifluperidol 排序比较（`PMID:6147806`）——这些是**动物实验中的并列**，不构成人体等效或效价结论；氟哌啶醇／droperidol 的 **QT 与尖端扭转结论一律不套用于本药**（本药无人特异性心电数据，§6） |
| 主要剂型与规格 | **本轮无官方文本**。文献可辨：普通口服制剂与**缓释（延迟作用）口服片**——1977 年瑞士的开放研究明确写为"the delayed-action form of the neuroleptic agent moperone hydrochloride""片剂的胃耐受性很好"（`PMID:323966`）。WHO 2026 索引列 **DDD 20 mg 口服、20 mg 非口服**（统计指标），但本条**没有取得任何注射剂型的人体文本**，不写注射用途与规格。盐酸盐为 JAN 收载名（`KEGG-D01105`） |
| 主要活性代谢物 | 未取得本药代谢物的鉴定结果。有 1970 年"神经阻滞剂的分布与代谢 Ⅱ．moperone 的药动学"专文（`PMID:5536800`，Arzneimittelforschung），**本轮只有题录、无摘要数值**，故不写代谢物名。取证单提到的 **perispiramide**：本轮以该词检索 PubMed 为 **0 条**（2026-10-25），无法核实其与本药或其代谢物的关系，**本条不写二者是否同一实体** |
| 关键药代摘要 | 未取得人体 Tmax、半衰期、生物利用度或蛋白结合数据；1970 年的药动学论文与 1969 年的大鼠分布研究（`PMID:5536800`、`PMID:5818759`）均只有题录。不写任何参数 |
| 中国管制状态 | **未发现列入上述现行目录（核查至 2026-10-06）**：逐项核对 2025 年版《药用类麻醉药品目录》《药用类精神药品目录》、2026 年第 58 号药用类精神药品增列、2025 年版《非药用类麻醉药品和精神药品目录》与 2026-07-01 生效的 16 种非药用类增列，均未命中"moperone"；再按公告结构定义核查四个整类范围——芬太尼类（母体芬太尼，条件一至四）、合成大麻素类（目录结构式图所列母核通式与 R1–R5、X、Y、Z 定义）、尼秦类（母体依托尼秦，条件一至四）、奥啡类（母体溴啡条件一至三、母体螺溴啡条件四至六）；结构核查以 PubChem 收录的分子式与结构式做预筛，预筛阳性与边界案例逐项人工回看公告条件，本药不落入其中任何一类的母核或所列替代条件。此表述不等于"非管制"，也不表示不存在处方、携带、进出口或其他法律限制（[核查基准](../SOURCES.md#中国麻醉药品和精神药品管制)） |
| 主要法域批准状态 | **本轮未取得任何法域的官方文本或批准／撤销记录**。美国 openFDA 三类检索与 DailyMed、法国 BDPM、西班牙 CIMA 均无记录，英国 emc 清单未取回（逐项检索式见 §11）；KEGG 的 JAN 收载名与"Luvatren"商品名标注说明该盐在日本或以英语系市场曾被命名与使用（`KEGG-D01105`），但**这不是监管证明**，本条不写"日本已批准"。取证单提到的比利时 **Dosen**、意大利 **Listom** 两个名称：本轮在 openFDA 商品名检索、PubMed 共现检索（`moperone AND dosen`＝0、`moperone AND luvatren`＝0）与 CIMA 中**均未取得指向本药证据**，故不写入商品名栏。1969 年挪威语与 1977 年瑞士德语的临床研究（`PMID:5354545`、`PMID:323966`）表明确曾有产品在欧洲使用。**中国**：上市与核准适应证待核实 |
| 身份与统计 | WHO ATC `N05AD04`；DDD **20 mg 口服／20 mg 非口服**；[ATC/DDD Index](https://atcddd.fhi.no/atc_ddd_index/?code=N05AD04)；KEGG DRUG [D02623](https://www.kegg.jp/entry/D02623)（INN）与 [D01105](https://www.kegg.jp/entry/D01105)（盐酸盐，JAN）；Wikidata [Q6908807](https://www.wikidata.org/wiki/Q6908807)；PubChem [CID 4249](https://pubchem.ncbi.nlm.nih.gov/compound/4249)；DrugBank [DB13554](https://www.drugbank.ca/r/DB13554) |

## 2. 评分

规则见 [SCORING.md](../SCORING.md)。本药的**人体证据只有一项 20 例开放研究**，其余全部是动物或分析方法学文献；因此六个维度里有四个只能是 `N/A`。凡"丁酰苯类通常怎样"的表述都不作为给分依据。

### 2.1 药物负担（1–5，越高越重）

| 维度 | 评分 | 依据 |
| --- | ---: | --- |
| 长期风险负担 | N/A | 未检得任何本药特异的长期随访、迟发性运动障碍、内分泌、代谢、心电或器官毒性数据；最长的人体记录只有 **5 周**开放用药（`PMID:323966`）。类别层面的丁酰苯风险（QT 延长、锥体外系、NMS）本药**从未被单独测定**，记 `N/A` 而不是按类别凑分 |
| 短期耐受负担 | 2 | 唯一的人体数据：20 例以慢性精神分裂症性精神病为主的开放研究，**5 例因各种原因提前退出，余 15 例在五周试验期后总体改善；3 例出现锥体外系反应，未观察到其他副作用；片剂胃耐受性良好**（`PMID:323966`）。样本小、无对照、无盲法，"3／20"没有分母意义（退出者未纳入），因此只给 2，并同时说明这一数字不能当作发生率 |
| 相互作用／监测负担 | N/A | 未取得本药的人体 CYP、蛋白结合或合并用药研究，也无监测要求文本。体外与动物线索（大鼠脑 α2 受体的中等竞争性结合，`PMID:6149771`；大鼠单次腹腔注射后血浆与肾上腺皮质酮升高，属该研究测试的丁酰苯之一，`PMID:6110713`）不能转化为临床监测要求 |
| 停药负担 | N/A | 未检得本药撤药症状报告或随机停药研究 |
| 滥用／误用潜力 | N/A | 未检得本药的人体强化效应、自身给药或带分母的非医疗使用证据。未列管、数据库无产品、说明书缺章节都不能单独支撑 1 分（按 SCORING 需药物特异证据） |
| 非适应证／潜在不适当处方风险（中国） | N/A | 本药在中国无上市与处方数据；本轮**未逐条复核** 2017 版中国老年 PIM 标准表 1 与 AGS Beers 2023，只按"抗精神病药"类别条款理解；没有当地处方偏离数据即记 `N/A` |

总体解释：moperone 是本轮 8 个药里**证据最薄**的一个。它的"风险画像"目前只能写成一句话：一项五周、20 例、开放、无对照的欧洲老研究中，锥体外系反应是唯一被记录的不良效应，且没有任何长期数据、没有现行文本、没有药动学参数。任何比这更具体的风险表述，都会超出本轮可核范围。

### 2.2 按使用场景适宜度（A–D）

本轮不设 A–D 行。理由：① 没有任何法域的现行或历史核准适应证可由官方文本核实；② 唯一的人体研究是 20 例开放设计（`PMID:323966`），主要终点是研究者总体印象，无对照、无盲法、无现代量表；③ 1969 年"本药在丁酰苯中的临床地位"一文本轮**只取得题录**（`PMID:5354545`，挪威语期刊），无法引用其结论；④ 该分子在现行数据库中无产品，历史用法不具当前决策价值。按 SCORING，"未取得文本""未获批"本身不构成 C／D 分理由，历史材料留在 §4／§5／§10。

## 3. 主要作用

可核的机制线索只有两类非临床结果：① 在受体筛查中，本药对大鼠皮层 [3H]-clonidine 与 [3H]-yohimbine 结合的**竞争强度位于"中等"一档**（顺序为 clocapramine／carpipramine ≫ perphenazine、fluphenazine、α,β-flupentixol > propericiazine、levomepromazine > chlorpromazine、pimozide > **moperone** ≫ haloperidol、sulpiride），作者据此讨论部分神经阻滞药的 α2 阻断与其抗抑郁样作用的可能关系（`PMID:6149771`）；② 在按"核团 Fos 表达差异"给抗精神病药分层的 rat 研究中，本药落在**中等"非典型指数"组**（与 zotepine、perospirone、sulpiride、sultopride、thioridazine 等并列；`PMID:15519367`）。这两条都是体外／动物结果，**不写 D2 Ki、不写占有率、不写人体"非典型"标签**。

## 4. 适应范围

**现行核准适应证：待核实。** 未取得任何法域说明书，因此不写核准措辞、剂量、禁忌与监测。

**文献中出现过的用途（非核准表述）**：慢性精神分裂症性精神病的口服（含缓释片）治疗（20 例开放研究，`PMID:323966`）；1969 年一篇讨论"本药在丁酰苯类中的临床地位"的挪威语文献（`PMID:5354545`，题录）。此外本药被用于眼科药理学实验模型（家兔眼压与眼血流，`PMID:6147806`、`PMID:1302433`、`PMID:8102175`、`PMID:2576433`）与胃溃疡大鼠模型（`PMID:866398`）——**这些是实验工具性使用，不是适应证**。

**剂量**：**不写**。可核的只有"该开放研究使用缓释片、疗程五周"这一事实，其具体 mg 数本轮未取得。WHO DDD 20 mg 口服／20 mg 非口服仅为统计口径。

**中国**：上市剂型与核准适应证待核实。

## 5. 实际效果与局限

- **唯一的人体研究**：瑞士一项开放临床试验，20 例多为慢性精神分裂症性精神病的患者，使用 moperone 盐酸盐**缓释片**，5 例因各种原因提前退出；其余 15 例在五周试验期后与既往神经阻滞剂治疗相比"总体明显改善"；3 例出现锥体外系反应，未观察到其他副作用；胃耐受性好（`PMID:323966`）。**设计与局限**：无对照、无盲法、终点为研究者总体印象、退出者未纳入分析、疗程仅五周，且作者本人在摘要中未给量表分值。**因此本条不写"有效"，只写"作者报告了什么"**。
- **未被取得的关键文献**：`PMID:5354545`（1969，本药在丁酰苯中的临床地位）、`PMID:5536800`（1970，本药药动学）、`PMID:5818759`（1969，大鼠分布与神经阻滞活性的关系）本轮**只有题录**，其结论、剂量与参数一律不引用。
- **眼科与胃肠模型的动物数据**：家兔实验中多巴胺拮抗剂（含本药）可降低人工升高的眼压并增加脉络膜／视网膜血流（`PMID:6147806`、`PMID:1302433`、`PMID:8102175`、`PMID:2576433`）；大鼠应激性与 reserpine 溃疡模型中，本药与 pimozide、trifluperidol、chlorpromazine 一样不影响溃疡形成（`PMID:866398`）。**这些不能外推为人体青光眼或胃保护效应**。
- **总体局限**：本药的临床证据不足以支撑任何疗效档位；真正的缺口是"当年是否有过随机对照"——本轮以通用名与 KEGG 给出的商品名（Luvatren）检索 PubMed 与 openFDA 均未见相关试验，但**检索为空不等于没有试验**。

## 6. 长期风险

**未检得任何本药特异的长期风险数据**（无迟发性运动障碍、无催乳素与内分泌、无体重与代谢、无血液与肝肾功能、无心电图与 QT 记录，§2.1）。

**类别与骨架不外推**：本药与氟哌啶醇共享"4-羟基-4-芳基哌啶丁酮"骨架（`PUBCHEM-ID`），但**氟哌啶醇与 droperidol 的 QT／尖端扭转向证据不能移给本药**；仓库已有的 [benperidol](benperidol.md) 等同类条目同样不能作本药的风险来源。丁酰苯类在老年痴呆人群死亡风险、锥体外系与 NMS 上的类别警示属于"类别层面、本药未单独测定"，本条只在 §2.1 以 `N/A` 表达这种空白，不写成已证实的本药风险。

## 7. 短期风险、停药与误用

**短期**：唯一可核的本药人体不良事件是**锥体外系反应（15 例继续用药者中 3 例）**，同一研究报告"未见其他副作用"与良好的胃耐受性（`PMID:323966`）——无镇静、低血压、口干、视野模糊等的量化数据。**驾驶与操作机器**：无资料。**停药**：无撤药报告，记 `N/A`。**误用**：无药物特异证据，记 `N/A`。**过量**：未取得中毒病例、致死量或处理经验，不引用其他丁酰苯的数据。

## 8. 重要相互作用

本轮未取得本药的人体相互作用研究，也无文本可引的禁忌清单。非临床线索只有：大鼠皮层 α2 受体结合处于中等强度（`PMID:6149771`）；单次给予大鼠后血浆与肾上腺皮质酮升高、该效应被地塞米松预处理或垂体切除阻断，说明经 ACTH 通路而非单纯低温所致（本药是该研究测试的丁酰苯之一，`PMID:6110713`）。锂、其他延长 QT 的药物、左旋多巴、抗胆碱能药等类别清单**在本条不列**，因为那是其他分子说明书的内容。

## 9. 特殊人群

**无现行文本，不写禁忌与剂量调整**。人体资料仅有 20 例慢性精神病成年患者（`PMID:323966`）；老年、儿童、妊娠与哺乳、肝肾功能全无数据。家兔与大鼠实验（§5）不能用于人群分层。以上为空白，不是"无特殊注意"。

## 10. 证据边界

1. **没有任何官方文本**：美国 openFDA（标签、NDC、drugs@fda）与 DailyMed、法国 BDPM、西班牙 CIMA 均无本药记录；英国 emc 清单未取回；比利时与意大利的监管机构公开检索入口为动态页面，本环境未取回（`OPENFDA`、`US-DAILYMED`、`FR-BDPM`、`ES-CIMA`、`UK-EMC`）。零命中只写检索事实，**不推断未批准、已撤市或不存在**。要升 `reviewed`，需要任一法域的现行或历史 RCP／说明书，或带规格、公告日与生效日的退市／撤销公告。
2. **DailyMed 本轮被拦**：接口返回 JS 验证页，未取得 `total_elements`。
3. **商品名与法域归属未定**：取证单把本药记为"比利时 Dosen／意大利 Listom"，本轮**未能核实**（openFDA 商品名检索 0；PubMed 共现检索 `moperone AND dosen`、`moperone AND luvatren` 均为 0 条）。KEGG 的 `Moperone hydrochloride (JAN); Luvatren (TN)` 属于转录性收载页，**不能作为"某国已批准"的证据**，本条据此只记录"存在过该命名"。
4. **perispiramide 关系未核**：以该词检索 PubMed 为 0 条；其与本药或其代谢物是否同一实体**不作判断、不写入正文**。
5. **人体证据只有 1 项开放研究、20 例、5 周**；其余为本药相关动物的分布、代谢、眼压、溃疡与受体研究，以及 3 篇只有题录的方法学／临床论文（`PMID:5354545`、`PMID:5536800`、`PMID:5818759`）。
6. **"未检索到随机试验"是检索事实**，不是"本药无随机试验"的结论；本药的历史商品名与别名不全，检索面本身受限（§10 第 3 项）。
7. **DDD 20 mg 口服／20 mg 非口服是统计指标**；WHO 给的非口服 DDD 不代表本条已核实存在注射剂型（§1）。
8. **中国字段**：沿用 2026-10-06 的目录核查结论与"不等于非管制"的限定；中国注册状态因 NMPA／CDE 入口不可脚本检索而待核实。

## 11. 深入分析与来源

本条目不建专题文件：唯一有独立价值的专题问题应是"本药为何在 1970 年代后从临床中消失"，但回答它需要监管撤市文件与当年的对照试验原文，本轮两者都没有；用 3 篇题录包装专题没有决策价值。

**监管与检索记录**：[openFDA 标签检索（NOT_FOUND）](https://api.fda.gov/drug/label.json?search=openfda.generic_name:%22moperone%22&limit=5)；[openFDA drugs@fda 申请检索（NOT_FOUND）](https://api.fda.gov/drug/drugsfda.json?search=openfda.generic_name:%22moperone%22&limit=1)；[DailyMed 按药名检索接口（本轮返回验证页）](https://dailymed.nlm.nih.gov/dailymed/services/v2/spls.json?drug_name=moperone)；[法国 BDPM 字母序检索 MOPER（0 行）](https://base-donnees-publique.medicaments.gouv.fr/api/recherche/alphabetique?startBy=MOPER&page=1&limit=20)；[西班牙 CIMA 检索入口](https://www.aemps.gob.es/cima/publico/home.html)；[英国 emc 检索页](https://www.medicines.org.uk/emc/search?s=moperone)；[KEGG DRUG D02623／D01105（转录／收载页，非监管原件）](https://www.kegg.jp/entry/D01105)；[NMPA 政务服务窗口](https://www.nmpa.gov.cn/zwfwqjd/index.html?type=pc) 与 [CDE 上市药品目录集](https://www.cde.org.cn/hzmp/)（均不可脚本检索）。

**研究**：[20 例慢性精神病患者的缓释片开放研究（PMID:323966）](https://pubmed.ncbi.nlm.nih.gov/323966/)；[本药在丁酰苯类中的临床地位（题录，PMID:5354545）](https://pubmed.ncbi.nlm.nih.gov/5354545/)；[moperone 药动学（题录，PMID:5536800）](https://pubmed.ncbi.nlm.nih.gov/5536800/)；[丁酰苯在大鼠的分布与神经阻滞活性（题录，PMID:5818759）](https://pubmed.ncbi.nlm.nih.gov/5818759/)；[神经阻滞药与抗抑郁药对大鼠脑 α2 受体的竞争（PMID:6149771）](https://pubmed.ncbi.nlm.nih.gov/6149771/)；[丁酰苯类对大鼠垂体—肾上腺活动的影响（PMID:6110713）](https://pubmed.ncbi.nlm.nih.gov/6110713/)；[多巴胺拮抗剂降低家兔眼压（PMID:6147806）](https://pubmed.ncbi.nlm.nih.gov/6147806/)；[家兔眼血流改善（PMID:1302433）](https://pubmed.ncbi.nlm.nih.gov/1302433/)；[眼脉搏性血流（PMID:8102175）](https://pubmed.ncbi.nlm.nih.gov/8102175/)；[经漩涡静脉注射后的眼压变化（PMID:2576433）](https://pubmed.ncbi.nlm.nih.gov/2576433/)；[大鼠实验性溃疡的无保护效应（PMID:866398）](https://pubmed.ncbi.nlm.nih.gov/866398/)；[24 种抗精神病药 Fos 非典型指数（含本药，PMID:15519367）](https://pubmed.ncbi.nlm.nih.gov/15519367/)。

**分类与身份**：[WHO ATC/DDD Index `N05AD04`](https://atcddd.fhi.no/atc_ddd_index/?code=N05AD04)；[PubChem CID 4249](https://pubchem.ncbi.nlm.nih.gov/compound/4249)；[Wikidata Q6908807](https://www.wikidata.org/wiki/Q6908807)；[DrugBank DB13554](https://www.drugbank.ca/r/DB13554)；English Wikipedia（标题指针，未复制正文）：[Moperone](https://en.wikipedia.org/wiki/Moperone)。

统计与缺口见 [目录索引](../catalog/index.md)。
