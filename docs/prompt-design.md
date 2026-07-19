# Prompt 设计说明

## 设计原则

1. 每个节点只完成一个明确任务。
2. 输出格式固定，便于下游节点读取。
3. 强制要求基于用户输入，减少幻觉。
4. 在题目和答案节点之间建立严格对应关系。
5. 复习计划必须结合用户基础、每日时间和复习周期。

## 变量说明

| 变量 | 含义 |
|---|---|
| exam_type | 考试类型 |
| subject | 科目名称 |
| book_name | 教材或书名 |
| chapter_title | 章节标题 |
| chapter_text | 教材内容/章节正文 |
| current_level | 当前基础 |
| daily_time | 每日可用时间 |
| review_period | 复习周期 |

## 六个节点

具体 Prompt 见 `prompts/` 文件夹。

