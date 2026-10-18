---
created: 2026-01-16
updated: 2026-10-18
---
# War Thunder Keybindings

This document lists the keybindings configured for War Thunder.

## Base Preset
- **Default Preset:** `config/hotkeys/hotkey.keyboard_shooter_ver3.blk`
- **Live Config File:** `~/.config/WarThunder/Saves/last/production/machine.blk`
- **Exported Backup:** [`~/bin/warthunder-controls.blk`](file:///home/sticks/bin/warthunder-controls.blk) & `~/.config/WarThunder/Saves/Full_CTLS.blk`
- **Note:** Only custom overrides are stored in user config. Standard controls use War Thunder's default values from `hotkey.keyboard_shooter_ver3.blk`.

## Custom Keybindings (`machine.blk` Overrides)

### Aircraft Flight & Propulsion
- **Pitch Up (`elevator_rangeMax`):** `S` (`keyboardKey: 31`)
- **Pitch Down (`elevator_rangeMin`):** `W` (`keyboardKey: 17`)
- **Throttle Up (`throttle_rangeMax`):** `Page Up` (`keyboardKey: 201`) / `Mouse Wheel`
- **Throttle Down (`throttle_rangeMin`):** `Page Down` (`keyboardKey: 209`) / `Mouse Wheel`
- **Ignite Boosters (`ID_IGNITE_BOOSTERS`):** `Ctrl + Alt + B` (`keyboardKey: 29, 56, 48`)

### Weapons & Ordnance (Aircraft & Helicopter)
- **Bombs Series Release (`ID_BOMBS_SERIES`):** `Space` *(Hold)* (`keyboardKey: 57`, `activationType: 1`)
- **Fire Rocket (Helicopter, `ID_ROCKETS_HELICOPTER`):** `4` (`keyboardKey: 5`)
- **Fire Rocket Salvo / Series (Helicopter, `ID_ROCKETS_SERIES_HELICOPTER`):** `Mouse Button 5` (`mouseButton: 4`)

### Scout UAV / Human UAV Controls
- **UAV Control Mode (`ID_CONTROL_MODE_HUMAN_UAV`):** `H` (`keyboardKey: 35`)
- **UAV Climb / Throttle Up:** `W` (`keyboardKey: 17`) / `Up Arrow` (`keyboardKey: 200`) / `Mouse Wheel` (`mouseAxisId: 7`)
- **UAV Descend / Throttle Down:** `S` (`keyboardKey: 31`) / `Down Arrow` (`keyboardKey: 208`)
- **UAV Pitch Up / Down:** `Page Down` (`keyboardKey: 209`) / `Page Up` (`keyboardKey: 201`)
- **UAV Roll Left / Right:** `A` (`keyboardKey: 30`) & `Left Arrow` (`keyboardKey: 203`) / `D` (`keyboardKey: 32`) & `Right Arrow` (`keyboardKey: 205`)
- **UAV Yaw Left / Right:** `Q` (`keyboardKey: 16`) / `E` (`keyboardKey: 18`)

### Communication & Audio
- **Internet Radio (`ID_INTERNET_RADIO`):** `Numpad 1` / `End` (`keyboardKey: 79`)

### General Controls
- **Flight / Pause Menu (`ID_FLIGHTMENU`):** `Esc` (`keyboardKey: 1`)
- **Continue (`ID_CONTINUE`):** `Space` (`keyboardKey: 57`)
- **Screenshot (`ID_SCREENSHOT`):** `Print Screen` (`keyboardKey: 183`) / `Shift + Print Screen` (`keyboardKey: 42, 183`)
- **Tactical Web Map Bridge (`wt-map-bridge`):** `M` (handled by `wt-map-bridge.service` & `wt-map-fix.service` on port `8111`)

## Control Settings

### Mouse Sensitivity
- **Mouse Sensitivity:** 0.5
- **Mouse Aim Sensitivity:** 0.5
- **Gunner View Sensitivity:** 0.5
- **Gunner View Zoom Sensitivity:** 0.5
- **Zoom Sensitivity:** 0
- **ATGM Aim Sensitivity (Helicopter):** 1.0
- **ATGM Aim Zoom Sensitivity (Helicopter):** 0.1

### Aircraft Controls
- **Ailerons Multiplier:** 0.79
- **Elevator Multiplier:** 0.64
- **Rudder Multiplier:** 0.43
- **Invert Y-Axis:** No
- **Invert X-Axis:** No
- **Mouse Smooth:** No

### Helicopter Controls
- **Cyclic Roll Multiplier:** 0.79
- **Cyclic Pitch Multiplier:** 0.64
- **Pedals Multiplier:** 0.43
- **Invert Y-Axis (Helicopter):** No
- **Invert Y-Axis (Helicopter Gunner):** No

### Tank Controls
- **Invert Y-Axis (Tank):** No

### Camera Controls
- **Camera Smooth:** 0
- **Camera Speed:** 0.95
- **Camera Mouse Speed:** 4.0
- **Camera FPS Physics Multiplier:** 0.5
- **Free Camera Inertia:** 1.0
- **Replay Camera Wiggle:** 1.0

### Other Settings
- **Hold Button for WEP:** No
- **Mouse Joystick:** No
- **Force Gain:** 1.0
- **Camera Shake Multiplier:** 1.0
- **Vibration:** Yes

---

## Default War Thunder Keybindings Reference (`hotkey.keyboard_shooter_ver3.blk`)

These are the standard default controls from War Thunder's `keyboard_shooter_ver3` preset that have not been overridden above.

### General Controls
- **Pause Menu:** `Esc`
- **Scoreboard:** `Tab` (hold)
- **Chat (All):** `T`
- **Chat (Team):** `Y`
- **Voice Chat (Team):** `V` (hold)
- **Map:** `M`
- **Mission Objectives:** `O`

### Aircraft Controls (Mouse Aim)
- **Pitch/Roll:** Mouse movement + `W` (Pitch Down) / `S` (Pitch Up)
- **Throttle Up / Down:** `Page Up` / `Page Down` / Mouse Wheel
- **Yaw Left / Right:** `Q` / `E`
- **Roll Left / Right:** `A` / `D`
- **Fire Primary Weapon:** Left Mouse Button
- **Release Bombs:** `Space`
- **Ignite Boosters:** `Ctrl + Alt + B`
- **Toggle Landing Gear:** `G`
- **Toggle Flaps:** `F`
- **Toggle Airbrake:** `H`
- **Engine Start/Stop:** `I`
- **Lock Target:** `X`
- **Zoom In:** `Z`
- **Free Look:** `C` (hold)

### Tank Controls
- **Move Forward / Backward:** `W` / `S`
- **Turn Left / Right:** `A` / `D`
- **Fire Main Gun:** Left Mouse Button
- **Fire Machine Gun:** `Space`
- **Switch Shell Type:** `1`, `2`, `3`, `4`
- **Sniper Mode / Sight:** `Shift`
- **Binoculars:** `B`
- **Smoke Grenades:** `G`
- **Toggle Cruise Control:** `Q` / `E`
- **Artillery Strike:** `5`

### Naval Controls
- **Throttle Up / Down:** `W` / `S`
- **Rudder Left / Right:** `A` / `D`
- **Fire Primary Guns:** Left Mouse Button
- **Fire Torpedoes:** `Space`
- **Free Look:** `C` (hold)
- **Binoculars:** `B`

---
*Configuration extracted from:* `~/.config/WarThunder/Saves/last/production/machine.blk`  
*Last Updated:* October 18, 2026
