# Dify Workflow 导入与使用指南

## 导入方式

1. 登录 Dify Cloud。
2. 创建应用或选择导入 DSL。
3. 上传 `studyagent-workflow.yml`。
4. 检查模型供应商是否可用。
5. 检查文件上传、文档提取器和各节点变量引用。
6. 运行测试样例。

## 推荐模型

当前项目测试使用 `deepseek-v4-flash`。模型可根据 Dify 工作区实际配置替换，但需要重新测试输出稳定性。

## 输入字段

| 字段 | 说明 |
|---|---|
| study_file | 上传教材文件，支持 Word/PDF 等文档 |
| exam_type | 考试类型，如考研、考公、教资 |
| subject | 科目名称 |
| book_name | 教材或书名 |
| chapter_title | 章节标题 |
| chapter_text | 教材内容或章节正文，作为文件上传的补充 |
| current_level | 当前基础，如薄弱、一般、较好 |
| daily_time | 每日可用时间 |
| review_period | 复习周期 |
| study_scope | 学习范围，如整本书或指定章节 |
| target_part | 具体章节或页码范围 |

## 输出字段

- 章节结构
- 本书重难点
- 背诵版笔记
- 自测题
- 答案与解析
- 复习计划

## 注意事项

- 扫描版 PDF 建议先 OCR 成可复制文本。
- 上传整本书时建议先测试目录或单章内容，避免上下文过长。
- 导入 DSL 后，如果变量失效，需要在 Dify 中重新通过变量选择器插入。
- 不要将 API Key、Token、私人邮箱等敏感信息写入 Prompt 或 GitHub。

