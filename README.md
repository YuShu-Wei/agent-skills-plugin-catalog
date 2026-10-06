# AI Agent Skills & Plugin Catalog

[English](README.md) | [简体中文](README.zh-CN.md)

[Download](https://github.com/YuShu-Wei/agent-skills-plugin-catalog/archive/refs/heads/main.zip) · [Example](examples/plugins.md) · [Report an issue](https://github.com/YuShu-Wei/agent-skills-plugin-catalog/issues/new/choose) · [Releases](https://github.com/YuShu-Wei/agent-skills-plugin-catalog/releases)

Remember what your AI skills and plugins do. Record their purpose, use cases, sources, and installation status in one Markdown file.

A Codex skill for maintaining an installed skills and plugins inventory. Other SKILL.md-compatible hosts have not been tested.

## Features

- Document confirmed downloads, installs, updates, and removals.
- Explain purpose and a practical use case for each entry.
- Update existing entries without duplicates; preserve notes and first recorded dates.
- Keep passwords and tokens out of the catalog.

This is an agent instruction skill, not a background monitor. It documents work in conversations where the skill is available and selected. Installations performed elsewhere need a backfill request.

## Installation

Ask Codex: “Install the plugin-catalog skill from https://github.com/YuShu-Wei/agent-skills-plugin-catalog, path skills/plugin-catalog.” Or follow the manual steps below.

Download or clone this repository. Copy `skills/plugin-catalog` into your Codex skills directory, normally `~/.codex/skills/`. For a custom `CODEX_HOME`, use its `skills` directory.

From the repository root, Windows PowerShell:

```powershell
Copy-Item -LiteralPath .\skills\plugin-catalog -Destination "$env:USERPROFILE\.codex\skills\plugin-catalog" -Recurse
```

macOS / Linux:

```bash
mkdir -p ~/.codex/skills
cp -R skills/plugin-catalog ~/.codex/skills/
```

These commands assume the destination does not exist. Update an existing installation deliberately instead of nesting another copy. The skill will be available on the next turn in Codex.

## Usage

```text
Install find-skills and use $plugin-catalog to record its purpose in ~/plugins.md.
```

```text
Use $plugin-catalog to backfill these already installed plugins in my catalog.
```

The default catalog is `~/plugins.md`. Choose an easy-to-find path and reuse it across projects. For a persistent local default, ask the agent to record your preferred absolute path in the installed SKILL.md. Do not commit private machine paths to a public fork.

Automatic selection is supported, but not guaranteed. Invoke `$plugin-catalog` explicitly to ensure it is used. This skill documents installations; it does not replace an installer.

## Real example

See [the example catalog](examples/plugins.md), based on the creator's actual records for `find-skills`, `setup-matt-pocock-skills`, and `plugin-catalog`. Personal paths have been replaced with portable examples. This is a snapshot, not proof of installation on your machine.

## Files

- `skills/plugin-catalog/SKILL.md`: agent instructions
- `examples/plugins.md`: English example
- `examples/plugins.zh-CN.md`: Simplified Chinese example
- `README.zh-CN.md`: Simplified Chinese documentation

## Contributing

Issues and pull requests are welcome. See [the contribution guide](CONTRIBUTING.md). Do not include credentials or private catalogs in reports.

## License

MIT. Third-party skills referenced in the example retain their own licenses; this repository does not redistribute them.
