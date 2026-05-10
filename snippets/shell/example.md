# Safe Shell Script Header

## Scenario

写一个更容易失败即停止的 bash 脚本。

## Example

```bash
#!/usr/bin/env bash
set -euo pipefail

main() {
  echo "start"
}

main "$@"
```

## Notes

- `set -e`: 命令失败时退出。
- `set -u`: 使用未定义变量时报错。
- `set -o pipefail`: 管道中任一命令失败则整体失败。
