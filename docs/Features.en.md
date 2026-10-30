# Features

Complete overview of all functions of the SC Deutsch Launcher (SCDL), with explanations and where to find each one in the interface. Screenshots are placeholders and will be replaced with real captures before release.

Back to: [README](../README.en.md)

🌐 [Deutsch](Features.md) · **English**

Ordered by what you see or use first in the launcher, not by technical importance. All modules are weighted equally.

## Contents

- [Initial setup](#initial-setup)
- [Dashboard](#dashboard)
- [Translation](#translation)
- [Channels and status](#channels-and-status)
- [Blueprints](#blueprints)
- [Strings and item values](#strings-and-item-values)
- [Background updates](#background-updates)
- [Profile backup](#profile-backup)
- [Playtime statistics](#playtime-statistics)
- [Troubleshooting](#troubleshooting)
- [SC settings](#sc-settings)
- [Startup programs](#startup-programs)
- [Cache Cleaner](#cache-cleaner)
- [System info](#system-info)
- [Overlay](#overlay)
- [Joysticks and bindings](#joysticks-and-bindings)
- [Streamer mode](#streamer-mode)
- [What's new](#whats-new)
- [Interface and window](#interface-and-window)
- [Command line and diagnostics](#command-line-and-diagnostics)

---

## Initial setup

### First-run wizard

On the very first launch, a wizard guides you step by step through setup: find the installation path or enter it manually, choose a channel, choose a translation variant. No technical knowledge required.

**How to reach it:** Starts automatically on the first program launch. Afterwards it can be triggered again via "Reset settings".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/029ce231-aa35-49ce-ad68-6a4fb98b9af2" />

---

## Dashboard

### Tile overview

Info column and tiles in the main window, the first thing you see after launch. Shows the most important metrics at a glance: channel status, latest backups, playtime, blueprint progress and other freely selectable tiles.

**How to reach it:** Main window → "Dashboard" tab. Which tiles appear and in what order is set by "Set up dashboard" via drag and drop.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/18a14b93-0f47-4436-8044-cc4c7e812715" />

<img width="1254" height="776" alt="dashboard" src="https://github.com/user-attachments/assets/937d5245-1895-4924-9fd5-e37b0688fb21" />

Further tiles: **Translation** (status per channel with traffic-light dot, game version and update button), **Location** (last place from the `Game.log`: start of a quantum route or opened inventory) and **Input devices** (connected joysticks and gamepads; with the "Bindings" module it also shows whether the joystick order is still correct).

---

## Translation

### Automatic path detection

Finds the Star Citizen installation on its own, so you don't have to search for folders.

**How to reach it:** Runs automatically at startup and in the first-run wizard.

### Manual path setting

If you have an unusual installation (e.g. on a second drive or via a symlink), you can set the path per channel by hand.

**How to reach it:** Settings → "Installations" tab → edit path.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/7abdd069-1763-47fb-94fa-1beabb7dfa90" />

### Language variants

Each channel has two freely nameable language buttons. Behind them is either a translation from the catalog (Deutsch, Deutsch+, Schwiizerdütsch, Français, Italiano, Português, 日本語, English directly from the `Data.p4k`) or a source URL you enter yourself. The launcher keeps already installed language files up to date automatically through version comparison (ETag).

**How to reach it:** Settings → "Languages" tab → choose a source per channel, or in the main window via "Choose language" to adopt one from the catalog.

### Repair translation

Resets the translation of a channel and installs it again. Helpful if a game update has overwritten the `global.ini`.

**How to reach it:** Main window → channel tile → "Repair".

---

## Channels and status

### Multi-channel management

LIVE, HOTFIX, PTU and TECH-PREVIEW are handled separately: own path, own language source, own traffic-light status, own backup. HOTFIX shares its language source with LIVE. PTU and TECH-PREVIEW start without a source of their own (English from the `Data.p4k`); you can enter one yourself.

**How to reach it:** Channel tiles in the main window, one tab per channel.

### Traffic-light status per channel

Green, yellow, red or gray shows at a glance, separately for each channel, whether a translation is up to date, outdated, faulty or not set up.

**How to reach it:** Visible directly on each channel tile in the main window and on the tray icon.

### Channel quick switch (experimental)

A power switch directly on the channel header to quickly turn a translation on or off without opening the settings.

**How to reach it:** Settings → enable the module switch "Channel quick switch" (off by default), then use the switch on the channel header.

---

## Blueprints

### Blueprint patching into mission texts

New ships and weapons often come with blueprints whose template texts are not yet translated. The SCDL automatically builds blueprint and mission details into the `global.ini`. The data comes from scmdb.net and is updated automatically.

**How to reach it:** Runs automatically after every translation update. Can be triggered manually via main window → "Blueprints" → "Rebuild".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/1f26b60a-fe59-469a-a1f7-52f514fce9e6" />

### Obtained blueprints overview

Keeps track of which blueprints have already been obtained, so that their template texts are no longer marked as "missing". Can be viewed, searched and adjusted by hand.

**How to reach it:** Main window → "Blueprints" → "Done" tab.

### Reading obtained blueprints from the Game.log

Scans the `Game.log` for hints of obtained blueprints and automatically adds them to the Done list, also as a live recording while you play.

**How to reach it:** Automatically in the background while Star Citizen is running. Manual scan via "Blueprints" → "Scan log".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/a657a098-846f-4fda-89b2-394e8c1162a6" />

### Back up and restore the obtained-blueprints file

The Done list can be exported, imported or reset without losing the rest of your blueprint progress.

**How to reach it:** "Blueprints" → "Done" tab → "Back up/Import" menu.

---

## Strings and item values

### Weapon and component texts

Adds the German translation to StarStrings texts for weapons, shields and other components, divided into four categories.

**How to reach it:** Runs automatically with the translation update. Setting under Settings → "Blueprints & Strings".

### Item values in descriptions

Fills real numeric values (damage, range, etc.) from the item stats data into the German item descriptions instead of leaving placeholder texts.

**How to reach it:** Active automatically, can be turned off via Settings → module switch "Item values".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/4bd4abea-1b35-4aa5-a208-21e0bbe3f8a0" />

---

## Background updates

### Automatic update schedule

Checks in the background at a fixed interval whether a new translation or new blueprints are available, and installs them quietly without interrupting the running game.

**How to reach it:** Runs automatically, no interaction needed. The interval can be viewed in the settings.

### Fallback on server outage

If the translation server is unreachable, the launcher reports this clearly and keeps working with the last known state instead of piling up errors.

**How to reach it:** Appears automatically as a notice banner as soon as an outage is detected.

### Update after game exit

Automatically detects when Star Citizen has been closed and then catches up on any updates left pending.

**How to reach it:** Automatic, based on process monitoring.

### Launcher self-update

The launcher updates itself via GitHub Releases, including a checksum comparison before installation.

**How to reach it:** Automatically at startup, with a notice before installation.

---

## Profile backup

### ZIP backup of user data

Backs up key bindings and other user data per channel as a ZIP archive, with automatic rotation of older versions.

**How to reach it:** Main window → "Profile backup" tab → guided flow: choose a profile → select what to back up → create backup.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/9ebe50b4-deae-4888-8836-96f3934619b1" />

### Restore

Restores an existing backup without losing files added since then or overwriting the backup itself.

**How to reach it:** "Profile backup" tab → select a backup → "Restore".

If a backup has been imported, the launcher does not put any contained scripts in their place but in a separate folder for review. Scripts from foreign backups could execute arbitrary code.

---

## Playtime statistics

### Evaluation from the Game.log

Reads the log files and shows playtime per session, obtained blueprints and other metrics, without Star Citizen itself having to be running. The mission statistics show mission type, party and failed objectives.

**How to reach it:** Main window → "Playtime" tab.

### Export of the statistics

The collected data can be exported, for example for your own analyses.

**How to reach it:** "Playtime" tab → "Export".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/65211b5c-ebc5-44a0-9dd2-9125c35011b2" />

---

## Troubleshooting

### Read-only system scan

Checks installation, paths and configuration without changing anything, and shows any problems found in an understandable way.

**How to reach it:** Main window → "Troubleshooting" tab → "Start scan".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/8888639a-5dde-41b5-a004-f5485f5a790c" />

### Path repair

Automatically fixes detected path problems, where this can be done unambiguously.

**How to reach it:** After the scan → "Repair" on the affected entries.

### Error report as ZIP

Bundles relevant logs and diagnostic data into a ZIP file for support, without credentials or personal content.

**How to reach it:** "Troubleshooting" tab → "Create error report".

---

## SC settings

### Graphics and display settings

Shows and changes selected Star Citizen settings (display, upscaling) directly from the launcher, separately per channel, without having to start the game.

**How to reach it:** Main window → "SC settings" tab.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/10978bee-465a-4e22-b7ca-425fbe5066a7" />

### user.cfg management

Edits the installation's `user.cfg` conveniently through the interface.

**How to reach it:** "SC settings" tab → "user.cfg".

---

## Startup programs

### Launch your own programs alongside

Automatically starts defined programs or scripts when the RSI Launcher or Star Citizen starts, such as voice tools or overlays (`.exe` as the target of a script is excluded, opt-in required). Window mode and wait time can be set per entry.

**How to reach it:** Settings → enable the module switch "Startup programs" (off by default), then "Startup programs" tab → add an entry.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/97ec9a79-0d30-45ae-adfd-62ca32977bba" />

---

## Cache Cleaner

### Clear shader cache

Deletes the Star Citizen shader cache with one click. Helps with graphics glitches after updates.

**How to reach it:** Cache Cleaner button in the title bar, dashboard tile "Cache" or tray → "Clean cache". Opens a modal in the main window.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/00d68527-422e-4ba6-8dd8-5522a8433062" />

---

## System info

### System data at a glance

Clearly shows relevant system information (hardware, drivers, paths), helpful for error reports.

**How to reach it:** Title bar → "System info" icon (or click the graphics or performance tile in the dashboard).

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/08f9f9c7-64a3-422f-b38b-d07188b33e5b" />

---

## Overlay

### Live bar above the game (alpha)

<img width="807" height="413" alt="overlay" src="https://github.com/user-attachments/assets/efb22b50-26ec-4ded-ab3e-2d2c569168c0" />

A small bar, always in the foreground: location, ship, movement, mission with the number of active missions, aUEC and income, server (only while Star Citizen runs), playtime and the latest events live from the `Game.log`. Scan mode reads the signature (RS value) with a hotkey or controller button and shows what is behind it, such as rock with count. Position, opacity and displayed values are adjustable, and the order of the elements can be changed by dragging. Visible only when Star Citizen runs in windowed or borderless mode.

**How to reach it:** Settings → enable the module switch "Overlay (live status)" (off by default), then the title bar icon "Set up overlay".

---

## Joysticks and bindings

### Axes, curves and error analysis (alpha)

<img width="1254" height="776" alt="joysticks" src="https://github.com/user-attachments/assets/34839fee-525a-431f-8c56-a2a2f27a0756" />

Adjusts deadzone, sensitivity and response curves of joysticks and gamepads and shows modifier overviews from the `actionmaps.xml`. A backup is created before every write. If Star Citizen is running, the launcher warns you. An error analysis measures noise, drift and stuck keys and generates an anonymized report (copy for Discord or ZIP).

**How to reach it:** Settings → enable the module switch "Joysticks" (off by default).

### Bindings (alpha)

<img width="1254" height="776" alt="bindings" src="https://github.com/user-attachments/assets/64e5cfe5-b3b9-4ba2-b327-043a4bc1d352" />

A separate window for changing key bindings by pressing a key, including modifier combinations. It also shows input devices and the joystick order from the `Game.log`, and imports CIG's factory layouts as well.

**How to reach it:** Settings → enable the module switch "Bindings" (off by default), then the title bar icon.

---

## Streamer mode

Blurs personal details: paths containing the Windows username, character name and location, in the launcher and in the overlay. A click on a blurred spot reveals it until the window loses focus.

**How to reach it:** Settings → "Streamer mode".

---

## What's new

### Release notes of the installed version

Shows the bundled page with the changes in this version. It is part of the program itself; nothing is loaded from the internet.

**How to reach it:** Appears once by itself after an update; any time via the bell in the title bar.

---

## Interface and window

### Tray icon with traffic-light dot

Shows the overall status of all channels directly in the tray, even when the window is closed.

**How to reach it:** Always visible in the Windows taskbar as long as the launcher is running.

### Multilingual interface

The launcher interface itself (not the in-game translation) is available in German, English, Spanish, French, Italian and Russian.

**How to reach it:** Settings → "Interface language".

### Color scheme

Light or dark appearance, optionally following the system.

**How to reach it:** Settings → "Appearance".

### Window size and scaling

Remembers window position and size, and supports zoom levels for different screens.

**How to reach it:** Drag/resize the window as usual, it is remembered automatically. Zoom via Ctrl + mouse wheel or the settings.

---

## Command line and diagnostics

### Command-line modes

The launcher can be controlled without a window and without a tray icon via the command line, for example from batch scripts or the Windows Task Scheduler: `--update`, `--check`, `--bp-reinject` and `--log-scan` per channel (`live`/`hotfix`/`ptu`/`tech-preview`/`all`), plus `--version` and `--export-log`.

**How to reach it:** e.g. `scdlauncher_setup.exe --update=live,hotfix` or `scdlauncher_setup.exe --check=all` in a console. If the SCDL is already running, the call aborts instead of writing to the same files.

### Debug console

Pressing F12 in the main window opens a self-test for system, configuration, paths and server reachability. Helpful for bug reports.

**How to reach it:** Main window → F12 → "Run checks" → "Export".

### Activity log

Shows a running log of launcher activity for troubleshooting.

**How to reach it:** Open the debug window (see Troubleshooting / support notes).
