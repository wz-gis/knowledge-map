# Git Pull Rebase Workflow

## Scenario

多设备同步 Obsidian Vault 前，先拉取远程更新。

## Commands

```bash
git status
git pull --rebase
git add .
git commit -m "docs: update notes"
git push
```

## Conflict Check

```bash
git status
```

## Notes

- 开始写之前先 pull。
- 写完及时 push。
- 遇到冲突时手动合并 Markdown，不要直接覆盖。
