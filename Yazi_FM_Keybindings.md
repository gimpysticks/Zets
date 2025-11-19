---
title: Yazi_FM_Keybindings
created: 2025-10-21
modified: 2025-10-21
---

# Yazi File Manager Keybindings Quick Reference

You can always press `~` or `F1` inside Yazi to view the complete list of shortcuts.

---
## Navigation & Movement

| Task | Shortcut(s) | Notes |
| :--- | :--- | :--- |
| **Move Up/Down** | **`k`** / **`j`** or **`↑`** / **`↓`** | Vim-style movement. |
| **Enter Directory** | **`l`** or **`→`** or **`Enter`** | |
| **Go to Parent Directory** | **`h`** or **`←`** | |
| Go to Top of List | **`g`** then **`g`** | Press `g` twice. |
| Go to Bottom of List | **`G`** | |
| Move Down Half Page | **`Ctrl + d`** | |
| Move Up Half Page | **`Ctrl + u`** | |
| Go to Home Directory | **`g`** then **`h`** | |
| Toggle Hidden Files | **`.`** | |

---
## File Operations (Yank, Paste, Delete)

Yazi uses **Yank** (`y`/`x`) for copy/cut operations.

| Task | Shortcut(s) | Notes |
| :--- | :--- | :--- |
| **Copy Selected File(s)** | **`y`** | Yanks files for copying. |
| **Cut Selected File(s)** | **`x`** | Yanks files for cutting/moving. |
| **Paste File(s)** | **`p`** | |
| Paste File(s) (Overwrite) | **`P`** | Overwrites if a file exists at the destination. |
| **Cancel Yank Status** | **`Y`** or **`X`** | Cancels any pending copy/cut operation. |
| **Create File/Directory** | **`a`** | Append with **`/`** to create a directory. |
| **Rename Selected File** | **`r`** | |
| **Delete to Trash** | **`d`** | |
| **Delete Permanently** | **`D`** | |
| **Open Selected File(s)** | **`o`** or **`Enter`** | Opens with the default application/editor. |
| **Open Interactively** | **`Shift + Enter`** or **`O`** | Lets you choose which application to open with. |

---
## Selection

| Task | Shortcut(s) | Notes |
| :--- | :--- | :--- |
| **Toggle Selection** | **`Spacebar`** | Selects the currently highlighted item. |
| **Enter Visual Mode** | **`v`** | For block or multi-item selection. |
| **Select All Files** | **`Ctrl + a`** | |
| **Inverse Selection** | **`Ctrl + r`** | |
| **Cancel Selection** | **`Esc`** or **`Ctrl + c`** | Also exits visual mode. |

---
## Multi-Tab Management

| Task | Shortcut(s) | Notes |
| :--- | :--- | :--- |
| **New Tab** | **`t`** | Opens a new tab in the current directory. |
| **Switch Tab** | **`1`** through **`9`** | Jumps to the numbered tab. |
| **Switch to Previous Tab** | **`[`** | |
| **Switch to Next Tab** | **`]`** | |
| **Close Current Tab** | **`Ctrl + c`** | Quits Yazi if it's the only remaining tab. |

---
## Copying Paths (Chained Commands)

These are chained commands, meaning you press the first key, release it, and then press the second key.

| Task | Shortcut(s) |
| :--- | :--- |
| Copy File Path | **`c`** then **`c`** |
| Copy Directory Path | **`c`** then **`d`** |
| Copy Filename | **`c`** then **`f`** |
| Copy Filename (No Extension) | **`c`** then **`n`** |
