# Projects Specification

This document defines the structure for entries in `PROJECTS.md`.

## Project Entry Structure

Each project in `PROJECTS.md` must contain the following fields:

| Field | Required | Description |
|-------|----------|-------------|
| `title` | Yes | Full project title |
| `tag` | Yes | Short, kebab-case identifier for linking notes (e.g., `my-paper`) |
| `status` | Yes | One of: `active`, `under-review`, `completed`, `paused` |
| `coauthors` | No | List of collaborators |
| `venue` | No | Target publication venue or context |
| `description` | Yes | 1-3 sentence summary of the project |
| `notes` | No | Additional context, next steps, or links |

### Example Entry

```markdown
## My Paper Title
- **tag:** my-paper
- **status:** active
- **coauthors:** Jane Doe, John Smith
- **venue:** NeurIPS
- **description:** A paper about X that argues Y.
- **notes:** Draft due March 15. Next step: finish related work section.
```
