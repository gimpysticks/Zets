# Zettelkasten Workflow

This document outlines the workflow for managing Zettelkasten notes.

## 1. Capture

- Quickly capture ideas, thoughts, and information as atomic notes.
- Each note should focus on a single idea.

## 2. Process

- Review captured notes.
- Refine and rephrase for clarity and conciseness.
- Assign unique identifiers (e.g., timestamps, UUIDs).

## 3. Connect

- Link new notes to existing relevant notes.
- Use bidirectional links to show relationships.
- Create index notes or "structure notes" to organize clusters of ideas.

## 4. Elaborate

- Expand on existing notes with new insights.
- Combine related notes into more comprehensive ones.

## 5. Review

- Regularly review notes to reinforce learning and discover new connections.
- Identify gaps in knowledge or areas for further exploration.

## Tools

- **Vim/Neovim:** For note-taking and editing.
- **`fd`:** For quickly finding notes.
- **`grep`:** For searching within note content.
- **`fzf`:** For fuzzy finding notes.

## Naming Convention

- `YYYYMMDDHHMM-keyword.md` (e.g., `202310271430-zettelkasten-principles.md`)
- Keywords should be concise and descriptive.

## Tags

- Use `#tags` within notes for categorization.
- Example: `#productivity #knowledge-management #workflow`

## Example Note Structure

```markdown
---
title: Zettelkasten Principles
date: 2023-10-27T14:30:00Z
tags: [productivity, knowledge-management]
---

# Zettelkasten Principles

The Zettelkasten method emphasizes atomic notes, interconnectedness, and iterative refinement...

## Key Principles

- **Atomicity:** Each note contains a single idea.
- **Autonomy:** Notes are self-contained and understandable on their own.
- **Connectivity:** Notes are linked to other relevant notes.
- **Generativity:** The system encourages new ideas and insights through connections.

## How it works

1.  **Fleeting Notes:** Quick captures of ideas.
2.  **Literature Notes:** Summaries of external sources.
3.  **Permanent Notes:** Refined, atomic notes linked into the system.

## Related Notes

- [[202310261000-note-taking-strategies]]
- [[202310280900-linking-ideas]]
```