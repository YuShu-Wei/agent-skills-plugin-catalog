# v1.0.0 — AI Skills & Plugin Catalog

## English

The first release of plugin-catalog: a Codex skill that records what installed AI agent skills and plugins do in one Markdown file.

- Purpose, practical use case, source, local path or plugin ID, status, and dates.
- Updates existing entries while preserving user notes and first recorded dates.
- Separate English and Simplified Chinese documentation and real catalog examples.
- MIT license and feedback templates.

Install `skills/plugin-catalog` in your Codex skills directory, then invoke `$plugin-catalog`. The default catalog is `~/plugins.md`; choose a different path when needed.

This is an agent instruction workflow, not an installation hook or background monitor. Other compatible agents have not been tested.

## 简体中文

plugin-catalog 首个版本：一个 Codex skill，将 AI skills（技能）与插件用途记录到同一份 Markdown 文件。

- 记录用途、使用场景、来源、本地路径或插件 ID、状态和日期。
- 更新已有条目，保留备注和首次记录日期。
- 独立的英文、简体中文使用说明与真实记录示例。
- MIT 许可证与反馈模板。

将 `skills/plugin-catalog` 安装到 Codex skills 目录，再使用 `$plugin-catalog`。默认清单为 `~/plugins.md`，可按需指定其他位置。

它是一套 agent 工作指令，不是安装钩子或后台监听器；其他兼容 agent 尚未测试。
