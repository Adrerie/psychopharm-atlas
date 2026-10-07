# Wave 1 审阅修补

> 分支：`feat/reviewed-drug-expansion-wave1`  
> 状态：12 个 Wave 1 条目主体已完成；本轮只修审阅发现的问题，不新增药物。

## 已直接修复

- `AGENTS.md` / `SCORING.md` / 模板：单方评分与固定复方分离；剂型特异风险作为 formulation modifier；主条目不能靠超长表格单元格规避精简。
- `clozapine.md`：FDA 已自 2025-06-13 移除 Clozapine REMS；ANC 监测仍继续。VERSACLOZ 更正为口服混悬液。
- `bupropion.md`：ZYBAN 品牌 discontinued 不等于美国戒烟适应证消失；现行安非他酮 SR 仿制标签仍明确获批戒烟。
- `olanzapine.md` / `fluoxetine.md`：固定复方的适应证、禁忌和风险移出单方评分逻辑。

## 剩余修补

### 1. 压缩过长主条目

只处理：

- `diazepam.md`
- `lithium.md`
- `bupropion.md`
- `zolpidem.md`
- `aripiprazole.md`

目标不是删证据，而是把主文件恢复成几分钟可读的快速判断页：

- 每个评分格只留 1–3 个决定性事实；
- 多个 RR/OR/HR、次要 PK 数字、互相冲突的观察研究细节退到来源；
- 保留真正改变评分或临床判断的数字；
- 不新建 analysis 文件来“存放删下来的内容”，原始来源本身就是细节承载处。

不要求固定字符数，也不为压缩而删掉法域差异、长期风险、停药/误用和证据边界。

### 2. 一次性一致性检查

快速检查 Wave 1 的 12 个条目：

- 固定复方风险没有进入单方基础评分；
- 长效注射、鼻喷、直肠等剂型独有风险只在对应场景/formulation modifier 中说明；
- 没有把品牌 discontinued 写成活性成分适应证消失；
- 没有把旧 REMS 文本当作当前监管状态。

发现明确问题才改，不重新做全量文献搜索。

## 验收

- reviewed 数量仍为 13（喹硫平 + Wave 1 十二药）；
- 不新增药物、不新增 analysis、数据库、CI、评分程序或爬虫；
- 不修改中国管制审计结果，除非发现明确事实错误；
- 更新本 PLAN 为完成，必要时同步 README；不合并 `main`。
