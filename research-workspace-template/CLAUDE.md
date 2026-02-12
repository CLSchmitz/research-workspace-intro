# Agent Instructions

You are working in a research workspace. This folder contains writing projects, reference data, and planning documents. Notes and reference management are handled via MCP tools.

When performing a task, find the minimal amount of context necessary. Read only the spec relevant to the current task. Avoid reading large files or searching broadly when a targeted read will do.

After every task, update PROJECTS.md if the task changed a project's status, details, or deliverables.

## Key Rules

- **Never overwrite** files under `zotero/exports/`. These are read-only reference copies from Zotero.
- **Never fabricate citations.** Every citekey must be verified in Zotero (via MCP or the export files).
- **Obsidian edits** are done exclusively through MCP tools. Do not create Obsidian note files in this workspace.
- **Zotero edits** (tags, collections, notes) are done exclusively through MCP tools.

## Specs

| Spec | Covers |
|------|--------|
| [LATEX_SPEC.md](LATEX_SPEC.md) | Building, git/Overleaf sync, writing conventions, citation workflow |
| [OBSIDIAN_SPEC.md](OBSIDIAN_SPEC.md) | Vault structure, note classification, frontmatter, project tags |
| [PROJECTS_SPEC.md](PROJECTS_SPEC.md) | Project entry format for PROJECTS.md |

## Workspace Layout

- `projects/` — Writing projects (e.g., LaTeX papers), each potentially its own git repo
- `zotero/exports/` — Read-only Zotero library exports (.bib, .json) for reference
- `implementation/` — Custom scripts and services
- Root `.md` files — Planning docs and specs
