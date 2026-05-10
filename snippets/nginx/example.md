# Nginx Reverse Proxy

## Scenario

将 `/api/` 代理到本地后端服务。

## Example

```nginx
server {
    listen 80;
    server_name example.com;

    location /api/ {
        proxy_pass http://127.0.0.1:8080/;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

## Check

```bash
nginx -t
curl -I http://example.com/api/health
```

## Notes

- 注意 `proxy_pass` 结尾 `/` 对路径转发的影响。
- 修改配置后先 `nginx -t` 再 reload。
