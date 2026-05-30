# 密码管理完全指南

在代理环境下安全使用密码管理器，推荐开源自托管方案。

## 为什么需要密码管理器

- 每个网站使用独立强密码
- 无需记忆大量密码
- 全设备同步
- 泄露监控预警

## Bitwarden 自托管（推荐）

Bitwarden 是开源密码管理器，支持 Docker 自托管。

### Docker 部署

```bash
docker run -d \
  --name bitwarden \
  -e KANBAN_MODE=true \
  -v /opt/bitwarden/data:/data \
  -p 80:8080 \
  --restart always \
  bitwarden/self-host:latest
```

## 密码安全最佳实践

| 建议 | 说明 |
|------|------|
| 长度 > 16位 | 密码越长越安全 |
| 包含符号 | 增加复杂度 |
| 不重复使用 | 每个网站独立密码 |
| 开启两步验证 | 额外安全层 |

## 其他推荐工具

- **1Password** - 商业方案，生态完善
- **LastPass** - 免费版够用
- **LessPass** - 无服务器密码生成器

---

推荐工具：

- [Clash for Windows](https://clashforwindows.site/)
- [ClashMI](https://clashmi.site/)
- [FlClash](https://flclash.us/)
