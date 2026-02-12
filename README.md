# AI-Assisted Research Workflows with Claude Code & MCP

Materials for Chris Schmitz's workshop on setting up an AI-assisted academic research workspace using Claude Code and MCP (Model Context Protocol).

## What's Here

| Path | Description |
|------|-------------|
| [`talk-outline.md`](talk-outline.md) | Full talk outline with speaker notes |
| [`presentation/`](presentation/) | LaTeX Beamer slides |
| [`research-workspace-template/`](research-workspace-template/) | Ready-to-use workspace template (copy this to get started) |

## The Template

The [`research-workspace-template/`](research-workspace-template/) folder is a self-contained starter workspace. It includes:

- `CLAUDE.md` — agent instructions (edit to match your workflow)
- `.mcp.json` — MCP server configuration (replace placeholders with your paths and credentials)
- Spec files (`LATEX_SPEC.md`, `OBSIDIAN_SPEC.md`, `PROJECTS_SPEC.md`) — domain conventions the agent follows
- `PROJECTS.md` — project registry
- Folder structure: `projects/`, `zotero/exports/`, `implementation/`

**To use it:** Copy `research-workspace-template/` to wherever you want your workspace, open it in VS Code, and follow the Quick Start below.

## Quick Start

1. **Copy the template folder** to your machine and rename it (e.g., `research/`).
2. **Open it in VS Code.**
3. **Edit `.mcp.json`** — replace the placeholder paths and credentials with your own.
4. **Edit `CLAUDE.md`** — customize the agent instructions for your workflow.
5. **Edit the spec files** (`LATEX_SPEC.md`, `OBSIDIAN_SPEC.md`, etc.) to match your conventions, or delete the ones you don't need.
6. **Open Claude Code** in VS Code and start working.

## Prerequisites

### Required
- [VS Code](https://code.visualstudio.com/)
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) VS Code extension (requires Anthropic API key)

### For Obsidian MCP
- [Node.js](https://nodejs.org/) (LTS, includes npm/npx)
- [Obsidian](https://obsidian.md/) with a vault folder

### For Zotero MCP
- [Python 3.10+](https://www.python.org/downloads/)
- [uv](https://docs.astral.sh/uv/getting-started/installation/) (Python package manager)
- [Zotero](https://www.zotero.org/download/) with an account
- [Zotero API key](https://www.zotero.org/settings/keys)

### For Google Docs MCP
- [Node.js](https://nodejs.org/)
- A [Google Cloud](https://console.cloud.google.com/) project with Docs & Drive APIs enabled and OAuth 2.0 credentials
- See [google-docs-mcp setup](https://github.com/a-bonus/google-docs-mcp) for detailed OAuth instructions

### For LaTeX / Overleaf
- [TeX Live](https://tug.org/texlive/) or [MiKTeX](https://miktex.org/)
- [Git](https://git-scm.com/) (for Overleaf sync via GitHub)

## Architecture

- **`CLAUDE.md`** is loaded automatically by Claude Code on every conversation. Keep it short: high-level rules, pointers to specs.
- **Spec files** contain domain-specific detail. The agent reads them only when needed, keeping context minimal and focused.
- **`.mcp.json`** configures which external tools the agent can access. Add or remove servers as needed.
- **Obsidian** is accessed exclusively through its MCP server — the vault lives outside this workspace.
- **Zotero** is canonical for references. The exports in `zotero/exports/` are informational read-only copies.
- **LaTeX projects** are each their own git repo, synced to GitHub and optionally to Overleaf.

## Customization

This template reflects one particular workflow (academic research with LaTeX, Zotero, Obsidian, and Google Docs). Adapt it freely:

- **Don't use Obsidian?** Delete `OBSIDIAN_SPEC.md` and remove the obsidian entry from `.mcp.json`. Consider a Notion MCP server instead.
- **Don't use LaTeX?** Delete `LATEX_SPEC.md` and maybe even the `projects/` folder.
- **Don't use Google Docs?** Remove the entry from `.mcp.json`.
- **Use other tools?** Add their MCP servers to `.mcp.json` and write a spec for your conventions. The pattern is always the same: install server → configure in `.mcp.json` → write a spec → iterate.

## Key Links

| Resource | URL |
|----------|-----|
| Claude Code | https://docs.anthropic.com/en/docs/claude-code |
| MCP Specification | https://modelcontextprotocol.io |
| Obsidian MCP | https://github.com/bitbonsai/mcp-obsidian |
| Zotero MCP | https://github.com/54yyyu/zotero-mcp |
| Google Docs MCP | https://github.com/a-bonus/google-docs-mcp |
