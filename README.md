# AI-For-Learning Skill

## 这个 skill 做什么

AI-For-Learning 是一套 AI 引导的学习方法：先了解你的目标与水平，再规划一条完整、清晰的学习路径；讲解时从背景讲起，逐步进入原理，最后通过提问、复述和动手实践确认你真的学会。

它不依赖一次性提示词的“运气”，而是用固定流程保证每一段学习都可检查、可复现、可沉淀。

## 学习如何学习

这个 skill 不是把知识直接灌给学习者，而是帮助学习者学习“如何学习”。

它通过苏格拉底式提问链，让费曼学习法自然发生：学习者必须用自己的话解释刚学到的内容，在解释中发现漏洞，再带着漏洞回到材料里重新理解。提问不是考核，而是让理解外显、让盲区现形的手段。

掌握了“如何学习”之后，换一个领域只是换了知识外壳，底层的学习方法依然可以迁移。

## 学习路径：从理解到实践

学习按三个阶段推进，层层递进：

1. 背景与目标：先理解这个领域为什么存在、解决什么问题、在整个知识版图中的位置，以及学完能做什么。
2. 原理与方法：再掌握核心概念和机制，理解不同方法之间的区别、适用边界，学会在什么场景选什么方法。
3. 实践与产出：最后跑通最小可行案例，完成一个完整项目或实验，把理解变成实际能力和可展示的成果。

先知道为什么，再理解怎么做，最后动手做出来。

---

## 先规划，后学习：全局观与固定契约

做事先有流程，是对学习者全局视野的构建，也是降低认知负荷的有效手段。不再依赖于提示词的“运气”，而是系统级别的固定契约。

学习者在开始前先看到完整路径，每一个知识点都有自己的位置和抵达方式，不会在细节里迷路。流程目录把“接下来学什么、为什么学、学到什么程度”变成可确认的契约，教学不再是即兴发挥，而是稳定可复现的系统行为。

## 教学主流程

1. 需求诊断（两种模式）：默认提问链模式从基本画像开始一次一问，持续追问到 95% 以上把握；文档导入模式下，用户发送简历或已有能力画像文档，模型先浏览提取，再只补问缺失且必要的信息。两种模式都必须先确认身份、专业或职位/职业、学生年级（大几/研几/博几），除非用户明确不想说
2. 生成流程目录：按 背景与目标 → 原理与方法 → 实践与产出 定制完整技术节点路径，包含中间动手实践和论文阅读，显式发给学习者确认
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

只要说“教我”、“我要学”、“想学”，或者要求解释代码、读论文、做作业，skill 会自动激活；也可以显式说“用 $ai-for-learning 教我”，直接进入完整流程。

学习过程中，选择对应内容并输入 `/mark`，可以把它标记为难点，后续会优先回顾。

## 交接机制：针对长程学习任务的优化机制

长期学习任务通过 `handoff.md` 跨对话接续：每完成流程目录中的一项任务，自动更新存档并明确告知用户；用户也可以随时输入 `/handoff` 手动交接。任务目录默认放在 `C:\Users\19935\Documents\Codex\learning-tasks\<任务名>\`，执行前会先确认该路径是否可用，不可用时与用户商讨位置；`handoff.md` 保存最新状态，并在文件开头的提示词中维护交接日期链、保留往期日期。文件开头包含接替提示词、任务目录/日期和交接日期链，下一段对话读取后直接从恢复点继续。

## 能力画像：一键生成简历式学习成果沉淀文档

能力画像与交接机制实时联动：每次更新 `handoff.md` 时同步刷新 `capability-summary.md`；用户也可以输入 `/summary` 手动生成。需求诊断时用户发送的简历或已有能力文档会被导入，模型只补问缺口并更新文档。文档与 `handoff.md` 放在同一任务目录，按简历式结构沉淀技术栈、知识范围和项目成果，其中项目描述会按完整简历叙事撰写，覆盖技术栈、实现细节、结果指标与口径，而不是简单一行；用户还可以随时补充内容。

## 论文拆解

发送论文链接或 PDF，或输入 `/paper <url|路径>` 开始拆解；输入 `/paper-search <关键词>` 可以检索相关论文。支持快速、完整、深挖三种阅读模式，拆解结果保存在任务目录的 `papers\` 下，并与 `handoff.md`、能力画像和 `/mark` 难点机制联动。

---

# AI-For-Learning Skill

## What This Skill Does

AI-For-Learning is an AI-guided learning method. It first identifies the learner's goals and current level, then plans a complete and clear learning path. Teaching starts with background, moves into principles, and ends with questions, self-explanation, and hands-on practice.

## Learning How to Learn

This skill does not simply feed knowledge to the learner. It helps the learner learn how to learn.

It uses a Socratic questioning chain to make the Feynman technique happen naturally: the learner explains newly learned content in their own words, discovers gaps during the explanation, and returns to the material with those gaps in mind. Questions are not exams; they make understanding visible and blind spots explicit.

Once the learner masters "how to learn," switching to a new field only changes the outer shell of knowledge, while the underlying learning method remains transferable.

## Learning Path: From Understanding to Practice

Learning follows three stages:

1. Background and goals: understand why a field exists, what problem it solves, where it fits, and what the learner will be able to do.
2. Principles and methods: learn the core concepts and mechanisms, compare methods and their trade-offs, and know how to choose.
3. Practice and outcomes: run a minimal working example and complete a project or experiment that turns understanding into usable skills.

Know why first, understand how next, then build it.

---

## Plan First, Then Learn: Global Perspective and a Fixed Contract

A workflow-first approach builds the learner's global perspective and reduces cognitive load. It no longer depends on the luck of a prompt; it is a fixed contract at the system level.

By seeing the full path before starting, the learner can place every knowledge point in context and never get lost in details. The flow catalog turns "what to learn next, why, and how far to go" into a confirmable contract. Teaching is no longer improvisation but stable, reproducible system behavior.

## Core Teaching Flow

1. Diagnosis (two modes): the default questioning-chain mode starts with the basic profile and asks one question at a time until 95%+ confidence; in document-import mode, the learner sends a resume or existing capability profile, the model reviews it first, then asks only for missing task-relevant information. Both modes must first confirm identity, major or job role, and student year (undergraduate year / master year / PhD year), unless the learner explicitly declines
2. Plan: build a path with complete technical nodes, mid-course practice, and paper reading, and explicitly ask the learner to confirm it
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

Say "教我", "我要学", "想学", or ask to explain code, read papers, or work on assignments, and the skill activates automatically. You can also explicitly invoke it with "Use $ai-for-learning to teach me" to enter the full flow directly.

During learning, select the relevant content and type `/mark` to mark it as a difficult point for later review.

## Handoff Mechanism: Optimization for Long-Range Learning Tasks

Long-term learning tasks continue across conversations through `handoff.md`: the checkpoint updates automatically after each completed task and notifies the user; the user can also type `/handoff` to trigger a manual handoff. The default task directory is `C:\Users\19935\Documents\Codex\learning-tasks\<task-name>\`; before creating it, confirm the path is usable and discuss the location with the user when it is not. `handoff.md` holds the latest state, and the takeover prompt keeps a date chain of past handoffs without overwriting earlier dates. The file starts with a takeover prompt including the task directory, date, and handoff date chain, so the next conversation can resume directly from the recovery point.

## Capability Profile: One-Click Resume-Style Learning Outcome Summary

The capability profile stays in sync with the handoff mechanism: it refreshes whenever `handoff.md` is updated, and the user can also generate it manually with `/summary`. A resume or existing capability document sent during diagnosis is imported first, and the model only asks for missing gaps before updating the document. It lives in the same task directory as `handoff.md` and accumulates tech stack, knowledge scope, and project outcomes in a resume-style structure, with project entries written as complete narratives covering tech stack, implementation details, results, and metrics caveats rather than one-liners; users can add their own notes at any time.

## Paper Deconstruction

Send a paper link or PDF, or type `/paper <url|path>` to start deconstruction; type `/paper-search <keywords>` to search for related papers. Three reading modes are available: quick, full, and deep. Results are saved under `papers\` in the task directory and stay linked with `handoff.md`, the capability profile, and the `/mark` difficulty mechanism.
