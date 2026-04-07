# 系统架构设计师备考资料体系 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 为2026年5月系统架构设计师考试构建完整的 Obsidian 备考知识体系，覆盖综合知识、案例分析、论文三科。

**Architecture:** 按红宝书重点级别组织优先级，综合知识按红宝书14章拆分为16个独立文件。每个 md 文件内部统一结构（mermaid思维导图 + 高/中/低频标注 + 双向链接）。

**Tech Stack:** Markdown + Mermaid + Obsidian（双向链接 `[[]]`、标签 `#tag`）

**Spec:** `docs/superpowers/specs/2026-04-06-system-architect-exam-prep-design.md`

**参考资料（按优先级）：**
- 红宝书：`assets/file/系统架构设计师红宝书一本全.pdf`（208页，2026年5月终稿v4.0）
- 教材PDF：`assets/file/系统架构设计师教程(第4版).pdf`（662页）

**审查追踪：** `docs/audit/revision-task-tracker.md`

---

## Phase 0: 基础骨架 ✅ 已完成

### Task 1: MOC 知识地图入口 ✅

**Files:** `MOC.md`

- [x] **Step 1: 创建 MOC.md** — 已完成 (`39a5ac0`)

### Task 2: 备考总攻略 ✅

**Files:** `00-备考总攻略.md`

- [x] **Step 1: 创建 00-备考总攻略.md** — 已完成 (`42bb547`)

### Task 3: 综合知识全景图 ✅

**Files:** `01-综合知识/00-综合知识全景图.md`

- [x] **Step 1: 创建目录结构** — 已完成 (`155d19e`)
- [x] **Step 2: 创建 00-综合知识全景图.md** — 已完成 (`155d19e`)

### Task 4: 第6章 系统架构设计基础知识 ✅

**Files:** `01-综合知识/06-系统架构设计基础知识.md`（后续将重命名为 `08-系统架构设计.md`）

- [x] **Step 1: 创建 06-系统架构设计基础知识.md** — 已完成 (`56ce80b`)
- [x] **Step 2: 内容审查修正（A1）** — 对齐红宝书，补充C2/闭环控制、4+1视图区分、ABSD关键词、软件产品线 (`7ae619c`)

---

## Phase A: 基础修正（修复现有内容）

### Task A1: 修正 06-系统架构设计基础知识.md ✅

- [x] 已完成 (`7ae619c`)

### Task A2: 更新设计文档和实施计划 🔄

**Files:**
- Modify: `docs/superpowers/specs/2026-04-06-system-architect-exam-prep-design.md`
- Modify: `docs/superpowers/plans/2026-04-06-system-architect-exam-prep.md`

- [ ] **Step 1: 按新16文件目录结构更新设计文档的文件结构、参考资料、优先级策略**
- [ ] **Step 2: 按新 Phase A-E 结构重写实施计划**

### Task A3: 更新 00-综合知识全景图

**Files:**
- Modify: `01-综合知识/00-综合知识全景图.md`
- Modify: `01-综合知识/00-综合知识全景图.canvas`（如有）

- [ ] **Step 1: 按新16文件目录结构调整全景图思维导图和链接**

### Task A4: 更新 MOC.md

**Files:**
- Modify: `MOC.md`

- [ ] **Step 1: 链接指向新文件名，补充新增文件入口**

### Task A5: 更新 00-备考总攻略.md

**Files:**
- Modify: `00-备考总攻略.md`

- [ ] **Step 1: 按红宝书优先级重排冲刺计划，更新文件引用**

---

## Phase B: P0 新增内容（超级重点缺漏）

### Task B1: 需求工程

**Files:**
- Create: `01-综合知识/06-需求工程.md`

- [ ] **Step 1: 创建 06-需求工程.md**

对应红宝书ch2（超级重点★★★★★★）。覆盖：
- 结构化分析SA：DFD/数据字典/E-R图
- 面向对象分析OOA
- UML 14种图（9种行为图+5种结构图）
- 需求管理：变更控制CCB、需求追踪矩阵

### Task B2: 系统设计

**Files:**
- Create: `01-综合知识/07-系统设计.md`

- [ ] **Step 1: 创建 07-系统设计.md**

对应红宝书ch3（超级重点★★★★★★）。覆盖：
- 面向对象设计：7大设计原则（SOLID+迪米特+合成复用）
- 结构化设计：模块独立性、内聚耦合7级
- 23种设计模式（创建型/结构型/行为型）

### Task B3: 系统质量属性与架构评估

**Files:**
- Create: `01-综合知识/09-系统质量属性与架构评估.md`

- [ ] **Step 1: 创建 09-系统质量属性与架构评估.md**

对应红宝书ch4.8（重点）。覆盖：
- 质量属性定义和分类（开发期 vs 运行期）
- 质量属性场景6要素
- SAAM/ATAM/CBAM 评估方法对比
- 效用树、敏感点、权衡点

---

## Phase C: P0-P1 内容（重要章节）

### Task C1: 数据库系统

**Files:**
- Create: `01-综合知识/04-数据库系统.md`

- [ ] **Step 1: 创建 04-数据库系统.md**

对应红宝书ch12（超级重点★★★★★★）。覆盖：
- 三级模式两级映射、关系运算
- 函数依赖、规范化1NF-BCNF
- 数据库设计6步骤、E-R方法
- 反规范化、NoSQL/CAP理论

### Task C2: 软件工程概述

**Files:**
- Create: `01-综合知识/05-软件工程概述.md`

- [ ] **Step 1: 创建 05-软件工程概述.md**

对应红宝书ch1（重点★★★★★）。覆盖：
- 过程模型对比（瀑布/原型/增量/螺旋/敏捷/RUP）
- 软件过程能力成熟度 CMMI
- 净室软件工程、CBSE

### Task C3: 系统可靠性

**Files:**
- Create: `01-综合知识/12-系统可靠性.md`

- [ ] **Step 1: 创建 12-系统可靠性.md**

对应红宝书ch7（次重点★★★☆）。覆盖：
- 可靠性度量（MTTF/MTTR/MTBF）
- 容错设计（NVP/RB）、双机热备/集群
- FTA/FMEA

### Task C4: 法律法规

**Files:**
- Create: `01-综合知识/15-法律法规.md`

- [ ] **Step 1: 创建 15-法律法规.md**

对应红宝书ch14（重点★★★★★）。覆盖：
- 著作权 vs 专利权对比
- 保护期限、侵权判定
- 标准分类与标准化机构

---

## Phase D: P1-P2 内容（次重点章节）

### Task D1: 计算机组成原理

**Files:** `01-综合知识/01-计算机组成原理.md`
- [ ] **Step 1: 创建** — 红宝书ch9 次重点★★★☆

### Task D2: 操作系统

**Files:** `01-综合知识/02-操作系统.md`
- [ ] **Step 1: 创建** — 红宝书ch11 次重点★★★☆

### Task D3: 计算机网络

**Files:** `01-综合知识/03-计算机网络.md`
- [ ] **Step 1: 创建** — 红宝书ch10 次重点★★★☆

### Task D4: 软件测试

**Files:** `01-综合知识/10-软件测试.md`
- [ ] **Step 1: 创建** — 红宝书ch5 次重点★★★☆

### Task D5: 系统运行与维护

**Files:** `01-综合知识/11-系统运行与维护.md`
- [ ] **Step 1: 创建** — 红宝书ch6 次重点★★★☆

### Task D6: 项目管理

**Files:** `01-综合知识/13-项目管理.md`
- [ ] **Step 1: 创建** — 红宝书ch8 次重点★★★☆

### Task D7: 信息安全

**Files:** `01-综合知识/14-信息安全.md`
- [ ] **Step 1: 创建** — 红宝书ch13 次重点★★★☆

---

## Phase E: P2-P3 + 收尾

### Task E1: 其他知识

**Files:** `01-综合知识/16-其他知识.md`
- [ ] **Step 1: 创建** — 合并信息系统/未来技术/数学/英语

### Task E2: 案例分析各专题

**Files:** `02-案例分析/` 下各文件
- [ ] **Step 1: 创建 00-案例分析解题框架.md**
- [ ] **Step 2: 创建 01~09 各专题文件**

### Task E3: 论文各方向+素材库

**Files:** `03-论文/` 下各文件
- [ ] **Step 1: 创建 00-论文写作框架.md**
- [ ] **Step 2: 创建 01~06 各方向+素材库文件**

### Task E4: 速查手册

**Files:** `04-速查手册.md`
- [ ] **Step 1: 创建考前速查手册** — 核心公式/口诀/对比表/易混概念汇总

### Task E5: 最终更新 MOC.md 全部链接

**Files:** `MOC.md`
- [ ] **Step 1: 确认所有文件已创建，更新全部双向链接确保可用**

---

## 执行说明

- 每个文件内部严格遵循设计文档中定义的"单文件内部结构规范"
- 内容产出后**必须对照红宝书审查校准**，再参考教材PDF补充细节
- 所有双向链接使用 Obsidian `[[]]` 语法
- 标签体系：`#高频` `#中频` `#低频` `#易错` `#必背` `#公式`
- mermaid 思维导图使用 `mindmap` 语法
