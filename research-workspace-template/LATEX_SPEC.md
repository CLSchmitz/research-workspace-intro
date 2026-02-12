# LaTeX Spec — Agent Guidance for Scientific Writing

## Building

Use `latexmk` to compile. Example:

```
latexmk -pdf main.tex
```

## Git and Overleaf Sync

- Each LaTeX project is its own git repo under `projects/`.
- Projects can sync to GitHub and from there to Overleaf.
- Always fetch and pull before starting work; merge conflicts are resolved locally, not on Overleaf.
- Never commit auxiliary build files (`.aux`, `.log`, `.bbl`, etc.). Use a `.gitignore`.

## Writing Style and Conventions

- Write clear, direct academic prose. Prefer active voice where appropriate.
- Keep paragraphs focused on one idea. Use topic sentences.
- Define acronyms on first use.
- Use `\cite{citekey}` for citations (or `\citep{}`/`\citet{}` if the project uses natbib).

## Citation Workflow

1. Find the citekey using Zotero MCP tools (search, semantic search) or by searching the export files under `zotero/exports/`.
2. Copy the BibTeX entry from the library export into the project's local `.bib` file if it's not already there.
3. Insert the `\cite{}` command at the appropriate location in the `.tex` file.
4. Never fabricate citations. Every citekey must exist in Zotero.

## File Conventions

- Main document is typically `main.tex` (check the project).
- Each project has its own `.bib` file — a curated bibliography for that paper only.
- Figures go in a `figs/` or similar directory within the project.
- Never edit files under `zotero/exports/` — those are read-only reference copies.
