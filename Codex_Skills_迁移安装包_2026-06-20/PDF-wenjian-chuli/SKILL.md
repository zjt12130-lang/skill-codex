---
name: PDF-wenjian-chuli
description: PDF 文件的读取、创建和视觉验证
---

---
name: PDF-wenjian-chuli
description: 读取、创建和验证 PDF 文件，注重视觉布局
---

# PDF 文件处理（插件版）

读取、创建、检查和验证 PDF 文件，注重视觉布局。使用 Poppler 渲染和 Python 工具（reportlab、pdfplumber、pypdf）。

## 工作流
1. 使用 pdftoppm 渲染页面为 PNG
2. 使用 reportlab 生成 PDF
3. 使用 pdfplumber/pypdf 提取文本
4. 每次更新后重新渲染验证
