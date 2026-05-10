# Docker Compose Healthcheck

## Scenario

为服务添加健康检查，避免依赖服务未启动时应用提前启动。

## Example

```yaml
services:
  redis:
    image: redis:7
    ports:
      - "6379:6379"
    healthcheck:
      test: ["CMD", "redis-cli", "ping"]
      interval: 5s
      timeout: 3s
      retries: 10

  app:
    image: my-app:latest
    depends_on:
      redis:
        condition: service_healthy
```

## Notes

- `depends_on.condition` 适用于 Docker Compose 规范，不等同于应用层重试。
- 生产应用仍应在代码中处理依赖短暂不可用。
