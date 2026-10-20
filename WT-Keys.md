---
created: 2026-01-16
updated: 2026-10-19
---
# War Thunder Keybindings

This document lists the active keybindings and control settings configured for War Thunder.

## Configuration Files & Preset Inheritance
- **Live Config File:** [`~/.config/WarThunder/Saves/last/production/machine.blk`](file:///home/sticks/.config/WarThunder/Saves/last/production/machine.blk) (synced with `Saves/133190654/production/machine.blk`, version `4126`)
- **Exported Active Controls:** [`~/bin/warthunder-controls.blk`](file:///home/sticks/bin/warthunder-controls.blk) & [`~/.config/WarThunder/Saves/Full_CTLS.blk`](file:///home/sticks/.config/WarThunder/Saves/Full_CTLS.blk)
- **Additional Saved Preset:**
  - [`~/.config/WarThunder/Saves/Default_CTLS.blk`](file:///home/sticks/.config/WarThunder/Saves/Default_CTLS.blk) — Extended preset with auto-assigned bindings for all unassigned actions (generated via [`~/bin/wt_fill_unassigned_keys.py`](file:///home/sticks/bin/wt_fill_unassigned_keys.py))
- **Preset Inheritance Chain:**
  `machine.blk` → `hotkey.keyboard_shooter_ver3.blk` → `hotkey.keyboard_shooter_ver2.blk` → `hotkey.base.keyboard_ma.blk` → `hotkey.base.keyboard.blk` → `hotkey.empty_ver1.blk` → `hotkey.event.human.blk`

---

## 1. Custom Keybinding Overrides (`machine.blk` / `Full_CTLS.blk`)

Only explicit overrides are stored in `machine.blk`; all other controls inherit from the `hotkey.keyboard_shooter_ver3.blk` preset chain below.

### Aircraft Flight & Propulsion
| Action | Action ID | Binding | Raw Config Code |
| :--- | :--- | :--- | :--- |
| **Pitch Up (Elevator Max)** | `elevator_rangeMax` | `S` | `keyboardKey: 31` |
| **Pitch Down (Elevator Min)** | `elevator_rangeMin` | `W` | `keyboardKey: 17` |
| **Throttle Up** | `throttle_rangeMax` | `Page Up` / `Mouse Wheel` | `keyboardKey: 201`, `mouseAxisId: 2` |
| **Throttle Down** | `throttle_rangeMin` | `Page Down` / `Mouse Wheel` | `keyboardKey: 209`, `mouseAxisId: 2` |
| **Ignite Boosters (JATO)** | `ID_IGNITE_BOOSTERS` | `Left Ctrl + Left Alt + B` | `keyboardKey: 29, 56, 48` |

### Weapons & Ordnance (Aircraft & Helicopter)
| Action | Action ID | Binding | Raw Config Code |
| :--- | :--- | :--- | :--- |
| **Drop Bomb Series** | `ID_BOMBS_SERIES` | `Space` *(Hold)* | `keyboardKey: 57`, `activationType: 1` |
| **Fire Rocket (Helicopter)** | `ID_ROCKETS_HELICOPTER` | `4` | `keyboardKey: 5` |
| **Fire Rocket Salvo (Helicopter)** | `ID_ROCKETS_SERIES_HELICOPTER` | `Mouse Button 5` | `mouseButton: 4` |

### Scout UAV / Human UAV Controls
| Action | Action ID | Binding | Raw Config Code |
| :--- | :--- | :--- | :--- |
| **UAV Control Mode** | `ID_CONTROL_MODE_HUMAN_UAV` | `H` | `keyboardKey: 35` |
| **UAV Climb / Ascend** | `human_uav_climb_rangeMax` | `W` | `keyboardKey: 17` |
| **UAV Descend** | `human_uav_climb_rangeMin` | `S` | `keyboardKey: 31` |
| **UAV Throttle Up** | `human_uav_throttle_rangeMax` | `W` / `Up Arrow` / `Mouse Wheel` | `keyboardKey: 17, 200`, `mouseAxisId: 7` |
| **UAV Throttle Down** | `human_uav_throttle_rangeMin` | `S` / `Down Arrow` | `keyboardKey: 31, 208` |
| **UAV Pitch Up (Nose Up)** | `human_uav_pitch_rangeMax` | `Page Down` | `keyboardKey: 209` |
| **UAV Pitch Down (Nose Down)** | `human_uav_pitch_rangeMin` | `Page Up` | `keyboardKey: 201` |
| **UAV Roll Left** | `human_uav_roll_rangeMin` | `A` / `Left Arrow` | `keyboardKey: 30, 203` |
| **UAV Roll Right** | `human_uav_roll_rangeMax` | `D` / `Right Arrow` | `keyboardKey: 32, 205` |
| **UAV Yaw Left** | `human_uav_yaw_rangeMin` | `Q` | `keyboardKey: 16` |
| **UAV Yaw Right** | `human_uav_yaw_rangeMax` | `E` | `keyboardKey: 18` |

### General, Audio & System
| Action | Action ID | Binding | Raw Config Code |
| :--- | :--- | :--- | :--- |
| **Flight / Pause Menu** | `ID_FLIGHTMENU` | `Esc` | `keyboardKey: 1` |
| **Continue** | `ID_CONTINUE` | `Space` | `keyboardKey: 57` |
| **Internet Radio Toggle** | `ID_INTERNET_RADIO` | `Numpad 1` (`End`) | `keyboardKey: 79` |
| **Screenshot** | `ID_SCREENSHOT` | `Print Screen` / `Left Shift + Print Screen` | `keyboardKey: 183` / `42, 183` |
| **Tactical Web Map Bridge** | `ID_TACTICAL_MAP` | `M` | `keyboardKey: 50` (assisted by `wt-map-bridge.service` & `wt-map-fix.service` on port `8111`) |

---

## 2. Resolved Preset Keybindings (`hotkey.keyboard_shooter_ver3.blk` Chain)

These are the active inherited bindings from `hotkey.keyboard_shooter_ver3.blk` → `hotkey.keyboard_shooter_ver2.blk` → `hotkey.base.keyboard_ma.blk` → `hotkey.base.keyboard.blk` → `hotkey.empty_ver1.blk`.

### General, Interface & Communication
| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Pause / Flight Menu** | `ID_FLIGHTMENU` | `Esc` |
| **Game Pause (Singleplayer)** | `ID_GAME_PAUSE` | `P` |
| **Help / Controls Reference** | `ID_HELP` | `F1` |
| **Statistics / Scoreboard** | `ID_MPSTATSCREEN` | `Tab` |
| **Tactical Map** | `ID_TACTICAL_MAP` | `M` |
| **Switch Tactical Map Type** | `ID_SWITCH_TACTICAL_MAP_TYPE` | `N` |
| **Show Mouse Cursor** | `ID_SHOW_MOUSE_CURSOR` | `Left Alt` *(Hold)* |
| **Multifunction Menu** | `ID_SHOW_MULTIFUNC_WHEEL_MENU` | `Y` |
| **Show Vehicle Modules (X-Ray)** | `ID_SHOW_HERO_MODULES` | `O` |
| **Collapse Action Bar** | `ID_COLLAPSE_ACTION_BAR` | `/` |
| **Hide HUD** | `ID_HIDE_HUD` | `Left Alt + Z` |
| **Screenshot Without HUD** | `ID_SCREENSHOT_WO_HUD` | `F12` |
| **Dump FPS Log** | `ID_DUMP_FPS_LOG` | `F11` |
| **Chat (Team)** | `ID_TOGGLE_CHAT_TEAM` | `Enter` / `Numpad Enter` |
| **Chat (All)** | `ID_TOGGLE_CHAT` | `Shift + Enter` |
| **Switch Chat Mode** | `ID_TOGGLE_CHAT_MODE` | `Tab` |
| **Push-to-Talk (In-Game Voice)** | `ID_PTT` | `Right Ctrl` |
| **Radio Messages for Team** | `ID_SHOW_VOICE_MESSAGE_LIST` | `T` |
| **Radio Messages for Squad** | `ID_SHOW_VOICE_MESSAGE_LIST_SQUAD` | `K` |
| **Quick Voice Messages 1–12** | `ID_VOICE_MESSAGE_1..12` | `1`–`0`, `-`, `=` (or `Numpad 1`–`Numpad +`) |
| **Set Target for Squad** | `ID_DESIGNATE_TARGET` | `C + Y` |
| **Bail Out / Leave Vehicle** | `ID_BAILOUT` | `J` *(Hold)* |

### Camera & View Controls
| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Toggle View** | `ID_TOGGLE_VIEW` | `V` |
| **Mouse Look / Free Look** | `ID_CAMERA_NEUTRAL` | `C` / `Numpad .` *(Hold)* |
| **Zoom Camera** | `ID_ZOOM_TOGGLE` | `Right Mouse Button (RMB)` |
| **Target Tracking Camera** | `ID_TARGET_CAMERA` | `Left Shift` (Aircraft) / `RMB` (Ground & Heli) |
| **Lock Target** | `ID_LOCK_TARGET` | `Middle Mouse Button (MMB)` / `X` |
| **Cockpit View** | `ID_CAMERA_FPS` | `F2` |
| ** External (3rd Person) View** | `ID_CAMERA_TPS` | `F3` |
| **Virtual Cockpit View** | `ID_CAMERA_VIRTUAL_FPS` | `F4` / `Left Shift + F1` |
| **Default View** | `ID_CAMERA_DEFAULT` | `F5` |
| **Gunner View** | `ID_CAMERA_GUNNER` | `F6` |
| **Bombsight / Bomb View** | `ID_CAMERA_BOMBVIEW` | `F7` |
| **Optics / Targeting View** | `ID_CAMERA_OPTICS` | `F8` |
| **Follow Bomb / Shell / Torpedo** | `ID_CAMERA_FOLLOW_OBJECT` | `U` |
| **Look Back** | `ID_CAMERA_VIEW_BACK` | `.` (Period) |
| **Look Down** | `ID_CAMERA_VIEW_DOWN` | `;` (Semicolon) |

### Aircraft Controls
| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Pitch Down / Up** | `elevator_rangeMin` / `Max` | `W` / `S` *(Custom Override)* |
| **Roll Left / Right** | `ailerons_rangeMin` / `Max` | `A` or `Left Arrow` / `D` or `Right Arrow` |
| **Yaw (Rudder) Left / Right** | `rudder_rangeMin` / `Max` | `Q` / `E` |
| **Throttle Up / Down** | `throttle_rangeMax` / `Min` | `Page Up` / `Page Down` / `Mouse Wheel` *(Custom Override)* |
| **Wheel Brakes (Left & Right)** | `brake_left` / `right_rangeMax` | `B` |
| **Fire Small-Caliber Guns (MGs)** | `ID_FIRE_MGUNS` | `Left Mouse Button (LMB)` / `1` |
| **Fire Large-Caliber Guns (Cannons)** | `ID_FIRE_CANNONS` | `Left Mouse Button (LMB)` / `2` |
| **Fire Additional Guns** | `ID_FIRE_ADDITIONAL_GUNS` | `Left Mouse Button (LMB)` / `2` |
| **Fire Primary Weapons** | `ID_FIRE_PRIMARY` | `Left Mouse Button (LMB)` |
| **Fire Secondary Weapons** | `ID_FIRE_SECONDARY` | `Space` |
| **Drop Bomb** | `ID_BOMBS` | `Space` / `Mouse Button 4` |
| **Drop Bomb Series** | `ID_BOMBS_SERIES` | `Space` *(Hold)* *(Custom Override)* |
| **Drop Guided Bombs** | `ID_GUIDED_BOMBS` | `Left Alt + Space` / `3` / `Mouse Button 4` |
| **Fire Rockets** | `ID_ROCKETS` | `Left Ctrl` / `Mouse Button 5` |
| **Fire Air-to-Ground Missile (AGM)** | `ID_AGM` | `Space` |
| **Fire Air-to-Air Missile (AAM)** | `ID_AAM` | `Left Alt + Left Ctrl` |
| **Weapon Lock (AAM / AGM)** | `ID_WEAPON_LOCK` | `Left Alt + X` |
| **Lock Guided Bombs** | `ID_GUIDED_BOMBS_LOCK` | `Left Alt + V` |
| **Lock AGM** | `ID_AGM_LOCK` | `Left Alt + C` |
| **Switch Primary Weapons** | `ID_SWITCH_SHOOTING_CYCLE_PRIMARY` | `Left Alt + 1` |
| **Switch Secondary Weapons** | `ID_SWITCH_SHOOTING_CYCLE_SECONDARY` | `Left Alt + 2` |
| **Secondary Weapon Ripple Quantity** | `ID_RESIZE_SECONDARY_WEAPON_SERIES` | `Left Alt + 3` |
| **Switch Countermeasures Type** | `ID_SWITCH_SHOOTING_CYCLE_COUNTER_MEASURE` | `Left Alt + 4` |
| **Exit Weapon Selection Mode** | `ID_EXIT_SHOOTING_CYCLE_MODE` | ``Left Alt + ` `` |
| **Open Visual Weapon Selector** | `ID_OPEN_VISUAL_WEAPON_SELECTOR` | `Caps Lock` |
| **Dispense Countermeasures / Flares** | `ID_FLARES` | `Left Alt + E` |
| **Reload Guns** | `ID_RELOAD_GUNS` | `R` |
| **Toggle Flaps** | `ID_FLAPS` | `F` |
| **Flaps Up / Down** | `ID_FLAPS_UP` / `ID_FLAPS_DOWN` | `[` / `]` |
| **Toggle Airbrake** | `ID_AIR_BRAKE` | `H` |
| **Toggle Landing Gear** | `ID_GEAR` | `G` |
| **Drag Chute** | `ID_CHUTE` | `Left Alt + G` |
| **Toggle Engine** | `ID_TOGGLE_ENGINE` | `I` |
| **Ignite Boosters** | `ID_IGNITE_BOOSTERS` | `Left Ctrl + Left Alt + B` *(Custom Override)* |
| **Fire Extinguisher** | `ID_TOGGLE_EXTINGUISHER` | `6` |
| **VTOL Thrust Vector Up / Down** | `vtol_rangeMax` / `Min` | `Left Alt + J` / `Left Alt + U` |
| **Weapon Aiming (Manual MCLOS)** | `weapon_aim_pitch` / `heading` | `Left Alt + W/S/A/D` |
| **Toggle Laser Designator** | `ID_TOGGLE_LASER_DESIGNATOR` | `Left Alt + L` |
| **Night Vision / Thermal (Aircraft)** | `ID_PLANE_NIGHT_VISION` | `Left Alt + N` |
| **Activate Target Point / Lock** | `ID_LOCK_TARGETING` / `AT_POINT` | `Left Alt + LMB` / `Left Alt + MMB` |
| **Deactivate Target Point** | `ID_UNLOCK_TARGETING` / `AT_POINT` | `Left Alt + RMB` / `Left Alt + Backspace` |
| **Switch Radar / IRST On/Off** | `ID_SENSOR_SWITCH` | `Left Alt + R` |
| **Switch Radar / IRST Search Mode** | `ID_SENSOR_TYPE_SWITCH` | `Left Alt + A` |
| **Radar Beyond/Within Visual Range (ACM)** | `ID_SENSOR_ACM_SWITCH` | `Left Alt + W` |
| **Switch Radar Scan Pattern** | `ID_SENSOR_SCAN_PATTERN_SWITCH` | `Left Alt + D` |
| **Switch Radar Scope Scale (Range)** | `ID_SENSOR_RANGE_SWITCH` | `Left Alt + Q` |
| **Select Radar/IRST Target to Lock** | `ID_SENSOR_TARGET_SWITCH` | `Left Alt + T` |
| **Lock Radar/IRST on Target** | `ID_SENSOR_TARGET_LOCK` | `Left Alt + F` |
| **Toggle Radar GUI Control Mode** | `ID_TOGGLE_AIR_RADAR_GUI_CONTROL_MODE` | `Left Alt + Y` |
| **Toggle Control Mode** | `ID_CONTROL_MODE` | `Left Alt + H` |
| **Trim Aircraft** | `ID_TRIM` | `T` / `Page Up` |
| **Aerobatics Smoke** | `ID_AEROBATICS_SMOKE` | `L` |
| **Toggle Collimator Sight** | `ID_TOGGLE_COLLIMATOR` | `'` (Apostrophe) |

### Helicopter Controls
| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Collective Pitch / Climb Up & Down** | `helicopter_collective_rangeMax` / `Min` | `W` / `S` (and `Mouse Wheel`) |
| **Cyclic Pitch Down / Up** | `helicopter_cyclic_pitch_rangeMin` / `Max` | `Left Shift` or `Page Up` / `Left Ctrl` or `Page Down` |
| **Cyclic Roll Left / Right** | `helicopter_cyclic_roll_rangeMin` / `Max` | `A` / `D` |
| **Tail Rotor Pedals Left / Right** | `helicopter_pedals_rangeMin` / `Max` | `Q` / `E` |
| **Hover Mode / FBW Mode** | `ID_CONTROL_MODE_HELICOPTER` | `H` |
| **Manual Roll Control Mode** | `ID_MANEUVERABILITY_MODE_HELICOPTER` | `Left Alt + M` |
| **Fire Guns / Cannons** | `ID_FIRE_MGUNS` / `CANNONS_HELICOPTER` | `Left Mouse Button (LMB)` / `1`, `2` |
| **Fire Rockets** | `ID_ROCKETS_HELICOPTER` | `4` *(Custom Override)* |
| **Fire Rocket Salvo** | `ID_ROCKETS_SERIES_HELICOPTER` | `Mouse Button 5` *(Custom Override)* |
| **Fire ATGM** | `ID_ATGM_HELICOPTER` | `Space` |
| **Fire Air-to-Air Missile (AAM)** | `ID_AAM_HELICOPTER` | `Left Alt + Space` |
| **Drop Bombs / Guided Bombs** | `ID_BOMBS_HELICOPTER` | `3` / `Mouse Button 4` |
| **Stabilize Sight / Lock Target Point** | `ID_LOCK_TARGETING_AT_POINT_HELICOPTER` | `F` |
| **Weapon Lock** | `ID_WEAPON_LOCK_HELICOPTER` | `Left Alt + X` |
| **Toggle Laser Designator** | `ID_TOGGLE_LASER_DESIGNATOR` | `Left Alt + L` |

### Ground Vehicle (Tank) Controls
| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Drive Forward / Backward** | `gm_throttle_rangeMax` / `Min` | `W` or `Up Arrow` / `S` or `Down Arrow` |
| **Steer Left / Right** | `gm_steering_rangeMax` / `Min` | `A` or `Left Arrow` / `D` or `Right Arrow` |
| **Cruise Control (Gear Up / Down)** | `ID_TRANS_GEAR_UP` / `DOWN` | `E` / `Q` |
| **Toggle Engine** | `ID_TOGGLE_GM_ENGINE` | `I` |
| **Fire Main Gun** | `ID_FIRE_GM` | `Left Mouse Button (LMB)` |
| **Fire Secondary Gun** | `ID_FIRE_GM_SECONDARY_GUN` | `Left Mouse Button (LMB)` |
| **Fire Machine Gun** | `ID_FIRE_GM_MACHINE_GUN` | `Space` |
| **Fire Special Gun** | `ID_FIRE_GM_SPECIAL_GUN` | `R` |
| **Select Primary Gun** | `ID_SELECT_GM_GUN_PRIMARY` | `Left Alt + 1` |
| **Select Secondary Gun** | `ID_SELECT_GM_GUN_SECONDARY` | `Left Alt + 2` |
| **Select Machine Gun** | `ID_SELECT_GM_GUN_MACHINEGUN` | `Left Alt + 3` |
| **Select Special Gun** | `ID_SELECT_GM_GUN_SPECIAL` | `Left Alt + F` |
| **Reset Weapon Selection** | `ID_SELECT_GM_GUN_RESET` | ``Left Alt + ` `` |
| **Sniper Mode (Gunner Sight)** | `ID_TOGGLE_VIEW_GM` | `Left Shift` |
| **Binoculars** | `ID_CAMERA_BINOCULARS` | `B` |
| **Zoom / Target Tracking** | `ID_ZOOM_TOGGLE` / `ID_TARGETING_HOLD_GM` | `Right Mouse Button (RMB)` |
| **Rangefinder** | `ID_RANGEFINDER` | `Left Alt + X` / `Mouse Button 5` |
| **Night Vision / Thermal Sight** | `ID_TANK_NIGHT_VISION` | `Left Alt + C` / `Mouse Button 4` |
| **Action Bar Items 1–4 (Shells)** | `ID_ACTION_BAR_ITEM_1..4` | `1`, `2`, `3`, `4` |
| **Artillery Strike** | `ID_ACTION_BAR_ITEM_5` | `5` (Confirm: `LMB`, Switch Mode: `MMB`, Cancel: `Esc`) |
| **Fire Extinguisher** | `ID_TOGGLE_EXTINGUISHER` | `6` |
| **Crew Replenishment / Action 7–12** | `ID_ACTION_BAR_ITEM_7..12` | `7`, `8`, `9`, `0`, `-`, `=` |
| **Field Repair** | `ID_REPAIR_TANK` | `F` *(Hold)* |
| **Repair Tracks** | `ID_REPAIR_TRACKS` | `F8` |
| **Smoke Grenades** | `ID_SMOKE_SCREEN` | `G` |
| **Engine Smoke Screen System (ESS)** | `ID_SMOKE_SCREEN_GENERATOR` | `H` |
| **Active Scouting** | `ID_SCOUT` | `V` |
| **Launch Scout UAV** | `ID_SCOUT_UAV` | `C + V` |
| **Switch To / Orbit Scout UAV** | `ID_START_SUPPORT_PLANE` / `ORBITING` | `Left Alt + U` / `H` |
| **Toggle Scout UAV Camera** | `ID_TOGGLE_UAV_CAMERA` | `Left Alt + H` |
| **Switch Radar / IRST On/Off (Tank)** | `ID_SENSOR_SWITCH_TANK` | `Left Alt + R` |
| **Select Radar / IRST Target (Tank)** | `ID_SENSOR_TARGET_SWITCH_TANK` | `Left Alt + T` |
| **Lock Radar / IRST on Target (Tank)** | `ID_SENSOR_TARGET_LOCK_TANK` | `Left Alt + F` |
| **Weapon Lock (Tank ATGM / SAM)** | `ID_WEAPON_LOCK_TANK` | `Left Alt + X` |
| **Target Lead Indicator (Tank)** | `ID_WEAPON_LEAD_TANK` | `Left Alt + L` |
| **Toggle Auto-Turret Targets** | `ID_TOGGLE_AUTOTURRET_TARGETS` | `Left Alt + J` |
| **Toggle Entrenching / Dozer Blade** | `ID_GM_TERRAFORM_TOGGLE` | `Left Ctrl + T` |
| **AA Complex Menu** | `ID_TOGGLE_AA_COMPLEX_MENU` | `C + R` |
| **Reload Custom User Sight** | `ID_RELOAD_USER_SIGHT_GM` | `Left Alt + F9` |

### Naval Controls
Full Action Bar icon reference: [`WT-Bluewater_Icon.md`](file:///home/sticks/zets/WT-Bluewater_Icon.md).

| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Ahead / Astern (Throttle)** | `ship_main_engine_rangeMax` / `Min` | `W` or `Up Arrow` / `S` or `Down Arrow` |
| **Stop Engines** | `ship_main_engine_rangeSet` | `W + S` |
| **Full Stop (Emergency Brake)** | `ID_SHIP_FULL_STOP` | `B` |
| **Rudder Left / Right** | `ship_steering_rangeMax` / `Min` | `A` or `Left Arrow` / `D` or `Right Arrow` |
| **Fire All / Selected Guns** | `ID_SHIP_WEAPON_ALL` | `Left Mouse Button (LMB)` |
| **Ranging Shot (Single Turret)** | `ID_SINGLE_SHOT_SHIP` | `Left Ctrl + LMB` |
| **Select Primary Calibers** | `ID_SHIP_WEAPON_PRIMARY` | `Left Alt + 1` |
| **Select Secondary Calibers** | `ID_SHIP_WEAPON_SECONDARY` | `Left Alt + 2` |
| **Select AA / Machine Guns** | `ID_SHIP_WEAPON_MACHINEGUN` | `Left Alt + 3` |
| **Switch Primary/Secondary Trigger** | `ID_SHIP_SWITCH_TRIGGER_GROUP` | `Left Ctrl + E` |
| **Toggle AI Gunners Mode** | `ID_SHIP_TOGGLE_GUNNERS` | `E` |
| **Manual AI Target (Primary / Sec / AA)** | `ID_SHIP_SELECT_TARGET_AI_*` | `X + 1` / `X + 2` / `X + 3` |
| **Torpedo Sight** | `ID_SHIP_TORPEDO_SIGHT` | `Q` |
| **Launch Torpedoes** | `ID_SHIP_WEAPON_TORPEDOES` | `Space` |
| **Drop Depth Charges / Mines** | `ID_SHIP_WEAPON_DEPTH_CHARGE` / `MINE` | `Left Ctrl` |
| **Fire Rockets / Mortar** | `ID_SHIP_WEAPON_ROCKETS` / `MORTAR` | `R` |
| **Depth Charge Fuse Cycle** | `ID_SHIP_BOMB_CYCLE_DEPTH` | `Left Alt + X` / `Left Alt + C` |
| **Aiming / Gunner View** | `ID_TOGGLE_VIEW_SHIP` | `Left Shift` |
| **Binoculars** | `ID_CAMERA_BINOCULARS` | `B` |
| **Lock Target** | `ID_LOCK_TARGET` | `Middle Mouse Button (MMB)` / `X` |
| **Shell Types / Action Bar 1–4** | `ID_SHIP_ACTION_BAR_ITEM_1..4` | `1`, `2`, `3`, `4` |
| **Artillery Support** | `ID_SHIP_ACTION_BAR_ITEM_5` | `5` |
| **Fire Extinguisher / Damage Preset 1** | `ID_TOGGLE_EXTINGUISHER` / `PRESET_1` | `6` |
| **Repair Modules / Damage Preset 2** | `ID_SHIP_ACTION_BAR_ITEM_11` / `PRESET_2` | `7` / `F` |
| **Pump Water / Breaches / Preset 3** | `ID_REPAIR_BREACHES` / `PRESET_3` | `8` |
| **Smoke Screen Generator** | `ID_SHIP_SMOKE_SCREEN_GENERATOR` | `G` |
| **Launch Catapult Recon Plane** | `ID_START_SUPPORT_PLANE_SHIP` | `U` (Orbit: `H`) |

### Spectator & Replay Controls
Full reference: [`Spectator-keybinds.md`](file:///home/sticks/zets/Spectator-keybinds.md).

| Action | Action ID | Active Binding |
| :--- | :--- | :--- |
| **Camera Forward / Backward** | `cam_fwd_rangeMax` / `Min` | `W` or `Left Shift` / `S` or `Left Ctrl` |
| **Camera Strafe Left / Right** | `cam_strafe_rangeMin` / `Max` | `A` / `D` |
| **Camera Up / Down** | `cam_vert_rangeMax` / `Min` | `E` / `Q` |
| **Spectator Camera Rotate** | `ID_SPECTATOR_CAMERA_ROTATION` | `Right Mouse Button` *(Hold)* + Mouse |
| **Previous / Next Player** | `ID_PREV_PLANE` / `ID_NEXT_PLANE` | `[` / `]` |
| **Toggle Following Camera** | `ID_TOGGLE_FOLLOWING_CAMERA` | `;` |
| **Pause / Resume Replay** | `ID_REPLAY_PAUSE` | `Space` |
| **Replay Speed Faster / Slower** | `ID_REPLAY_FASTER` / `SLOWER` | `Page Up` / `Page Down` |
| **Replay Camera Zoom In / Out** | `ID_REPLAY_CAMERA_ZOOM_IN` / `OUT` | `Insert` / `Delete` |
| **Replay Camera Modes** | `ID_REPLAY_CAMERA_*` | `Left Ctrl + F1`..`F6` (Gun, Wing, Flyby, Operator, Free, Random) |
| **Replay Toggle Markers** | `ID_REPLAY_SHOW_MARKERS` | `.` (Period) |

---

## 3. Control & Sensitivity Settings (`machine.blk`)

### Mouse Sensitivity
- **Mouse Sensitivity (`mouseSens`):** `0.5`
- **Mouse Aim Sensitivity (`mouseAimSens`):** `0.5`
- **Gunner View Sensitivity (`gunnerViewSens`):** `0.5`
- **Gunner View Zoom Sensitivity (`gunnerViewZoomSens`):** `0.5`
- **Zoom Sensitivity (`zoomSens`):** `0`
- **ATGM Aim Sensitivity (Helicopter):** `1.0`
- **ATGM Aim Zoom Sensitivity (Helicopter):** `0.1`

### Flight Multipliers & Axis Inversion
- **Ailerons / Cyclic Roll Multiplier:** `0.79`
- **Elevator / Cyclic Pitch Multiplier:** `0.64`
- **Rudder / Pedals Multiplier:** `0.43`
- **Invert Y-Axis (All Modes):** `No`
- **Invert X-Axis:** `No`
- **Mouse Smooth:** `No`
- **Hold Throttle for WEP (`holdThrottleForWEP`):** `No`
- **Mouse Joystick (`mouseJoystick`):** `No`

### Camera & Audio Settings
- **Camera Smooth:** `0`
- **Camera Speed:** `0.95`
- **Camera Mouse Speed:** `4.0`
- **Camera FPS Physics Multiplier:** `0.5`
- **Free Camera Inertia:** `1.0`
- **Replay Camera Wiggle:** `1.0`
- **My Engine Volume (`SND_TYPE_MY_ENGINE`):** `0.27` (Enemy/Allied Engines: `1.0`)
- **RWR / VWS Volume:** `0.7`
- **Tinnitus Volume:** `0.5`

---
*Configuration extracted from:* [`~/.config/WarThunder/Saves/last/production/machine.blk`](file:///home/sticks/.config/WarThunder/Saves/last/production/machine.blk)  
*Last Updated:* October 19, 2026

