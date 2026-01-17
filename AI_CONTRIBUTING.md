# AI Contributing Guidelines

This repository uses AI-assisted development. AI agents are contributors, not owners of state.

## Guiding Principles

AI contributors are expected to:
- Follow task specifications
- Update documentation when behaviour changes
- Record design decisions when applicable
- Respect scope boundaries

This framework prioritises long-term clarity over raw speed.

## Documentation Expectations

When completing a task, consider updating:

### PROGRESS.md
A dated summary of what changed. Keep entries concise and factual.

### DECISIONS.md
Record *why* decisions were made, but only when a meaningful choice was involved. Don't document obvious implementation details.

### ARCHITECTURE.md
Update only when system structure, boundaries, or data flow changes.

## Commit Message Format

Consider using structured commit messages:

```
<type>(scope): summary

Task: T-XXX
Docs updated: PROGRESS.md[, DECISIONS.md][, ARCHITECTURE.md]
```

This makes git history more readable.

## What This Prevents

- Undocumented behaviour changes
- Silent refactors that surprise future maintainers
- Loss of architectural intent
- "Why does this exist?" moments

## Flexibility

This is a framework, not rigid rules. Adapt it to your workflow. The core principle is simple:

**If it matters, document it.**
