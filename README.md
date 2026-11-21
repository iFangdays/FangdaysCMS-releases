# FangdaysCMS Releases

FangdaysCMS 官方签名升级包与 `FDU1` 升级清单公开分发仓库。仅存放公开版本升级包与经厂商 Ed25519 私钥（`fd-2026`）签名的清单，不包含任何站点数据、配置或签发私钥。

## 最新版本：2.0.1

- **最新清单（国内推荐 CDN 源）**：`https://cdn.jsdelivr.net/gh/iFangdays/FangdaysCMS-releases@main/latest.fdu1`
- **最新清单（GitHub 源）**：`https://raw.githubusercontent.com/iFangdays/FangdaysCMS-releases/main/latest.fdu1`
- **2.0.1 升级包地址**：`https://cdn.jsdelivr.net/gh/iFangdays/FangdaysCMS-releases@main/releases/2.0.1/fangdayscms-2.0.1.zip`
- **包大小**：`9921776` bytes（1,011 个运行文件）
- **SHA-256**：`df2cac4c76ef328ddf7cde527ad2a6a29f8f4490caefa2537053fe5bc42b56eb`

### 2.0.1 签名清单（FDU1）

```text
FDU1.eyJrZXlfaWQiOiJmZC0yMDI2IiwidmVyc2lvbiI6IjIuMC4xIiwic2hhMjU2IjoiZGYyY2FjNGM3NmVmMzI4ZGRmN2NkZTUyN2FkMmE2YTI5ZjhmNDQ5MGNhZWZhMjUzNzA1M2ZlNWJjNDJiNTZlYiIsInNpemUiOjk5MjE3NzYsInVybCI6Imh0dHBzOi8vY2RuLmpzZGVsaXZyLm5ldC9naC9pRmFuZ2RheXMvRmFuZ2RheXNDTVMtcmVsZWFzZXNAbWFpbi9yZWxlYXNlcy8yLjAuMS9mYW5nZGF5c2Ntcy0yLjAuMS56aXAiLCJub3RlcyI6IkZhbmdkYXlzQ01TIDIuMC4xIOato-W8j-eJiO-8mlxuMS4g5paw5aKe5YmN5Y-w5L6n6L655Zyo57q_5a6i5pyN5rWu56qX5LiO5ZCO5Y-w5Y-v57yW6L6R6YKu5Lu26YCa55-l5qih5p2_XG4yLiDlhazlj7jkv6Hmga_mlK_mjIHnmb7luqYv6auY5b635Zyw5Zu-5Z2Q5qCH5qCH5rOo5LiO5YmN56uv5Zyw5Zu-5Y2h54mH5bGV56S677yM6buY6K6k5Li76aKY6KeG6KeJ54SV5pawXG4zLiBHRU8g5LyY5YyW5paw5aKe54us56uL5o6o6YCB6K6w5b2V6aG1562-44CB5bel5L2c5Y-w5b6F5o6o6YCB55yL5p2_44CB55m-5bqm5pel6YWN6aKd6L-96LW25o6o6YCB5LiO5ouS57ud6K6h5pWw5L-u5q2jXG40LiDlnKjnur_ljYfnuqfmlK_mjIEgY1VSTCDkvJjlhYjkvKDovpPkuI4ganNEZWxpdnIg5a6Y5pa55aSa6ZWc5YOP6Ieq5Yqo5Zue6YCA77yM6Kej5Yaz5Zu95YaF6Jma5ouf5Li75py655u06L-eIEdpdEh1YiDotoXml7bpl67popgiLCJyZWxlYXNlZF9hdCI6MTc5NTI0NzE1N30.HxKjoLM-aSUz4miV01SacwnA8Xi6EKC8J_AMVkKQ4UKHTWNssLScZMGL2ftlzthGpTi1DXrn25lovpcAmBo9Dw
```

## 线上客户升级指引

1. **1.0.0 线上站点升级到 2.0.1**：
   - 登录站点后台，进入「系统设置 → 在线升级」（`/admin/upgrade`）。
   - 将上方 `FDU1...` 签名清单完整粘贴到「签名清单」输入框，点击「校验清单」。
   - 校验通过后点击「下载并暂存」，再点击「安装升级」。系统会自动备份旧文件到 `var/upgrades/backups/`、保留站点 `config/app.php`、数据库、上传文件与已激活授权码，并在首次访问时自动完成数据库结构迁移。
2. **2.0.0 及以上站点后续升级**：
   - 后台默认每 6 小时自动检测本仓库的 `latest.fdu1`（国内主机建议将更新源设为 `https://cdn.jsdelivr.net/gh/iFangdays/FangdaysCMS-releases@main/latest.fdu1`；2.0.1+ 已内置多镜像自动回退），检测到新版本后在后台顶部横幅与左侧菜单显示提醒，进入 `/admin/upgrade` 点击「下载并暂存新版本」→「安装升级」即可一键升级。
