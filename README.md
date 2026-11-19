# NicDev Brain

A lightweight, Git-versioned knowledge base for reusable software engineering knowledge and AI-agent workflows.

## Goals

- Preserve verified lessons learned across independent projects.
- Help Codex, Claude Code, and other agents retrieve useful context selectively.
- Keep project-specific requirements in their original repositories and task trackers.
- Maintain a portable knowledge base using Markdown, with no infrastructure or API costs.

This repository is **not** a universal instruction authority, task tracker, secrets vault, or dump of every agent conversation.

## Start here

1. Read [INDEX.md](INDEX.md) to locate relevant notes.
2. Read [AGENTS.md](AGENTS.md) if an AI agent will use or contribute to this repository.
3. Use [templates/knowledge-note.md](templates/knowledge-note.md) for reusable findings.
4. See [workflows/linear-codex.md](workflows/linear-codex.md) for a practical delivery workflow.

## Scope

Store reusable patterns, troubleshooting write-ups, technical decisions with broad applicability, and validated workflows. Prefer links to original PRs/docs over duplicating long material.

Do not store passwords, API tokens, private customer data, non-public employer information, or sensitive personal context. **This repository is public.**

## Repository layout

```text
README.md
AGENTS.md
INDEX.md
templates/
  knowledge-note.md
workflows/
  linear-codex.md
```

Add new categories (e.g. `patterns/` or `troubleshooting/`) only as useful notes accumulate.

## Contributing a note

- Check [INDEX.md](INDEX.md) for related notes first.
- Record the context, evidence, approach, limitations, and review date.
- Distinguish observed behavior from advice and hypotheses.
- Verify claims against the current project and upstream documentation.
- Link the new note in INDEX.md.
- Review changes before committing; agents should propose edits, not silently rewrite shared knowledge.

## Using in another repository

Clone this repo alongside other projects, or make it available through an authorized GitHub connection. Add a short pointer in each project's `AGENTS.md`:

> Optional global engineering context: consult NicMota/nicdev-brain/INDEX.md only when relevant. Local requirements, tested code, and project documentation take precedence.

Local filesystem paths are not automatically available in cloud agents. Configure access explicitly.
