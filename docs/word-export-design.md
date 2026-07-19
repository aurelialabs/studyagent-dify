# Word 输出设计方案

## 1. 目标

将考途 StudyAgent 的最终学习报告从纯文本输出升级为可下载的 Word 文档，便于用户保存、打印、二次编辑和作为复习资料使用。

## 2. 推荐实现路径

### MVP 方案：Markdown 排版输出

先将最终结果统一整理为结构化 Markdown：

```text
# 考途 StudyAgent｜章节学习报告

## 一、章节结构

## 二、重点知识

## 三、背诵笔记

## 四、自测题

## 五、答案与解析

## 六、复习计划
```

用户可以复制到 Word、飞书文档或 Notion。

### 进阶方案：Word 导出工具

在 Dify Workflow 末尾增加一个 Word 导出工具节点：

```text
六个 LLM 节点
↓
模板转换节点：汇总 Markdown 报告
↓
Word 导出工具节点：Markdown → DOCX
↓
输出节点：返回 Word 文件
```

## 3. Dify 节点设计

### Template 节点

作用：把六个节点输出汇总成一份稳定的 Markdown 报告。

输入变量：

- 章节结构解析 / text
- 重难点提炼 / text
- 背诵笔记生成 / text
- 自测题生成 / text
- 答案与解析生成 / text
- 复习计划生成 / text

输出变量：

- report_markdown

### Word 导出节点

作用：将 `report_markdown` 转换为 `.docx` 文件。

输入：

- markdown_content：Template / output
- document_name：考途StudyAgent_学习报告

输出：

- Word 文件

## 4. 备选实现

如果 Dify Cloud 当前工作区没有可用的 Word 导出插件，可以先采用：

1. Dify 输出 Markdown 报告；
2. 本地脚本或在线文档工具将 Markdown 转为 Word；
3. 在作品集中说明“Word 导出”为后续迭代能力。

## 5. 产品价值

- 降低用户整理资料成本。
- 让 AI 输出结果更像正式学习资料。
- 支持下载、打印和二次编辑。
- 更符合教育产品的交付场景。

## 6. 当前项目建议

当前阶段建议先完成 Markdown 排版输出，并在作品集文档中展示 Word 导出方案。等 Dify 插件或外部导出服务可用后，再接入自动生成 DOCX。

