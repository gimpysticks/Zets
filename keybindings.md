# Key Bindings Reference Guide

> **System Profile**
> - **User**: `sticks`
> - **OS**: Linux (Pop!_OS 22.04 LTS / GNOME `pop:GNOME`)
> - **Shell**: `/usr/bin/zsh`
> - **Window Manager**: Pop Shell (Auto-tiling) + Mutter / GNOME Shell
> - **Generated**: September 5, 2026

---

## Table of Contents
1. [Antigravity CLI Keybindings](#1-antigravity-cli-keybindings)
2. [Pop Shell Tiling Window Manager](#2-pop-shell-tiling-window-manager)
3. [Custom Application & Script Shortcuts](#3-custom-application--script-shortcuts)
   - [AI & Productivity Services](#ai--productivity-services)
   - [Terminal, Code & Developer Tools](#terminal-code--developer-tools)
   - [Custom Utilities & Helper Scripts](#custom-utilities--helper-scripts)
   - [System Monitoring & Hardware](#system-monitoring--hardware)
   - [Media, Graphics & Wallpaper](#media-graphics--wallpaper)
   - [Communication & Social Media](#communication--social-media)
   - [Gaming](#gaming)
4. [GNOME Desktop & Window Management](#4-gnome-desktop--window-management)
   - [Window Management](#window-management)
   - [Workspaces & Navigation](#workspaces--navigation)
   - [Screenshots & Screen Recording](#screenshots--screen-recording)
   - [System & Media Keys](#system--media-keys)
5. [Tmux Multiplexer Keybindings](#5-tmux-multiplexer-keybindings)
6. [Shell (Zsh) & Command-Line Keybindings](#6-shell-zsh--command-line-keybindings)
7. [Neovim (LazyVim) Reference](#7-neovim-lazyvim-reference)

---

## 1. Antigravity CLI Keybindings

Configured in [`~/.gemini/antigravity-cli/keybindings.json`](file:///home/sticks/.gemini/antigravity-cli/keybindings.json).

### CLI Navigation & Session Control
| Key Binding | Action Identifier | Description |
| :--- | :--- | :--- |
| `Ctrl + L` | `cli.clear_screen` | Clear the terminal viewport |
| `Shift + Tab` | `cli.cycle_mode` | Cycle through CLI interaction modes |
| `Enter` | `cli.enter` | Submit prompt / select item |
| `Ctrl + C` / `Esc` | `cli.escape` | Cancel input / return to idle prompt |
| `Ctrl + D` | `cli.exit` | Exit the CLI session |
| `Ctrl + Z` | `cli.suspend` | Suspend process to background |

### Prompt Text Editing
| Key Binding | Action Identifier | Description |
| :--- | :--- | :--- |
| `Ctrl + G` | `edit.open_editor` | Open external editor (`$EDITOR` / `nvim`) for long prompt writing |
| `Ctrl + V` | `edit.paste` | Paste text into the prompt input |
| `Ctrl + Shift + Z` | `edit.redo` | Redo undone edit |
| `Ctrl + _` / `Ctrl + Shift + -` | `edit.undo` | Undo edit in prompt buffer |
| `Ctrl + Y` | `edit.yank` | Yank / paste from kill-ring |
| `Alt + Enter` / `Ctrl + J` / `Shift + Enter` | `prompt.insert_newline` | Insert literal newline without submitting |

### Subagents & Execution Flow
| Key Binding | Action Identifier | Description |
| :--- | :--- | :--- |
| `Ctrl + K` | `subagent.approve_fast` | Fast-approve pending subagent / task step |
| `Alt + J` | `subagent.jump_to_waiting` | Switch focus directly to subagent awaiting input |
| `Ctrl + R` | `view.review_artifact` | Open artifact review viewer |
| `Ctrl + O` | `view.toggle_trajectory` | Toggle trajectory / reasoning trace visibility |

### Confirmation Dialogs & Item Management
| Key Binding | Action Identifier | Description |
| :--- | :--- | :--- |
| `y` | `confirm.yes` | Confirm affirmative action |
| `n` | `confirm.no` | Cancel / reject action |
| `e` | `confirm.edit_command` | Edit command in prompt before running |
| `F2` | `item.rename` | Rename selected item or conversation |
| `F4` | `item.delete` | Delete selected item or conversation |
| `F5` | `voice.start_dictation` | Start / stop voice dictation input |

### List & History Navigation
| Key Binding | Action Identifier | Description |
| :--- | :--- | :--- |
| `Up` / `Down` | `navigation.up` / `down` | Move selection / command history |
| `Left` / `Right` | `navigation.left` / `right` | Cursor positioning |
| `Ctrl + Home` | `navigation.go_to_top` | Jump to very top of conversation / history |
| `Ctrl + End` | `navigation.go_to_bottom` | Jump to latest output at bottom |
| `PgUp` / `Shift + Up` | `navigation.page_up` | Scroll up one screen |
| `PgDn` / `Shift + Down` | `navigation.page_down` | Scroll down one screen |
| `Tab` | `navigation.tab` | Tab autocomplete / next focus target |

### Vim Mode Overrides
| Key Binding | Action Identifier | Mode | Description |
| :--- | :--- | :--- | :--- |
| `Alt + Enter` / `Ctrl + J` / `Enter` / `Shift + Enter` | `vim.insert.insert_newline` | Insert | Insert newline |
| `Ctrl + Enter` / `Ctrl + S` | `vim.insert.submit` | Insert | Submit prompt from insert mode |
| `Ctrl + Enter` / `Ctrl + S` | `vim.normal.submit` | Normal | Submit prompt from normal mode |

---

## 2. Pop Shell Tiling Window Manager

Configured in `org.gnome.shell.extensions.pop-shell` (Pop!_OS auto-tiling).

### Focus Navigation (Vim & Arrow Keys)
| Key Binding | Action |
| :--- | :--- |
| `Super + h` or `Super + Left` | Move focus to left window |
| `Super + j` or `Super + Down` | Move focus to window below |
| `Super + k` or `Super + Up` | Move focus to window above |
| `Super + l` or `Super + Right` | Move focus to right window |

### Window Layout & Tiling Control
| Key Binding | Action | Description |
| :--- | :--- | :--- |
| `Super + y` | `toggle-tiling` | Toggle Pop Shell auto-tiling on/off |
| `Super + g` | `toggle-floating` | Toggle currently focused window floating |
| `Super + s` | `toggle-stacking-global` | Toggle window stacking mode for current tile group |
| `Super + o` | `tile-orientation` | Toggle tiling split orientation (horizontal / vertical) |

### Window Adjustment Mode
Press **`Super + Enter`** to enter Pop Shell Adjustment Mode. In adjustment mode:

| Key | Action |
| :--- | :--- |
| `h` / `j` / `k` / `l` or `Arrows` | Move window location in tile tree |
| `Shift + (h / j / k / l)` or `Shift + Arrows` | Resize current window |
| `Ctrl + (h / j / k / l)` or `Ctrl + Arrows` | Swap current window with neighbor |
| `s` | Toggle window stacking |
| `o` | Change orientation |
| `Enter` | Accept changes and exit adjustment mode |
| `Esc` | Reject changes and exit adjustment mode |

---

## 3. Custom Application & Script Shortcuts

Configured in GNOME Settings Daemon Media Keys (`/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/`).

> [!NOTE]
> In GNOME, `<Super>` is the Windows/Meta key, `<Primary>` is `Ctrl`, and `<Alt>` is the Alt key.

### AI & Productivity Services
| Key Binding | Label | Command / Action |
| :--- | :--- | :--- |
| `Primary + Super + a` | AI Urls | `/home/sticks/bin/aiurls` |
| `Primary + Super + o` | ChatGPT Web | `xdg-open https://www.chatgpt.com` |
| `Shift + Super + o` | ChatGPT Direct | `xdg-open https://chatgpt.com/` |
| `Alt + Super + g` | Gemini | `xdg-open https://gemini.google.com/app` |
| `Alt + Super + k` | Grok | `xdg-open https://www.grok.com` |
| `Alt + Super + m` | Midjourney | `xdg-open https://www.midjourney.com` |
| `Alt + Super + e` | Eleven Labs | `xdg-open https://elevenlabs.io/app/home` |
| `Super + e` | Gmail | `gtk-launch gmail` |
| `Shift + Alt + s` | Standard Notes | `xdg-open https://app.standardnotes.com/` |

### Terminal, Code & Developer Tools
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Super + t` | Open Terminal | `x-terminal-emulator` |
| `F12` | Guake Dropdown | `guake` |
| `Super + F2` | VimWiki / Neovim | `gnome-terminal -- zsh -l -c "nvim"` |
| `Alt + Super + w` | Warp Terminal | `warp-terminal` |
| `Alt + Super + b` | Change Browser | `/home/sticks/bin/chgbrowser` |

### Custom Utilities & Helper Scripts
| Key Binding | Label | Target Script |
| :--- | :--- | :--- |
| `Primary + Super + r` | Read Human TTS | [`/home/sticks/bin/readgTTS.sh`](file:///home/sticks/bin/readgTTS.sh) |
| `Alt + Super + n` | Toggle Nerd Dictation | [`/home/sticks/bin/nerddict`](file:///home/sticks/bin/nerddict) |
| `Alt + Super + l` | Linktree to Clipboard | [`/home/sticks/bin/cplinktree`](file:///home/sticks/bin/cplinktree) |
| `Shift + Alt + w` | Work URLs | `bash -c /home/sticks/bin/workurls` |
| `Alt + Super + w` | Workspace URLs | `/usr/bin/bash /home/sticks/bin/workurls` |
| `Primary + Alt + BackSpace` | Restart X Display | [`/home/sticks/bin/restartx`](file:///home/sticks/bin/restartx) |

### System Monitoring & Hardware
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Primary + Super + b` | Bpytop System Monitor | `gnome-terminal -- bash -c "bpytop"` |
| `Primary + Alt + g` | Glances System Monitor | `gnome-terminal -x glances` |
| `Primary + Alt + o` | OpenRGB Controller | `flatpak run org.openrgb.OpenRGB` |
| `Primary + Alt + p` | Polychromatic Applet | `/usr/bin/polychromatic-tray-applet` |
| `Primary + Super + c` | GNOME Connections (Remote) | `flatpak run org.gnome.Connections` |
| `Launch1` | WiFi Settings | `gnome-control-center wifi` |

### Media, Graphics & Wallpaper
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Super + F3` | GIMP | `/bin/gimp` |
| `Super + F4` | Inkscape | `/bin/inkscape` |
| `Shift + Super + s` | Shotcut Video Editor | `flatpak run org.shotcut.Shotcut` |
| `Alt + Super + o` | OBS Studio | `flatpak run com.obsproject.Studio` |
| `Primary + Alt + d` | DigiKam Photo Manager | `flatpak run org.kde.digikam` |
| `Super + F10` | YouTube Music | `xdg-open https://music.youtube.com/` |
| `Alt + Super + h` | Hypnotix IPTV | `/usr/bin/hypnotix` |
| `Alt + Right` / `Primary + Alt + Right` | Variety Next Wallpaper | `variety --next` |
| `Alt + Left` / `Primary + Alt + Left` | Variety Previous Wallpaper | `/usr/bin/variety --previous` |

### Communication & Social Media
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Primary + Super + d` | Discord Desktop | `flatpak run com.discordapp.Discord` |
| `Alt + Super + d` | Discord Web Channel | `xdg-open https://discord.com/channels/...` |
| `Primary + Alt + b` | Beeper Unified Chat | `AppImageLauncher ~/Applications/Beeper-...AppImage` |
| `Alt + Super + f` | Facebook | `xdg-open https://www.facebook.com/gimpysticks` |
| `Alt + Super + i` | Instagram | `xdg-open https://www.instagram.com/gimpysticks` |
| `Alt + Super + x` | X.com (Twitter) | `xdg-open https://x.com/home` |
| `Alt + Super + t` | TikTok | `xdg-open https://www.tiktok.com` |
| `Shift + Super + t` | Twitch | `/usr/bin/firefox www.twitch.com` |
| `Alt + Super + r` | Redbubble Portfolio | `xdg-open https://www.redbubble.com/...` |

### Gaming
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Primary + Super + s` | Steam Client | `flatpak run com.valvesoftware.Steam` |
| `Primary + Super + w` | War Thunder | Steam Applaunch `236390` |

---

## 4. GNOME Desktop & Window Management

### Window Management
| Key Binding | Action |
| :--- | :--- |
| `Super + q` or `Alt + F4` | Close active window |
| `Super + m` | Toggle window maximized |
| `Alt + Space` | Open window control menu |
| `Alt + F7` | Move floating window |
| `Alt + F8` | Resize floating window |
| `Super + Tab` / `Alt + Tab` | Switch applications (Forward) |
| `Shift + Super + Tab` / `Shift + Alt + Tab` | Switch applications (Backward) |
| `Super + ~` / `Alt + ~` | Switch windows within the same application |

### Workspaces & Navigation
| Key Binding | Action |
| :--- | :--- |
| `Super + d` | Pop Launcher / Shell Overview |
| `Super + a` | Show Applications grid |
| `Super + v` | Toggle notification message tray |
| `Super + n` | Focus active notification popup |
| `Ctrl + Super + Down` or `Ctrl + Super + j` | Switch to workspace down |
| `Ctrl + Super + Up` or `Ctrl + Super + k` | Switch to workspace up |
| `Super + Home` | Switch directly to Workspace 1 |
| `Super + End` | Switch directly to Last Workspace |
| `Shift + Super + Home` | Move active window to Workspace 1 |
| `Shift + Super + End` | Move active window to Last Workspace |
| `Super + p` | Switch display / monitor configuration |

### Screenshots & Screen Recording
| Key Binding | Action |
| :--- | :--- |
| `Print` | Open interactive screenshot GUI |
| `Alt + Print` | Capture screenshot of active window immediately |
| `Shift + Print` | Capture screenshot of custom area |
| `Ctrl + Shift + Alt + R` | Open Screen Recording UI |

### System & Media Keys
| Key Binding | Action |
| :--- | :--- |
| `Super + Escape` | Lock screen / activate screensaver |
| `Ctrl + Alt + Delete` | Open Log Out / Power dialog |
| `Super + b` | Launch default web browser |
| `Super + f` | Open Files (Nautilus Home folder) |
| `Alt + F2` | Open "Run a Command" dialog |
| `Alt + Super + 8` | Toggle Zoom Magnifier |
| `Alt + Super + =` / `-` | Zoom Magnifier In / Out |
| `Alt + Super + s` | Toggle Screen Reader |

---

## 5. Tmux Multiplexer Keybindings

Configured in [`~/.tmux-live.conf`](file:///home/sticks/.tmux-live.conf) with **`Ctrl + b`** as the default Prefix key.

### Window Splits
| Key Binding | Action |
| :--- | :--- |
| `Prefix + \|` or `Prefix + \` or `Prefix + Ctrl-\` | Split window horizontally (side-by-side panes) |
| `Prefix + -` or `Prefix + _` | Split window vertically (top/bottom panes) |

### Pane Navigation & Resizing (Vim Keys)
| Key Binding | Action |
| :--- | :--- |
| `Prefix + h` | Select left pane |
| `Prefix + j` | Select down pane |
| `Prefix + k` | Select up pane |
| `Prefix + l` | Select right pane |
| `Prefix + Ctrl-h` | Resize pane left by 1 cell |
| `Prefix + Ctrl-j` | Resize pane down by 1 cell |
| `Prefix + Ctrl-k` | Resize pane up by 1 cell |
| `Prefix + Ctrl-l` | Resize pane right by 1 cell |

### Session & Pane Lifecycle
| Key Binding | Action |
| :--- | :--- |
| `Prefix + x` | Kill current pane (prompts confirmation) |
| `Prefix + Ctrl-x` | Kill entire tmux server (confirm kill-server) |
| `Prefix + r` | Reload tmux configuration from `~/.tmux-live.conf` |
| `Prefix + [` | Enter Vi copy mode (`mode-keys vi` active) |

---

## 6. Shell (Zsh) & Command-Line Keybindings

Configured in [`~/.zshrc`](file:///home/sticks/.zshrc) and [`~/.zshrc-personal`](file:///home/sticks/.zshrc-personal).

| Key Binding | Mode / Binding | Function |
| :--- | :--- | :--- |
| `Ctrl + R` | `fzf-history-widget` | Interactive fuzzy search through command history (via `fzf`) |
| `Ctrl + A` | Emacs Mode (`bindkey -e`) | Move cursor to beginning of line |
| `Ctrl + E` | Emacs Mode | Move cursor to end of line |
| `Ctrl + U` | Emacs Mode | Clear entire line before cursor |
| `Ctrl + K` | Emacs Mode | Kill line from cursor to end |
| `Ctrl + W` | Emacs Mode | Delete previous word |
| `Ctrl + Y` | Emacs Mode | Paste (yank) deleted word/line |
| `Alt + B` / `Alt + F` | Emacs Mode | Jump backward / forward one word |

---

## 7. Neovim (LazyVim) Reference

Configured in [`~/.config/nvim/`](file:///home/sticks/.config/nvim/) with `<Space>` as Leader.

| Key Sequence | Action |
| :--- | :--- |
| `<Space> f f` | Find files (Telescope / fzf-lua) |
| `<Space> s g` | Live grep codebase search |
| `<Space> e` | Toggle Neo-tree file explorer |
| `<Space> b d` | Delete / close current buffer |
| `<Space> q q` | Quit Neovim |
| `Ctrl + h/j/k/l` | Seamless window navigation between Neovim splits |
| `<Space> c a` | Code action |
| `g d` | Go to definition |
