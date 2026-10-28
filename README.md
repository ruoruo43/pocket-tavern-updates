# 掌中酒馆 APK 更新

本仓库提供 Android ARM64 安装包、更新清单与校验说明。开发源码、签名备份和详细验证资料保存在私有开发仓库。

## 最新正式版：1.5.18

[下载 1.5.18 完整 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.18/pocket-tavern-1.5.18-arm64.apk) · [发行说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.18)

资料库分为角色卡、世界书、聊天记录；API连接和存储备份移到应用管理。聊天设置按对话与剧情、阅读与媒体、管理与高级分组，保留八个目标页，分类页返回先回首页。连接草稿、原有保存范围和旧入口保留，暖白与紫色排版延续。

兼容升级DOMPurify3.4.17、Multer2.5.0、ws8.22.0、Express4.22.3、form-data4.0.6、Handlebars4.7.10，补入安全补丁。继续固定SillyTavern1.19.0、Node24.22.1和已验证扩展，保持资料格式。

17组当前源码回归、465项单元测试、1107项原生断言、4项导出测试、25项Android15 x86_64验收及71个包内生产文件核对通过。包括覆盖17保留资料、原生返回、真实软键盘、卡片与问号隐藏、中转多种响应与限流恢复。664个生产依赖来源及19946文件校验、23项依赖冒烟和59个界面模板对照通过；没有将这些结果表述为整个项目无漏洞。

2026-10-28使用此前保存的BUZZ密钥，在原地址https://api.buzzgw.com/v1对gemini-3.8-flash实测：两次流式、一次非流式、一次冷启动后聊天均正常输出，约4.1至6.1秒，无需重填密钥。服务商后续可用性可能变化。本轮未验收ARM64手机、长期运行或真实生图。

Android8.0+ / ARM64，versionCode24，沿用1.5.8–1.5.17签名，可保留应用覆盖安装。旧1.5.6/1.5.7签名不同，按[迁移说明](MIGRATION-1.5.8.md)先导出并确认备份后迁移。

APK SHA256：1d9c7765d016346686b2c0749fef37b9dc941ba411350b84f6fdacae4377f509

## 更新与功能入口

- 应用内：聊天右上角“设置 → 更新与扩展 → 更新中心”。
- [最新正式发行页](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)。
- 固定更新源：https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json
- API连接与备份：资料库 → 应用管理。
- 图片生成与识别：聊天设置 → 图片前端；生图需配置可用服务，入口通过不等于真实出图验收。
- 安全预览保留静态结构并隔离原卡脚本，完整交互仍需对应兼容模式和扩展。

更新器核对大小、SHA256、包名、版本和证书，再交给Android确认安装。请先保存聊天与草稿。

## 历史版本

[1.5.17：运行环境与记忆缓存](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.17) · [1.5.16：暖白布局](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.16) · [1.5.15：HTML增量检查](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.15) · [1.5.14：阅读与分类设置](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.14)

历史实测只代表对应日期和环境。应用不附带AI账号、API密钥、私人卡片、聊天或生图服务。SillyTavern及预装扩展保留各自许可证；APK运行资产包含对应源码和许可。
