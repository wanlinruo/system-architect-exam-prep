# E2-09 大数据架构设计 细化 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 将 `02-案例分析/09-大数据架构设计.md` 从骨架（132 行）细化为完整版（320-400 行），覆盖 5V、Lambda、Kappa、Hadoop、Spark/Flink、数据湖/仓库 + 2 道真题示例。

**Architecture:** 单文件重写。完成后用户验证 → 更新 tracker → 双提交。

**Tech Stack:** Markdown + Obsidian callout + Mermaid mindmap + Block ID 锚点。

**Spec:** [2026-05-05-e2-09-bigdata-architecture-design.md](../specs/2026-05-05-e2-09-bigdata-architecture-design.md)

---

## Task 1：重写文件（单次 Write 完成所有 4 节内容）

**Files:**
- Modify: `02-案例分析/09-大数据架构设计.md`（重写为细化版）

> 内容详尽参照 spec 三、各节内容设计。

- [ ] **Step 1: 写入 frontmatter**

更新 date 为 2026-05-05，tags / aliases 保留并补充 OLAP/OLTP / Lakehouse 等。

- [ ] **Step 2: 写入标题与 warning callout**

```markdown
# 大数据架构设计

> [!warning] 高频考点
> 核心考点：==Lambda 架构==（批+流双层）、==Kappa 架构==（仅流）、==Hadoop 生态==（HDFS / MapReduce / YARN）、==Spark vs Flink==、==数据湖 vs 数据仓库==、==大数据 5V==。
>
> **状态**：✅ 已细化
>
> **速查跳转**：[[#9.2.1 Lambda 架构（必考核心）|Lambda]] · [[#9.2.2 Kappa 架构（必考核心）|Kappa]] · [[#9.2.6 数据湖 vs 数据仓库（必考）|数据湖vs仓库]] · [[#9.4 真题与练习|真题]]
```

- [ ] **Step 3: 写入知识全景 mindmap**

含 7 大分支：5V / Lambda / Kappa / Hadoop / Spark vs Flink / 数据湖 vs 数据仓库 / OLAP vs OLTP

- [ ] **Step 4: 写入 9.1 核心概念**

3 个子节：
- 9.1.1 大数据 5V 特征表（block ID `^bigdata-5v`）
- 9.1.2 批处理 vs 流处理对比（block ID `^batch-vs-stream`）
- 9.1.3 OLAP vs OLTP 对比（引用 [[../01-综合知识/04-数据库系统]]）

callout：`> [!important]` 5V + 批/流、`> [!tip]` 量速样真值口诀

- [ ] **Step 5: 写入 9.2 关键技术与架构**

6 个子节：
- 9.2.1 Lambda 架构 3 层（批/速度/服务）+ 文本架构图（block ID `^lambda-architecture`）
- 9.2.2 Kappa 架构（仅流 + Kafka 重放，block ID `^kappa-architecture`）
- 9.2.3 Lambda vs Kappa 6 维对比（block ID `^lambda-vs-kappa`）
- 9.2.4 Hadoop 生态（HDFS/MapReduce/YARN/Hive/HBase/Pig/Sqoop，block ID `^hadoop-ecosystem`）
- 9.2.5 Spark vs Flink 6 维对比（block ID `^spark-vs-flink`）
- 9.2.6 数据湖 vs 数据仓库（Schema-on-Read vs Schema-on-Write、ETL vs ELT，block ID `^datalake-vs-warehouse`）

callout：`> [!important]` Lambda 3 层、Kappa 单层、数据湖 vs 仓库、`> [!tip]` ETL vs ELT

- [ ] **Step 6: 写入 9.3 典型考点与解题套路**

3 个子节：
- 9.3.1 Lambda / Kappa 选择题三段论模板
- 9.3.2 关键字判定速查（6 行表，block ID `^bigdata-keywords`）
- 9.3.3 数据湖/仓库选型套路（适合场景 + 湖仓一体 Lakehouse）

callout：`> [!tip]` 答题模板、关键字判定、湖仓一体

- [ ] **Step 7: 写入 9.4 真题与练习**

2 道真题（题目 + 完整答题）：
- 9.4.1 真题示例 1：互联网公司 Lambda vs Kappa 选型（block ID `^realexam-lambda-kappa`）
- 9.4.2 真题示例 2：零售企业数据湖 vs 数据仓库（block ID `^realexam-lake-vs-warehouse`）

每道真题答题按"理论 + 分点 + 结论"三段论。

- [ ] **Step 8: 保留关联链接**

```markdown
## 关联链接

- 返回案例分析索引：[[00-案例分析解题框架]]
- 返回主索引：[[../MOC]]
- 关联综合知识章节：
    - [[../01-综合知识/04-数据库系统]]：分布式数据库、数据仓库 OLAP / OLTP
    - [[../01-综合知识/02-操作系统]]：分布式文件系统基础
    - [[../01-综合知识/16-其他知识]]：大数据 5V 特征、云计算
- 关联案例分析：[[04-云原生架构设计]]（容器化部署 Hadoop/Spark）
```

- [ ] **Step 9: 校对**

- 文件行数 320-400
- block ID 锚点 ≥10 个：`^bigdata-5v`、`^batch-vs-stream`、`^lambda-architecture`、`^kappa-architecture`、`^lambda-vs-kappa`、`^hadoop-ecosystem`、`^spark-vs-flink`、`^datalake-vs-warehouse`、`^bigdata-keywords`、`^realexam-lambda-kappa`、`^realexam-lake-vs-warehouse`
- 对比表 ≥6 个
- 真题示例 2 道
- 与 spec 三、各节内容设计 一致

---

## Task 2：用户验证暂停

- [ ] **Step 1: 报告完成，请用户在 Obsidian 中检查**

校对项：
- mindmap 渲染（7 大分支）
- 所有 callout 颜色正确
- 跨文件链接 [[00-案例分析解题框架]]、[[04-云原生架构设计]]、[[../01-综合知识/04-数据库系统]] 可点击
- Lambda / Kappa 文本架构图渲染正常
- 真题示例 2 道完整呈现

- [ ] **Step 2: 等用户确认无异常后再进入 Task 3**

---

## Task 3：用户验证后更新 tracker 并提交

**Files:**
- Modify: `docs/audit/revision-task-tracker.md`

- [ ] **Step 1: 提交 docs commit**

```bash
cd "/Users/wanlinruo/Library/Mobile Documents/iCloud~md~obsidian/Documents/project-003"
git add "02-案例分析/09-大数据架构设计.md"
git commit -m "docs(E2-09): 细化大数据架构设计专题，骨架→完整版

Co-Authored-By: Claude Opus 4.7 (1M context) <noreply@anthropic.com>"
```

- [ ] **Step 2: 追加 tracker 日志条目**

```markdown
| 2026-05-05 | E2-09 | 细化大数据架构设计专题骨架→完整版380+行：9.1核心概念(5V特征量速样真值Volume/Velocity/Variety/Veracity/Value+批处理vs流处理对比+OLAP vs OLTP)/9.2关键技术(Lambda 3层架构批处理层/速度层/服务层+Kappa单层流处理+Kafka重放+Lambda vs Kappa 6维对比+Hadoop生态HDFS/MapReduce/YARN/Hive/HBase+Spark微批vs Flink纯流6维+数据湖vs数据仓库Schema-on-Read/Write+ETL vs ELT)/9.3解题套路(Lambda/Kappa三段论模板+6行关键字判定+数据湖/仓库选型套路+湖仓一体Lakehouse)/9.4真题2道(题1:互联网公司Lambda vs Kappa Schema演化频繁选Kappa+题2:零售企业数据湖+数据仓库湖仓一体)；11个block ID锚点 | `<commit-hash>` | 通过 |
```

- [ ] **Step 3: 提交 chore commit**

```bash
git add docs/audit/revision-task-tracker.md
git commit -m "chore(E2-09): 更新任务日志，大数据架构设计细化完成

Co-Authored-By: Claude Opus 4.7 (1M context) <noreply@anthropic.com>"
```

- [ ] **Step 4: 验证 git 状态**

```bash
git log --oneline -5
git status
```

预期：两条新提交在顶部，工作区 clean。

---

## 自检（Self-Review）

- ✅ Spec 覆盖：spec 三、各节内容设计 全部映射到 Task 1
- ✅ 无占位符：内容详细参照 spec
- ✅ 类型一致：block ID 命名与 spec 4.1 一致
- ✅ 风格统一：与 E2-02 至 E2-08 完全对齐
