# AI Integration Guide

本文档说明未来如何让 Codex、Claude Code、ChatGPT Agent 直接读取和维护这个知识库。

## Agent Reading Order

AI Agent 进入知识库后，推荐按以下顺序读取：

1. `README.md`: 理解目录结构和基本原则。
2. `NAMING.md`: 理解文件、图片、prompt、项目、日志命名。
3. `GIT.md`: 理解提交和同步规则。
4. `OBSIDIAN.md`: 理解 Obsidian 使用约定。
5. 当前任务相关目录，例如 `01_projects/xxx/` 或 `02_areas/java/`。

## Recommended Directories

| Agent Task | Preferred Directory |
| --- | --- |
| 临时收集、未分类内容 | `00_inbox/` |
| 项目规划、实现记录、决策记录 | `01_projects/` |
| 长期技术沉淀 | `02_areas/` |
| 外部资料索引和可复用参考 | `03_resources/` |
| Prompt 编写和迭代 | `prompts/` |
| 可复用命令、配置、代码片段 | `snippets/` |
| 日志总结 | `daily/` |
| 图片和附件 | `assets/YYYY/` |

## Prompt Invocation Pattern

给 Agent 的推荐启动 prompt：

```text
你正在维护一个 Obsidian Markdown 知识库。

请先读取：
- README.md
- AI-README.md
- NAMING.md
- GIT.md
- OBSIDIAN.md

工作要求：
- 只使用 Markdown 原生文件。
- 不引入数据库或在线 SaaS。
- 不创建新的顶级目录。
- 不新增 02_areas 下的领域目录，除非用户明确要求。
- 图片统一放入 assets/YYYY/。
- 修改前先理解现有结构。
- 修改后给出变更摘要和建议的 Git commit message。

当前任务：
<填写任务>
```

## Codex Workflow

适合 Codex 的任务类型：

- 根据代码阅读结果生成项目笔记。
- 整理 bug 复盘。
- 生成 architecture 记录。
- 更新 snippets。
- 根据 daily log 提炼 learning note。

推荐指令：

```text
请在这个 Obsidian Vault 中完成以下整理任务：
1. 读取相关目录和命名规范。
2. 只编辑必要的 Markdown 文件。
3. 使用相对路径引用 assets。
4. 不创建复杂任务系统。
5. 完成后列出修改文件和建议 commit message。

任务：<具体任务>
```

## Claude Code Workflow

适合 Claude Code 的任务类型：

- 长上下文代码库分析后写入长期笔记。
- 把项目中的设计决策整理到 `01_projects/`。
- 生成跨文件架构说明。
- 把复杂问题复盘到 `02_areas/system-design/` 或 `02_areas/devops/`。

推荐指令：

```text
请把当前代码库分析结果沉淀进 KnowledgeBase。
先阅读 KnowledgeBase/AI-README.md 和 KnowledgeBase/NAMING.md。
输出应是稳定 Markdown，不要依赖外部平台。
```

## ChatGPT Agent Workflow

适合 ChatGPT Agent 的任务类型：

- 根据长对话生成结构化学习笔记。
- 归纳 prompt 模板。
- 整理英语学习材料。
- 从资料中提炼长期资源索引。

推荐指令：

```text
请把以下内容整理为 Obsidian Markdown 笔记。
目标目录：<目录>
使用命名规范：kebab-case，必要时带日期。
图片统一引用 assets/YYYY/。
不要创建新的顶级目录。
```

## Agent Write Rules

- 先读后写，不凭空改变结构。
- 新项目放入 `01_projects/project-name/`。
- 长期主题放入 `02_areas/<fixed-area>/`。
- 临时内容放入 `00_inbox/`。
- 可复用命令放入 `snippets/<topic>/`。
- Prompt 放入 `prompts/<tool-or-agent>/`。
- 图片放入 `assets/YYYY/`。
- 不要在项目目录下创建独立 assets。
- 不要生成 SQL 模块。
- 不要生成复杂任务管理目录。

## Git Workflow For Agents

Agent 修改知识库后，应输出：

```text
Changed files:
- path/to/file.md

Summary:
- ...

Suggested commit:
docs(kb): update <topic>
```

默认不要自动 push，除非用户明确要求。

## Safe Automation Boundaries

Agent 可以自动做：

- 格式整理。
- 补全模板字段。
- 从 daily log 提炼 learning。
- 从项目记录生成 README。
- 把散乱片段迁移到 snippets。

Agent 不应自动做：

- 删除历史笔记。
- 大规模重命名。
- 改变顶级目录。
- 新增插件依赖。
- 改变 Git 远程地址。
- 暴露私有 token、密钥或账号信息。
