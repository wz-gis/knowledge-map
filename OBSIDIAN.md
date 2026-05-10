# Obsidian Setup

本 Vault 使用 Obsidian，但不依赖复杂插件。目标是 Markdown 原生、Git 可管理、长期稳定。

## Recommended Core Settings

| Setting | Recommended Value |
| --- | --- |
| Files and links > New link format | Relative path to file |
| Files and links > Use Markdown links | Enabled |
| Files and links > Default location for new attachments | In the folder specified below |
| Files and links > Attachment folder path | `assets` |
| Files and links > Automatically update internal links | Enabled |
| Editor > Default editing mode | Live Preview or Source Mode |
| Editor > Strict line breaks | Disabled |

## Recommended Core Plugins

启用：

- File explorer
- Search
- Backlinks
- Outgoing links
- Templates
- Graph view
- Command palette
- Daily notes

可选：

- Canvas
- Outline

## Community Plugins

推荐插件不超过 10 个：

1. Obsidian Git
2. Dataview
3. Templater
4. Calendar
5. Tasks
6. Advanced Tables
7. Linter
8. Omnisearch

使用原则：

- 默认只安装 Obsidian Git。
- Dataview、Templater、Calendar 按需安装。
- Tasks 只用于轻量 check list，不要把 Vault 变成复杂 GTD。
- 不安装会改变 Markdown 存储形态的插件。

## Template Settings

Templates 插件目录设置为：

```text
templates
```

推荐快捷入口：

- 新项目：`templates/project-template.md`
- 日志：`templates/daily-log-template.md`
- Bug 复盘：`templates/bug-template.md`
- 架构记录：`templates/architecture-template.md`
- Prompt：`templates/prompt-template.md`
- 学习笔记：`templates/learning-template.md`

## Daily Notes Settings

| Setting | Value |
| --- | --- |
| Date format | `YYYY-MM-DD` |
| New file location | `daily` |
| Template file location | `templates/daily-log-template.md` |

## Attachments

- 所有图片和附件统一放到 `assets/YYYY/`。
- 不在项目目录内创建独立 assets。
- Markdown 中使用相对路径。
- 图片命名遵循 [NAMING.md](./NAMING.md)。

## Recommended Sync Plan

主方案：

```text
Local Obsidian Vault + GitHub Private Repo + Obsidian Git
```

备选方案：

```text
Local Obsidian Vault + Git CLI + GitHub Private Repo
```

不推荐：

- 同时使用多个自动同步工具写同一个 Vault。
- 用网盘和 Git 同时同步 `.git/`。
- 依赖专有云笔记平台作为主数据源。
