# Spring Boot Actuator Health

## Scenario

开启健康检查端点，用于本地调试或容器健康检查。

## Example

```yaml
management:
  endpoints:
    web:
      exposure:
        include: health,info
  endpoint:
    health:
      probes:
        enabled: true
```

## Check

```bash
curl http://localhost:8080/actuator/health
```

## Notes

- 生产环境谨慎暴露 Actuator 端点。
- 不要公开敏感端点，例如 `env`、`heapdump`。
