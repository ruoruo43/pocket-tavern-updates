# 掌中酒馆 APK 更新

本仓库公开提供 Android ARM64 安装包、版本清单、SHA-256 校验和说明。开发源码及签名备份保存在私人仓库，不会作为本公开仓库附件发布。

## 1.5.11 正式版 · 原角色卡安全预览修复

[下载 1.5.11 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.11-safe-card-data/pocket-tavern-1.5.11-arm64.apk) · [版本说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.11-safe-card-data)

修复依靠消息读取脚本填充的心声/键值状态卡在安全预览中空白的问题：从当前消息填入只读卡片，保留原排版并支持原生折叠，原卡脚本仍不执行。完整脚本交互继续使用自动兼容。该有限结构适配不承诺任意脚本卡片均能静态还原。

原角色卡和聊天在最终业务资源一致的 Android x86_64 架构对照包通过八项验收：原正文、两个候选回复的安全/自动显示，实际触摸折叠和历史重载；卡片内容与当前消息一致。名字旁问号在普通/高级状态隐藏，没有可见代码块按钮。Node 413/413、浏览器隔离预览 22 项、APK v2/v3、zipalign、同签名和 63 个生产文件核对通过。**生产 ARM64 手机、长期运行和真实图片服务待验收。** 本轮未重新调用 BUZZ，网络代码未改；下方 1.5.10 真实 BUZZ 结果为历史证据。

**可直接覆盖 1.5.8 / 1.5.9 / 1.5.10 新签名版，建议先导出备份，无需卸载。1.5.6 / 1.5.7 旧签名版不能直接覆盖，请先导出并确认备份，再按[迁移说明](https://github.com/ruoruo43/pocket-tavern-updates/blob/main/MIGRATION-1.5.8.md)安装和恢复。** 用户原卡、聊天、模板和私人截图只留本地。公开附件仅 APK、更新清单、说明和校验；完整源码与脱敏验收归档到私人仓库。1.5.11 已正式上线并设为 Latest，固定更新源现指向本版。

2026-10-22 按用户要求从预发布转为正式上线，沿用同一 APK、update.json 和已校验哈希。发布附件内的预发布字样保留为构建归档状态；正式状态以本节及 Release 的 Latest 标记为准。验证范围不因上线而扩大。

## 1.5.10 BUZZ 与前端显示修复预发布（历史记录）

[下载 1.5.10 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.10-buzz-display-fixes/pocket-tavern-1.5.10-arm64.apk) · [版本说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.10-buzz-display-fixes)

**1.5.8 / 1.5.9 新签名版可直接覆盖升级，建议先导出备份，无需卸载。** 修复名字旁问号在高级状态重新出现、显示正则生成的多 HTML 卡片只剩代码按钮，以及 BUZZ gemini-3.8-flash 原生非流式无正文的兼容。

已用实际密钥验证 Base URL `https://buzzai.cc/v1`、模型 `gemini-3.8-flash`：最终 Android 业务资源复测非流式约 5.7 秒、流式约 5.0 秒均返回正文。原 `api.buzzgw.com` 对照仍有仅心跳无正文；应用不会自动替换域名，请在连接设置中改为已验证地址。服务商上游曾拒绝或提前断开，客户端不能保证其永久稳定。

Node 413/413、浏览器预览 21 项、签名/对齐/62 个生产文件核对通过；最终业务资源对应的 x86_64 Android 对照包验证两张正则卡片、安全/自动模式、图片入口与普通/高级问号。**ARM64 手机、用户原角色卡与真实图片服务仍待验收。** 安全预览保留静态排版，完整动态卡片需自动兼容和相应扩展。本版保持预发布，正式 latest 保留 v1.5.7。

## 1.5.9 模拟器修复预发布（历史记录）

[下载 1.5.9 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.9-emulator-fixes/pocket-tavern-1.5.9-arm64.apk) · [版本说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.9-emulator-fixes)

**1.5.8 新签名版可以直接覆盖升级。1.5.6/1.5.7 原签名版仍须先备份迁移。** 名字旁自定义 API 问号随时间信息收起，安全预览修复本机图片，生成失败恢复控件，并补全首次输出和非流式正文超时保护。

Node 406/406、最终 Android 架构对照包六种模拟中转场景、六项预览/图片入口及两项非流式场景通过。**BUZZ gemini-3.8-flash 模型列表通过，真实聊天仍未收到可确认回复；ARM64 真机与真实生图服务待验收。** 模拟器使用保留业务资源的 x86 对照包，不能代替生产 ARM64 真机验收。

本版保持预发布，原 1.5.7 正式通道保留。完整源码和验收资料保存在私人开发仓库，签名继续使用 1.5.8 的新签名。

## 1.5.8 新签名迁移预发布（历史记录）

[下载 1.5.8 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.8-new-signer/pocket-tavern-1.5.8-arm64.apk) · [版本说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.8-new-signer)

安装只需下载 `.apk`；Release 中的 `.part` 和差分 ZIP 是上传校验资料，无需下载或拼接。

**本次签名与旧版 1.5.6/1.5.7 不同，不能直接覆盖安装。先在旧版导出并确认备份，再卸载旧版、安装新包并恢复。未备份前请勿卸载。** 后续使用本次同一新签名的版本可覆盖本包。

本版修复 HTML 自动兼容、中转 API 回复等待，增加图片生成/识别配置入口，优化启动和备份效率并调整排版。已通过本机回归、Android 编译、APK v2/v3 验签、对齐和内置源码核对；尚未完成本轮手机或模拟器安装、真实中转账号和真实生图服务验收，故以预发布提供，不替换旧签名正式更新通道。

备份 ZIP 需解压后按分类导入，当前没有一键整包恢复；API 密钥需要重新填写。详见 [迁移操作步骤](MIGRATION-1.5.8.md)。

## 正式更新通道

- [下载最新正式版](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)
- 固定更新源：`https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json`
- 应用内：聊天右上角「设置 → 更新中心」。

只有相同签名的普通更新才能直接覆盖安装；更新器会验证包名、递增版本、签名及下载 SHA-256，最后由 Android 系统确认。1.5.8 换签迁移适用上方单独说明。请先保存聊天和草稿。

普通扩展在「设置 → 插件与扩展市场」管理。SillyTavern 核心、本机适配及固定预装扩展经验证后随 APK 发布；带用户修改、分支切换或主动删除的副本保留。

应用不附带 AI 账号、API 密钥、私人角色卡、聊天或生图服务。测试范围与哈希以每个 Release 为准。SillyTavern、酒馆助手及提示词模板保留各自许可证；APK 内 `assets/sillytavern.zip` 和 `assets/bundled-extensions.zip` 提供实际运行源码和许可。
