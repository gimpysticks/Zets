---
created: 2026-01-06
---
To clear the entire content of a file while keeping the file itself (retaining the filename) in Neovim, you have a few options depending on whether you are already inside Neovim or want to do it from the terminal.

### 1. From within Neovim (Ex-Command)

The fastest way to wipe the current buffer is the **`%d`** command.

- Press `:` to enter command mode.
- Type **`%d`** and hit **Enter**.
- `%` represents the entire file (all lines).
- `d` stands for delete.

> **Tip:** If you want to delete everything and immediately enter **Insert Mode**, you can use **`:%c`** (change) instead.

---

### 2. From the Terminal (CLI)

If you want to clear a file's content without ever opening it, you don't actually need Neovim. You can use standard shell redirection.

```bash
# Using redirection (works in Bash/Zsh)
> filename.txt

# Using the 'truncate' command (more explicit)
truncate -s 0 filename.txt

```

---

### 3. Combining both: Launch Neovim with an Empty File

If you want to open Neovim, clear the file immediately, and keep working in that same file, use the `-c` flag we discussed earlier:

```bash
nvim filename.txt -c "%d"

```

If you want to clear the file, save the empty version, and exit immediately (useful for logs):

```bash
nvim filename.txt -c "%d" -c "wq"

```

---

### Comparison of Methods

| Method            | Best For...                         | Command             |
| ----------------- | ----------------------------------- | ------------------- |
| **Inside Neovim** | Quick clearing while editing        | `:%d`               |
| **Pure CLI**      | Resetting log files or scripts      | `> filename`        |
| **Launch Flag**   | Automating a "fresh start" via nvim | `nvim file -c "%d"` |

**Would you like me to help you create a custom Neovim mapping (like `<leader>ce`) so you can clear your current file with a single key combination?**
