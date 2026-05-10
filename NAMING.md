# Naming Rules

命名目标：长期可扩展、便于搜索、便于 Git diff、便于 AI Agent 理解。

## General Rules

- 文件和目录使用小写英文。
- 单词之间使用 `-`。
- 避免空格、中文标点、特殊符号。
- 文件名表达主题，不使用泛泛的 `note.md`、`misc.md`。
- 日期统一使用 `YYYY-MM-DD`。
- 稳定内容不要频繁改名，避免 Git 历史分散。

## File Naming

推荐格式：

```text
topic-name.md
topic-name-detail.md
YYYY-MM-DD-topic-name.md
```

示例：

```text
redis-cache-penetration.md
java-thread-pool.md
2026-05-10-debug-nginx-502.md
```

## Project Naming

项目目录使用：

```text
project-name/
```

项目内部推荐：

```text
README.md
architecture.md
decisions.md
bugs.md
notes.md
```

示例：

```text
01_projects/payment-service/
01_projects/personal-dev-os/
```

## Daily Log Naming

每日日志使用：

```text
YYYY-MM-DD.md
```

示例：

```text
daily/2026-05-10.md
```

## Image Naming

图片统一放入 `assets/YYYY/`。

推荐格式：

```text
YYYY-MM-DD-topic-description.ext
```

示例：

```text
assets/2026/2026-05-10-redis-cache-flow.png
assets/2026/2026-05-10-system-design-sketch.jpg
```

Markdown 引用使用相对路径：

```md
![redis cache flow](../assets/2026/2026-05-10-redis-cache-flow.png)
```

## Prompt Naming

Prompt 文件推荐格式：

```text
tool-purpose-template.md
tool-project-task.md
agent-role-task.md
```

示例：

```text
prompts/codex/codex-code-review.md
prompts/claude/claude-architecture-review.md
prompts/agents/research-agent-template.md
```

## Snippet Naming

Snippet 文件推荐格式：

```text
topic-command.md
topic-config.md
topic-troubleshooting.md
```

示例：

```text
snippets/docker/docker-compose-healthcheck.md
snippets/git/git-rebase-workflow.md
snippets/nginx/nginx-reverse-proxy.md
```

## Search Tags

可以在正文中使用少量标签，但不要依赖标签做主分类。

推荐：

```md
tags: [java, concurrency, production]
```

避免：

```md
tags: [todo, important, urgent, misc, random]
```

## Do Not Use

- `final-final.md`
- `new-note.md`
- `未命名.md`
- `杂项.md`
- `2026.05.10.md`
- `project_1.md`
- `IMG_1234.png`
