# AI skills（技能）与插件用途清单

[简体中文](README.zh-CN.md) | [English](README.md)

安装了很多 AI skills 和插件，却忘了它们有什么用？这个 skill 帮你把用途、使用场景、来源和安装状态记录到同一个 Markdown 文件。

主要用于 Codex，帮助维护已安装的技能与插件清单。其他支持 SKILL.md 的 agent 尚未测试。

## 功能

- 记录已确认的下载、安装、更新和卸载结果。
- 说明每个项目的用途和典型使用场景。
- 更新已有条目，避免重复，保留备注和首次记录日期。
- 不将密码或 token 写入清单。

它是一套 agent 工作指令，不是后台监听器。当 skill 可用并被选用时，它记录对话中的安装操作；在其他地方安装的项目需要让 agent 补录。

## 安装

下载或克隆本仓库，将 `skills/plugin-catalog` 文件夹复制到 Codex 的 skills 目录，通常为 `~/.codex/skills/`。设置了自定义 `CODEX_HOME` 时，使用该目录下的 `skills` 文件夹。

在仓库根目录执行，Windows PowerShell：

```powershell
Copy-Item -LiteralPath .\skills\plugin-catalog -Destination "$env:USERPROFILE\.codex\skills\plugin-catalog" -Recurse
```

macOS / Linux：

```bash
mkdir -p ~/.codex/skills
cp -R skills/plugin-catalog ~/.codex/skills/
```

以上命令假定目标尚不存在；已有安装请更新原目录，避免产生嵌套副本。安装后在 Codex 下一轮对话使用。

## 使用方法

```text
安装 find-skills，并使用 $plugin-catalog 把用途记录到 D:\Codex\plugins.md。
```

```text
使用 $plugin-catalog 将这些已安装的插件补录到我的清单。
```

默认清单路径为 `~/plugins.md`。首次使用时选择容易找到的路径，跨项目沿用。如果需要长期固定位置，可以让 agent 将绝对路径写入已安装的本地 SKILL.md。不要将个人电脑路径提交到公开仓库。

支持自动选择，但不能保证每次请求都触发。需要确保使用时，请明确写 `$plugin-catalog`。它配合安装流程记录结果，本身不负责安装插件。

## 真实示例

查看[记录文档示例](examples/plugins.zh-CN.md)：来自作者实际使用的清单，包含 `find-skills`、`setup-matt-pocock-skills` 和 `plugin-catalog`。个人路径已替换为通用示例。示例是记录快照，不代表读者已安装这些项目。

## 文件说明

- `skills/plugin-catalog/SKILL.md`：agent 指令
- `examples/plugins.zh-CN.md`：简体中文记录示例
- `examples/plugins.md`：英文记录示例
- `README.md`：英文使用说明

## 贡献

欢迎通过 Issues 和 PR 改进文档或清单流程。请勿在反馈中提交凭据或私人清单。

## 许可证

MIT。示例引用的第三方 skills 仍遵循各自许可证，本仓库不分发它们。
