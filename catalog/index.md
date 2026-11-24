# 精神药物分类目录索引

本索引以 WHO ATC/DDD Index 2026 为核心分类依据，提供六个核心 ATC 组及跨组专题档案的入口。ATC 分类与具体药品产品、适应证及监管批准状态分别核对。

## 核心 ATC 组

| ATC 组 | 官方分类名称 | 五级编码数 | 独立档案数 | 目录 |
| --- | --- | ---: | ---: | --- |
| N05A | ANTIPSYCHOTICS | 70 | 70 | [N05A](N05A.md) |
| N05B | ANXIOLYTICS | 39 | 36 | [N05B](N05B.md) |
| N05C | HYPNOTICS AND SEDATIVES | 76 | 68 | [N05C](N05C.md) |
| N06A | ANTIDEPRESSANTS | 68 | 68 | [N06A](N06A.md) |
| N06B | PSYCHOSTIMULANTS, AGENTS USED FOR ADHD AND NOOTROPICS | 38 | 38 | [N06B](N06B.md) |
| N06C | PSYCHOLEPTICS AND PSYCHOANALEPTICS IN COMBINATION | 3 | 0 | [N06C](N06C.md) |
| **合计** |  | **294** | **280** |  |

## 跨组专题档案

核心六组之外，仓库另收录跨 ATC 主题药物档案。补充目录目前选录 91 项，其中 89 项对应具体药物档案，2 项仅保留为分类记录。

- [跨组补充目录](related.md)

仓库 `drugs/` 共包含 **384 份药物档案**，其中核心六组 280 份，跨组主题 104 份。

## 档案状态

| 状态 | 数量 | 含义 |
| --- | ---: | --- |
| `reviewed` | 257 | 基本信息、适应范围、管制状态、关键临床证据、主要风险、重要相互作用与证据边界已按项目标准系统核查。 |
| `basic` | 120 | 已有可靠基础临床或安全信息，但核心模块尚未完成系统核查。 |
| `indexed` | 7 | 药物身份与分类已核实。 |
| **合计** | **384** | 按各药物档案顶部状态字段汇总，统计基准为 2026-11-24。 |

核心六组状态为 178 `reviewed`、98 `basic`、4 `indexed`。跨组主题档案为 79 `reviewed`、22 `basic`、3 `indexed`。Wave 17 处理 38 份 `basic` 档案，5 份达到 `reviewed`，33 份保持 `basic`，详见 [Wave 17 计划完成记录](../plans/wave17_basic_cleanup/00_MASTER_PLAN.md)。

部分 `basic` 档案另有「临床现状」与「研究处置」标签，用于说明是否仍有现实人用价值及后续补证方向。这些标签不替代档案证据状态。标记为「仅保留历史档案」的条目仍可保持 `basic`，不代表已达到 `reviewed` 标准。

## 分类与阅读边界

- ATC 编码用于分类，不直接证明药物具有该组名称所暗示的临床适应证。
- 固定复方应作为独立产品核对，不从单方档案继承适应证、剂量或安全性结论。
- 不指明全部成分的复方分类代码仅作分类记录，不自动建立具体药物档案。
- 具体适应证与监管状态应回到相应药物档案，并核对法域、产品、剂型及说明书版本。
- 中国管制状态与上市批准状态分开记录。

专题分析入口：[专题索引](analyses.md)。

分类依据：[WHO ATC/DDD Index](https://atcddd.fhi.no/atc_ddd_index/)，版本 2026。
