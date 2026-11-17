# 微信读书 for Kindle

Isword 开发的 Kindle 第三方微信读书客户端。此仓库为 `v0.3.10` 版安装包提供下载和使用说明。

## 下载

在仓库的 **Releases → v0.3.10 → Assets** 下载 `Isword-weread-0.3.10-install.zip`（约 44.9 MiB）。版本改动见[更新日志](CHANGELOG.md)。

在 macOS 上，将安装包与 [SHA256SUMS.txt](SHA256SUMS.txt) 保存到同一目录后，可在该目录运行以下命令校验文件。

```sh
shasum -a 256 -c SHA256SUMS.txt
```

## 安装

设备须为已越狱的 Kindle，并已安装 KUAL 或 SH_Integration／Scriptlets 文档启动器。

1. 解压安装包，将 `weread`、`documents`、`extensions`、`fonts` 四个目录合并复制到 Kindle USB 根目录。完整复制 `fonts`，保留 `noto` 子目录和随附的 `.LICENSE` 文件。
2. 安全弹出 Kindle 并断开 USB。从文档列表或 KUAL 打开「微信读书」。
3. 联网后用微信扫描登录二维码，并在手机上确认。

## 从旧版本升级

1. 先用旧版联网同步待上报的阅读时长和笔记，然后正常退出。保留旧版安装包，并备份个人阅读数据和自定义字体。
2. 按安装步骤覆盖文件，完整复制 `fonts` 目录，保留原账号目录、书籍缓存和自定义字体。
3. **升级后必须重新登录。** 打开新版，联网进入「我的 → 设置 → 退出登录」，再扫码登录。如果已显示二维码，可直接扫码。

安全模式默认开启，此模式下整本下载按钮不可用。阅读时长账本和队列格式已更新。若需回退，请使用旧版和对应的数据备份。

## 问题反馈

通过「微信读书兼容性检查」文档，或 **KUAL → 微信读书 → 生成兼容报告（只读）**，获取 `documents/微信读书兼容性报告.txt`。反馈时请注明 Kindle 型号、固件版本、应用版本、故障时间和复现步骤，并附上 `weread/launch.log` 及故障对应的 `weread/runs/<会话目录>/app.log` 和 `session.log`（如有）。提交前请移除登录凭据、Cookie、令牌及书籍或笔记正文。

## 署名

客户端作者为 **Isword**。随附的 Noto 字体许可位于安装包的 `fonts/noto/` 目录。
