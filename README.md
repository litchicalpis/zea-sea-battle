# Zea Sea Battle

FVTT v12 开发测试模组，当前 **0.1.0-dev.12**，Core 0.3.10 / Schema 2.9.0 / 规则数据 1.2.0，目标 PF1 11.11。44 项规则特性不变，本次集中修正存档、裁决结构及输入体验。

## 安装与入口

Setup → Add-on Modules → Install Module → Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/zea-sea-battle/main/module.json
```

完整安装包、摘要与升级说明：[v0.1.0-dev.12 Pre-release](https://github.com/litchicalpis/zea-sea-battle/releases/tag/v0.1.0-dev.12)。已安装时在 Setup 检查更新；先备份 World，关闭旧客户端，安装后全部 GM 和玩家一起刷新。不要使用 Create Module 空壳或 GitHub 自动 Source code ZIP。

默认自动打开棋盘，也可使用左侧 Token 工具栏锚形按钮、设置菜单或 `Shift+Z`。HTTP 和 HTTPS 均支持，不依赖原生 UUID 或 `crypto.subtle`，不需要额外服务。

## 本版修改

- 固定同一 GM 自动载入，不再申请／接管、选举或写周期租约；保留窗口令牌，刷新后旧窗口拒写。
- GM 默认只看 P2 本方地图、单位与私报；完整 Authority 地图默认折叠，手动展开才生成，且只读。
- P1 玩家与 GM/P2 各自部署本方，包括本方自动部署；Authority 只负责验证、串行保存及同步。
- 心跳不重绘输入框；保留数值中间态、中文输入法、复选框、恢复原因、响应选择和 JSON 草稿。
- Journal 完整信封改为 XChaCha20-Poly1305 密文；32 字节密钥仅保留 GM 浏览器，提供恢复密钥导出／导入、密文备份和显式旧明文迁移。

## 升级及恢复必读

首次写入前必须在管理区**下载恢复密钥并确认另行安全保存**。密钥不能发给玩家或上传 World／聊天；密钥和全部恢复副本都丢失后，密文无法恢复。更换浏览器、域名／端口或清理站点存储后须导入对应 World／GM 的原密钥。

旧明文战局不会自动覆盖：先备份 World 和旧存档，再保存恢复密钥并确认迁移。迁移不能收回玩家已收到的明文，也不删除历史服务器备份。只迁移当前兼容 Core／Schema；旧版本回滚须恢复匹配的旧包与旧 World。协议升级为 2，禁止混用旧客户端。

## 验证范围

373 项自动测试、52 文件打包和 40 浏览器模块检查通过。真实 FVTT 12.343 匿名 ApplicationV2 窗口通过数字、中文组合、映射勾选和跨状态更新输入复测，使用纯虚构内存 Runtime；没有登录或改动现有 World，**不等于真实 Journal／Socket 或正式保密验收**。服务器未自动升级。

仍限独立测试 World 和虚构数据，保留测试写入确认。即使玩家可读取 Journal 原始 flags，本版应仅暴露密文及允许元数据；实际安装后须重新检查创建、更新和刷新。HTTP 不抵御恶意网络脚本替换，Socket 未签名；共享 GM 浏览器、恶意模组或 XSS 可读密钥。窗口令牌不是服务端原子锁，不支持恶意多 GM 并发安全保证。

默认分支只托管 README 和更新清单；完整客户端、规则、说明及第三方 LICENSE／来源位于安装 ZIP。旧 Release 附件保留，本次不修改贸易地图。
