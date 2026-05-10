# Redis Basic Troubleshooting

## Scenario

排查 Redis 延迟、慢查询、内存和连接数。

## Commands

```bash
redis-cli INFO memory
redis-cli INFO clients
redis-cli INFO stats
redis-cli SLOWLOG GET 20
redis-cli --latency
```

## Safe Key Scan

```bash
redis-cli --scan --pattern "prefix:*" | head -100
```

## Notes

- 避免在线上大 key 空间执行 `KEYS *`。
- 排查大 key 时优先使用 scan 类命令。
