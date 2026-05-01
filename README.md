# TensorPM Skill — Claude Code Plugin Marketplace

Official Claude Code plugin for [TensorPM](https://tensorpm.com), an AI-powered, context-driven project management desktop app.

This repo is a Claude Code **plugin marketplace** containing the `tensorpm-agentic-pm` skill. Once installed, agents (Claude Code, Codex, etc.) can manage TensorPM projects and action items via MCP tools or the A2A protocol exposed by the desktop app.

## Install

In Claude Code:

```
/plugin marketplace add Neo552/TensorPM-Skill
/plugin install tensorpm-agentic-pm@tensorpm
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

See [tensorpm.com/skill](https://tensorpm.com/skill) for full installation paths.

## What's Inside

- **MCP tools** — typed CRUD on projects, action items, workspaces, AI keys
- **A2A protocol** — local agent endpoint at `http://localhost:37850` for conversational, context-aware planning
- **Skill docs** — routing rules between MCP and A2A, action-item schema, dependency types

## Repo Layout

```
.claude-plugin/marketplace.json          # Marketplace catalog
plugins/tensorpm/
├── .claude-plugin/plugin.json           # Plugin metadata
└── skills/tensorpm/
    ├── SKILL.md                         # Main skill entry
    ├── MCP-TOOLS.md                     # MCP tool catalog
    ├── A2A-API.md                       # A2A endpoints, JSON-RPC, REST
    └── ACTION-ITEMS.md                  # Fields, dependencies, payloads
```

## Versioning

Skill version tracks the minimum-supported TensorPM desktop app version. Skill releases are decoupled from app releases — the skill ships when its docs / tool catalog change, not on every app build.

`compatibility.minTensorPMVersion` in `plugin.json` is the source of truth.

## Links

- TensorPM: <https://tensorpm.com>
- Desktop releases: <https://github.com/Neo552/TensorPM-Releases>
- Skill docs (web): <https://tensorpm.com/skill>
