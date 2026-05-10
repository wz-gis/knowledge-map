# Prompts

Prompt 目录用于管理可复用的 AI 指令。

## Structure

```text
prompts/
├── codex/
├── claude/
├── chatgpt/
└── agents/
```

## Rules

- Prompt 文件使用 Markdown 保存。
- 文件名使用小写英文和 `-`。
- 系统 prompt、项目 prompt、agent prompt 分开管理。
- 重要 prompt 保留版本记录。
- 不在 prompt 中写入密钥、token、私有账号信息。

## Template Types

- `prompt-template.md`: 通用 prompt 模板。
- `system-prompt-template.md`: 系统级 prompt 模板。
- `project-prompt-template.md`: 项目级 prompt 模板。
- `agents/agent-prompt-template.md`: Agent 角色和工作流模板。
