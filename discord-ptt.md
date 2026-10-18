---
title: discord-ptt
created: 2026-10-17
tags: [discord, wayland, cosmic, push-to-talk, pipewire, evdev, pop_os]
---

# Discord Wayland Push-to-Talk (`discord-ptt`)

> **Primary Daemon / CLI:** `/home/sticks/.local/bin/discord-ptt`  
> **Systemd User Service:** `discord-ptt.service` (`/home/sticks/.config/systemd/user/discord-ptt.service`)  
> **Default Startup Mode:** `OFF (Open Mic)` *(so browser web apps like Gemini work normally by default)*  
> **Push-to-Talk Keybind (Hold):** `Ctrl + Alt + V`  
> **Mode Toggle Keybind (PTT ↔ Open Mic):** `Ctrl + Alt + Shift + V`  

---

## 1. Overview & Background

On Pop!_OS COSMIC (Wayland), Discord's built-in Push-to-Talk keybind listener (`discord_utils.node`) is hardcoded to X11 (`XInput2`) and cannot intercept global key events under native Wayland (`--ozone-platform=wayland`). Additionally, browser-based Discord Web tabs cannot capture unfocused keystrokes across windows or full-screen games.

`discord-ptt` solves this globally at the kernel and PipeWire level:
- Reads physical keyboard events directly from `/dev/input/event*` using `python3-evdev`.
- Starts in **Open Mic (`OFF`)** mode by default on login/service start so browser web apps (such as the Gemini web app in Brave) can use the microphone normally without interference.
- Uses **`Ctrl + Alt + V`** (avoiding Brave Browser's `Ctrl + Alt + T` Split View accelerator and all COSMIC/OBS/Handy/TildaZ bindings).
- When Push-to-Talk mode is enabled (`Ctrl + Alt + Shift + V` or `discord-ptt --on`), gates PipeWire microphone input streams (`Source Outputs`) via `pactl` for both **Discord Standalone** (`WEBRTC VoiceEngine` / `com.discordapp.Discord`) and **Discord Web** (`Brave input`, `Chromium input`, `Firefox`, etc.).
- Leaves other microphone consumers—such as **Handy** (`Ctrl+Space` speech-to-text)—completely untouched.
- While Push-to-Talk mode is **`ON`**, automatically detects and mutes newly created Discord/Browser voice streams in real time via `pactl subscribe`.

---

## 2. Required Discord Configuration

In **User Settings → Voice & Video** (for both Discord Standalone and Discord Web):
- Set **Input Mode** to **Voice Activity**.

By default, `discord-ptt` starts in **Open Mic Mode (`OFF`)** so web apps in Brave/browsers can freely use the microphone. When you toggle `discord-ptt` into **Push-to-Talk Mode (`ON`)** via `Ctrl + Alt + Shift + V` (or `discord-ptt --on`), it keeps the Discord/Browser PipeWire input stream muted (`Mute: yes`) until `Ctrl + Alt + V` is held down, so zero audio reaches Discord until you press the key combo.

---

## 3. Keyboard Shortcuts

| Shortcut | Action | Description |
| :--- | :--- | :--- |
| **`Ctrl + Alt + V`** *(Hold)* | **Push-to-Talk** | Unmutes Discord/Browser mic streams immediately while held (when PTT mode is `ON`); re-mutes 90ms after `V` is released. |
| **`Ctrl + Alt + Shift + V`** | **Toggle Mode (PTT ↔ Open Mic)** | Switches between **Open Mic Mode (`OFF`, default)** (mic stays unmuted for browser web apps and normal Voice Activity) and **Push-to-Talk Mode (`ON`)** (mic muted unless `Ctrl+Alt+V` is held), with a desktop notification. |

---

## 4. Command-Line Usage

You can also toggle or query the daemon from any terminal or script:

```bash
# Check current mode (prints "ON (Push-to-Talk)" or "OFF (Open Mic)")
discord-ptt --status

# Toggle between Push-to-Talk and Open Mic
discord-ptt --toggle

# Explicitly enable Push-to-Talk mode
discord-ptt --on

# Explicitly disable Push-to-Talk (switch to Open Mic / Voice Activity)
discord-ptt --off
```

---

## 5. Systemd Service Management

The daemon runs automatically on login as a `systemd --user` service:

```bash
# Check service status and attached keyboards
systemctl --user status discord-ptt.service

# Restart the service
systemctl --user restart discord-ptt.service

# Stop the service (automatically unmutes all streams on exit)
systemctl --user stop discord-ptt.service

# Start the service
systemctl --user start discord-ptt.service
```

---

## 6. Files & System Configuration

| File Path | Purpose |
| :--- | :--- |
| `/home/sticks/.local/bin/discord-ptt` | Python `asyncio` + `evdev` + `pactl` Push-to-Talk daemon and CLI. |
| `/home/sticks/.config/systemd/user/discord-ptt.service` | Systemd user unit starting `discord-ptt` after PipeWire. |
| `/etc/udev/rules.d/99-input-uaccess.rules` | Grants active seat user (`uaccess`) read access to `/dev/input/event*` without root. |
| `/home/sticks/.config/autostart/com.discordapp.Discord.desktop` | Autostart desktop entry launching Discord on login with Wayland Ozone flags. |
| `/home/sticks/.var/app/com.discordapp.Discord/config/discord-flags.conf` | Persistent flags (`--enable-features=UseOzonePlatform`, `--ozone-platform=wayland`) for all Discord Flatpak launches. |
