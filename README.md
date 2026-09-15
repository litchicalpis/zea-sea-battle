# Zea Sea Battle

《渡海入林》海战棋的 Foundry VTT v12 开发测试模块发布仓库。

当前预发布：**0.1.0-dev.9**；Core **0.3.8** / Schema **2.7.0**。第九批包括群落增殖、最后的波纹、Resurgam、残骸拼修和桑当湾亡雾。300 项本地自动测试通过。

## 纯界面安装

Foundry Setup → Add-on Modules → Install Module → Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/zea-sea-battle/main/module.json
```

安装后，在独立测试 World 的“管理模组”启用。目标为 FVTT v12 + PF1 11.11；GM 仍须明确启用虚构数据测试模式。

本仓库仅存放安装入口与说明；完整模块代码、规则数据和详细手册在 [Release 安装包](https://github.com/litchicalpis/zea-sea-battle/releases/tag/v0.1.0-dev.9) 中。不要下载 GitHub 自动生成的 Source code ZIP 作为模组安装包。

`main/module.json` 是开发测试更新渠道，固定版本清单也随 Release 提供。Pre-release 不依赖 `releases/latest` 路由；更新前先检查说明，不建议开启无人值守升级。

## 测试与升级边界

- 仅限虚构、可公开的数据测试；真实 FVTT 权限隔离、服务器重启和多客户端验收尚未完成。
- Core 0.3.8 / Schema 2.7.0 不自动迁移 0.3.0–0.3.7 旧局。升级前结束或归档旧局、备份 World，新版本新建测试局。
- 不发布真实 World、战局日志、密钥、浏览器资料或工作区其他项目。
- 服务器必须能匿名访问 GitHub、raw.githubusercontent.com 及 Release 下载域名；浏览器能打开不等于服务器网络可达。
- 本项目没有额外授予既有规则或素材的再分发许可。
