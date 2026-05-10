# Linux Service Troubleshooting

## Scenario

排查 systemd 服务失败原因。

## Commands

```bash
systemctl status my-service --no-pager
journalctl -u my-service -n 200 --no-pager
journalctl -u my-service -f
```

## Network Checks

```bash
ss -lntp
curl -v http://127.0.0.1:8080/health
```

## Notes

- `journalctl -f` 会持续输出日志，适合观察重启过程。
- 生产环境先读日志，再重启服务。
