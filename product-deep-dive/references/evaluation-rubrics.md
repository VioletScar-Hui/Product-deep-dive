# Evaluation Rubrics

Use this reference when writing section 2 `测试评估体系`. The purpose is to build a product-specific rubric, not a generic scoring table.

## Core Rule

The main dimensions are fixed:

| Main Dimension | Lens | Core Question |
|---|---|---|
| 端到端 | 黑盒评测 | Can the product complete the user's target scenario and produce a usable final result? |
| 过程能力 | 玻璃盒评测 | Is the intermediate process, decision path, state handling, and recovery reliable? |
| 综合评测 | 白盒评测 | Does the full system hold together across output, process, model/data, technical architecture, cost, safety, and business value? |

Do not replace these main dimensions. Generate second-level indicators under them according to product type and target scenario.

## Required Output Blocks

Section 2 should include:

1. Test scenario definition.
2. Evaluation dimension explanation table.
3. Scenario-specific scoring table.
4. Weight rationale.
5. Evidence and missing-test notes.

## Test Scenario Definition

Write a compact scenario block:

```markdown
### 本次测试场景
- 用户目标：
- 输入材料：
- 成功结果：
- 关键路径：
- 主要风险：
```

The scenario must be concrete enough that another evaluator can run it.

## Dimension Explanation Table

Every main dimension must answer `评什么`, `为什么重要`, and `怎么评`.

```markdown
| 主维度 | 评测视角 | 维度说明 |
|---|---|---|
| 端到端 | 黑盒评测 | 评什么：...；为什么重要：...；怎么评：... |
| 过程能力 | 玻璃盒评测 | 评什么：...；为什么重要：...；怎么评：... |
| 综合评测 | 白盒评测 | 评什么：...；为什么重要：...；怎么评：... |
```

## Second-Level Indicator Families

| Family | Covers | Common Placement |
|---|---|---|
| 端到端结果层 | Final output, scenario completion, delivery completeness, user-perceived usefulness. | 端到端 |
| 用户层 | Entry, user path, friction, controllability, trust, feedback, retention trigger, Aha Moment. | 过程能力 or 综合评测 |
| 模型数据层 | Model fit, routing, context, RAG/data grounding, memory, freshness, personalization, hallucination risk. | 过程能力 or 综合评测 |
| 技术层 | Workflow orchestration, agent/tool calls, state management, latency, stability, error recovery, permissions, integrations. | 过程能力 or 综合评测 |
| 安全合规层 | Content safety, privacy, moderation, copyright, enterprise risk. | 综合评测 |
| 商业价值层 | Willingness to pay, cost efficiency, retention, growth, monetization leverage. | 综合评测 |

## Scenario-Specific Rubric Templates

### AI 陪伴 / 角色互动

| 主维度 | 二级指标 | 评估重点 |
|---|---|---|
| 端到端 | 对话满足度 | 是否完成陪伴、倾诉、角色互动、剧情推进等目标。 |
| 过程能力 | 用户层 | 情绪承接、角色一致性、回复节奏、边界感、记忆唤起。 |
| 过程能力 | 模型数据层 | 人设保持、长期记忆、上下文连续性、幻觉和越界控制。 |
| 综合评测 | 留存/安全综合 | 是否兼顾沉浸、长期留存、内容安全和付费动机。 |

### AI Agent / Workflow

| 主维度 | 二级指标 | 评估重点 |
|---|---|---|
| 端到端 | 任务完成度 | 是否从用户目标到最终交付闭环。 |
| 过程能力 | 决策路径 | 任务分解、计划、工具选择、状态更新是否可理解。 |
| 过程能力 | 技术层 | Tool use、权限、异常恢复、重试、上下文管理是否可靠。 |
| 综合评测 | 生产可用性 | 是否达到可推荐、可复用、可进入生产工作流的水平。 |

### AI 视频 / 图片生成

| 主维度 | 二级指标 | 评估重点 |
|---|---|---|
| 端到端 | 生成结果质量 | 画面/视频质量、指令遵循、风格一致性、可交付性。 |
| 过程能力 | 用户层 | Prompt、参考图、编辑、重生成、资产管理是否顺畅。 |
| 过程能力 | 模型数据层 | 多模态理解、风格迁移、时序一致性、内容安全。 |
| 综合评测 | 成本/版权/效率 | 生成成本、版权风险、生产效率、商业可用性。 |

### AI 搜索 / 研究

| 主维度 | 二级指标 | 评估重点 |
|---|---|---|
| 端到端 | 答案可用性 | 是否给出完整、准确、可行动的答案。 |
| 过程能力 | 信息路径 | 检索、筛选、引用、综合过程是否透明。 |
| 过程能力 | 模型数据层 | 来源质量、时效性、事实 grounding、幻觉控制。 |
| 综合评测 | 可追溯性/可信度 | 是否能支持严肃研究、决策或团队复用。 |

### AI 编程 / DevTool

| 主维度 | 二级指标 | 评估重点 |
|---|---|---|
| 端到端 | 代码任务完成度 | 是否实现需求、修复问题、通过测试或给出可用代码。 |
| 过程能力 | 开发者工作流 | Repo 理解、编辑范围控制、测试、解释、回滚意识。 |
| 过程能力 | 技术层 | 上下文读取、工具调用、依赖处理、错误定位。 |
| 综合评测 | 工程可靠性 | 代码质量、安全、维护性、效率提升、团队协作价值。 |

## Scoring Table Template

```markdown
| 主维度 | 二级指标 | 维度说明 | 评估项 | 评分逻辑 | 权重/满分 | 当前得分 | 证据/待验证 |
|---|---|---|---|---|---|---|---|
| 端到端 | 端到端结果层 | ... | ... | ... | ... | 待实测 | ... |
| 过程能力 | 用户层 | ... | ... | ... | ... | 待实测 | ... |
| 过程能力 | 模型数据层 | ... | ... | ... | ... | 待实测 | ... |
| 过程能力 | 技术层 | ... | ... | ... | ... | 待实测 | ... |
| 综合评测 | 全流程综合 | ... | ... | ... | ... | 待实测 | ... |
```

## Weighting Rules

- Weight should reflect the product's value promise.
- Do not assign equal weights by default unless the product is genuinely balanced.
- For consumer entertainment products, user layer and retention may deserve higher weight.
- For professional productivity products, end-to-end task completion and technical reliability may deserve higher weight.
- For enterprise or research products, evidence, safety, traceability, and integration reliability may deserve higher weight.

## Common Failure Modes

- Only evaluating final output while ignoring process and system quality.
- Replacing `端到端`, `过程能力`, `综合评测` with product-specific labels.
- Using the same rubric for every AI product type.
- Giving a score without explaining `评什么`, `为什么重要`, and `怎么评`.
- Claiming a score from untested behavior instead of marking `待实测`.
