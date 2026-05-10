# Git Setup

本知识库适合使用 GitHub Private Repo 同步。Git 是版本管理和多设备同步的基础，不承担任务管理职责。

## Initialize Local Repo

在 `KnowledgeBase/` 目录下执行：

```bash
git init
git add .
git commit -m "chore: init personal dev os"
```

## Create GitHub Private Repo

1. 打开 GitHub。
2. New repository。
3. Repository name 推荐：`personal-dev-os` 或 `knowledge-base`。
4. Visibility 选择 `Private`。
5. 不勾选初始化 README、`.gitignore`、license。
6. 创建后复制远程地址。

## Connect Remote

SSH 推荐：

```bash
git remote add origin git@github.com:<user>/<repo>.git
git branch -M main
git push -u origin main
```

HTTPS 也可用：

```bash
git remote add origin https://github.com/<user>/<repo>.git
git branch -M main
git push -u origin main
```

## Daily Git Workflow

推荐轻量流程：

```bash
git pull --rebase
git status
git add .
git commit -m "docs: update daily notes"
git push
```

## Commit Message Style

推荐：

```text
docs: update java notes
docs: add redis snippets
docs: archive old project
chore: update obsidian settings
```

避免：

```text
update
misc
save
final
```

## Multi-device Rules

- 每台设备开始写之前先 `git pull --rebase`。
- 写完后及时 `git push`。
- 避免多台设备同时编辑同一个文件。
- 冲突优先手动解决，不要直接覆盖。
- 手机端如果使用 Git 插件，同步前先确认没有未完成编辑。

## Obsidian Git Plugin Recommended Settings

插件：Obsidian Git。

推荐配置：

| Setting | Value |
| --- | --- |
| Auto pull interval | 10 到 30 分钟 |
| Auto commit-and-sync interval | 30 到 60 分钟 |
| Commit message | `vault backup: {{date}} {{time}}` |
| Pull before push | Enabled |
| Disable push | Disabled |
| Show status bar | Enabled |

说明：

- 如果你经常在多设备间切换，建议开启自动 pull。
- 如果你担心自动 commit 产生噪音，可以只开启手动 sync。
- 不建议把 Git 当作实时同步工具；它更适合稳定版本同步。

## Conflict Handling

当出现冲突：

```bash
git status
```

打开冲突文件，保留需要的内容，删除冲突标记：

```text
<<<<<<< HEAD
...
=======
...
>>>>>>> branch
```

然后：

```bash
git add .
git rebase --continue
git push
```

如果不在 rebase 中：

```bash
git add .
git commit -m "docs: resolve sync conflict"
git push
```
