<h1 align="center">SC Desktop Launcher (SCDL)</h1>

<p align="center">
  🌐 <a href="README.md">Deutsch</a> · <strong>English</strong>
</p>

<p align="center">
  <a href="https://github.com/rjcncpt/scdl-releases/releases/latest"><img src="https://img.shields.io/github/v/release/rjcncpt/scdl-releases?style=for-the-badge&label=Version&labelColor=232323&color=4f8ef7&logo=github&logoColor=white" alt="Latest version"></a>
  <a href="https://github.com/rjcncpt/scdl-releases/releases"><img src="https://img.shields.io/github/downloads/rjcncpt/scdl-releases/scdlauncher_setup.exe?displayAssetName=false&style=for-the-badge&label=Downloads&labelColor=232323&color=78c324&logo=download&logoColor=white" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?style=for-the-badge&labelColor=232323&logo=windows&logoColor=0078D4" alt="Platform: Windows 10 / 11">
  <a href="https://discord.gg/5VZsTk3qjR"><img src="https://img.shields.io/discord/1234564972198236261?style=for-the-badge&labelColor=232323&logo=discord&logoColor=5865F2&label=Discord&color=5865F2" alt="Discord members"></a>
  <a href="https://www.sc-deutsch-launcher.de"><img src="https://img.shields.io/badge/sc--deutsch--launcher.de-232323?style=for-the-badge&logo=googlechrome&logoColor=f97316" alt="Website"></a>
  <a href="https://ko-fi.com/scdeutsch"><img src="https://img.shields.io/badge/Support%20on%20Ko--fi-232323?style=for-the-badge&logo=kofi&logoColor=FF5E5B" alt="Support on Ko-fi"></a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Electron-44-47848F?style=for-the-badge&labelColor=232323&logo=electron&logoColor=47848F" alt="Electron 44">
  <img src="https://img.shields.io/badge/Node.js-24-339933?style=for-the-badge&labelColor=232323&logo=nodedotjs&logoColor=339933" alt="Node.js 24">
  <img src="https://img.shields.io/badge/JavaScript-ES2022-F7DF1E?style=for-the-badge&labelColor=232323&logo=javascript&logoColor=F7DF1E" alt="JavaScript ES2022">
</p>

<p align="center">
  The unofficial launcher for Star Citizen: installs and maintains community translations automatically, patches blueprints into mission texts, and keeps everything up to date without manual effort.
</p>

<p align="center">
  <a href="https://www.sc-deutsch-launcher.de">Website</a> ·
  <a href="https://github.com/rjcncpt/scdl-releases/releases/latest">Download</a> ·
  <a href="docs/Features.en.md">All features</a>
</p>

<p align="center">
  <img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/f6c308b8-b271-4a57-b3f2-2594423122da" />
</p>

---

## What is the SCDL?

Star Citizen comes without an official German translation. The community project **StarCitizen-Deutsch** fills that gap: game texts, missions, item descriptions, all translated. The **SCDL** makes sure this translation actually ends up in your installation, stays up to date, and is automatically re-patched with every new blueprint. Besides German, further community translations are available, such as Français, Italiano, Português or 日本語.

It runs alongside the RSI Launcher, finds your installation on its own, and treats **LIVE**, **HOTFIX**, **PTU** and **TECH-PREVIEW** as separate environments. Once set up, you barely notice the launcher in everyday use. It keeps the translation running in the background.

## Origin of the name

The SCDL has been an active German community project since December 25, 2025, and at first it exclusively installed and maintained the German translation for Star Citizen. Blueprints came later, and from that point on there was a strong wish to open the SCDL up to international users. The app was originally called "SC Deutsch Launcher". By now the program covers many languages and far more than just the translation, so the original name no longer matched its current scope. It was therefore renamed to `SC Desktop Launcher`, so that the abbreviation (SCDL) could stay.

## Who is it for?

For everyone who wants to play Star Citizen with useful information in the game texts, such as blueprints and additional item details, and with a community translation. No technical knowledge is required: the first-run wizard finds your installation, suggests the right channel, and sets up the rest by itself.

## Key features at a glance

Ordered by what you see or use first in the launcher.

| | |
|---|---|
| **Dashboard** | Info column and tiles in the main window: channel status, playtime, blueprint progress and more at a glance, freely configurable. |
| **Automatic translation** | Finds the Star Citizen installation, installs a translation from the catalog or from a custom source, and keeps it up to date through a background schedule. |
| **Multi-channel support** | LIVE, HOTFIX, PTU and TECH-PREVIEW run separately, each with its own language source. A traffic-light status in the window and in the tray icon shows what is up to date, outdated or not set up. |
| **Blueprint patching** | Automatically builds blueprint and mission details into the mission texts, including a progress list for blueprints already obtained, read from the `Game.log`. |
| **Quiet background operation** | Checks for and installs updates automatically without disturbing the running game, and backs off cleanly when servers are down. |
| **Profile backup** | Backs up key bindings and other user data per channel as a ZIP, with its own rotation and restore. |
| **Playtime statistics** | Evaluates the `Game.log` and shows playtime, ships, missions and other metrics. |
| **Troubleshooting** | Read-only system scan, path repair, and an error report as a ZIP for support. |
| **SC settings** | Graphics, display and upscaling options per channel, without starting the game. |
| **Startup programs** | Starts your own programs or scripts together with the RSI Launcher or with Star Citizen. |
| **Cache Cleaner** | Deletes outdated shader and graphics driver caches with one click. |
| **System info** | Shows hardware and graphics values clearly, exportable as a report. |
| **Overlay (alpha)** | A small bar above the game with live values from the `Game.log`: location, ship, movement, mission with the number of active missions, aUEC and income, server, playtime and recent events. Scan mode reads signatures with a hotkey. |
| **Joysticks and bindings (alpha)** | Deadzone, sensitivity and curves per axis, plus key binding by key press, directly in the `actionmaps.xml`. |
| **Streamer mode** | Blurs personal details such as Windows username, character name and location in the launcher and in the overlay. |
| **Multilingual interface** | The launcher interface itself is available in German, English, Spanish, French, Italian and Russian. |

The complete list with screenshots and explanations is in **[docs/Features.en.md](docs/Features.en.md)**.

## Installation

1. Download the latest setup from the [releases page](https://github.com/rjcncpt/scdl-releases/releases/latest).
2. Run `scdlauncher_setup.exe`.
3. On first launch, the setup wizard guides you through installation path, channel and language selection.

After that, the launcher updates itself; a new manual download is normally not necessary.

## Supported channels

| Channel | Description |
|---|---|
| **LIVE** | The public live server |
| **HOTFIX** | Short-term patches for the live server, uses the same language source as LIVE |
| **PTU** | Public Test Universe |
| **TECH-PREVIEW** | Technical preview |

Each channel is detected, translated and updated separately.

## Third-party resources used

The SCDL does not translate anything itself. It only downloads and installs what these projects maintain.

| Resource | Provider |
|---|---|
| Icons | [Lucide](https://lucide.dev) (ISC license) |
| German translation, Deutsch+, Schwiizerdütsch | [StarCitizen-Deutsch-INI](https://github.com/rjcncpt/StarCitizen-Deutsch-INI), Schwiizerdütsch by **Doesewicht** |
| French & Italian translation | [Dymerz/StarCitizen-Localization](https://github.com/Dymerz/StarCitizen-Localization) |
| Portuguese translation | [yucatan/StarCitizen-PT-BR](https://github.com/yucatan/StarCitizen-PT-BR) |
| Japanese translation | [stdblue/StarCitizenJapaneseResources](https://github.com/stdblue/StarCitizenJapaneseResources) |
| Blueprint data | [scmdb.net](https://scmdb.net/?page=fab) |

## Disclaimer

The SCDL is an unofficial, community-made tool. It is not affiliated with or endorsed by Cloud Imperium Games or Roberts Space Industries. Star Citizen and all related names and trademarks are the property of their respective owners. Use of the launcher is at your own risk.

## License

Not an official Cloud Imperium Games product. Star Citizen and all related trademarks are the property of Cloud Imperium Games.
