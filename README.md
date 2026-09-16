# Zea Sea Battle

FVTT v12 开发测试模组，当前 **0.1.0-dev.11.1**，内嵌 Core 0.3.10 / Schema 2.9.0，目标 PF1 11.11。

## 安装与入口

Setup → Add-on Modules → Install Module → Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/zea-sea-battle/main/module.json
```

完整安装包、校验表及升级说明见 [v0.1.0-dev.11.1 Pre-release](https://github.com/litchicalpis/zea-sea-battle/releases/tag/v0.1.0-dev.11.1)。已安装时在 Setup 检查更新；备份 World，安装后全部 GM 和玩家一起刷新。不要使用 Create Module 空壳或 GitHub 自动生成的 Source code ZIP。

启用模组后默认自动打开棋盘；也可使用**左侧 Token 工具栏锚形按钮**、“游戏设置 → 配置设置 → 模组设置”入口或 `Shift+Z`。dev.11.1 修复翻译路径及中文回退、Foundry v12 平台类注入、重启后 Authority 租约时间基准及 GM 创建者 ownership 兼容。

普通 HTTP 和 HTTPS 均支持，不依赖原生 UUID 或 `crypto.subtle`。44 项特性已编译；本补丁不改变规则、Core 或 Schema。

## 测试状态

349 项自动测试、44 文件打包和 34 浏览器模块检查通过。2026-09-16 在真实 FVTT 12.343 / PF1 11.11、HTTP、GM 与普通玩家隔离浏览器中完成首轮联调；修复通过客户端响应覆盖验证，完成虚构建局、保存与 P1 同步，未替换服务器模块。

**未通过完整状态读取隔离：普通玩家仍可读取 Journal canonical flags，刷新后也可读取。** 发现后停止后续战局验收；本补丁不解决该问题，不宣称敌方状态、RNG 或私报保密。攻击、终局导出、恢复和双 GM 故障测试尚未完成。只允许专用测试 World 和可公开虚构数据，禁止正式战局秘密，仍须 GM 明确确认测试写入。

存档明文、消息未签名，不能抵御恶意客户端。dev.11 与本补丁 Core / Schema 相同；跨 Schema 旧局不自动迁移。回滚须使用匹配的旧包和 World 备份。发布不会自动更新任何 Foundry 服务器。

默认分支只托管 README 和更新清单；客户端代码、规则数据与必要资源位于完整安装 ZIP。旧 Release 附件保留，不覆盖。本渠道为开发测试 Pre-release，不是生产验收声明。
