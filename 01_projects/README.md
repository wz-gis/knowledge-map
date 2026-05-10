# Projects

项目目录用于管理有明确目标、上下文和结束条件的工程工作。

## Project Folder Structure

推荐每个项目使用：

```text
01_projects/project-name/
├── README.md
├── architecture.md
├── decisions.md
├── bugs.md
└── notes.md
```

## Project Rules

- 一个项目一个目录。
- 项目名使用小写英文和 `-`。
- 项目完成、暂停或废弃后移动到 `04_archive/`。
- 图片仍然放入 `assets/YYYY/`，不要在项目内创建 assets。
- 与项目无关的长期知识，抽取到 `02_areas/`。
