---
name: recall-vault
description: Persistent memory for Claude Code using Obsidian + QMD
version: 1.0.0
---

# Claude Code Memory Skill

This skill provides Claude Code with a persistent memory layer via an Obsidian vault.

## Trigger Conditions
- Every task cycle: Before start and after completion.

## Operating Principles

### 1. Pre-Task Retrieval
Before executing any task, check the `recall-vault` to provide relevant context:
1. Identify key concepts (user prefs, tech stack, patterns).
2. Query the Obsidian vault using `qmd`.
3. Use the retrieved context to inform the task plan.

### 2. Post-Task Reflection
After any task, evaluate what should be remembered:
1. **Patterns:** Did we find a new reusable pattern?
2. **Decisions:** Was an important design choice made?
3. **Errors:** Did we hit a tricky bug that might recur?
4. **Preferences:** Did Seko adjust any workflows?

If relevant, draft a QMD-formatted note and commit it to the vault.

## Search Pattern
```bash
qmd query "search terms" -c sparkymind -n 5
```

## Write Pattern
1. Create a structured markdown note in `vault-template/` or the appropriate sub-folder.
2. Ensure QMD frontmatter is present for indexing.
3. Commit/index the vault: `qmd update && qmd embed -c sparkymind`
