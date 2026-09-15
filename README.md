# Zea Sea Battle

FVTT v12 开发测试模组，当前 **0.1.0-dev.11**，内嵌 Core 0.3.10 / Schema 2.9.0，目标 PF1 11.11。

## 界面安装

Setup → Add-on Modules → Install Module → Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/zea-sea-battle/main/module.json
```

完整安装包、校验表及升级说明见 [v0.1.0-dev.11 Pre-release](https://github.com/litchicalpis/zea-sea-battle/releases/tag/v0.1.0-dev.11)。不要使用 Create Module 空壳或 GitHub 自动生成的 Source code ZIP。

HTTP 和 HTTPS 均支持，不再依赖原生 UUID／subtle。第十／十一批完成，44 项特性全部编译；献猎、猎获防护、旧潮、Thunder Child、冰崖眩晕、白鲸强制行动接入内核、界面和恢复。规则口径与操作说明随完整 ZIP 提供。

348 项自动测试、44 文件／34 浏览器模块检查通过；双包真实非 loopback HTTP 的 45 项同页浏览器检查通过，但 Foundry API 为模拟对象。**真实 FVTT 权限、多 GM、服务器重启、共同启用仍待验收。**

仅限虚构数据与可信封闭会话，仍须 GM 确认测试写入。存档明文、消息未签名，不承诺原始 Journal 保密或抗篡改。旧局不自动迁移；先旧包归档、备份 World，再升级新建，回滚使用匹配旧包和旧 World。

本仓库默认分支只托管发布 README 和更新清单；客户端代码、规则数据与必要资源在完整安装 ZIP 中。旧 Release 附件保留，不因更新覆盖。本渠道是开发测试 Pre-release，不是生产验收声明。
