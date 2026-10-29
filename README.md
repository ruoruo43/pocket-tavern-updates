# 掌中酒馆 APK 更新

本仓库提供 Android ARM64 安装包、更新清单与校验说明。开发源码、签名备份和详细验证资料保存在私有开发仓库。

## 最新正式版：1.5.20

[下载1.5.20完整APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.20/pocket-tavern-1.5.20-arm64.apk) · [发行说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.20)

基于已发布1.5.19完整源码合并，保留设置搜索、聊天行距、更新提示与现有资料。资料库继续分为角色卡、世界书和聊天记录，API连接/存储备份独立放在应用管理。

本版补齐CUSTOM非流式错误正文的原请求截止与64KiB上限，清理正文、socket及取消监听器；成功正文与流式规则保留，不自动重试。最终APK的静默HTTP429错误体约180.9秒后明确结束等待、关闭上游并能继续聊天；超大错误体约1.4秒结束。

长聊天只对确定的末尾追加定向检查，局部状态事件同帧合并，结构/设置/作用域变化仍全刷。1000行追加格式检查1001→1，十次局部状态检查10000→1；资料库概览少4个重复列表请求，650份样例lstat3831→1921，统计一致。这是减少本地工作，不代表模型提速。

compression1.8.1升级1.8.2，释放中断响应的压缩资源并修复no-transform大小写处理。其余已验证核心、扩展和依赖保留：SillyTavern1.19.0、Node24.22.1、酒馆助手4.11.3及提示词模板1.17.9。

20组当前源码回归、505项单元、4项导出、1107项原生断言、25项Android15 x86_64验收及73项包内生产文件核对通过。[BUZZ原地址](https://api.buzzgw.com/v1) 的gemini-3.8-flash实际重复流式、非流式与冷启动四次均输出，约4.1–5.7秒，保留19密钥无需重填。后续服务可用性仍由服务商决定。

Android8.0+ / ARM64，versionCode26，沿用1.5.8–1.5.19签名，可保留应用覆盖安装。旧1.5.6/1.5.7签名不同，按[迁移说明](MIGRATION-1.5.8.md)备份迁移。ARM64真机、长期运行和真实生图本轮未验收，图片仅确认入口与配置。

APK SHA256：37f2c4849e2c3f5c20e477030d9e762fff0fe69b1b0bd358cc8706646dc9641b

## 更新与功能入口

- 应用内：聊天右上角“设置 → 更新与扩展 → 更新中心”。
- [最新正式发行页](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)。
- 固定更新源：https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json
- API连接与备份：资料库 → 应用管理。
- 图片生成与识别：聊天设置 → 图片前端；生图需配置可用服务，入口通过不等于真实出图验收。
- 安全预览保留静态结构并隔离原卡脚本，完整交互仍需对应兼容模式和扩展。

更新器核对大小、SHA256、包名、版本和证书，再交给Android确认安装。请先保存聊天与草稿。

## 历史版本

[1.5.19：设置搜索与行距](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.19) · [1.5.18：界面重组](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.18) · [1.5.17：运行环境与记忆缓存](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.17) · [1.5.16：暖白布局](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.16) · [1.5.15：HTML增量检查](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.15) · [1.5.14：阅读与分类设置](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.14)

历史实测只代表对应日期和环境。应用不附带AI账号、API密钥、私人卡片、聊天或生图服务。SillyTavern及预装扩展保留各自许可证；APK运行资产包含对应源码和许可。
