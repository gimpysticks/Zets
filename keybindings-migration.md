# Keybinding Migration Reference — Pop!_OS 22.04 → COSMIC (24.04)

Raw dconf backup: `~/bin/custom-keybindings.dconf`

---

## Web Shortcuts (xdg-open) — should work as-is in COSMIC

| Binding | Name | Command |
|---|---|---|
| `Alt+Super+I` | Instagram | `xdg-open https://www.instagram.com` |
| `Alt+Super+X` | X.com | `xdg-open https://x.com/home` |
| `Alt+Super+G` | Gemini | `xdg-open https://gemini.google.com/app` |
| `Alt+Super+F` | Facebook | `xdg-open https://www.facebook.com/gimpysticks` |
| `Alt+Super+M` | Midjourney | `xdg-open https://www.midjourney.com/archive` |
| `Shift+Super+O` | ChatGPT | `xdg-open https://chatgpt.com/` |
| `Shift+Alt+S` | Standard Notes | `xdg-open https://app.standardnotes.com/` |
| `Alt+Super+D` | Discord Web | `xdg-open https://discord.com/channels/411154143567282177/1182420235672887397` |
| `Alt+Super+R` | Redbubble | `xdg-open https://www.redbubble.com/portfolio/manage_works?ref=account-nav-dropdown` |
| `Alt+Super+K` | Grok | `xdg-open https://www.grok.com` |
| `Super+F10` | Youtube Music | `xdg-open https://music.youtube.com/` |
| `Ctrl+Super+O` | ChatGPT (dupe) | `xdg-open https://www.chatgpt.com` |
| `Alt+Super+T` | TikTok | `xdg-open https://www.tiktok.com` |
| `Alt+Super+E` | Eleven Labs | `xdg-open https://elevenlabs.io/app/home` |
| `Shift+Super+T` | Twitch | `/usr/bin/firefox www.twitch.com` |

---

## App Launchers — should work as-is

| Binding | Name | Command |
|---|---|---|
| `Ctrl+Super+D` | Discord | `flatpak run com.discordapp.Discord` |
| `Shift+Super+S` | Shotcut | `flatpak run org.shotcut.Shotcut` |
| `Super+F3` | GIMP | `/bin/gimp` |
| `Super+F4` | Inkscape | `/bin/inkscape` |
| `Ctrl+Super+S` | Steam | `/usr/games/steam` |
| `Ctrl+Super+W` | War Thunder | `flatpak run com.valvesoftware.Steam steam://rungameid/236390` |
| `Alt+Super+W` | Warp | `warp-terminal` |
| `Alt+Super+O` | OBS Studio | `flatpak run com.obsproject.Studio` |
| `Ctrl+Alt+O` | OpenRGB | `flatpak run org.openrgb.OpenRGB` |
| `Ctrl+Alt+D` | Digikam | `flatpak run org.kde.digikam` |
| `Alt+Super+H` | Hypnotix | `/usr/bin/hypnotix` |

---

## Custom Scripts (~/bin) — should work as-is

| Binding | Name | Command |
|---|---|---|
| `Ctrl+Super+R` | Read Human | `~/bin/readhuman.sh` |
| `Shift+Alt+W` | Work URLs | `bash -c ~/bin/workurls` |
| `Alt+Super+B` | Change Browser | `~/bin/chgbrowser` |
| `Ctrl+Super+A` | AI URLs | `~/bin/aiurls` |
| `Alt+Super+L` | Linktree to Clipboard | `~/bin/cplinktree` |
| `Alt+Super+N` | Toggle Nerd Dict | `~/bin/nerddict` |

---

## NEEDS FIXING — GNOME-dependent commands

| Binding | Name | Current Command | What to change |
|---|---|---|---|
| `Super+T` | Open Terminal | `x-terminal-emulator` | Change to `cosmic-term` |
| `F12` | Guake | `guake` | **No COSMIC equivalent** — drop-down terminal won't work |
| `Super+F2` | VimWiki | `gnome-terminal -- zsh -l -c "nvim"` | Change to `cosmic-term -e zsh -l -c "nvim"` (check syntax) |
| `Ctrl+Super+B` | Bpytop | `gnome-terminal -- bash -c "bpytop"` | Change to `cosmic-term -e bpytop` |
| `Ctrl+Alt+G` | Glances | `gnome-terminal -x glances` | Change to `cosmic-term -e glances` |
| `Ctrl+Super+C` | Connections | `flatpak run org.gnome.Connections` | GNOME Connections — may still work as a Flatpak, but test it |
| `Ctrl+Alt+P` | Polychromatic Tray | `/usr/bin/polychromatic-tray-applet` | Tray applets work differently in COSMIC — test it |
| `Ctrl+Alt+BackSpace` | Restart X | `~/bin/restartx` | COSMIC uses Wayland, not X — this script is obsolete |

---

## LIKELY BROKEN — Variety Wallpaper

| Binding | Name | Command | Issue |
|---|---|---|---|
| `Ctrl+Alt+Right` | Variety Next | `variety --next` | Variety may not set wallpapers on COSMIC/Wayland |
| `Ctrl+Alt+Left` | Variety Previous | `variety --previous` | Same |
| `Alt+Right` | Variety Next (dupe) | `variety --next` | Same |
| `Alt+Left` | Variety Previous (dupe) | `variety --previous` | Same |

---

## OBSOLETE

| Binding | Name | Command | Issue |
|---|---|---|---|
| `Ctrl+Alt+B` | Beeper | `AppImageLauncher ~/Applications/Beeper-4.0.747.AppImage` | AppImageLauncher is archived; Beeper has moved to a new app |

---

## Additional Notes

- **`Launch1` → WiFi** (`gnome-control-center wifi`) — Replace with `cosmic-settings wifi` or equivalent.
- **`gnome-pomodoro`** (custom30) has no binding set but references a GNOME app that won't exist.

### Duplicate/conflicting bindings to clean up
- Two entries for **Steam** on `Ctrl+Super+S`
- Two for **Facebook** (`Alt+Super+F` — different URLs)
- Two for **Midjourney** (`Alt+Super+M` — one to /archive, one to main)
- Two for **Variety Next** (`Ctrl+Alt+Right` and `Alt+Right`)
- Two for **Variety Previous** (`Ctrl+Alt+Left` and `Alt+Left`)
- Two for **Redbubble** (`Alt+Super+R`)
- Two for **Instagram** (`Alt+Super+I`)
- Two for **Work URLs/Workspace** (`Shift+Alt+W` and `Alt+Super+W`)
- **Audacity** and **AI URLs** both on `Ctrl+Super+A`
