# Obsidian Notes Specification

## Vault Structure

Customize this to match your Obsidian vault layout. Example:

```
vault/
├── projects/           # Project-specific notes
│   └── {tag}/          # One folder per project
├── input/              # Things you've consumed
│   ├── papers/         # Paper notes
│   ├── books/          # Book notes
│   ├── talks/          # Talk/lecture notes
│   └── conferences/    # Conference notes
├── output/             # Things you're producing
│   ├── papers/         # Draft papers
│   ├── posts/          # Blog posts
│   └── reviews/        # Peer reviews
├── admin/              # Administrative notes
│   └── meetings/       # Meeting notes
└── ideas/              # Idea sketches
```

## Note Classification

When creating or moving a note, use this decision tree:

```
Is the note about a specific project?
├─ YES → projects/{tag}/
└─ NO →
    ├─ Paper/book/talk I consumed → input/
    ├─ Something I'm writing → output/
    ├─ Meeting or admin → admin/
    └─ Idea sketch → ideas/
```

## Frontmatter Template

Every note should have frontmatter:

```yaml
---
note-type: paper-notes    # or: meeting-notes, idea, draft-paper, etc.
projects: [project-tag]   # array of relevant project tags (can be empty [])
date: 2026-01-15          # YYYY-MM-DD
---
```

## Tool Usage

- **Prefer** `update_frontmatter` + `move_note` + `patch_note` (lightweight operations)
- **Avoid** `write_note` except when creating new notes from scratch
- Obsidian vault is separate from this workspace — all edits go through MCP tools only
