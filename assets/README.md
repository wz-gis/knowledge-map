# Assets Rules

所有图片和附件统一放在 `assets/` 目录。

## Structure

```text
assets/
├── 2026/
├── 2027/
└── ...
```

## Rules

- 图片按年份分类。
- 不允许在项目目录内创建独立 assets。
- Markdown 使用相对路径引用图片。
- 图片文件名使用日期、主题和描述。
- 不保留无意义截图名，例如 `IMG_1234.png`。
- 大文件慎重加入 Git，必要时使用压缩后的图片。

## Image Naming

```text
YYYY-MM-DD-topic-description.ext
```

示例：

```text
2026-05-10-nginx-502-error.png
2026-05-10-redis-cache-flow.png
```

## Markdown Example

从 `daily/2026-05-10.md` 引用图片：

```md
![nginx 502 error](../assets/2026/2026-05-10-nginx-502-error.png)
```

从 `02_areas/java/thread-pool.md` 引用图片：

```md
![thread pool state](../../assets/2026/2026-05-10-thread-pool-state.png)
```

## Maintenance

- 每季度清理重复图片。
- 删除图片前先搜索是否仍被引用。
- 对重要架构图优先保存源文件说明。
