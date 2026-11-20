# FangdaysCMS Releases

FangdaysCMS 官方签名升级包与 `FDU1` 升级清单公开分发仓库。仅存放公开版本升级包与经厂商 Ed25519 私钥（`fd-2026`）签名的清单，不包含任何站点数据、配置或签发私钥。

## 最新版本：2.0.0

- **最新清单（HTTPS 更新源）**：`https://raw.githubusercontent.com/iFangdays/FangdaysCMS-releases/main/latest.fdu1`
- **2.0.0 升级包地址**：`https://raw.githubusercontent.com/iFangdays/FangdaysCMS-releases/main/releases/2.0.0/fangdayscms-2.0.0.zip`
- **包大小**：`9880046` bytes（1,005 个运行文件）
- **SHA-256**：`0a1e8d2555b402ebb6df1c8b069dfdbe26970fa0ac234bcffc40d3f0f115900c`

### 2.0.0 签名清单（FDU1）

```text
FDU1.eyJrZXlfaWQiOiJmZC0yMDI2IiwidmVyc2lvbiI6IjIuMC4wIiwic2hhMjU2IjoiMGExZThkMjU1NWI0MDJlYmI2ZGYxYzhiMDY5ZGZkYmUyNjk3MGZhMGFjMjM0YmNmZmM0MGQzZjBmMTE1OTAwYyIsInNpemUiOjk4ODAwNDYsInVybCI6Imh0dHBzOi8vcmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbS9pRmFuZ2RheXMvRmFuZ2RheXNDTVMtcmVsZWFzZXMvbWFpbi9yZWxlYXNlcy8yLjAuMC9mYW5nZGF5c2Ntcy0yLjAuMC56aXAiLCJub3RlcyI6IkZhbmdkYXlzQ01TIDIuMC4wIOato-W8j-eJiO-8mlxuMS4g5YWo6Z2i5pSv5oyBIEdFTyDkvJjljJbvvIjlk4HniYzkuovlrp7lupPjgIHmlLblvZXmjqjpgIHjgIHlhoXlrrnor4TliIbjgIHmlYjmnpznm5HmjqfjgIFBSSDmjqXlj6PvvIlcbjIuIOe9keermeiPnOWNleeLrOeri-euoeeQhuS4juaJuemHj-Wkp-e6suaWsOWinuOAgeihqOWNleaMiemcgOiBlOWKqOOAgeWkmuWfn-WQjee7keWumuS4juaOiOadg-aPkOmGkueugOWMllxuMy4g5YiX6KGo5q2j5paH5oyJ6ZyA5Yqg6L2944CB6aG16Z2i57yT5a2Y5oyJ6K6-5aSH6ZqU56a744CB5pegIHNvZGl1bS9jaG1vZCDomZrmi5_kuLvmnLrlhbzlrrlcbjQuIOWcqOe6v-WNh-e6p-aUr-aMgeWQjuWPsOiHquWKqOajgOa1i-WumOaWueetvuWQjeaWsOeJiOacrOOAgemhtumDqOaoquW5heS4juiPnOWNleW-veagh-aPkOmGkuOAgeS4gOmUruS4i-i9veaaguWtmOS4juWkh-S7veWNh-e6pyIsInJlbGVhc2VkX2F0IjoxNzk1MTY2NjI1fQ.CI0lKuwa2egRh0-ZQghKlfjKiwOIE7oAAJGgdZXgm8iBLMM7I3Y0elakjpWjLNsOnO27FU00XAp8jS4ywCh7BQ
```

## 线上客户升级指引

1. **1.0.0 线上站点升级到 2.0.0**：
   - 登录站点后台，进入「系统设置 → 在线升级」（`/admin/upgrade`）。
   - 将上方 `FDU1...` 签名清单完整粘贴到「签名清单」输入框，点击「校验清单」。
   - 校验通过后点击「下载并暂存」，再点击「安装升级」。系统会自动备份旧文件到 `var/upgrades/backups/`、保留站点 `config/app.php`、数据库、上传文件与已激活授权码，并在首次访问时自动完成数据库结构迁移。
2. **2.0.0 及以上站点后续升级**：
   - 后台默认每 6 小时自动检测本仓库的 `latest.fdu1`，检测到新版本后在后台顶部横幅与左侧菜单显示提醒，进入 `/admin/upgrade` 点击「下载并暂存新版本」→「安装升级」即可一键升级。
