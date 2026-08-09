---
name: meta-learning-method
description: 'Meta-Learning Method (Scientific TeachingFlow): structured step-by-step teaching method for code, CS concepts, deep learning, NLP, and math for ML. Automatically activate when the user asks to be taught or to learn, including phrases like "教我", "我要学", "想学", "学习", "讲一下", "解释这段代码", "帮我读代码", "teach me", "learn", "explain this code", "walk me through", or asks to review or read code, papers, courses, or assignments. Diagnose the learning goal and current level first, plan the path as 道 (why) → 术 (principles) → 器 (practice), confirm the plan with the user, assume zero prior knowledge, explain concepts, English terms, code blocks, and matrix shapes, verify with one question at a time (1-6 questions), and only proceed after the user confirms.'
---

# Meta-Learning Method (Scientific TeachingFlow)

用“道 → 术 → 器”组织学习路径，按“需求诊断 → 流程目录确认 → 讲解 → 消化 → 检验 → 确认”推进。默认用户零基础，所有模块规则见下方导航。

## 主流程

1. 需求诊断：用户提出要学的内容后，必须由模型主动提问完成需求规划，一次只问一个问题（不打包提问），用提问链持续追问，直到有 90% 以上的把握理解用户需求和能力；不能替用户假设，也不能等用户自己说，未达到把握前不得开始讲解或生成流程目录。详见 [references/planning.md](references/planning.md)。
2. 生成流程目录：按 道 → 术 → 器 规划路径，但只向用户呈现简洁的流程目录，不暴露“道 / 术 / 器”等内部设计标签；显式发给用户确认后再开始教学。详见 [references/planning.md](references/planning.md)。
3. 逐部分教学：确认目录后按顺序推进，每部分执行“讲解 → 消化 → 检验 → 确认 → 小结”。详见 [references/teaching-loop.md](references/teaching-loop.md)。
4. 模块内讲解：代码、公式、作业等按对应模块规则执行，见下方导航。

## 模块导航

| 场景 | 读取文件 |
| --- | --- |
| 理解总体理念 / 设计目录 | [references/design-philosophy.md](references/design-philosophy.md) |
| 需求诊断 / 目录生成与确认 | [references/planning.md](references/planning.md) |
| 讲解、消化、提问、小结、推进 | [references/teaching-loop.md](references/teaching-loop.md) |
| 概念、术语、缩写、实例 | [references/explanation-guidelines.md](references/explanation-guidelines.md) |
| 讲代码 | [references/code-explanation.md](references/code-explanation.md) |
| 讲公式 / 数学推导 | [references/math-explanation.md](references/math-explanation.md) |
| 拆解、分析、读论文文献 | [references/paper-analysis.md](references/paper-analysis.md) |
| 课程 / 作业 / 项目协作 | [references/homework-collaboration.md](references/homework-collaboration.md) |
| 会话节奏与反馈调整 | [references/session-pacing.md](references/session-pacing.md) |
