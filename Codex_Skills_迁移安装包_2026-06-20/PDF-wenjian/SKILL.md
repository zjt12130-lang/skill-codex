---
name: PDF-wenjian
description: PDF 文件的读取、创建和审查，注重渲染和排版质量
---

---
name: PDF-wenjian
description: 读取、创建、审查 PDF 文件，注重渲染效果和排版
---

# PDF 文件处理

## 何时使用
- 读取或审查 PDF 内容，关注布局和视觉效果
- 程序化创建格式化 PDF 文件
- 交付前验证最终渲染效果

## 工作流程
1. 优先视觉审查：用 Poppler 渲染 PDF 页面为 PNG
2. 用 reportlab 创建新 PDF 文档
3. 用 pdfplumber 或 pypdf 进行文本提取
4. 每次有意义更新后重新渲染验证

## 依赖
```
uv pip install reportlab pdfplumber pypdf
```
系统工具：`brew install poppler`

## 渲染命令
```
pdftoppm -png $INPUT_PDF $OUTPUT_PREFIX
```

## 质量要求
- 一致的排版、间距、边距和章节层级
- 无渲染问题：裁剪文本、重叠元素、不可读字符
- 图表清晰、对齐、标注明确

## 最终检查
- 最新 PNG 检查无视觉或格式缺陷才可交付
- 确认页眉/页脚、页码、章节过渡流畅
