---
title: repo_sync_automation_guide
created: 2026-10-13
tags: [git, automation, sync-repos, push-repos, python, bash, pop_os, gimpysticks]
---

# Git Repository Synchronization & Push Automation Guide

> **Primary Command:** `push-repos` (or `sync-repos`)  
> **Source Script:** `/home/sticks/bin/sync-repos`  
> **Symlinks:** `push-repos`, `repo-sync`, `git-sync`  
> **Target GitHub User:** `@gimpysticks`  

---

## 1. Overview

`push-repos` automates repository synchronization across all user-owned Git repositories:
1. **Analyzes changes**: Differentiates untracked (`??`), added (`A`), modified (`M`), deleted (`D`), and mode-changed (`100644` -> `100755`) files.
2. **Synthesizes commit messages**:
   - Analyzes Markdown documents for `# Title` headings.
   - Analyzes Python docstrings (`"""..."""`) and shell script header comments.
   - Formats conventional commit subjects (`feat:`, `docs:`, `config:`, `chore:`, `fix:`) under 72 characters.
   - Builds detailed multi-line bullet points in the commit body.
3. **Interactive Review**:
   - `<Enter>`: Accept and proceed.
   - `e`: Open in `$EDITOR` (`nvim`).
   - `m`: Type manual commit message.
   - `s`: Skip current repository.
   - `q`: Quit.
4. **Stages, pulls, and pushes**:
   - Stages all files with `git add -A`.
   - Safely pulls remote updates using `git pull --rebase`.
   - Pushes to the upstream branch (`git push -u origin <branch>`).
5. **Safety Barriers**:
   - Detects and skips repositories mid-rebase or in merge conflicts (e.g. `Documents/chats`).
   - Restricts multi-repo scans to `@gimpysticks` owned repositories, preventing accidental push attempts to third-party forks.

---

## 2. Command Options

| Command | Action |
| :--- | :--- |
| `push-repos` | Sync current repository (if inside one) or scan all |
| `push-repos --all` (or `-a`) | Scan and synchronize all user repositories across `~` |
| `push-repos --dry-run` (or `-n`) | Preview analysis and proposed commit messages safely |
| `push-repos --list` (or `-l`) | List pending changes across all repositories |
| `push-repos -y` (or `--yes`) | Unattended mode (auto-accepts commit messages and pushes) |
| `push-repos -m "custom message"` | Override commit message |
| `push-repos --guide` | Display documentation directly in terminal |
| `push-repos <repo-name>` | Target a specific repo (e.g. `push-repos Prompt_library`) |
| `push-repos <path>` | Target a specific repo path (e.g. `push-repos ~/.config/variety`) |
| `push-repos --no-push` | Stage and commit locally without pushing |
| `push-repos --no-pull` | Skip pulling remote updates before pushing |

---

## 3. Repositories Managed

* `~/bin` (`https://github.com/gimpysticks/binfiles.git`) — Master branch
* `~/.config/variety` (`https://github.com/gimpysticks/variety-config.git`) — Main branch
* `~/Documents/Prompt_library` (`https://github.com/gimpysticks/Prompt_library.git`) — Master branch
* `~/Documents/gimpysticks_canonical_prompt_system` (`https://github.com/gimpysticks/gimpysticks_canonical_prompt_system.git`) — Master branch
* `~/repos/ai-art-challenges` (`https://github.com/gimpysticks/ai-art-challenges.git`) — Master branch
* `~/repos/nvim-config` (`https://github.com/gimpysticks/nvim-config.git`) — Main branch
* `~/.config/nvim` (`https://github.com/gimpysticks/nvim-config.git`) — Master branch
* `~/zets` (`https://github.com/gimpysticks/Zets.git`) — Master branch
