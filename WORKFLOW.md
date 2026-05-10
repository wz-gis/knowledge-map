# Operating Workflow

这份文档是日常使用建议。它保持轻量，不把知识库变成复杂任务系统。

## Recommended Plugins

不超过 10 个，按优先级排序：

1. Obsidian Git
2. Dataview
3. Templater
4. Calendar
5. Tasks
6. Advanced Tables
7. Linter
8. Omnisearch

建议：

- 初始只安装 Obsidian Git。
- 需要模板增强时再安装 Templater。
- 需要查询索引时再安装 Dataview。
- Tasks 只做轻量 check list，不做完整 GTD。

## Recommended Sync Plan

主方案：

```text
Obsidian local Vault
        ↓
Git local repo
        ↓
GitHub Private Repo
        ↓
Other devices pull
```

原则：

- GitHub Private Repo 是同步和备份中心。
- 本地 Markdown 文件是主数据。
- 不要用多个同步系统同时写同一个 Vault。
- 不要把 `.git/` 放进网盘同步目录。

## Recommended Git Workflow

每天开始：

```bash
git pull --rebase
```

写作或整理后：

```bash
git status
git add .
git commit -m "docs: update knowledge base"
git push
```

更具体的 commit message：

```text
docs: add java thread pool notes
docs: update codex prompts
docs: add nginx snippets
docs: archive old project notes
```

## Daily Habits

- 临时内容先放 `00_inbox/`。
- 每天只写一个 daily log，不追求完整。
- 重要问题用 `bug-template.md` 复盘。
- 架构和设计选择用 `architecture-template.md` 固化。
- 可复用命令放进 `snippets/`。
- Prompt 迭代放进 `prompts/`。
- 图片只放 `assets/YYYY/`。

## Weekly Maintenance

每周 30 分钟即可：

- 清理 `00_inbox/`。
- 把可复用内容迁移到 `02_areas/`、`03_resources/` 或 `snippets/`。
- 把完成项目移动到 `04_archive/`。
- 检查是否有未提交 Git 变更。
- 删除没有引用价值的临时内容。

## Knowledge Distillation Rhythm

推荐节奏：

| Frequency | Action |
| --- | --- |
| Daily | 记录 Today、Problems、Fixes、Learnings、Next Actions |
| Weekly | 从 daily log 提炼 1 到 3 篇长期笔记 |
| Per bug | 使用 bug 模板记录原因、修复、预防 |
| Per project | 维护 README、architecture、decisions |
| Per learning topic | 写入 `02_areas/<area>/` |
| Per reusable command | 写入 `snippets/<topic>/` |

## Lightweight Rule

当你不知道内容该放哪里：

1. 临时内容放 `00_inbox/`。
2. 有明确结束条件放 `01_projects/`。
3. 长期能力放 `02_areas/`。
4. 外部资料索引放 `03_resources/`。
5. 过期内容放 `04_archive/`。

不要为了一个笔记创建一个新分类。
