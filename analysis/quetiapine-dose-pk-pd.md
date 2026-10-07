# quetiapine｜剂量—暴露—靶点占用—临床结局

> 配套主条目 [drugs/quetiapine.md](../drugs/quetiapine.md) ｜ 最后核查 2026-10-07  
> 本页只放支撑主条目结论的定量材料与其口径冲突；实验操作细节直接回原始文献。  
> 引用键同主条目：`US-IR`／`US-XR`＝美国现行处方资料（DailyMed 更新 2026-04-10）；`UK-IR`／`UK-XL`＝英国 SmPC。

## 1. 受体亲和力：标签口径

数值取自 `US-IR` §12.2，单位 nM。**标签未在该表内注明物种、受体来源（克隆或原生组织）、配体与测定方法**，因此只能用于同一来源内的相对比较。

| 靶点 | quetiapine | norquetiapine |
| --- | --- | --- |
| D1 | 428 | 99.8 |
| D2 | 626 | 489 |
| 5-HT1A | 1040 | 191 |
| 5-HT2A | 38 | 2.9 |
| H1 | 4.4 | 1.1 |
| M1 | 1086 | 38.3 |
| α1b | 14.6 | 46.4 |
| α2 | 617 | 1290 |

可读出的结论只有两条：母药对 H1、α1b、5-HT2A 的亲和力高于 D2；代谢物在所列靶点普遍强于母药，其中 M1 由 1086 nM 降至 38.3 nM（与 `UK-XL` §5.1 的定性描述一致）。两份标签均未给出 NET 数值。

## 2. NET 与 5-HT1A：原始临床前定量

来源 `PMID:26436896`／`PMCID:PMC4813385`（Cross 等，Br J Pharmacol 2016;173:155-66；作者供职并受资于 AstraZeneca），数值已回全文核对：转运体数据在原文表 1、受体数据在原文表 2，方法见原文 Methods（克隆人靶点细胞膜、`[3H]`-MeNER SPA 结合、荧光法功能摄取、GTPγS SPA 测 5-HT1A 激动效能；pKi 由 Cheng–Prusoff 换算，取 ≥3 次独立测定均值）。

| 药物 | hNET 结合 pKi ± SD | hNET 摄取 pKi ± SD |
| --- | --- | --- |
| quetiapine | IA | IA |
| norquetiapine | 7.54 ± 0.05 | 7.47 ± 0.17 |
| duloxetine | 7.62 ± 0.04 | 7.65 ± 0.19 |
| reboxetine | 8.73 ± 0.29 | 8.83 ± 0.14 |
| atomoxetine | 8.35 ± 0.05 | 8.83 ± 0.21 |
| clozapine | 5.44 ± 0.04 | 6.38 ± 0.09 |
| aripiprazole | 5.93 ± 0.02 | 6.05 ± 0.15 |
| risperidone | IA | IA |

IA 为原文标注的 inactive；pKi 为负对数口径，norquetiapine 的 7.54 约相当于 Ki 29 nM。原文将其 NET 亲和力描述为接近部分抗抑郁药（与 duloxetine、imipramine 7.24 ± 0.03 最接近），低于 desipramine、reboxetine、nisoxetine 与 atomoxetine，较 clozapine 与 aripiprazole 高约 30–100 倍。同表中 norquetiapine 对 SERT 仅弱摄取抑制（5.94 ± 0.19，结合 IA），对 DAT 结合与摄取均 IA，母药在三种转运体全部 IA。

5-HT1A：两者均为低效力、高 Emax 的激动剂——quetiapine pEC50 4.77 ± 0.22、Emax 89 ± 8%；norquetiapine pEC50 5.47 ± 0.16、Emax 90 ± 8%；对照 aripiprazole pEC50 7.87 ± 0.28 但 Emax 仅 65 ± 3%。谷氨酸受体方面，母药与代谢物在 50 µM 以下均无可检出结合（原文表 S1）。

在体（大鼠／小鼠，不外推人体）：norquetiapine 皮下给药使蓝斑 `[3H]`-MeNER 结合的 NET 占有率 ED50 约 2 mg/kg（reboxetine 约 0.05、desipramine 约 0.15 mg/kg）；30 mg/kg 减少 BALB/c 小鼠强迫游泳不动时间（母药无效），5 mg/kg 减少 Wistar 大鼠习得性无助的逃跑失败次数，其增强惩罚冲突反应率的作用可被 WAY100635 0.1 mg/kg 阻断（母药 10 mg/kg 同向但未达显著）。

## 3. 同一文献与标签的 D2 数值冲突（必须保留）

Cross 2016 **原文表 2 按行给出** hD2 结合 pKi：quetiapine 7.25 ± 0.25、norquetiapine 7.23 ± 0.40（同表 h5-HT2A 分别 7.54 ± 0.30 与 8.29 ± 0.47）。但结果段落同一句写作 "norquetiapine and quetiapine pKi = 7.25 ± 0.25 and 7.23 ± 0.40, respectively"，把两个数值归属给相反的对象——表格与正文自相矛盾。本页以表 2 的行归属为准并保留该冲突。

- 两值仅差 0.02 个对数单位，"母药与代谢物在 D2 上亲和力相近"这一结论不受归属歧义影响。
- 无论按哪种读法，Cross 的母药 D2 值（约 56–59 nM）比 `US-IR` §12.2 的 626 nM 高约一个数量级；5-HT2A（约 29 nM 对 38 nM）则接近。两套数值来自不同实验体系与不同报告口径（pKi ± SD 对 Ki nM），不取平均、不互相替换，也不据此推导任何剂量下的选择性。

## 4. 人体靶点占用（PET）

| 指标 | 数值 | 测量条件 | 来源 |
| --- | --- | --- | --- |
| 纹状体 D2 占用（末次给药后 12–14 h） | 0%–27% | 12 名精神分裂症患者，`[11C]raclopride`，150／300／450／600 mg/d（每组 3 人），治疗 3 周后扫描 | `PMID:10839333` |
| D2 占用（单次给药后 2–3 h） | 58%–64% | 另 2 名患者，同示踪剂，峰时相 | `PMID:10839333` |
| 速释 vs 缓释的 D2 占用 | 峰、谷时相占用无显著差异 | 开放标签交叉 PET，12 名受试者，等每日剂量 300／600／800 mg/d | `PMID:18312041` |
| 丘脑 NET 占用 | 150 mg/d 后 19%；300 mg/d 后 35% | 9 名健康男性（21–33 岁），`(S,S)-[18F]FMeNER-D2`，缓释 150 或 300 mg/d 共 6–8 天，尾状核作参考区 | `PMID:23809226` |
| NET 50% 占用对应 norquetiapine 血浆浓度 | 161 ng/ml（丘脑，估算） | 同上 | `PMID:23809226` |
| NET 50% 占用对应剂量与浓度 | 缓释 256 mg（下丘脑，第 2 周）；norquetiapine 36.8 µg/L | 5 名 MDD ＋5 名双相患者，`(S,S)-[11C]O-methyl reboxetine`，目标剂量 150 mg（MDD）／300 mg（双相） | `PMID:29016993` |

四研究样本 2–12 人，脑区、示踪剂与时相各不相同；两项 NET 研究的"50% 占用"估算值相差数倍，按原文并列而不合并。D2 占用均为特定时相单点测量，不能用来建立剂量与疗效的对应关系；`PMID:10839333` 作者本人的结论亦限于"短时高占用可能足以产生抗精神病效应"这一假设。

## 5. IR／XR 关键药代

| 项目 | 速释 | 缓释 | 来源 |
| --- | --- | --- | --- |
| Tmax | 约 1.5 h | 约 6 h | `US-IR` §12.3；`US-XR` §12.3；`UK-XL` §5.2 |
| 终端 t½ | 约 6 h | quetiapine 约 7 h；norquetiapine 约 12 h | 同上 |
| 进食 | Cmax +25%、AUC +15% | 高脂餐使 50／300 mg 片 Cmax +44%–52%、AUC +20%–22%；轻餐无显著影响；建议空腹或仅配轻餐 | `US-IR`／`US-XR` §12.3、§2.1；`UK-XL`（记约 50% 与 20%） |
| 生物利用度 | 片剂相对口服溶液 100% | 与等总日剂量分两次速释相比 AUC 相当、Cmax 低 13%，norquetiapine AUC 低 18% | `US-IR` §12.3；`UK-XL` §5.2 |
| 代谢与代谢物暴露 | 主要经肝 CYP3A4 亚砜化与氧化为母体酸（均无药理活性） | 稳态 norquetiapine Cmax 为母药 21%–27%、AUC 46%–56%（`US-XR`）；SmPC 记稳态摩尔峰浓度为母药 35%（`UK-XL`）——口径不同，未合并 | `US-IR`／`US-XR` §12.3；`UK-XL` §5.2 |
| 分布与排泄 | Vd 10±4 L/kg；蛋白结合 83%；`14C` 剂量约 73% 经尿、20% 经粪回收，原药 <1% | 同（SmPC 记尿 73%／粪 21%，未变化原药 <5%） | 同上 |
| 稳态与线性 | 2 天内达稳态，治疗剂量内呈剂量比例 | 800 mg/d 以内线性 | 同上 |
| CYP 抑制 | 母药与 9 种代谢物对 1A2／2C9／2C19／2D6／3A4 的体内抑制作用很小 | 弱抑制，仅出现在人体 300–800 mg/d 浓度的约 5–50 倍处 | `US-IR` §12.3；`UK-XL` §5.2 |

特殊人群：≥65 岁口服清除率降 40%（`US-IR` §12.3、§8.5）／SmPC 记平均清除率较 18–65 岁低约 30%–50%；肝损 8 例平均口服清除率降 30%，其中 2 例 AUC 与 Cmax 达常见值 3 倍（SmPC 建议 50 mg/d 起始）；重度肾损（Clcr 10–30）清除率降 25% 但浓度仍在正常范围内，两文件均记无需调整；10–17 岁按剂量与体重校正后母药 AUC 低 41%、Cmax 低 39%，norquetiapine 校正后与成人相似（`US-XR` §12.3、§8.4）。性别、种族与吸烟对药代无影响（`US-IR` §12.3）。

## 6. 剂量 → 暴露 → 占用 → 结局：能被证据支持到哪一步

1. **剂量→暴露**：治疗剂量范围内近似线性、2 天达稳态（§5）；CYP3A4 抑制／诱导可把暴露改变数倍（酮康唑 AUC +6.2 倍、苯妥英清除率 +约 5 倍）。
2. **暴露→占用**：仅有小样本 PET。D2 占用呈明显**时相依赖**（峰时 58%–64% 对谷时 0%–27%），而速释与缓释在等日剂量下的峰谷占用无显著差异；NET 占用随剂量上升（150→300 mg/d 时 19%→35%），两项研究的"50% 占用浓度"估算互不一致。
3. **占用→结局**：无证据链闭合。标签的剂量—反应形态因适应证而异，且方向不统一：精神分裂症 400 mg 的 PANSS 差值小于 600 与 800 mg（−6.1 对 −12.1、−12.5）；双相抑郁 600 mg 未优于 300 mg（标签注明无额外获益）；MDD 辅助 150 mg 在一项试验未与安慰剂分离；GAD 汇总分析中 300 mg 效应量反而低于 150 mg。
4. 因此**不能**写成"剂量越高越有效"，也不能由 Ki 或占用率推算个体剂量。DDD 0.4 g／日只是群体统计指标，与标签按适应证、剂型与滴定制规定的区间口径不同。

## 7. 注册试验主要终点（供主条目引用，不逐例复述）

主要疗效终点均为"药物减安慰剂的最低二乘均值变化差值（95% CI）"，量表分值越高表示症状越重。速览：精神分裂症 6 周缓释 400／600／800 mg PANSS −6.1／−12.1／−12.5；青少年（13–17 岁）速释 400／800 mg −8.2／−9.3；双相 I 躁狂 3 周缓释 400–800 mg YMRS −3.8，12 周速释 200–800 mg −4.0 与 −7.9，儿童青少年（10–17 岁）−5.2 与 −6.6；双相抑郁 8 周 MADRS 缓释 300 mg −5.5、速释 300 mg −6.1 与 −5.0、600 mg −6.5 与 −4.1；MDD 辅助 6 周缓释 150 mg −1.9（未分离）与 −3.1、300 mg −3.0 与 −2.7。维持期：精神分裂症 171 名开放标签稳定后随机者缓释组至复发时间更长（期中分析）；双相 I 维持两项试验（n=1326，均继续锂或丙戊酸）时间至任意心境事件复发均优于安慰剂。全部数值与设计限制见 `US-XR` §14 表 26–29 与图 1。

## 8. 已知数值不一致清单

| 指标 | 一处 | 另一处 | 处理 |
| --- | --- | --- | --- |
| 母药 D2 亲和力 | 标签 626 nM | Cross 2016 表 2 约 56 nM | 体系不同，并列保留 |
| Cross 2016 D2 归属 | 表 2 行归属 | 结果段文字 | 以表格为准并记录冲突 |
| norquetiapine 相对暴露 | `US-XR` Cmax 21%–27% | `UK-XL` 摩尔峰浓度 35% | 口径不同，不合并 |
| 半衰期 | `US-IR` 速释约 6 h | `US-XR`／`UK-XL` 约 7 h | 剂型与文件不同，并列 |
| 癫痫发生率 | `US-XR` 速释 0.5%／缓释 0.05% | `UK-XL` §4.4"对照试验中与安慰剂无差异" | 表述层级不同，并列 |
| 与 CYP3A4 抑制剂合用 | `US-XR` 剂量减至 1/6 | `UK-XL` §4.3 列为禁忌 | 法域实质差异 |
| 年龄下限 | 美国批准 10–17 岁双相躁狂、13–17 岁精神分裂症 | 英国 18 岁以下不推荐 | 不得写成全球统一状态 |

## 9. 来源

- 美国 SEROQUEL 速释片处方资料（NDA020639，DailyMed 更新 2026-04-10）：[setid 8ae62aaf…](https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=8ae62aaf-f8c5-417f-baac-0098369ca322)；SEROQUEL XR（NDA022047）：[setid ab959a35…](https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=ab959a35-d0ba-4f18-8f2e-6619d88b16e3)。§9.1／§9.2 滥用与依赖表述另经 openFDA 标签接口核对（effective 2026-04-10）：[api.fda.gov/drug/label.json](https://api.fda.gov/drug/label.json?search=openfda.brand_name:%22SEROQUEL%22)。
- 英国 SmPC：[Seroquel XL 300 mg（emc 7603）](https://www.medicines.org.uk/emc/product/7603/smpc)、[Seroquel 25 mg（emc 5495）](https://www.medicines.org.uk/emc/product/5495/smpc)。
- `PMID:26436896` Cross AJ 等（含表 1、表 2 与 Methods）：[PubMed](https://pubmed.ncbi.nlm.nih.gov/26436896/)｜[PMC4813385 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4813385/)
- `PMID:10839333` Kapur S 等 [Arch Gen Psychiatry](https://pubmed.ncbi.nlm.nih.gov/10839333/)；`PMID:18312041` Mamo DC 等 [J Clin Psychiatry](https://pubmed.ncbi.nlm.nih.gov/18312041/)；`PMID:23809226` Nyberg S 等 [Int J Neuropsychopharmacol](https://pubmed.ncbi.nlm.nih.gov/23809226/)；`PMID:29016993` Yatham LN 等 [同刊](https://pubmed.ncbi.nlm.nih.gov/29016993/)
- `PMID:24249315` Asmal L 等 Cochrane 头对头综述 [PubMed](https://pubmed.ncbi.nlm.nih.gov/24249315/)｜[PMC4167871](https://pmc.ncbi.nlm.nih.gov/articles/PMC4167871/)；`PMID:16172203` CATIE [PubMed](https://pubmed.ncbi.nlm.nih.gov/16172203/)
- `PMID:24394383` Montgomery SA 等 GAD 汇总后分析 [PubMed](https://pubmed.ncbi.nlm.nih.gov/24394383/)；`PMID:25007003` Gao K 等 双相抑郁合并 GAD 阴性试验 [PubMed](https://pubmed.ncbi.nlm.nih.gov/25007003/)；`PMID:27544830` Thompson W 等 失眠系统综述 [PubMed](https://pubmed.ncbi.nlm.nih.gov/27544830/)
- 中国处方与药物利用证据见主条目 §2.1 与 §11：`PMID:34315410`、`PMID:42756141`。
