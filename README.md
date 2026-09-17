# Zea Sea Battle

FVTT v12 / PF1 11.11 开发测试模组，当前 **0.1.0-dev.13**。Core 0.3.11 / Schema 2.10.0 / 规则数据 1.2.1，保留 44 项规则特性。

## 安装与入口

Setup → Add-on Modules → Install Module → Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/zea-sea-battle/main/module.json
```

完整安装包及摘要见 [v0.1.0-dev.13 Pre-release](https://github.com/litchicalpis/zea-sea-battle/releases/tag/v0.1.0-dev.13)。不要使用 Create Module 空壳或 GitHub 自动 Source code ZIP。默认分支仅托管 README 和清单，完整代码、规则、说明及第三方 LICENSE 在 Release ZIP；旧 Release 保留。

默认自动打开棋盘，也可从左侧 Token 工具栏锚形按钮、设置菜单或 `Shift+Z` 进入。HTTP／HTTPS 均支持，不需要额外裁决服务器。

## 本版修改

- 黑色逐日者发射 PC 后，每个新轮次开始时未满回收 1 位，以开局人数为容量；额外行动、挂起恢复和重载不重复回收。
- 本方界面显示在船 PC／开局容量，回收事件仅本方可见。PC 为零仍不能移动，回收后按人数重新判断移动与探照灯资格。
- 初始武装小艇基础航速 4、主炮 1、鱼雷 1，主炮与鱼雷分别计次。
- 自动裁决反馈统一写作「系统返回」，信息可见范围不变。主持方兼任 P2 与技术 Authority，不另设独立裁判玩家。

## 升级与恢复

**dev.13 不能直接续玩旧 Core／Schema 战局。** 先用旧包结束／归档并备份 World，再更新全部客户端、重新加载并新建测试局。需要继续旧局时保留匹配旧包；不要手改存档版本号。回滚同时恢复旧包和匹配 World 备份。

保留固定 Authority、双方独立部署、P2 默认投影与懒加载只读全图、输入草稿／中文组合保留。Journal 完整信封使用 XChaCha20-Poly1305，32 字节密钥仅在主持方的 GM 浏览器；首次写入前必须下载恢复密钥并确认安全保存。

密钥不可发给其他玩家或上传 World；密钥及全部恢复副本丢失后无法解密。换浏览器／来源或清理站点存储后须导入匹配密钥。旧明文只显式迁移，不迁移不兼容 Core／Schema。

管理区「初始化海战并清除所有对局」仍仅限当前 Authority，确认后删除海战 Journal、快照、日志及请求记录。**初始化不可撤销，升级不要求初始化；务必先备份。** 电脑已下载文件不受影响，两模组分别管理各自数据。

## 验证边界

381 项本地回归、数据检查、52 文件打包和 40 个浏览器模块装载通过；P1 界面在独立虚构局渲染验证。上述不等于真实 Journal／Socket 或正式安全验收，请在独立测试 World 复验。

仅限虚构数据和封闭可信测试会话。HTTP 不抵御恶意网络脚本替换，Socket 未签名，共享 GM 浏览器／恶意模组／XSS 可读密钥；窗口令牌不是服务端原子锁。发布不会自动更新 Foundry 服务器或改动现有 World。
