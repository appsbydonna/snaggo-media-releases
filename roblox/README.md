# San Diego Roleplay – Claude / Codex / ChatGPT collaboration

Place: https://www.roblox.com/games/136020512003847/San-Diego-Roleplay

## Layout
- `default.project.json` – Rojo project (`src/` syncs into Studio)
- `.mcp.json` – Claude Code MCP config; `.codex/config.toml` – Codex MCP config
- `docs/research.md` (Codex), `docs/design.md` (shared), `docs/handoff.md` (all agents log here)

## Setup (on your computer)
1. Install Roblox's Studio MCP server (github.com/Roblox/studio-rust-mcp-server) and its Studio plugin; review the source first.
2. Replace `REPLACE_WITH_PATH_TO/rbx-studio-mcp` in `.mcp.json` and `.codex/config.toml`.
   Codex reads `~/.codex/config.toml` or a project `.codex/config.toml` in trusted projects.
3. Install Rojo (`rojo serve`) and connect via the Studio Rojo plugin.
4. Open the place in Studio, then start Claude Code / Codex in this folder.

## Rules
- MCP gives agents hands in Studio; the repo is the shared memory. Log every change in `docs/handoff.md`.
- Edit code in `src/` (Rojo), not directly in Studio, to avoid conflicts.
- ChatGPT: no local MCP; use for research/design and paste results into `docs/`.
