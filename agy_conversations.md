---
title: agy_conversations
created: 2026-09-09
tags: [antigravity, adb, scrcpy, android, pop_os, linux, notes]
---

# Antigravity Session: File Attachments & Android Phone Control Setup

## 1. How to Attach / Reference Files in Antigravity

Antigravity provides multiple methods to feed files and context into conversations:

### A. Graphical Interfaces (Antigravity IDE & Antigravity 2.0 Desktop)
* **`@` Mentions (Fastest):** Type `@` in the chat input to trigger the auto-complete dropdown for files, folders, symbols, rules, and MCP tools in your workspace.
* **Drag-and-Drop:** Drag files or images directly from your system file manager (or IDE file tree) into the chat prompt area.
* **Paperclip / Plus Button:** Click the file attachment icon adjacent to the chat input to browse and select files.
* **Clipboard Paste:** Copy images or text snippets and paste (<kbd>Ctrl</kbd>+<kbd>V</kbd>) directly into the chat prompt.
* **Direct Path Mentions:** Type relative or absolute paths (e.g., `~/Documents/...`) directly in your message; the agent reads workspace files on demand.

### B. Command-Line Interface (`agy`)
* **Path Reference:** Mention paths directly in prompts (e.g., `agy "Review ./src/config.json"`).
* **STDIN Redirection / Piping:**
  ```bash
  cat error.log | agy "Analyze this trace"
  # or
  agy "Summarize document" < notes.txt
  ```

---

## 2. Android Phone Control Setup (`scrcpy` & `adb`)

Based on reference guide: `~/Documents/Prompt_library/HexSec_Android_Phone_Control_Guide.md`

### System Environment
* **OS:** Pop!_OS 22.04 LTS (x86_64)
* **Target Device:** Moto G Stylus 5G (2022)

### Actions Taken on Host System

#### 1. Installed `scrcpy`
Installed `scrcpy` and `scrcpy-server` via APT:
```bash
sudo apt update && sudo apt install -y scrcpy
```
* **Installed Version:** `scrcpy 1.21`

#### 2. Upgraded ADB from v28.0.2 to Latest v37.0.1
The default Ubuntu 22.04 repository package (`android-tools-adb` v28.0.2-debian) is outdated and frequently encounters issues with modern Android versions and wireless pairing.

Upgraded directly to official Google Android SDK Platform-Tools:
```bash
# Download official Google platform-tools
mkdir -p ~/.local/share/android
curl -L -o /tmp/platform-tools.zip https://dl.google.com/android/repository/platform-tools-latest-linux.zip
unzip -q -o /tmp/platform-tools.zip -d ~/.local/share/android/
rm /tmp/platform-tools.zip

# Symlink binaries to override distro packages
ln -sf ~/.local/share/android/platform-tools/adb ~/.local/bin/adb
ln -sf ~/.local/share/android/platform-tools/fastboot ~/.local/bin/fastboot
sudo ln -sf ~/.local/share/android/platform-tools/adb /usr/local/bin/adb
sudo ln -sf ~/.local/share/android/platform-tools/fastboot /usr/local/bin/fastboot

# Restart daemon
adb kill-server
adb start-server
```
* **Active Version:** `Android Debug Bridge version 1.0.41 (Version 37.0.1-15733141)`

#### 3. USB Permissions Configuration
Added user `sticks` to the `plugdev` group for non-root hardware access:
```bash
sudo usermod -aG plugdev sticks
```

---

## 3. Quick Reference: Phone Connection & Control

### Step 1: Prepare the Phone
1. Go to **Settings > About Phone**.
2. Tap **Build Number** 7 times to enable Developer Mode.
3. Open **Settings > System > Developer Options**.
4. Enable **USB Debugging**.
5. Connect phone via USB data cable.
6. When prompted on the phone, check **"Always allow from this computer"** and tap **Allow**.

### Step 2: Verify Connection
```bash
adb devices -l
```
Expected state:
```text
List of devices attached
ZY22GF3NT8    device usb:3-4.7.3 product:milan model:moto_g_stylus_5G device:milan
```
*(If it shows `unauthorized`, unlock your phone and accept the prompt.)*

### Step 3: Launch Mirroring & Remote Control
```bash
# Basic screen mirror & mouse/keyboard control
scrcpy

# Control with screen turned off (saves battery, prevents phone from heating up)
scrcpy --turn-screen-off --stay-awake

# Better physical keyboard emulation
scrcpy --keyboard=uhid

# Record session to MP4 file
scrcpy --record=session.mp4
```

### Step 4: Wireless Mode (No Cable)
Once connected once over USB:
```bash
# Switch ADB daemon on phone to TCP/IP mode
scrcpy --tcpip

# Or manually:
adb tcpip 5555
adb connect <PHONE_IP>:5555

# Disconnect USB cable and run scrcpy wirelessly:
scrcpy -e
```

### Essential `scrcpy` Shortcuts
* **MOD + H**: Home
* **MOD + B**: Back
* **MOD + S**: App Switcher
* **MOD + P**: Power button
* **MOD + O**: Turn phone screen off (keeps mirroring active on PC)
* **MOD + V**: Paste PC clipboard to phone
* **CTRL + drag**: Pinch-to-zoom simulation
*(Note: `MOD` is typically Left Alt or Left Super/Windows key).*

---

## 4. Installed Launcher Scripts (`~/bin/scrcpy_scripts`)

Launcher scripts created and symlinked into `~/bin` for one-command terminal access:

| Command | Script Path | Description |
| :--- | :--- | :--- |
| `phone` / `scrcpy-menu` | `~/bin/scrcpy_scripts/scrcpy-menu` | Interactive terminal menu to select any action |
| `scrcpy-usb` | `~/bin/scrcpy_scripts/scrcpy-usb` | USB mirroring with `--stay-awake` |
| `scrcpy-screen-off` | `~/bin/scrcpy_scripts/scrcpy-screen-off` | Screen-off battery saver mode |
| `scrcpy-wifi` | `~/bin/scrcpy_scripts/scrcpy-wifi` | Auto-detect IP over USB, enable TCP/IP, and connect wirelessly |
| `scrcpy-record` | `~/bin/scrcpy_scripts/scrcpy-record` | Record mirror session to `~/Videos/scrcpy_recordings/*.mp4` |
| `scrcpy-screenshot` | `~/bin/scrcpy_scripts/scrcpy-screenshot` | Save screenshot directly to `~/Pictures/Screenshots/*.png` |

---

## 5. Device-Specific Quirk & Fix: Motorola Moto G Stylus 5G (Android 13)

1. **Android 13 Compatibility:**
   * Upgraded to `scrcpy 4.1` via Snap because `v1.21` (APT) lacks Android 12/13 clipboard and media codec APIs.
   * Connected Snap interfaces for hardware acceleration (`mesa-2404:gpu-2404`, `ffmpeg-2404:ffmpeg-2404`, `gnome-46-2404:gnome-46-2404`, and `raw-usb`).
2. **Hardware Video Encoder Alignment:**
   * Motorola's Qualcomm video encoder (`c2.qti.avc.encoder`) requires resolution scaling to prevent `IllegalArgumentException` on native display dimensions.
   * Added `-m 1024` to all launcher scripts for smooth, crash-free streaming.
