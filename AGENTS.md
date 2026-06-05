# ps-1c-code-quality-tools — Agent Guide

## What this is

Pure Markdown documentation project for **1C:Enterprise** code quality (BSL language). Not a software project — no build, test, lint, typecheck, or CI pipeline. Content is in Russian and English, aimed at 1C developers in Kazakhstan/CIS.

The repo is also an **Obsidian vault** (`.obsidian/` config present).

## Known structural issues (do not recreate)

- **`LICENSE`** contains `ROADMAP.md` content instead of a license — the roadmap was written into the wrong file.
- **`ROADMAP.md`** is empty (its content is in `LICENSE`).
- **`docs/coding-standards.md`** has the code review prompt (`tools/code-review-prompts/1c-code-review.md`) merged into lines 77–126. That prompt belongs in its own file.
- **`templates/module-header-template.md`** has unrelated Russian OpenAI form notes appended at line 15+.
- **`tools/code-review-prompts/1c-code-review.md`** is empty — its content is orphaned inside `docs/coding-standards.md`.

## Populated files (the only real deliverables)

| File | Content |
|------|---------|
| `docs/coding-standards.md` | Naming, server/client separation, queries, error handling (with orphaned prompt at bottom) |
| `tools/static-analysis-checklists/1c-static-analysis-checklist.md` | 46-line checklist (module structure, naming, queries, error handling, performance, security) |
| `tools/quality-gates/release-quality-gate.md` | 38-line pre-release checklist (functional, code quality, data safety, docs, approval) |
| `templates/code-review-report.md` | 51-line review report template with tables for issues + decision field |

All other directories (`src/`, `examples/`, `rules/`, `ai-workflows/`, `tests/`) contain only empty README stubs — scaffold, no content.

## Commands

No build, test, or lint commands exist. There is nothing to run.

## Conventions

- 1C BSL code snippets use `bsl` code fence.
- Follow existing checklist/template formatting (markdown tables, `- [ ]` checklists, `| № | Issue | ... |` style).
- Keep examples practical, no client confidential data, no proprietary configs (per `CONTRIBUTING.md`).
- Fix the file-swap bugs (LICENSE→ROADMAP, orphaned prompt) if the task touches those files.

## Git

- Remote: `vadim1C-svs/ps-1c-code-quality-tools`
- Single branch: `main`
- Managed via SourceTree
