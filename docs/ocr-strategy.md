# 扫描版资料 OCR 策略

扫描版 PDF 本质是图片，Dify 文档提取器可能无法稳定识别。当前 MVP 建议用户先使用 OCR 工具将扫描资料转为可复制文本，再按章节上传或粘贴。

后续可接入：

- PaddleOCR
- Tesseract OCR
- 云厂商 OCR API
- 多模态模型识别

处理流程：

```text
扫描 PDF → OCR → 文本清洗 → 分章节输入 → StudyAgent 分析
```

