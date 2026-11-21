# FangdaysCMS Releases

FangdaysCMS 官方签名升级包与 `FDU1` 升级清单公开分发仓库。仅存放公开版本升级包与经厂商 Ed25519 私钥（`fd-2026`）签名的清单，不包含任何站点数据、配置或签发私钥。

## 最新版本：2.0.2

- **最新清单（国内推荐 CDN 源）**：`https://cdn.jsdelivr.net/gh/iFangdays/FangdaysCMS-releases@main/latest.fdu1`
- **最新清单（GitHub 源）**：`https://raw.githubusercontent.com/iFangdays/FangdaysCMS-releases/main/latest.fdu1`
- **2.0.2 升级包地址**：`https://cdn.jsdelivr.net/gh/iFangdays/FangdaysCMS-releases@main/releases/2.0.2/fangdayscms-2.0.2.zip`
- **包大小**：`7734640` bytes（755 个后端与管理后台运行文件；不包含任何前台模板、主题静态资源、配置或数据库）
- **SHA-256**：`f07c97c4f50b97fdfeb146dfc1b9a5d18184f3ee6f992b78e7f0cb4cd3575ed5`

### 2.0.2 签名清单（FDU1）

```text
FDU1.eyJrZXlfaWQiOiJmZC0yMDI2IiwidmVyc2lvbiI6IjIuMC4yIiwic2hhMjU2IjoiZjA3Yzk3YzRmNTBiOTdmZGZlYjE0NmRmYzFiOWE1ZDE4MTg0ZjNlZTZmOTkyYjc4ZTdmMGNiNGNkMzU3NWVkNSIsInNpemUiOjc3MzQ2NDAsInVybCI6Imh0dHBzOi8vY2RuLmpzZGVsaXZyLm5ldC9naC9pRmFuZ2RheXMvRmFuZ2RheXNDTVMtcmVsZWFzZXNAbWFpbi9yZWxlYXNlcy8yLjAuMi9mYW5nZGF5c2Ntcy0yLjAuMi56aXAiLCJub3RlcyI6IkZhbmdkYXlzQ01TIDIuMC4yIOato-W8j-eJiO-8mlxuMS4g5Zyo57q_5Y2H57qn5YyF5b275bqV5o6S6Zmk5bm25L-d5oqk5omA5pyJ5YmN5Y-w5qih5p2_5LiO5Li76aKY6Z2Z5oCB6LWE5rqQ77yIdGVtcGxhdGVzL-OAgXB1YmxpYy90ZW1wbGF0ZS_jgIFwdWJsaWMvc3RhdGljL-OAgXB1YmxpYy9pbWFnZXMv44CBdmlld3Mvc2l0ZS_vvInvvIzku4XljYfnuqflkI7nq68gQ01TIOS4jueuoeeQhuWQjuWPsO-8jOe7neS4jeimhuebluWuouaIt-WJjeWPsOmhtemdouOAgemFjee9ruS4juaVsOaNruW6k1xuMi4g5ZCO5Y-w44CM5Zyo57q_5Y2H57qnIOKGkiDmnIDov5HljYfnuqforrDlvZXjgI3mlrDlop7kuIDplK7lm57pgIDlip_og73vvIzmlK_mjIHjgIzku4XmgaLlpI3liY3lj7DmqKHmnb_jgI3vvIjkv53nlZnlvZPliY3lkI7nq68gQ01TIOeJiOacrO-8ieS4juOAjOaVtOWMheWbnumAgOOAjeS4pOenjeaooeW8jyIsInJlbGVhc2VkX2F0IjoxNzk1MjQ4MDYwfQ.qermLN9ypyvlItuR8bpdHuz_wp_MEyTWWx4gA3hYCH3w5Vn-BLLfNeEpvs90qierV6tTceH2Pb9yIvtZZwJFCg
```

## 线上客户升级指引

1. **1.0.0 线上站点升级到 2.0.2**：
   - 登录站点后台，进入「系统设置 → 在线升级」（`/admin/upgrade`）。
   - 将上方 `FDU1...` 签名清单完整粘贴到「签名清单」输入框，点击「校验清单」。
   - 校验通过后点击「下载并暂存」，再点击「安装升级」。系统会自动备份旧文件到 `var/upgrades/backups/`、保留站点前台模板、配置、数据库、上传文件与已激活授权码，并在首次访问时自动完成数据库结构迁移。
2. **2.0.0 及以上站点后续升级**：
   - 后台默认每 6 小时自动检测本仓库的 `latest.fdu1`（国内主机建议将更新源设为 `https://cdn.jsdelivr.net/gh/iFangdays/FangdaysCMS-releases@main/latest.fdu1`；2.0.1+ 已内置多镜像自动回退），检测到新版本后在后台顶部横幅与左侧菜单显示提醒，进入 `/admin/upgrade` 点击「下载并暂存新版本」→「安装升级」即可一键升级。
   - 升级后如需回退，可在 `/admin/upgrade` 底部的「最近升级记录」中点击「仅恢复前台模板」或「整包回退」。
