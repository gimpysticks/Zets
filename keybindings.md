# Key Bindings Reference Guide

> **System Profile**
> - **User**: `sticks`
> - **OS**: Linux (Pop!_OS 24.04 LTS / COSMIC Wayland `COSMIC`)
> - **Shell**: `/usr/bin/zsh`
> - **Window Manager / Compositor**: `cosmic-comp` (Auto-tiling Wayland Compositor)
> - **Primary Backup Repository**: [`~/bin`](file:///home/sticks/bin) (`https://github.com/gimpysticks/binfiles.git`)
> - **Updated**: October 26, 2026

---

## Table of Contents
1. [Antigravity CLI Keybindings](#1-antigravity-cli-keybindings)
2. [Pop!_OS COSMIC Tiling & Window Management](#2-pop_os-cosmic-tiling--window-management)
3. [Custom Application & Script Shortcuts (COSMIC)](#3-custom-application--script-shortcuts-cosmic)
   - [AI & Productivity Services](#ai--productivity-services)
   - [Terminal, Code & Developer Tools](#terminal-code--developer-tools)
   - [Custom Utilities & Helper Scripts](#custom-utilities--helper-scripts)
   - [System Monitoring & Remote Desktop](#system-monitoring--remote-desktop)
   - [Media, Graphics & Wallpaper](#media-graphics--wallpaper)
   - [Communication & Social Media](#communication--social-media)
   - [Gaming](#gaming)
4. [Global Wayland Input & Audio Daemons (`evdev`)](#4-global-wayland-input--audio-daemons-evdev)
5. [TildaZ Drop-Down Terminal Keybindings](#5-tildaz-drop-down-terminal-keybindings)
6. [OBS Studio Hotkeys](#6-obs-studio-hotkeys)
7. [Tmux Multiplexer Keybindings](#7-tmux-multiplexer-keybindings)
8. [Shell (Zsh) & Command-Line Keybindings](#8-shell-zsh--command-line-keybindings)
9. [Neovim (LazyVim) Reference](#9-neovim-lazyvim-reference)

---

## 1. Antigravity CLI Keybindings

Configured in [`~/.gemini/antigravity-cli/keybindings.json`](file:///home/sticks/.gemini/antigravity-cli/keybindings.json).

### CLI Navigation & Session Control
| Key Binding | Action Identifier | Description |
| :--- | :--- | :--- |
| `Ctrl + L` | `cli.clear_screen` | Clear the terminal viewport |
| `Shift + Tab` | `cli.cycle_mode` | Cycle through CLI interaction modes |
| `Enter` | `cli.enter` | Submit prompt / select item |
| `Alt + M` | `prompt.submit_alternate` | Alternate prompt submit |
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
| `PgUp` | `navigation.page_up` | Scroll up one full page |
| `PgDn` | `navigation.page_down` | Scroll down one full page |
| `Shift + Up` | `navigation.half_page_up` | Scroll up half a page |
| `Shift + Down` | `navigation.half_page_down` | Scroll down half a page |
| `Tab` | `navigation.tab` | Tab autocomplete / next focus target |

### Vim Mode Overrides
| Key Binding | Action Identifier | Mode | Description |
| :--- | :--- | :--- | :--- |
| `Alt + Enter` / `Ctrl + J` / `Enter` / `Shift + Enter` | `vim.insert.insert_newline` | Insert | Insert newline |
| `Ctrl + Enter` / `Ctrl + S` | `vim.insert.submit` | Insert | Submit prompt from insert mode |
| `Ctrl + Enter` / `Ctrl + S` | `vim.normal.submit` | Normal | Submit prompt from normal mode |

---

## 2. Pop!_OS COSMIC Tiling & Window Management

Configured in `~/.config/cosmic/com.system76.CosmicSettings.Shortcuts/v1/` (backed up to [`~/bin/cosmic-custom-keybindings.ron`](file:///home/sticks/bin/cosmic-custom-keybindings.ron) and [`~/bin/cosmic-system-actions.ron`](file:///home/sticks/bin/cosmic-system-actions.ron)).

### Built-In COSMIC System & Tiling Shortcuts
| Key Binding | Action in COSMIC |
| :--- | :--- |
| `Super + t` | Open Terminal (`cosmic-term`, configured in `system_actions`) |
| `Super + b` | Open Default Web Browser |
| `Super + f` | Open Files (`cosmic-files`) |
| `Super + /` | Open COSMIC Launcher |
| `Super + a` | Open Applications Library |
| `Super + w` | Open Workspaces Overview |
| `Super + q` | Close Focused Window |
| `Super + m` | Maximize / Unmaximize Focused Window |
| `Super + y` | Toggle Auto-Tiling |
| `Super + g` | Float / Unfloat Focused Window |
| `Super + s` | Toggle Window Stacking |
| `Super + o` | Toggle Split Orientation |
| `Super + x` | Swap Window Position |
| `Super + h/j/k/l` or `Super + Arrows` | Move Window Focus |
| `Super + Shift + h/j/k/l` or `Super + Shift + Arrows` | Move Window in Tile Tree |
| `Super + 1..9, 0` | Switch to Workspace 1..9, Last |
| `Super + Shift + 1..9, 0` | Move Window to Workspace 1..9, Last |
| `Super + Ctrl + Left/Right/Up/Down` | Navigate Workspaces |
| `Super + Alt + Left/Right/Up/Down` | Switch Output Monitor Display |
| `Alt + Tab` | Window Switcher |
| `Print` | Interactive Screenshot |

---

## 3. Custom Application & Script Shortcuts (COSMIC)

Configured in `~/.config/cosmic/com.system76.CosmicSettings.Shortcuts/v1/custom` (**43 active bindings**) and synced via [`~/bin/update_keybinds`](file:///home/sticks/bin/update_keybinds) / [`~/bin/restore_keybinds`](file:///home/sticks/bin/restore_keybinds).

### AI & Productivity Services
| Key Binding | Label | Command / Action |
| :--- | :--- | :--- |
| `Super + Ctrl + a` | AI Urls | [`/home/sticks/bin/aiurls`](file:///home/sticks/bin/aiurls) |
| `Super + Ctrl + g` | agy | `cosmic-term -e agy` (Antigravity CLI) |
| `Super + F8` | Handy Speech to Text | `/home/sticks/.local/bin/handy --toggle-transcription` |
| `Super + Ctrl + o` | ChatGPT | `xdg-open https://www.chatgpt.com` |
| `Super + Shift + o` | ChatGpt | `xdg-open https://chatgpt.com/` |
| `Super + Alt + g` | Gemini | `xdg-open https://gemini.google.com/app` |
| `Super + Alt + k` | Grok | `xdg-open https://www.grok.com` |
| `Super + Alt + m` | Midjourney | `xdg-open https://www.midjourney.com` |
| `Super + Alt + e` | Eleven Labs | `xdg-open https://elevenlabs.io/app/home` |
| `Alt + Shift + s` | Standard Notes | `xdg-open https://app.standardnotes.com/` |

### Terminal, Code & Developer Tools
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `F12` | TildaZ_0 | `/home/sticks/.local/opt/tildaz/tildaz --toggle 0` (Drop-down terminal replacing Guake) |
| `Super + t` | Open Terminal | `cosmic-term` (COSMIC system action) |
| `Super + F2` | VimWiki | `gnome-terminal -- zsh -l -c "nvim"` (shimmed via `~/.local/bin/gnome-terminal` to `cosmic-term`) |
| `Super + Alt + w` | Warp Terminal | `warp-terminal` |
| `Super + Alt + b` | Change Browser | [`/home/sticks/bin/chgbrowser`](file:///home/sticks/bin/chgbrowser) |

### Custom Utilities & Helper Scripts
| Key Binding | Label | Target Script |
| :--- | :--- | :--- |
| `Super + Ctrl + r` | Read Human | [`/home/sticks/bin/readgTTS`](file:///home/sticks/bin/readgTTS) |
| `Super + Alt + l` | Linktree to Clipboard | [`/home/sticks/bin/cplinktree`](file:///home/sticks/bin/cplinktree) |
| `Alt + Shift + w` | Work URLS | `bash -c /home/sticks/bin/workurls` |
| `Super + Shift + m` | Monitor Off | [`/home/sticks/bin/monitor-off`](file:///home/sticks/bin/monitor-off) (DPMS power off via `wlopm`) |
| `Super + l` | Lock Screen | `loginctl lock-session` |
| `Super + Escape` | Lock Screen | `loginctl lock-session` |
| `Ctrl + Alt + BackSpace` | Restart X | [`/home/sticks/bin/restartx`](file:///home/sticks/bin/restartx) |

### System Monitoring & Remote Desktop
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Super + Ctrl + b` | Bpytop | `gnome-terminal -- bash -c "bpytop"` |
| `Super + Ctrl + c` | Connections | `flatpak run org.gnome.Connections` |

### Media, Graphics & Wallpaper
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Super + F3` | Gimp | `/bin/gimp` |
| `Super + F4` | Inkscape | `/bin/inkscape` |
| `Super + Shift + s` | Shotcut | `flatpak run org.shotcut.Shotcut` |
| `Super + Alt + o` | OBS-Studio | `flatpak run com.obsproject.Studio` |
| `Super + F10` | Youtube Music | `xdg-open https://music.youtube.com/` |
| `Alt + Right` | Variety Next | `/usr/bin/variety --next` |
| `Ctrl + Alt + Right` | Variety Next | `variety --next` |
| `Alt + Left` | variety Previous | `/usr/bin/variety --previous` |
| `Ctrl + Alt + Left` | Variety Previous | `/usr/bin/variety --previous` |

### Communication & Social Media
| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Super + e` | Thunderbird | `gtk-launch thunderbird` |
| `Super + Ctrl + d` | Discord | `flatpak run com.discordapp.Discord` |
| `Super + Alt + d` | Discord Web | `xdg-open https://discord.com/channels/411154143567282177/1182420235672887397` |
| `Super + Alt + f` | Facebook | `xdg-open https://www.facebook.com/gimpysticks` |
| `Super + Alt + i` | Instagram | `xdg-open https://www.instagram.com` |
| `Super + Alt + x` | X.com | `xdg-open https://x.com/home` |
| `Super + Alt + t` | TikTok | `xdg-open https://www.tiktok.com` |
| `Super + Shift + t` | Twitch | `xdg-open https://www.twitch.tv` |
| `Super + Alt + r` | Redbubble | `xdg-open https://www.redbubble.com/portfolio/manage_works?ref=account-nav-dropdown` |

### Gaming
In-game War Thunder keybindings reference: [`WT-Keys.md`](file:///home/sticks/zets/WT-Keys.md) (Spectator/Replay: [`Spectator-keybinds.md`](file:///home/sticks/zets/Spectator-keybinds.md), Naval: [`WT-Bluewater_Icon.md`](file:///home/sticks/zets/WT-Bluewater_Icon.md)).

| Key Binding | Label | Command / Target |
| :--- | :--- | :--- |
| `Super + Ctrl + s` | Steam | `steam` (native `.deb` installation) |
| `Super + Ctrl + w` | War Thunder | `steam steam://rungameid/236390` |


---

## 4. Global Wayland Input & Audio Daemons (`evdev`)

Configured in [`~/.local/bin/discord-ptt`](file:///home/sticks/.local/bin/discord-ptt) (backed up at [`~/bin/discord-ptt`](file:///home/sticks/bin/discord-ptt)) and managed by `discord-ptt.service` (`~/.config/systemd/user/discord-ptt.service`). Detailed documentation: [`discord-ptt.md`](file:///home/sticks/zets/discord-ptt.md).

| Key Binding | Action | Description |
| :--- | :--- | :--- |
| `Ctrl + Alt + V` *(Hold)* | **Discord Push-to-Talk** | Unmutes Discord Standalone & Browser WebRTC PipeWire microphone streams while held (when PTT mode is `ON`); re-mutes 90ms after release |
| `Ctrl + Alt + Shift + V` | **Toggle PTT ↔ Open Mic Mode** | Toggles between **Open Mic Mode (`OFF`, default on login)** so browser web apps (e.g., Gemini) work normally and **Push-to-Talk Mode (`ON`)** |

---

## 5. TildaZ Drop-Down Terminal Keybindings

Configured in [`~/.config/tildaz/config_0.toml`](file:///home/sticks/.config/tildaz/config_0.toml).

| Key Binding | Action |
| :--- | :--- |
| `F12` | Toggle TildaZ drop-down terminal globally |
| `Alt + 1..9` | Switch directly to Tab 1..9 |
| `Ctrl + Shift + Left/Right/Up/Down` | Split pane Left / Right / Up / Down |
| `Alt + Left/Right/Up/Down` | Focus pane Left / Right / Up / Down |
| `Shift + Alt + Left/Right/Up/Down` | Resize pane Left / Right / Up / Down |
| `Shift + Alt + 0` | Equalize pane sizes |
| `Ctrl + Shift + Z` | Zoom / unzoom active pane |
| `Ctrl + Shift + X` | Close active pane |
| `Ctrl + Shift + F` | Find in terminal scrollback |
| `Ctrl + Shift + C` / `Ctrl + Shift + V` | Copy / Paste clipboard |
| `Alt + Enter` / `Shift + Alt + Enter` | Toggle Fullscreen / Fullscreen Workarea |
| `Ctrl + Shift + P` | Open TildaZ configuration |

---

## 6. OBS Studio Hotkeys

Configured in `~/.var/app/com.obsproject.Studio/config/obs-studio/basic/profiles/Sticks/basic.ini` and `Untitled.json`. Full reference: [`OBS_Keys.md`](file:///home/sticks/zets/OBS_Keys.md).

| Key Binding | Action |
| :--- | :--- |
| `F7` / `F8` | Start Streaming / Stop Streaming |
| `F9` / `F10` | Start Recording / Stop Recording |
| `Ctrl + F9` / `Ctrl + F10` | Pause Recording / Unpause Recording |
| `F5` / `F6` / `Ctrl + F6` | Start Replay Buffer / Stop Replay Buffer / Save Replay Buffer |
| `F1` / `F2` | Start Virtual Cam / Stop Virtual Cam |
| `F3` / `F4` | Split Recording File / Add Chapter Marker |
| `Shift + F11` / `Shift + F12` | Screenshot / Scene Transition |
| `Ctrl + 1` / `Ctrl + 2` / `Ctrl + 3` | Select Scene: Full Camera / Desktop / Both |
| `Numpad 1` / `Numpad 2` / `Numpad 0` | Switch to Scene: Camera / Desktop / Desk_Cam |

---

## 7. Tmux Multiplexer Keybindings

Configured in [`~/.tmux.conf`](file:///home/sticks/.tmux.conf) and [`~/.tmux-live.conf`](file:///home/sticks/.tmux-live.conf) with **`Ctrl + b`** as the default Prefix key.

### Window Splits
| Key Binding | Action |
| :--- | :--- |
| `Prefix + \|` or `Prefix + \` or `Prefix + Ctrl-\` | Split window horizontally (side-by-side panes) |
| `Prefix + -` or `Prefix + _` | Split window vertically (top/bottom panes) |

### Pane Navigation & Resizing (Vim Keys)
| Key Binding | Action |
| :--- | :--- |
| `Prefix + h/j/k/l` | Select left / down / up / right pane |
| `Prefix + Ctrl-h/j/k/l` | Resize pane left / down / up / right by 1 cell |

### Session & Pane Lifecycle
| Key Binding | Action |
| :--- | :--- |
| `Prefix + x` | Kill current pane (prompts confirmation) |
| `Prefix + Ctrl-x` | Kill entire tmux server (confirm kill-server) |
| `Prefix + r` | Reload tmux configuration from `~/.tmux-live.conf` |
| `Prefix + [` | Enter Vi copy mode (`mode-keys vi` active) |

---

## 8. Shell (Zsh) & Command-Line Keybindings

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

## 9. Neovim (LazyVim) Reference

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
