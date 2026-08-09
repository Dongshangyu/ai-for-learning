# Meta-Learning Method (Scientific TeachingFlow)

## 元学习：学习如何学习

这个 skill 不是把知识直接灌给学习者，而是帮助学习者学习“如何学习”，也就是元学习。

它通过苏格拉底式提问链，把费曼学习法变成一套被动发生的流程：学习者必须用自己的话解释刚学到的内容，在解释中发现漏洞，再带着漏洞回到材料里重新理解。提问不是考核，而是让理解外显、让盲区现形的手段。

当学习者掌握了“如何学习”之后，换一个领域只是换了知识外壳，底层的学习方法依然可以迁移。

## 设计理念：道 → 术 → 器

一个完整的学习系统，需要同时回答三个层面的问题：为什么、怎么做、用什么落地。

道，回答的是动机与位置。 学习者需要先理解一个领域为什么存在、它解决了什么根本问题、在整个知识版图中处于什么位置。没有这个层面的认知，后续的所有细节都是悬浮的，学到的只是孤立的技术片段，而非一套可迁移的思维框架。

术，回答的是原理与选择。 在理解了“为什么”之后，学习者需要进入核心机制的博弈层——理解不同方法之间的本质差异、各自的适用边界、以及它们之间的演化逻辑。这个阶段的目标不是记住所有细节，而是建立判断力：在什么场景下选择什么路径。

器，回答的是落地与实践。 一切认知最终需要被压缩进可执行的行动中。这个层面不追求宏大，追求具体：跑通一个最小可行案例，亲手触碰一次完整流程，把前两个层面的理解转化为身体记忆。只有到了这一步，才算真正完成了一个领域的认知闭环。

道让你不迷路，术让你不肤浅，器让你不悬浮。三者层层递进，缺一不可。一个好的学习系统，应当引导学习者自然地沿着这条路径前进，而不是只停留在某一个层面。

---

## 先规划，后学习：全局观与固定契约

做事先有流程，是对学习者全局视野的构建，也是降低认知负荷的有效手段。不再依赖于提示词的“运气”，而是系统级别的固定契约。

学习者在开始前先看到完整路径，每一个知识点都有自己的位置和抵达方式，不会在细节里迷路。流程目录把“接下来学什么、为什么学、学到什么程度”变成可确认的契约，教学不再是即兴发挥，而是稳定可复现的系统行为。

## 教学主流程

1. 需求诊断：先从用户基本画像问起，再用提问链一次一个问题地问清目的、水平等关键信息，不打包提问，直到有 95% 以上把握确定终点和起点
2. 生成流程目录：按 道 → 术 → 器 定制完整技术节点路径，包含中间动手实践和论文阅读，显式发给学习者确认
3. 逐层推进：每部分都遵循 讲解 → 消化 → 检验 → 确认 → 小结
4. 提问检验：一次一问，1-6 个问题，直到有 95% 以上把握确认彻底理解
5. 收尾确认：反问是否还有疑问，并提供 3 个左右的延伸例子/问题供选择
6. 阶段性小结：全部疑问确认解决后，让用户用自己的话复述核心逻辑，模型再做补充总结
7. 确认后继续下一部分

## 模块结构

| 模块 | 作用 |
| --- | --- |
| planning.md | 需求诊断、流程目录生成与确认 |
| teaching-loop.md | 讲解、消化、提问、小结、推进 |
| explanation-guidelines.md | 概念、术语、缩写、实例规范 |
| code-explanation.md | 代码块拆分与逐句讲解 |
| math-explanation.md | 公式与数学推导讲解 |
| paper-analysis.md | 论文检索、拆解与分析 |
| homework-collaboration.md | 课程与作业协作 |
| session-pacing.md | 会话节奏与反馈调整 |
| handoff-mechanism.md | 长期任务交接与学习存档 |
| capability-summary.md | 能力画像：简历式学习成果沉淀 |

## 使用方式

只要说“教我”、“我要学”、“想学”，或者要求解释代码、读论文、做作业，skill 会自动激活；也可以显式说“用 $meta-learning-method 教我”，直接进入完整流程。

学习过程中，选择对应内容并输入 `/mark`，可以把它标记为难点，后续会优先回顾。

## 交接机制：针对长程学习任务的优化机制

长期学习任务通过 `handoff.md` 跨对话接续：每完成流程目录中的一项任务，自动更新存档并明确告知用户；用户也可以随时输入 `/handoff` 手动交接。任务目录默认放在 `C:\Users\19935\Documents\Codex\learning-tasks\<任务名>\`，执行前会先确认该路径是否可用，不可用时与用户商讨位置；`handoff.md` 保存最新状态，并在文件开头的提示词中维护交接日期链、保留往期日期。文件开头包含接替提示词、任务目录/日期和交接日期链，下一段对话读取后直接从恢复点继续。

## 能力画像：一键生成简历式学习成果沉淀文档

能力画像与交接机制实时联动：每次更新 `handoff.md` 时同步刷新 `capability-summary.md`；用户也可以输入 `/summary` 手动生成。文档与 `handoff.md` 放在同一任务目录，按简历式结构沉淀技术栈、知识范围和项目成果，用户还可以随时补充内容。

## 论文拆解

发送论文链接或 PDF，或输入 `/paper <url|路径>` 开始拆解；输入 `/paper-search <关键词>` 可以检索相关论文。支持快速、完整、深挖三种阅读模式，拆解结果保存在任务目录的 `papers\` 下，并与 `handoff.md`、能力画像和 `/mark` 难点机制联动。

---

# Meta-Learning Method (Scientific TeachingFlow)

## Meta-Learning: Learning How to Learn

This skill does not simply feed knowledge to the learner. It helps the learner learn how to learn, which is meta-learning.

It uses a Socratic questioning chain to turn the Feynman technique into a naturally occurring process: the learner must explain newly learned content in their own words, discover gaps during the explanation, and return to the material with those gaps in mind. Questions are not exams; they make understanding visible and blind spots explicit.

Once the learner masters "how to learn," switching to a new field only changes the outer shell of knowledge, while the underlying learning method remains transferable.

## Design Philosophy: 道 (Way) → 术 (Method) → 器 (Tool)

A complete learning system must answer three questions: why, how, and with what.

道 (Way) addresses motivation and position. The learner first needs to understand why a field exists, what fundamental problem it solves, and where it sits in the broader knowledge map. Without this layer, every detail floats; the learner picks up isolated technical fragments instead of a transferable mental framework.

术 (Method) addresses principles and choices. After understanding the "why," the learner enters the core mechanism layer, comparing essential differences among methods, their applicability boundaries, and their evolutionary logic. The goal is not memorizing details but building judgment: which path to choose in which scenario.

器 (Tool) addresses implementation and practice. Knowledge must ultimately be compressed into executable action. This layer is not about grandeur but about concreteness: run a minimal viable case, touch a complete workflow with your own hands, and turn the first two layers of understanding into embodied memory. Only then is the cognitive loop of a field truly closed.

道 keeps you oriented, 术 keeps you deep, 器 keeps you grounded. The three layers progress in sequence and none can be skipped. A good learning system guides the learner naturally along this path instead of stopping at a single layer.

## Plan First, Then Learn: Global Perspective and a Fixed Contract

A workflow-first approach builds the learner's global perspective and reduces cognitive load. It no longer depends on the luck of a prompt; it is a fixed contract at the system level.

By seeing the full path before starting, the learner can place every knowledge point in context and never get lost in details. The flow catalog turns "what to learn next, why, and how far to go" into a confirmable contract. Teaching is no longer improvisation but stable, reproducible system behavior.

## Core Teaching Flow

1. Diagnosis: start with the learner's basic profile, then use a questioning chain to ask about the goal, level, and other key factors one question at a time without bundling, until there is 95%+ confidence in the destination and the starting point
2. Plan: build a 道 → 术 → 器 path with complete technical nodes, mid-course practice, and paper reading, and explicitly ask the learner to confirm it
3. Progress: each part follows explain → digest → check → confirm → summarize
4. Questioning: one question at a time, 1-6 questions total, until confidence is above 95%
5. Close-out: ask whether the learner has other questions and offer about 3 follow-up examples or questions
6. Staged summary: after all questions are resolved, ask the learner to restate the core logic, then the model adds a structured summary
7. Continue only after the learner confirms

## Module Structure

| Module | Purpose |
| --- | --- |
| planning.md | Diagnosis, flow catalog generation, and confirmation |
| teaching-loop.md | Explain, digest, question, summarize, and progression rules |
| explanation-guidelines.md | Concepts, terms, abbreviations, and examples |
| code-explanation.md | Code block splitting and line-by-line explanation |
| math-explanation.md | Formula and mathematical derivation guidance |
| paper-analysis.md | Paper search, deconstruction, and analysis |
| homework-collaboration.md | Course, assignment, and project collaboration |
| session-pacing.md | Pacing and feedback adjustment |
| handoff-mechanism.md | Long-term task handoff and learning checkpoint |
| capability-summary.md | Capability profile: resume-style learning outcome summary |

## Usage

Say "教我", "我要学", "想学", or ask to explain code, read papers, or work on assignments, and the skill activates automatically. You can also explicitly invoke it with "Use $meta-learning-method to teach me" to enter the full flow directly.

During learning, select the relevant content and type `/mark` to mark it as a difficult point for later review.

## Handoff Mechanism: Optimization for Long-Range Learning Tasks

Long-term learning tasks continue across conversations through `handoff.md`: the checkpoint updates automatically after each completed task and notifies the user; the user can also type `/handoff` to trigger a manual handoff. The default task directory is `C:\Users\19935\Documents\Codex\learning-tasks\<task-name>\`; before creating it, confirm the path is usable and discuss the location with the user when it is not. `handoff.md` holds the latest state, and the takeover prompt keeps a date chain of past handoffs without overwriting earlier dates. The file starts with a takeover prompt including the task directory, date, and handoff date chain, so the next conversation can resume directly from the recovery point.

## Capability Profile: One-Click Resume-Style Learning Outcome Summary

The capability profile stays in sync with the handoff mechanism: it refreshes whenever `handoff.md` is updated, and the user can also generate it manually with `/summary`. It lives in the same task directory as `handoff.md` and accumulates tech stack, knowledge scope, and project outcomes in a resume-style structure; users can add their own notes at any time.

## Paper Deconstruction

Send a paper link or PDF, or type `/paper <url|path>` to start deconstruction; type `/paper-search <keywords>` to search for related papers. Three reading modes are available: quick, full, and deep. Results are saved under `papers\` in the task directory and stay linked with `handoff.md`, the capability profile, and the `/mark` difficulty mechanism.
