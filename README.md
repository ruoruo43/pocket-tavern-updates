# 掌中酒馆 APK 更新

本仓库提供 Android ARM64 安装包、更新清单、校验和说明。开发源码和构建验证资料保存在私人仓库。

## 最新正式版：1.5.15

[下载 1.5.15 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.15/pocket-tavern-1.5.15-arm64.apk) · [发行说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.15)

本版基于 1.5.14，减少流式聊天中 HTML 卡片的重复检查，修复文本节点更新后卡片不刷新、替换消息及历史编号变化后卡片设置按钮失效。自动整理记忆时发送有明确提示、保留草稿；普通点击减少记忆读取。阅读位置、分类设置和已有连接保持兼容。

160 条消息、24 次流式更新的固定测试中，消息检查次数从 3840 降为 24，减少约 99.4%；这不是整机速度或模型出字速度。456 项单元测试、15 组发布回归（174 项浏览器检查）、1090 项 Java 断言、13 项 Android 架构对照验收及 69 个包内生产文件核对通过。所有模型回复均为本机合成测试；本轮未验证真实 BUZZ/生图、ARM64 手机或长期运行。

Android 8.0+ / ARM64，versionCode 21，沿用 1.5.8–1.5.14 签名，可直接覆盖更新，无需卸载。旧 1.5.6/1.5.7 使用不同签名，按[迁移说明](MIGRATION-1.5.8.md)先导出并确认备份后迁移。

APK SHA-256：28c61d44857faa8de5a8920958da156222bceada1c699d02b42f2a1a62b99e8b

## 更新与功能入口

- 应用内：聊天右上角“设置 → 更新与扩展 → 更新中心”。
- [最新正式发行页](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)
- 固定更新源：https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json
- 图片生成、图片识别和角色表情已内置；生图需自行配置可用服务。入口可用不代表实际出图验收。
- 安全预览保留静态内容并隔离原卡脚本；完整动态交互需自动兼容和对应扩展。

更新器核对文件大小、SHA-256、包名、版本和证书，最后交给 Android 系统确认安装。请先保存聊天与草稿。

## 历史版本

[1.5.14：阅读位置与分类设置](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.14) · [1.5.13：回复字数](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.13) · [1.5.12：排版与安装诊断](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.12) · [1.5.11：原卡安全预览](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.11-safe-card-data)

历史实测只代表对应日期与环境，不能作为当前真实服务可用的保证。应用不附带 AI 账号、API 密钥、私人卡片、聊天或生图服务。SillyTavern、酒馆助手及提示词模板保留各自许可证；APK 的运行资产包含对应源码与许可。
