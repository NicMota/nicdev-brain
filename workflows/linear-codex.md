---
title: Linear + Codex + GitHub delivery workflow
status: provisional
tags: [agents, linear, codex, github, delivery]
last_reviewed: 2026-11-19
---

# Linear + Codex + GitHub workflow

## Purpose

Deliver small, verifiable changes while keeping the human developer in control of product decisions, merges, and production releases. This workflow is tool-independent in principle: Codex may be replaced with another coding agent.

## Responsibilities

- **Human / product owner:** validate the problem, prioritize and approve scope, review the outcome.
- **Linear:** record the objective, acceptance criteria, dependencies and progress.
- **Coding agent:** inspect the repository, implement only the scoped change, test and present a reviewable diff.
- **GitHub:** version code, run checks and host pull requests.
- **Project AGENTS.md:** provide local conventions, commands, guardrails and architecture pointers.

## Issue template

### Context
Why is this change needed? What current behavior is relevant?

### Objective
One observable outcome.

### Requirements
- Specific behavior to implement.
- Relevant constraints and security considerations.

### Acceptance criteria
- [ ] Behavior can be verified by a test or reproducible manual procedure.
- [ ] Error cases and authorization are covered when relevant.
- [ ] Existing behavior remains intact.

### Out of scope
Features, refactors or integrations not included.

### Dependencies
Related issues or prerequisites, if any.

## Execution sequence

1. **Select:** pick an unblocked, small Linear issue. Validate that its requirement still makes sense.
2. **Orient:** read the local project's AGENTS.md, relevant source and tests. Consult [INDEX.md](../INDEX.md) only for reusable context that might help.
3. **Plan proportionally:** a brief note for straightforward work; a short explicit plan for security-sensitive or architectural changes.
4. **Implement:** focus on one issue per branch/PR. Avoid opportunistic refactors.
5. **Validate:** run applicable lint, typecheck, unit/integration tests and build. For deployment work, execute targeted smoke checks.
6. **Review:** inspect for scope creep, test gaps, security problems, secrets and unexpected schema changes.
7. **PR:** reference the Linear issue; summarize changes, checks, limitations and any manual setup.
8. **Human approval:** review and merge deliberately. Deploy only with appropriate authorization.
9. **Capture learning:** propose a global note only when there is a transferable, evidenced lesson.

## Pull request checklist

- [ ] Acceptance criteria covered.
- [ ] Applicable checks actually executed; failures documented.
- [ ] No unrelated changes or exposed secrets.
- [ ] Authorization and data isolation checked when relevant.
- [ ] Migration and deployment implications considered.
- [ ] PR links its Linear issue.

## Token and context efficiency

- Retrieve only the issue and files needed to implement it.
- Avoid loading the entire global brain.
- Use a planning/review agent only when complexity or risk warrants it.
- Store project-specific decisions in the project, not in the global knowledge base.
- Do not copy full issue histories or agent transcripts into notes.

## Limitations

Integrations and permissions vary by environment. A coding agent may lack access to Linear, GitHub, a local checkout, or deployment secrets. Confirm access instead of assuming it. The workflow is a recommended practice, not evidence that any particular integration is configured.

## Verification status

**Provisional:** suitable as a starting workflow. Adjust based on completed PRs, actual delivery times and observed failure modes.
