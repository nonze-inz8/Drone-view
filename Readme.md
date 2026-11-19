# Drone View

[![Game](https://img.shields.io/badge/Game-Nuclear%20Option-red.svg)](https://store.steampowered.com/app/2168680/Nuclear_Option/)
[![Framework](https://img.shields.io/badge/Framework-BepInEx%205-blue.svg)](https://github.com/BepInEx/BepInEx)
[![Version](https://img.shields.io/badge/Version-1.0.0-green.svg)](https://github.com/Nonze/Drone-View/releases)
[![Author](https://img.shields.io/badge/Author-Nonze-purple.svg)](#)

An autonomous tactical reconnaissance UAV mod for **Nuclear Option**.

This mod allows pilots to deploy an orbital surveillance drone directly from the Tactical Map, switch to its live optical/thermal camera feed mid-flight, designate targets for onboard weapon systems, and monitor active ordnance in real time.

---

## Key Features

### 1. Tactical Map Deployment & Economy
- **Direct Map Tasking:** Open the Tactical Map (`M`), configure flight duration (**1 to 15 minutes**), click **DEPLOY DRONE**, and designate any target zone on the map.
- **Balanced Resource Cost:** Each minute of UAV operation costs `$2.0M` (configurable) deducted directly from your player allocation balance.
- **Inbound & Cooldown Timers:** Features a realistic **10-second** deployment timer upon launch and a **7-minute** cooldown after battery depletion or manual recall.

### 2. Autonomous Orbit & Dynamic Relocation
- **Hands-Free Surveillance:** The UAV automatically orbits the designated area at **5,000 m** altitude (1,500 m radius, 150 m/s), letting you focus on flying and engaging targets.
- **Live Map Overlay:** Displays the drone's orbital position, surveillance zone radius, and remaining battery timer directly on the Tactical Map.
- **Mid-Mission Relocation:** Need to shift focus? Click **CHANGE POS** on the map to move the drone to a new sector (**7-second** transit) without resetting its remaining battery.

### 3. Military MFD & Thermal Sensor Suite
- **Authentic MFD Symbology:** Clean, adaptive military display scaled automatically for 1080p, 1440p, 4K, and ultrawide monitors.
- **Multi-Mode Optics:** Cycle between **CCD** (Daylight TV), **WHOT** (White-Hot Thermal), and **BHOT** (Black-Hot Thermal) sensors with `K`.
- **Balanced Recon Limits:** Capped at a 14 km render distance and 12 km hostile marker detection range to preserve tactical balance.

### 4. Realistic Datalink & EW Jamming Interference
- **Authentic UAV Feed:** Simulated 720p tactical datalink with subtle scanlines, compression grain, and lens vignette.
- **Electronic Warfare Effects:** Nearby enemy **Radar Jamming Pods** and EW interference degrade the video signal with static and glitch bars, resulting in a full `NO SIGNAL // EW JAMMING` blackout under heavy jamming.

### 5. Target Designation & Live Ordnance Tracker
- **Zoom-Stable Tracking:** Lock ground coordinates (**AREA**) or moving enemy units (**POINT**) without reticle drift across zoom levels.
- **Direct Weapon Integration:** Select and deselect targets directly through the drone feed for your aircraft's weapons.
- **Ordnance Telemetry:** Displays active missiles and bombs with target designations and **TOF (Time of Flight)** countdowns on the right side of the MFD — showing all active ordnance in `AREA`/`INR` mode, or filtering exclusively to your locked target in `POINT` mode.

---

## Controls

| Key | Action |
| :--- | :--- |
| **`M`** | Open Tactical Map (Deploy / Relocate / Recall / Rebind Key) |
| **`J`** *(rebindable)* | Switch to Drone View / Return to Aircraft |
| **`Mouse`** | Slew camera optics |
| **`Mouse Wheel`** | Zoom in / out |
| **`LMB`** | Select target / Lock unit (`POINT`) or ground (`AREA`) / Unlock |
| **`RMB`** / **`Backspace`** | Deselect target / Clear track |
| **`K`** | Cycle sensor mode (`CCD` / `WHOT` / `BHOT`) |

- **In-Game Key Rebinding:** Click `VIEW KEY` on the Tactical Map panel while the drone is active to assign a custom toggle key (persisted across sessions).
- **Auto-Return:** Opening the map, pause menu, switching cameras, or losing your aircraft automatically returns the view to your cockpit.

---

## Installation

### Prerequisites
- Ensure you have [BepInEx 5.4.x (x64)](https://github.com/BepInEx/BepInEx/releases) installed in your game directory.

### Setup
1. Download the latest `DroneViewMod.dll` from the [Releases](https://github.com/Nonze/Drone-View/releases) section.
2. Navigate to your Nuclear Option installation folder:
   ```text
   ...\Steam\steamapps\common\Nuclear Option\BepInEx\plugins\
