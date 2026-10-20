---
created: 2026-01-06
updated: 2026-10-19
---
# War Thunder Naval Action Bar Icons & Keybindings

Reference for the Naval Action Bar icons, damage control presets (`USEROPT_SHIP_PRESET_BASED_DAMAGE_CONTROL:b=yes`), and naval combat keybindings configured in [`machine.blk`](file:///home/sticks/.config/WarThunder/Saves/last/production/machine.blk) (see [`WT-Keys.md`](file:///home/sticks/zets/WT-Keys.md)).

## 1. Naval Action Bar & Damage Control Keys

| Active Key | Action ID | Action | Icon Description | Function in Naval Battles |
| :---: | :--- | :--- | :--- | :--- |
| **`1`** | `ID_SHIP_ACTION_BAR_ITEM_1` | **Shell Type 1** | Shell casing with an explosion symbol (typically **HE**). | Loads the first ammunition type for the active weapon group. |
| **`2`** | `ID_SHIP_ACTION_BAR_ITEM_2` | **Shell Type 2** | Shell casing penetrating an armor plate (typically **AP** / **SAP**). | Loads the second ammunition type for the active weapon group. |
| **`3`** | `ID_SHIP_ACTION_BAR_ITEM_3` | **Shell Type 3** | Penetrating shell with internal burst or proximity fuse (**APHE** / **HE-VT**). | Loads the third ammunition type (if equipped). |
| **`4`** | `ID_SHIP_ACTION_BAR_ITEM_4` | **Shell Type 4** | Specialized shell icon. | Loads the fourth ammunition type (if equipped). |
| **`5`** | `ID_SHIP_ACTION_BAR_ITEM_5` / `ID_SHIP_KILLSTREAK_WHEEL_MENU` | **Artillery Support / Event Wheel** | Binocular reticle or mortar/shell icon. | Calls offshore artillery support (`LMB` to fire, `MMB` to toggle view, `Esc` to cancel). |
| **`6`** | `ID_TOGGLE_EXTINGUISHER` / `ID_SHIP_DAMAGE_CONTROL_PRESET_1` | **Fire Extinguishing / Damage Preset 1** | Flame with nozzle/extinguisher cylinder. | Triggers fire extinguishing or activates Damage Control Preset 1 (Firefighting priority). |
| **`7`** / **`F`** | `ID_SHIP_ACTION_BAR_ITEM_11` / `ID_SHIP_DAMAGE_CONTROL_PRESET_2` | **Field Repair / Damage Preset 2** | Crossed hammer and wrench. | Initiates module repairs (guns, engines, steering) or activates Damage Control Preset 2. |
| **`8`** | `ID_REPAIR_BREACHES` / `ID_SHIP_DAMAGE_CONTROL_PRESET_3` | **Sealing Bulkheads & Pumps / Preset 3** | Water waves with pump/valve symbol. | Repairs hull breaches and pumps water to stop flooding, or activates Damage Control Preset 3. |
| **`9`** / **`0`** | `ID_SHIP_ACTION_BAR_ITEM_10` | **Ship-Specific Utilities** | Varies by vessel. | Activates auxiliary action bar items. |
| **`G`** | `ID_SHIP_SMOKE_SCREEN_GENERATOR` | **Smoke Screen Generator** | Smoke cloud / stern generator trail. | Deploys a smoke screen from the stern or funnels to conceal the vessel. |
| **`U`** | `ID_START_SUPPORT_PLANE_SHIP` | **Launch Catapult Recon Aircraft** | Floatplane / catapult aircraft icon. | Launches the shipboard reconnaissance aircraft (`H` to toggle orbiting). |

## 2. Naval Weapon Group & Fire Control Shortcuts

| Active Key | Action ID | Function |
| :---: | :--- | :--- |
| **`Left Alt + 1`** | `ID_SHIP_WEAPON_PRIMARY` | Switch control to Primary Caliber guns |
| **`Left Alt + 2`** | `ID_SHIP_WEAPON_SECONDARY` | Switch control to Secondary Caliber guns |
| **`Left Alt + 3`** | `ID_SHIP_WEAPON_MACHINEGUN` | Switch control to Anti-Aircraft (AA) / Machine Guns |
| **`Left Ctrl + E`** | `ID_SHIP_SWITCH_TRIGGER_GROUP` | Toggle combined primary/secondary trigger group |
| **`E`** | `ID_SHIP_TOGGLE_GUNNERS` | Cycle AI gunners mode (All / AA Only / Surface Only / Off) |
| **`X + 1` / `2` / `3`** | `ID_SHIP_SELECT_TARGET_AI_*` | Designate manual target for AI Primary (`X+1`), Secondary (`X+2`), or AA (`X+3`) gunners |
| **`Left Ctrl + LMB`** | `ID_SINGLE_SHOT_SHIP` | Fire a single ranging shot from one turret |
| **`Q`** / **`Space`** | `ID_SHIP_TORPEDO_SIGHT` / `TORPEDOES` | Toggle Torpedo Sight (`Q`) and Launch Torpedoes (`Space`) |
| **`Left Ctrl`** | `ID_SHIP_WEAPON_DEPTH_CHARGE` / `MINE` | Drop Depth Charges or Naval Mines |
| **`R`** | `ID_SHIP_WEAPON_ROCKETS` / `MORTAR` | Fire Naval Rockets or Mortars |
| **`B`** | `ID_SHIP_FULL_STOP` / `ID_CAMERA_BINOCULARS` | Emergency Full Stop (`W + S` stops engines) & Binoculars |

