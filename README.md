# Zea Sea Battle

FVTT v12 / PF1 11.11 开发测试模组，当前 **0.1.0-dev.12.2**。Core 0.3.10 / Schema 2.9.0 / 规则数据 1.2.0，44 项规则特性不变。

## 安装与入口

Setup → Add-on Modules → Install Module → Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/zea-sea-battle/main/module.json
```

完整安装包及摘要见 [v0.1.0-dev.12.2 Pre-release](https://github.com/litchicalpis/zea-sea-battle/releases/tag/v0.1.0-dev.12.2)。不要使用 Create Module 空壳或 GitHub 自动 Source code ZIP。默认分支仅托管 README 和清单，完整代码、规则、说明及第三方 LICENSE 在 Release ZIP；旧 Release 保留。

默认自动打开棋盘，也可从左侧 Token 工具栏锚形按钮、设置菜单或 `Shift+Z` 进入。HTTP／HTTPS 均支持，无需原生 UUID 或 subtle，不需要额外裁决服务器。

## 本版修改

- 商船统一正式名称「重装SS Sharknado」，旧存档载入后同步更新显示。
- 管理区新增「初始化海战并清除所有对局」，仅当前 Authority 会话可执行。确认后删除当前、归档和旧格式海战 Journal，清除快照、日志及请求记录，同步玩家回到未建局状态。
- 清理期间暂停队列并检查 Authority；完成后轮换会话，旧请求不能重新生成对局。保留 GM 密钥和玩家授权。
- 合并未单独发布的 dev.12.1：深色输入框、下拉选项、文本框及标题栏的文字和按钮对比度修复。

**初始化不可撤销。** 请先备份需要保留的资料；电脑已下载文件和服务器外部备份不受模组控制。此功能不更改地图模组状态，两模组分别初始化。

## 升级与恢复

保留固定 GM、双方独立部署、GM 默认 P2 投影及懒加载只读全图、输入草稿／中文组合保留。Journal 完整信封使用 XChaCha20-Poly1305，32 字节密钥仅在 GM 浏览器，首次写入前必须下载恢复密钥并确认安全保存。

密钥不可发给玩家或上传 World；密钥及全部恢复副本丢失后无法解密。换浏览器／来源或清理站点存储后，导入匹配 World／GM 的原密钥。旧明文不会自动覆盖，先备份再显式迁移；不迁移不兼容 Core／Schema。回滚同时恢复旧包和匹配 World。

## 验证边界

377 项自动测试、52 文件／40 浏览器模块及 67 项双包 HTTP 浏览器检查通过，初始化及多人接口使用模拟 Foundry API；不等于真实 Journal／Socket、初始化或正式安全验收。请在独立测试 World 交付 PC 复验。

仅限虚构数据和封闭可信测试会话。HTTP 不抵御恶意网络脚本替换，Socket 未签名，共享 GM 浏览器／恶意模组／XSS 可读密钥；窗口令牌不是服务端原子锁。升级前备份 World，结束旧客户端，全员更新刷新。发布不会自动更新 Foundry 服务器。
