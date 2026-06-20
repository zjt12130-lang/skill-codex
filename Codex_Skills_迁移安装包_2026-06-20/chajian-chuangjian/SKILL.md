---
name: chajian-chuangjian
description: 创建和搭建 Codex 插件目录和市场条目
---

---
name: chajian-chuangjian
description: 创建和搭建 Codex 插件目录，包含 .codex-plugin/plugin.json 和市场条目
---

# 插件创建器

## 快速开始
1. 运行脚手架脚本：
```bash
python3 scripts/create_basic_plugin.py <plugin-name>
```
2. 编辑 plugin.json 添加元数据
3. 生成市场条目：
```bash
python3 scripts/create_basic_plugin.py my-plugin --with-marketplace
```

## 结构
- .codex-plugin/plugin.json - 必需清单文件
- skills/ - 插件提供的技能目录
- assets/ - 资源文件
- scripts/ - 辅助脚本

## 命名规则
- 插件名使用小写连字符格式
- 不超过 64 字符
- 生成目录名与 plugin.json 中的 name 一致
