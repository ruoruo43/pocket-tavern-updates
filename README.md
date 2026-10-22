# 掌中酒馆 APK 更新

本仓库公开提供 Android ARM64 安装包、版本清单、SHA-256 校验和说明。开发源码及签名备份保存在私人仓库，不会作为本公开仓库附件发布。

## 1.5.8 新签名迁移预发布

[下载 1.5.8 新签名迁移版](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.8-new-signer)

**本次签名与旧版 1.5.6/1.5.7 不同，不能直接覆盖安装。先在旧版导出并确认备份，再卸载旧版、安装新包并恢复。未备份前请勿卸载。** 后续使用本次同一新签名的版本可覆盖本包。

本版修复 HTML 自动兼容、中转 API 回复等待，增加图片生成/识别配置入口，优化启动和备份效率并调整排版。已通过本机回归、Android 编译、APK v2/v3 验签、对齐和内置源码核对；尚未完成本轮手机或模拟器安装、真实中转账号和真实生图服务验收，故以预发布提供，不替换旧签名正式更新通道。

## 正式更新通道

- [下载最新正式版](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)
- 固定更新源：`https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json`
- 应用内：聊天右上角「设置 → 更新中心」。

只有相同签名的普通更新才能直接覆盖安装；更新器会验证包名、递增版本、签名及下载 SHA-256，最后由 Android 系统确认。1.5.8 换签迁移适用上方单独说明。请先保存聊天和草稿。

普通扩展在「设置 → 插件与扩展市场」管理。SillyTavern 核心、本机适配及固定预装扩展经验证后随 APK 发布；带用户修改、分支切换或主动删除的副本保留。

应用不附带 AI 账号、API 密钥、私人角色卡、聊天或生图服务。测试范围与哈希以每个 Release 为准。SillyTavern、酒馆助手及提示词模板保留各自许可证；APK 内 `assets/sillytavern.zip` 和 `assets/bundled-extensions.zip` 提供实际运行源码和许可。
