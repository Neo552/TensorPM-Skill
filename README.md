# TensorPM Skill — Claude Code Plugin Marketplace

Official Claude Code plugin marketplace for [TensorPM](https://tensorpm.com): **Agentic Project Memory and AI project management software** for Claude Code, Codex, OpenClaw, and any MCP/A2A agent.

This is the **canonical** marketplace home. Files are also mirrored to [`Neo552/TensorPM-Releases`](https://github.com/Neo552/TensorPM-Releases) for backward compatibility with bots and agents that already discover TensorPM there.

## Install

In Claude Code:

```
/plugin marketplace add Neo552/TensorPM-Skill
/plugin install tensorpm@tensorpm-marketplace
```

## Requirements

- TensorPM desktop app **v0.8.0+** running locally
- Platforms: macOS, Windows, Linux

Install TensorPM:

```bash
# macOS
brew install --cask neo552/tensorpm/tensorpm

# Windows
winget install --id Neo552.TensorPM
```

See [tensorpm.com](https://tensorpm.com) for details.

## What's Inside

- **MCP tools** — typed CRUD on projects, action items, workspaces, AI keys
- **A2A protocol** — local agent endpoint at `http://localhost:37850` for conversational, context-aware planning
- **External MCP server config** — agents can wire external MCP servers into TensorPM's AI chat
- **Skill docs** — routing rules between MCP and A2A, action-item schema, dependency types

## Repo Layout

```
.claude-plugin/marketplace.json          # Marketplace catalog (tensorpm-marketplace)
plugins/tensorpm/
├── .claude-plugin/plugin.json           # Plugin manifest (tensorpm)
└── skills/tensorpm/
    └── SKILL.md                         # Skill entry (tensorpm-agentic-pm)

# Raw markdown for direct fetching (mirrored on tensorpm.com):
SKILL.md
MCP-TOOLS.md
A2A-API.md
ACTION-ITEMS.md
```

## Versioning

The marketplace and plugin versions track the minimum-supported TensorPM desktop app version. The skill ships independently of every app build — only when its docs or MCP/A2A surface change.

`compatibility.minTensorPMVersion` in `plugin.json` is the source of truth.

## Source of Truth

The skill content is generated from the (private) TensorPM source repo on each release. This repo and `TensorPM-Releases` are downstream mirrors — do not edit files here directly; edit upstream.

## Links

- TensorPM: <https://tensorpm.com>
- Skill docs (web): <https://tensorpm.com/SKILL.md>
- Desktop releases: <https://github.com/Neo552/TensorPM-Releases>
