# Personal Dev OS

这是一个面向程序员长期维护的 Obsidian 知识库。它使用 Markdown 原生文件、本地优先存储、Git 版本管理，并为未来 Codex、Claude Code、ChatGPT Agent 等 AI Agent 读写预留了清晰边界。

## Core Principles

- Markdown first: 所有正文内容使用 `.md` 文件。
- Local first: 本地 Vault 是主数据源，GitHub Private Repo 只做同步和备份。
- Git friendly: 文件名稳定、目录清晰、变更可 diff。
- AI friendly: Agent 可以从 `README.md`、`AI-README.md`、`NAMING.md`、`GIT.md`、`OBSIDIAN.md` 快速理解规则。
- Lightweight: 不引入数据库、Notion、在线 SaaS 笔记系统或复杂 GTD。
- Long term: 目录结构按 5 到 10 年维护设计，少分类、少插件、可迁移。

## Directory Map

```text
KnowledgeBase/
├── 00_inbox/
├── 01_projects/
├── 02_areas/
│   ├── web3/
│   ├── java/
│   ├── ai/
│   ├── english/
│   ├── system-design/
│   └── devops/
├── 03_resources/
├── 04_archive/
├── prompts/
│   ├── codex/
│   ├── claude/
│   ├── chatgpt/
│   └── agents/
├── snippets/
│   ├── docker/
│   ├── redis/
│   ├── shell/
│   ├── linux/
│   ├── springboot/
│   ├── git/
│   ├── nginx/
│   └── web3/
├── templates/
├── daily/
└── assets/
```

## Folder Rules

| Directory | Purpose | Rule |
| --- | --- | --- |
| `00_inbox/` | 临时收集区 | 未整理内容先放这里，定期清空或迁移 |
| `01_projects/` | 有明确目标和结束条件的项目 | 一个项目一个目录 |
| `02_areas/` | 长期能力领域 | 只保留固定 6 个领域，不新增随意分类 |
| `03_resources/` | 可复用资料、索引、清单 | 不按项目归属，按长期参考价值归档 |
| `04_archive/` | 完成、废弃、过期内容 | 只归档，不删除历史 |
| `prompts/` | Prompt 和 Agent 指令 | 按工具和用途管理 |
| `snippets/` | 可复用代码片段和命令 | 每个技术栈保留 README 和 example |
| `templates/` | Obsidian 模板 | 所有新笔记从模板开始 |
| `daily/` | 日志和工作记录 | 用日期命名，避免任务系统化 |
| `assets/` | 图片和附件 | 按年份集中管理 |

## Start Here

1. 用 Obsidian 打开 `KnowledgeBase/` 作为 Vault。
2. 阅读 [NAMING.md](./NAMING.md) 确认命名规范。
3. 阅读 [GIT.md](./GIT.md) 初始化 Git 和 GitHub Private Repo。
4. 阅读 [OBSIDIAN.md](./OBSIDIAN.md) 配置 Obsidian。
5. 阅读 [AI-README.md](./AI-README.md) 了解 Agent 读写方式。
6. 阅读 [WORKFLOW.md](./WORKFLOW.md) 建立日常使用节奏。

## Daily Workflow

1. 捕获：临时内容先进入 `00_inbox/` 或当天 daily log。
2. 整理：每周把 inbox 中的内容迁移到 project、area、resource 或 archive。
3. 沉淀：重要问题优先写成 bug、architecture、learning 或 snippet。
4. 提交：每天或每次重要整理后执行一次 Git commit。
5. 同步：通过 GitHub Private Repo 在多设备之间同步。

## What This Vault Is Not

- 不是复杂 GTD 系统。
- 不是任务管理器。
- 不是数据库。
- 不是在线平台锁定方案。
- 不是无限分类的收藏夹。

它的目标很简单：让你的工程知识在多年后仍然能被你、Git 和 AI Agent 稳定读取。
