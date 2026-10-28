# 掌中酒馆 APK 更新

本仓库提供 Android ARM64 安装包、更新清单、校验和说明。开发源码和构建验证资料保存在私人仓库。

## 最新正式版：1.5.17

[下载 1.5.17 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.17/pocket-tavern-1.5.17-arm64.apk) · [发行说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.17)

本版基于1.5.16，升级Android Node LTS 24.22.1及证书、DNS和SQLite依赖；酒馆助手4.11.3更新到2026-10-25编译提交，继续保留离线资源和安全模式适配。长聊天记忆检查复用未变化消息的指纹，正文、名字、角色变化仍会重新校验。保留暖白排版、分类设置、角色/聊天范围隔离、中转等待处理、卡片与图片入口。

1000条约209万字符的合成历史重复检查20次，正文指纹字符读取由84,175,600次降至0；这只是减少重复计算，不代表整机或模型出字速度。16组当前源码回归、465项单元测试、1107项原生断言、4项导出测试、16项Android架构对照验收及71个包内生产文件核对通过。中转测试包含流式、JSON、无DONE、非流式、限流错误恢复及真实触屏发送。本轮未验证真实BUZZ/生图、ARM64手机或长期后台。

Android 8.0+ / ARM64，versionCode23，沿用1.5.8–1.5.16签名，可直接覆盖更新，无需卸载。旧1.5.6/1.5.7使用不同签名，按[迁移说明](MIGRATION-1.5.8.md)先导出并确认备份后迁移。

APK SHA-256：468d9d30435be8e5d9cc94568f030c0f7fec4665466a29465e9b874eb4222d7b

## 更新与功能入口

- 应用内：聊天右上角“设置 → 更新与扩展 → 更新中心”。
- [最新正式发行页](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)
- 固定更新源：https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json
- 图片生成、图片识别和角色表情已内置；生图需自行配置可用服务。入口可用不代表实际出图验收。
- 安全预览保留静态内容并隔离原卡脚本；完整动态交互需自动兼容和对应扩展。

更新器核对文件大小、SHA-256、包名、版本和证书，最后交给Android系统确认安装。请先保存聊天与草稿。

## 历史版本

[1.5.16：暖白布局与扩展设置](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.16) · [1.5.15：HTML增量检查](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.15) · [1.5.14：阅读位置与分类设置](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.14) · [1.5.13：回复字数](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.13) · [1.5.12：排版与安装诊断](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.12) · [1.5.11：原卡安全预览](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.11-safe-card-data)

历史实测仅代表对应日期与环境，不作为当前真实服务的保证。应用不附带AI账号、API密钥、私人卡片、聊天或生图服务。SillyTavern、酒馆助手及提示词模板保留各自许可证；APK运行资产包含对应源码和许可。
