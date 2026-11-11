# dsh-media-desk

DeepSeek Harness 自媒体工作台插件的公开安装包。源码开发仓库保持私有；这里仅提供安装说明和预构建 Release 附件，无需 GitHub 登录、Token 或激活码。

## 安装 / 更新

桌面用户先打开 Harness 一次完成初始化，再完全退出应用后执行：

```sh
dsh plugin --profile desktop add https://github.com/alphane-ai/dsh-media-desk-releases/releases/download/v2.6.9/dsh-media-desk-2.6.9.tgz
```

安装后重新打开 Harness。Web 用户将 `desktop` 改成 `web`。需 DeepSeek Harness `>=0.2.1-rc.5 <0.3.0`，使用与当前 Harness 配套的 CLI。

macOS 未配置 `dsh` 命令时：

```sh
"/Applications/DeepSeek Harness.app/Contents/Resources/runtime/cli/bin/dsh" plugin --profile desktop add https://github.com/alphane-ai/dsh-media-desk-releases/releases/download/v2.6.9/dsh-media-desk-2.6.9.tgz
```

也支持转发安装包后从本地安装：

```sh
dsh plugin --profile desktop add /absolute/path/dsh-media-desk-2.6.9.tgz
```

## 卸载

```sh
dsh plugin --profile desktop remove dsh-media-desk
```

保留已有稿件和账号数据，不执行全量数据清除。安装、更新、卸载时请先退出 Harness，完成后重新打开。

## 内容与说明

包含 Codex 本机认证绘图、Catbus 多账号连接与采集、内容详情保存、账号风格提炼和 MemeWiki 成稿工具。相关服务按需单独安装，使用每位用户自己的账号与额度；不携带发布者凭证。Codex 图片模型跟随其默认配置，不能固定 GPT Image 2.6。

从 [Releases](https://github.com/alphane-ai/dsh-media-desk-releases/releases) 下载 `.tgz` 附件，不要使用自动生成的 Source code 归档。安装包包含可读的运行时 JavaScript 和上游 MIT 许可证，不含私有仓库 Git 历史。

基于 [woniuniuniu/dsh-media-desk](https://github.com/woniuniuniu/dsh-media-desk) 扩展。遵循 [DSH 官方插件安装方式](https://github.com/deepseek-ai/deepseek-harness/blob/master/docs/user/develop/basic/publish.md)。
