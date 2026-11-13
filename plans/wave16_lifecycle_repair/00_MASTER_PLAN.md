# Wave 16 临床生命周期分类修补

分支：`wave16/basic-upgrade`  
基线：2026-11-13 完成的 125 份 `basic` 临床现状筛查  
范围：只修正临床现状与研究处置，不重做临床综述、评分或历史研究。

## 已直接修复

- 将 19 份没有正面撤市／停供证据、§10 又明确承认证据缺口的档案改为 `待核实`／`有限补证`：`acetylglycinamide-chloral-hydrate`、`allobarbital`、`aprobarbital`、`barbital`、`butriptyline`、`camazepam`、`carbromal`、`chloralodol`、`etallobarbital`、`fencamfamin`、`fluanisone`、`heptabarbital`、`hexapropymate`、`iproclozide`、`nialamide`、`proxibarbal`、`quinupramine`、`reposal`、`vinylbital`。
- `paraldehyde` 改为 `地区性人用`／`有限补证`，补入英国 NHS 处方集与 special-order 临床使用资料，并明确其未获英国上市许可。
- `oxitriptan` 改为 `地区性人用`／`有限补证`，补入意大利 TRIPT-OH AIC、缺氧后肌阵挛适应证与现有供应信息。
- `veralipride` 从 `已淘汰（人用）` 降为 `历史停用`／`有限补证`，因为法国撤回状态与 EMA 建议已核实，但欧委会最终决定尚未取得。
- 修正 `amineptine`、`tacrine` 的状态依据措辞，避免把未取得的 ANSM 文件或未证实的肝毒性撤市原因写成正式监管记录。
- 修复 `pivagabine` §10 内部矛盾，补明意大利 1998 年撤销 Tonerg 授权的正式法令。
- 为 `methaqualone` 补入美国 1984 年 Federal Register 与司法部年报，区分合法生产停止、Schedule I 列管和 NDA 撤销。
- 为 `propentofylline` 补入欧盟兽药数据库的有效犬用 Karsivan 授权记录。
- 恢复 `niaprazine.md` 与 `secobarbital.md` 两份不属于本次筛查范围的格式改动。
- 已同步收紧 `AGENTS.md` 对历史停用、地区性人用及 special-order 供应证据的要求。

## DS 一次性修补任务

1. 逐一复核当前 125 份 `basic` 的临床现状与研究处置字段。只核生命周期分类所需证据，不重做适应证、风险、评分或完整说明书。
2. 对剩余 `历史停用` 条目逐项确认是否有具体法域、具体产品的正面撤市／撤销／停供证据。只有零命中、无现行标签、历史商品名、旧文献、管制记录或报销目录移除的，改为 `待核实`／`有限补证`。
3. 对 `已淘汰（人用）` 条目检查正式退出证据、主要法域现行使用资料与第二条独立证据线。证据不够时降为 `历史停用` 或 `待核实`，不得为了维持原统计而保留。
4. 定点核实以下未决问题：
   - `amobarbital`：英国 dm+d 有 Sodium Amytal Special Order 产品记录。确认其是否有当前临床处方集或专业使用证据。该记录本身不等于实际临床使用。
   - `butobarbital`：英国 dm+d 有 Soneryl Special Order 产品记录。按同一标准核实。
   - `adrafinil`、`talbutal`、`triflupromazine`：复核现有已淘汰判断的正面退出证据与法域范围。
   - `camazepam`：核实意大利 AIC 聚合站转引能否由 AIFA 原始记录支持。
   - `tofisopam`：核实斯洛伐克 Grandaxin 的现行授权依据，并确认是否应纳入地区性人用名单。
   - `deanol`：区分 deanol 与 deanol aceglumate，不跨实体继承批准状态。
   - `acepromazine`、`bromides`：核实仅兽用结论的人用排除范围。
   - `amineptine`、`veralipride`：如能取得 ANSM 或欧委会最终决定，再更新当前缺口。
5. 只修改有证据支持的状态字段、必要的 §10 证据边界与来源链接。不要改评分、临床结论或其他无关段落。
6. 完成后统一重算 125 份档案的临床现状与研究处置，更新 `catalog/index.md`、`README.md`、`HANDOFF.md` 与 `PLAN.md`。保留 `reviewed/basic/indexed` 原有证据完成度统计，不因生命周期调整而升级档案状态。

## 验收

- 每份当前 `basic` 恰有一项临床现状和一项研究处置。
- 每个 `历史停用` 有正面退出证据及明确法域，不把数据库零命中当成撤市证据。
- 每个 `地区性人用` 有现行产品或权威临床使用证据；special-order／进口／未许可供应必须明示。
- 每个 `已淘汰（人用）` 满足 `AGENTS.md` 的独立证据线要求。
- 目录、README、接手说明与逐份档案统计一致。
- 只检查本次改动的 diff、状态计数与新增链接。不要运行重型 CI、批量评分器或无关验证。

## 执行边界

在当前分支一次完成。不得修改 `main`，不得合并。不要新增子计划、子代理、自动化脚本、数据库、CI 或额外验证流程。完成后提交并推送分支，等待人工审阅。
