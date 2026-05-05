# E2-01 系统计划 细化 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 将 `02-案例分析/01-系统计划.md` 从骨架（98 行）细化为完整版（280-350 行），覆盖可行性 4 维度、NPV/IRR、规划方法、新旧系统比较 + 2 道真题示例。

**Architecture:** 单文件重写。完成后用户验证 → 更新 tracker → 双提交。

**Tech Stack:** Markdown + Obsidian callout + Mermaid mindmap + Block ID 锚点。

**Spec:** [2026-05-05-e2-01-system-planning-design.md](../specs/2026-05-05-e2-01-system-planning-design.md)

---

## Task 1：重写文件（单次 Write 完成所有 4 节内容）

**Files:**
- Modify: `02-案例分析/01-系统计划.md`（重写为细化版）

> 内容详尽参照 spec 三、各节内容设计。

- [ ] **Step 1: 写入 frontmatter**

更新 date 为 2026-05-05，tags / aliases 保留并补充 BSP/CSF/SST/VCA/TCO 等。

- [ ] **Step 2: 写入标题与 warning callout**

```markdown
# 系统计划

> [!warning] 中频考点（约 1-2 年考一次）
> 核心考点：==可行性研究 4 维度==（经济/技术/操作/法律）、==成本效益分析==（NPV / IRR / 投资回收期）、==系统规划方法==（BSP / CSF / SST / VCA）、==新旧系统比较==。
>
> **状态**：✅ 已细化
>
> **速查跳转**：[[#1.1.3 可行性研究 4 大维度（必背）|可行性4维]] · [[#1.2.1 成本效益分析（经济可行性核心）|NPV/IRR]] · [[#1.4 真题与练习|真题]]
```

- [ ] **Step 3: 写入知识全景 mindmap**

含 5 大分支：可行性 4 维度 / 成本效益 NPV-IRR / 规划方法 4 种 / 新旧系统比较 / 立项流程

- [ ] **Step 4: 写入 1.1 核心概念**

3 个子节：
- 1.1.1 系统规划生命周期（6 阶段表）
- 1.1.2 立项与可行性流程（4 步）
- 1.1.3 可行性研究 4 大维度（block ID `^feasibility-4dim`）

callout：`> [!important]` 可行性 4 维度、`> [!tip]` 立项 4 步

- [ ] **Step 5: 写入 1.2 关键技术与架构**

4 个子节：
- 1.2.1 成本效益分析公式（NPV / IRR / 投资回收期，block ID `^npv-irr-formula`）+ NPV 计算示例（block ID `^npv-example`）
- 1.2.2 4 种规划方法 BSP/CSF/SST/VCA（block ID `^planning-methods`）
- 1.2.3 新旧系统比较与替代方案权衡矩阵
- 1.2.4 投资估算与 TCO

callout：`> [!important]` NPV/IRR 公式 + 4 种规划方法、`> [!tip]` BSP 最常考

- [ ] **Step 6: 写入 1.3 典型考点与解题套路**

3 个子节：
- 1.3.1 可行性分析三段论模板
- 1.3.2 关键字判定速查（7 行表，block ID `^feasibility-keywords`）
- 1.3.3 NPV/IRR 计算 4 步套路 + 判断准则

callout：`> [!tip]` 答题模板、关键字判定

- [ ] **Step 7: 写入 1.4 真题与练习**

2 道真题：
- 1.4.1 真题示例 1：连锁餐饮会员系统可行性 4 维分析（block ID `^realexam-feasibility-4dim`）
- 1.4.2 真题示例 2：1000 万投资 + 3 年现金流 NPV 计算（block ID `^realexam-npv`）

每道真题答题按"理论 + 分点 + 结论"三段论。

- [ ] **Step 8: 保留关联链接**

```markdown
## 关联链接

- 返回案例分析索引：[[00-案例分析解题框架]]
- 返回主索引：[[../MOC]]
- 关联综合知识章节：
    - [[../01-综合知识/06-需求工程]]：需求获取与分析
    - [[../01-综合知识/13-项目管理]]：EMV 决策、风险管理
    - [[../01-综合知识/11-系统运行与维护]]：系统转换与切换
- 关联案例分析：[[02-信息系统架构设计]]（信息化战略对齐）
```

- [ ] **Step 9: 校对**

- 文件行数 280-350
- block ID 锚点 ≥7 个：`^feasibility-4dim`、`^npv-irr-formula`、`^planning-methods`、`^npv-example`、`^feasibility-keywords`、`^realexam-feasibility-4dim`、`^realexam-npv`
- 对比表 ≥4 个
- 真题示例 2 道
- 与 spec 三、各节内容设计 一致

---

## Task 2：用户验证暂停

- [ ] **Step 1: 报告完成，请用户在 Obsidian 中检查**

校对项：
- mindmap 渲染（5 大分支）
- 所有 callout 颜色正确
- NPV 计算示例数据正确（363.6 + 413.2 + 450.8 - 1000 ≈ 227.6）
- 跨文件链接可点击
- 真题 2 道完整呈现

- [ ] **Step 2: 等用户确认无异常后再进入 Task 3**

---

## Task 3：用户验证后更新 tracker 并提交

**Files:**
- Modify: `docs/audit/revision-task-tracker.md`

- [ ] **Step 1: 提交 docs commit**

```bash
cd "/Users/wanlinruo/Library/Mobile Documents/iCloud~md~obsidian/Documents/project-003"
git add "02-案例分析/01-系统计划.md"
git commit -m "docs(E2-01): 细化系统计划专题，骨架→完整版

Co-Authored-By: Claude Opus 4.7 (1M context) <noreply@anthropic.com>"
```

- [ ] **Step 2: 追加 tracker 日志条目**

```markdown
| 2026-05-05 | E2-01 | 细化系统计划专题骨架→完整版300+行：1.1核心概念(系统规划6阶段战略/可行性/立项/需求/设计/运维+立项4步项目建议书/可行性研究/项目论证/任务下达+可行性4维度经济/技术/操作/法律必背)/1.2关键技术(NPV=Σ现金流/(1+r)^t-C₀+NPV>0可行+IRR>基准收益率+投资回收期≤5年+计算示例1000万投资3年400/500/600现金流10%折现NPV=227.6万+4种规划方法BSP自上而下U/C矩阵/CSF关键成功因素/SST战略集合转化/VCA价值链分析+新旧系统替代方案权衡矩阵+TCO总拥有成本)/1.3解题套路(可行性4维三段论模板+7行关键字判定+NPV计算4步套路)/1.4真题2道(题1:连锁餐饮500门店会员系统可行性4维分析+题2:1000万投资NPV计算)；7个block ID锚点 | `<commit-hash>` | 通过 |
```

- [ ] **Step 3: 提交 chore commit**

```bash
git add docs/audit/revision-task-tracker.md
git commit -m "chore(E2-01): 更新任务日志，系统计划细化完成

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
- ✅ 风格统一：与 E2-02 至 E2-09 完全对齐
