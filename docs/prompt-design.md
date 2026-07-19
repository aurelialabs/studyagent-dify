# Prompt 设计文档

## 设计目标

通过多节点 Prompt 设计，让模型输出更稳定、可解释、可复用，并降低一次性生成长报告造成的结构混乱。

## 设计原则

1. 明确角色：每个节点设定具体专家角色。
2. 明确任务：每个 Prompt 只负责一个核心任务。
3. 明确输入：列出上游变量和用户变量。
4. 明确输出：固定 Markdown 输出结构。
5. 限制编造：要求基于输入，推断内容需标注。
6. 稳定字段：保证下游节点能引用上游结构。

## 节点 Prompt

- [章节结构解析](../prompts/chapter-analysis.md)
- [重点知识提炼](../prompts/key-points.md)
- [背诵笔记生成](../prompts/memorization-notes.md)
- [自测题生成](../prompts/quiz-generation.md)
- [答案与解析生成](../prompts/answer-analysis.md)
- [复习计划生成](../prompts/review-plan.md)

## 特别约束

答案与解析生成节点必须根据自测题生成节点输出逐题回答，不能重新生成题目。复习计划生成节点需要综合章节结构、核心重点、知识难度、用户可用时间和复习周期。

