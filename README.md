# 掌中酒馆 APK 更新

## 最新正式版：1.5.22

[下载1.5.22完整ARM64 APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.22/pocket-tavern-1.5.22-arm64.apk) · [正式发行说明](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.22)

版本代码28，192058554字节。SHA256：95c27360a16272d0d54954a5d0f37ca29b2f13fe92d715e47852e66151ad9332。

- 通知拒绝后不反复自动询问；权限或存储异常不阻断本地服务启动。
- 常规完整静态卡片保留流式浏览状态，前后正文同步字号、行距和排版；动态卡、自定义嵌套与普通代码复制控件保留原兼容路径。
- 多卡片刷新减少重复扫描：500卡片/1000消息负载中，全局Map访问500500→500，保留断开节点清理。

22组发布检查、518项单元0跳过、4项导出、1178项原生断言、75项包内生产文件核对通过；最终Android15 x86_64同业务包完成22项检查。正式1.5.21直接升级保留原资料，实际卡片HTTP流式24段保持上下文，等待可停止并恢复发送，全新安装拒绝通知及冷启动通过。2026-11-02使用原BUZZ连接gemini-3.8-flash完成4次真实聊天，均HTTP200、有可见正文且发送状态恢复。

ARM64真机、长期运行与真实图片生成未验收；真实服务结果仅代表当次测试。沿用1.5.8至1.5.21签名，可直接覆盖同签名版本保留资料。

应用内固定更新清单：[update.json](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json)。安装包与更新JSON均使用固定SHA256和字节数；发布后需重新下载完整APK校验。

完整对应源码、签名历史及详细验收资料保存在私有开发仓库，不把GitHub自动Source code ZIP当作完整源码。保留各开源组件许可证。

---

以下为1.5.21及更早版本的历史说明，按当时版本理解：

## 历史资料：1.5.21

本仓库提供 Android ARM64 安装包、更新清单与校验说明。开发源码、签名备份和详细验收资料保存在私有开发仓库。

### 历史正式版：1.5.21

[下载1.5.21完整APK](https://github.com/ruoruo43/pocket-tavern-updates/releases/download/v1.5.21/pocket-tavern-1.5.21-arm64.apk) · [发行说明与校验](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.21)

本版将聊天、资料库、连接、设置整理为四个固定一级入口。资料库集中管理角色卡、世界书和聊天记录；连接独立管理 API；存储与备份归入设置。设置按用途分组，应用更新和扩展管理可从设置直接进入。

统一系统返回与页面父级，保留资料库查询和阅读位置、聊天草稿及未保存连接。同一管理页切换不堆积历史；未保存连接跨页前保留确认；聊天恢复失败时保护设置深链。沿用1.5.20中转错误正文截止、资源释放和长聊天优化，核心、扩展、依赖与签名保持原已验证版本。

21组回归、518项单元（0跳过）、4项导出、1161项原生断言、23项Android15 x86_64安装验收及75个APK生产文件核对通过。模拟器完成同签名1.5.20覆盖升级和冷启动，原聊天、角色、世界书、笔记及显示偏好保留；本地模拟中转的流式及非流式聊天均有正文。安全卡片、名字旁问号处理、图片入口均检查通过。

2026-11-02补充真实服务验收：使用原BUZZ地址 https://api.buzzgw.com/v1 与gemini-3.8-flash，连续两次流式、一次非流式、冷启动后流式共四次实际聊天均有可见正文，约3.97–4.71秒，生成结束且无前端错误，冷启动无需重填密钥。非流式原回复包含换行，按原文保留；未发现应用端无输出故障，未修改安装包。此结果仅代表本次环境和时间；ARM64真机、长期运行及真实生图仍待验收。

Android8.0+ / ARM64，versionCode27。沿用1.5.8–1.5.20签名，可保留资料覆盖安装。旧1.5.6/1.5.7按[迁移说明](MIGRATION-1.5.8.md)备份迁移。

APK：192054458字节。SHA256：e0e8a3e5cc79f9f8c24165d1a0d22dec9a67c31edd1ef099c4ff65e028c540e9

## 更新与功能入口

- 底部四入口：聊天 / 资料库 / 连接 / 设置。
- 应用更新：设置 → 应用更新。
- 扩展管理：设置 → 扩展管理。
- 存储与备份：设置 → 存储与备份。
- 图片生成与识别：聊天设置 → 图片前端；生图需要可用服务配置。
- [最新正式发行页](https://github.com/ruoruo43/pocket-tavern-updates/releases/latest)。
- 固定更新源：https://github.com/ruoruo43/pocket-tavern-updates/releases/latest/download/update.json

更新器核对大小、SHA256、包名、版本和证书，再交给Android确认安装。请先保存聊天与草稿。安全预览保留静态结构并隔离原卡脚本；复杂交互取决于对应兼容模式和扩展。

## 历史版本

[1.5.20：中转与长聊天稳定性](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.20) · [1.5.19：设置搜索与行距](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.19) · [1.5.18：界面重组](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.18) · [1.5.17：运行环境与记忆缓存](https://github.com/ruoruo43/pocket-tavern-updates/releases/tag/v1.5.17)

应用不附带AI账号、API密钥、私人卡片、聊天或生图服务。SillyTavern及预装扩展保留各自许可证，APK运行资产包含对应源码和许可。
