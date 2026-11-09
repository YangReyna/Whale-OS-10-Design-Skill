---
layout: default
title: Skill 编写与维护约定
permalink: /skills/
---

# Skill 编写与维护约定

本目录存放 Whale OS 相关设计 Skills，已收录 [whale-os10-design](https://github.com/YangReyna/Whale-OS-10-Design-Skill/tree/main/skills/whale-os10-design)。本页用于约定后续的组织方式与编写要求。

## 组织方式

每个 Skill 使用独立目录，目录名采用小写英文和连字符。示例：

```text
skills/
└── whale-tv-focus-review/
    ├── SKILL.md
    ├── references/   # 按需添加：规范、规则和完整示例
    ├── assets/       # 按需添加：输出模板与素材
    └── scripts/      # 按需添加：重复性操作脚本
```

只有 `SKILL.md` 是必需入口，其余目录按实际需要创建。上面的目录仅用于说明结构，不代表已收录的能力。

## SKILL.md 内容

在文件开头使用 YAML front matter，至少声明 `name` 和 `description`。下面是结构示例，正式使用前需要补齐实际流程：

```yaml
---
name: whale-tv-focus-review
description: 检查 Whale OS 电视端页面的遥控器焦点与按键导航，适用于已有页面状态稿或交互流程的设计审查。
---
```

正文应包含：

| 内容 | 需要说明的问题 |
| --- | --- |
| 使用范围 | 何时触发，适用的 Whale OS 版本与页面范围，哪些任务不适用 |
| 输入要求 | 需要哪些需求、设计稿、状态画面或参考文档 |
| 执行流程 | 先检查什么，再处理什么，资料缺失时如何推进 |
| 输出要求 | 交付物的结构、字段、格式和必要示例 |
| 检查标准 | 如何判断任务完成，如何复核关键状态与边界情况 |
| 参考资料 | 使用哪些规范、资源，以及何时需要读取它们 |

## 写作要求

- `description` 应同时说明能力和使用时机，便于 AI 助手判断何时加载。
- 使用明确、可执行的指令，避免只有目标、没有操作步骤。
- 主文件保留核心规则，长篇资料放入 `references/`，并在主文件中写明读取条件。
- 引用支持文件时使用相对于当前 Skill 目录的路径，保持整个目录可以独立迁移。
- 对未提供的信息和未确认的规则说明处理方法，避免将假设写成既定规范。
- 包含脚本时说明依赖、输入与输出，并用实际示例验证。

## 提交前检查

1. 目录名、`name` 和 `description` 是否清晰且一致。
2. 所有引用文件是否存在，适用版本和规范来源是否明确。
3. 输入、执行步骤、输出格式与完成标准是否齐全。
4. 是否用真实任务检查过流程，并覆盖资料缺失或边界情况。
5. 是否同步更新仓库首页的 Skills 目录。

[返回仓库](https://github.com/YangReyna/Whale-OS-10-Design-Skill)
