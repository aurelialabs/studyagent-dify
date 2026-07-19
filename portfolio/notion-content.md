# 考途 StudyAgent｜备考教材重难点梳理智能体

## 1. 项目封面

使用 `assets/product-cover.png` 作为项目封面。

## 2. 一句话介绍

基于 Dify Workflow 的备考教材重点梳理与个性化复习智能体，帮助用户将教材章节转化为知识框架、重点笔记、自测题、答案解析和复习计划。

## 3. 我的角色

独立完成产品定位、用户问题拆解、Workflow 搭建、Prompt 设计、测试记录、GitHub 项目整理和作品集文档输出。

## 4. 项目周期

项目原型阶段：2026 年 7 月。具体持续迭代时间以 GitHub 提交记录为准。

## 5. 项目背景

备考用户需要处理大量教材内容，但人工整理重点、笔记、题目和计划的成本较高。通用大模型虽然能总结文本，但缺少固定流程和稳定输出结构。

## 6. 用户问题

- 教材内容长，人工整理效率低。
- 章节结构和考试重点难以快速识别。
- 背诵、做题和计划相互割裂。
- 通用 AI 输出结构不稳定。

## 7. 解决方案

通过 Dify Workflow 将学习材料处理拆分为多个节点，让每个节点完成一个明确任务，并最终汇总为结构化复习报告。

## 8. 产品流程

```text
用户输入 → 章节结构解析 → 重点知识提炼 → 背诵笔记生成 → 自测题生成 → 答案与解析生成 → 复习计划生成 → 输出
```

## 9. Workflow 设计

可插入 `assets/workflow.png`。

## 10. Prompt 设计

Prompt 采用多节点拆分，每个节点明确角色、任务、输入、输出格式和质量标准。答案解析节点特别限制不得重新生成题目，必须对应自测题。

## 11. 产品截图

建议插入：

- `assets/screenshots/input-example.png`
- `assets/screenshots/output-example.png`
- `assets/screenshots/publish-page.png`

## 12. 用户测试

当前完成了一次 PDF 教材上传测试。测试结果显示系统能够生成与教材相关的知识框架和复习内容。更多用户测试仍待开展，不虚构真实用户数量和满意度数据。

## 13. 产品迭代

- V0.1：完成基础 Workflow 和 Demo 发布。
- V0.2：计划优化异常输入、长文本、扫描 PDF 和输出一致性。
- V2.0：计划增加 OCR、知识库和 Word 导出。

## 14. 项目成果

- 可运行 Dify Web App Demo
- 可导入 Dify DSL
- GitHub 项目文档
- PRD、Prompt、测试报告、迭代记录
- 简历和面试材料

## 15. 反思与后续规划

当前项目证明了 Workflow 化的教育 Agent 原型可行，但仍需要更多真实教材、用户反馈和边界场景测试。后续会重点增强长文本处理、扫描版资料 OCR 和学习报告导出。

## 16. GitHub 链接

<https://github.com/aurelialabs/studyagent-dify>

## 17. Demo 链接

<https://udify.app/workflow/Ml6LKD4l0pltIw54q>

