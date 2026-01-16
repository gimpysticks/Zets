Since you're on **Pop!_OS**, you have the best environment for this. You don't need any bulky software; you can do this directly through your terminal in about 60 seconds.

### 1. Install ADB

Open your terminal (**Super + T**) and run:

```bash
sudo apt update && sudo apt install android-tools-adb -y

```

### 2. Connect to your Fire Stick

Ensure your Fire Stick and your Pop!_OS machine are on the **same Wi-Fi network**.

* Go to **Settings** > **My Fire TV** > **About** > **Network** on your Fire Stick to get its **IP Address** (e.g., `192.168.1.50`).
* In your terminal, type:

```bash
adb connect [YOUR_FIRE_STICK_IP]

```

> **Watch your TV screen!** A popup will appear asking to "Allow USB Debugging." Check the box for **"Always allow"** and select **OK**.

### 3. Send the "No Sleep" Command

Once it says `connected to ...`, run this final command:

```bash
adb shell settings put secure sleep_timeout 0

```

---

### Verification (Optional)

If you want to make sure the setting actually saved, you can run:

```bash
adb shell settings get secure sleep_timeout

```

If it returns `0`, your Fire Stick will no longer go to sleep automatically. It will stay on your photo gallery or whatever app you have open until you manually turn it off.

### Important Note on Power

Since the Fire Stick will now stay "awake" indefinitely, it may keep your TV's backlight on or prevent the TV itself from entering its own power-save mode. Make sure your **TV's internal sleep timer** isn't going to fight with the Fire Stick.

**Would you also like the command to prevent the screensaver from starting, or do you want the photos to still pop up automatically?**