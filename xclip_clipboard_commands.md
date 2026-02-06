---
created: 2026-01-27
---
# xclip Clipboard Commands (Linux)

This document collects the most common and useful ways to copy text to the clipboard using **xclip**.

---

## Basic: Copy Text to Clipboard

```bash
echo "your text here" | xclip -selection clipboard
```

Copies text to the **system clipboard** (paste with **Ctrl+V**).

---

## Copy a File’s Contents

```bash
xclip -selection clipboard < file.txt
```

Copies the entire contents of `file.txt` into the clipboard.

---

## Copy Command Output

```bash
ls -la | xclip -selection clipboard
```

Copies the output of a command directly to the clipboard.

---

## Primary Selection (Middle-Click Paste)

```bash
echo "text" | xclip
```

Uses the **primary selection**, which can be pasted with a middle mouse click.

---

## Helpful Alias

Add this to your shell configuration file (`.bashrc`, `.zshrc`, etc.):

```bash
alias clip='xclip -selection clipboard'
```

Then you can quickly copy anything:

```bash
echo "hello world" | clip
```

---

## Notes

- `clipboard` → Ctrl+V paste
- `primary` → middle-click paste
- Works under **X11** (for Wayland, consider `wl-copy` instead)

---

*Markdown-friendly and suitable for Standard Notes, Obsidian, or Git-based dotfiles.*
