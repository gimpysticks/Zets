---
created: 2026-01-06
---
This issue with the ThinkCentre M715q (especially the "Tiny" models) is often related to a power-state glitch in the USB controllers or a specific BIOS setting called **Smart USB Protection**.

Here is a troubleshooting guide ordered from the most likely "quick fixes" to deeper hardware resets.

---

## 1. The "60-Second" Hard Power Reset

This is the most common fix for Lenovo Tiny desktops when USB ports stop providing power or data suddenly. It clears the static electricity from the motherboard.

1. **Unplug** the power cable from the back of the M715q.
2. **Disconnect** all USB devices (keyboard, mouse, etc.).
3. Press and **hold the Power Button for 60 seconds**.
4. Plug the power cable back in.
5. Plug the keyboard and mouse into the **rear USB 2.0 ports** (usually the black ones) rather than the blue USB 3.0 ports in the front, and turn it on.

## 2. Check for "Smart USB Protection" in BIOS

If your keyboard works to get into the BIOS but stops working once Windows starts, a security feature might be blocking them.

* **How to enter BIOS:** Tap **F1** repeatedly as soon as you press the power button.
* **The Setting:** Navigate to **Devices** > **USB Configuration**.
* Look for **Smart USB Protection**. If it is enabled, it may be set to "Read Only" or "Disabled," which can block input devices. Set it to **Disabled** (which actually *enables* normal USB use) or ensure it's not blocking HID devices.
* **Load Defaults:** While in BIOS, you can also press **F9** to load setup defaults and **F10** to save and exit.

## 3. Disable "Fast Startup" (If it works after a Restart)

If the keyboard/mouse doesn't work on a "Cold Boot" (turning it on for the first time) but *does* work if you force a restart, Windows Fast Startup is likely the culprit.

1. Go to **Control Panel** > **Hardware and Sound** > **Power Options**.
2. Click **"Choose what the power buttons do"**.
3. Click **"Change settings that are currently unavailable"** at the top.
4. Uncheck **"Turn on fast startup (recommended)"**.
5. Save changes and shut down.

---

### Hardware Quick-Check Table

| Component | Action |
| --- | --- |
| **Front Ports** | Often use more power; try the **Rear Ports** for basic input. |
| **USB Hubs** | Avoid them for now. Plug the keyboard directly into the PC. |
| **CMOS Battery** | If the PC is 4+ years old, a dying CR2032 battery can cause USB boot issues. |

**Would you like me to find the specific BIOS update for your M715q model to see if there is a known firmware fix for USB stability?**

---

[Lenovo USB Troubleshooting](https://www.youtube.com/watch?v=U864YYWpngo)
This video provides a visual walkthrough of common driver and hardware fixes for Lenovo USB devices that are not being recognized by the system.
