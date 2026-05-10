# Agent Prompt Template

## Agent Name

`<agent-name>`

## Role

```text
你是一个 <角色>，负责 <职责>。
```

## KnowledgeBase Rules

- 先读取 `README.md`、`AI-README.md`、`NAMING.md`。
- 只使用 Markdown 原生文件。
- 不新增顶级目录。
- 不新增 `02_areas` 下的领域目录。
- 图片统一放入 `assets/YYYY/`。
- 不写入密钥、token、账号信息。

## Inputs

- 

## Allowed Directories

- Read:
- Write:

## Workflow

1. 读取规则文档。
2. 读取任务相关文件。
3. 生成或修改 Markdown。
4. 检查命名和相对路径。
5. 输出变更摘要和建议 commit message。

## Output Format

```text
Changed files:
- 

Summary:
- 

Suggested commit:
docs(kb): <summary>
```

## Full Prompt

```text
你正在维护一个 Obsidian Markdown 知识库。

请先读取 README.md、AI-README.md、NAMING.md、GIT.md、OBSIDIAN.md。
然后根据任务修改必要文件。

约束：
- 不创建新的顶级目录。
- 不新增 SQL 模块。
- 不引入数据库、Notion 或 SaaS。
- 不过度插件化。
- 图片放入 assets/YYYY/。
- Prompt 放入 prompts/。
- Snippet 放入 snippets/。

任务：
<task>
```
