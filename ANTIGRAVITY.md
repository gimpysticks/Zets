# 󰚩 Antigravity (`agy`) Integration for LazyVim

This guide details the Antigravity keybindings, commands, and workflow integration configured for your Neovim / LazyVim setup.

---

## ⚡ Quick Reference: Keybindings

All Antigravity keybindings are grouped under the `<leader>a` prefix (with which-key support).

| Keybinding | Mode | Command / Action | Description |
| :--- | :---: | :--- | :--- |
| `<leader>aa` | Normal | Toggle Terminal | Open or hide the main persistent Antigravity (`agy`) session |
| `<leader>ag` | Normal | Toggle Terminal (alias) | Convenient alternative for `<leader>aa` |
| `<leader>ac` | Normal | Resume Session | Launch `agy -c` to resume your last conversation |
| `<leader>ap` | Normal | Interactive Prompt | Open an input dialog to send an initial task/prompt |
| `<leader>af` | Normal | Send Current File | Send active buffer path + custom task to Antigravity |
| `<leader>as` | Visual | Send Selected Code | Send highlighted snippet (with line numbers) + task |
| `<leader>ar` | Normal | Review Git Changes | Launch LazyGit (`<cmd>LazyGit<cr>`) to inspect diffs |

---

## 💻 Neovim Commands

You can also trigger Antigravity from Neovim command mode (`:`):

| Command | Usage | Description |
| :--- | :--- | :--- |
| `:Antigravity` | `:Antigravity` | Toggle the main interactive session. |
| `:Antigravity <prompt>` | `:Antigravity Refactor auth.ts` | Start a new session with an initial prompt. |
| `:AntigravityContinue` | `:AntigravityContinue` | Continue previous conversation (`agy -c`). |

---

## 🪟 Floating Window Navigation & Controls

The Antigravity CLI runs inside a floating window powered by LazyVim's `snacks.nvim`.

* **Hide the window**:
  * Press `<Esc><Esc>` to switch from Terminal mode into Normal mode, then press `q` to hide.
  * Or press `<leader>aa` / `<C-/>` from outside the window to toggle it.
* **Persistent State**:
  * Toggling the window does **not** terminate `agy`. The session, history, and background tasks remain running in the background.
* **Exit the session entirely**:
  * Inside `agy`, type `/exit`, `/quit`, or press `Ctrl+D Ctrl+D`.

---

## 🔄 Automatic File Sync (`autoread`)

When Antigravity modifies files on disk:
1. **`vim.opt.autoread = true`** is enabled in `lua/config/options.lua`.
2. An autocmd in `lua/config/autocmds.lua` triggers `checktime` automatically whenever you switch back to Neovim (`FocusGained`), switch buffers (`BufEnter`), or pause cursor movement (`CursorHold`).
3. If the buffer is unmodified in Neovim, it updates instantly with zero prompts. If you have unsaved edits in Neovim, Neovim will protect your work and notify you of the conflict.

---

## 🛠 Recommended Workflow Loop

1. **Write & Inspect**: Open your project in LazyVim.
2. **Delegate**:
   * Need a quick question or agentic task? Press `<leader>ap`.
   * Need review on current buffer? Press `<leader>af`.
   * Need to refactor a specific function? Highlight it in visual mode and press `<leader>as`.
   * Want an interactive terminal assistant? Press `<leader>aa`.
3. **Review**:
   * Press `<leader>ar` to open LazyGit.
   * Stage accepted hunks with `[Space]`, or discard unwanted edits.
4. **Iterate**: Re-open `<leader>aa` to give Antigravity follow-up feedback.

---

## 📂 Configuration Files

* Integration spec: [`lua/plugins/antigravity.lua`](lua/plugins/antigravity.lua)
* Autoread option: [`lua/config/options.lua`](lua/config/options.lua)
* Sync autocmds: [`lua/config/autocmds.lua`](lua/config/autocmds.lua)
