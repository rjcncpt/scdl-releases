<h1 align="center">SCDL</h1>

<p align="center">
  <a href="https://github.com/rjcncpt/scdl-releases/releases/latest"><img src="https://img.shields.io/github/v/release/rjcncpt/scdl-releases?style=for-the-badge&label=Version&labelColor=232323&color=4f8ef7&logo=github&logoColor=white" alt="Neueste Version"></a>
  <a href="https://github.com/rjcncpt/scdl-releases/releases"><img src="https://img.shields.io/github/downloads/rjcncpt/scdl-releases/scdlauncher_setup.exe?displayAssetName=false&style=for-the-badge&label=Downloads&labelColor=232323&color=78c324&logo=download&logoColor=white" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?style=for-the-badge&labelColor=232323&logo=windows&logoColor=0078D4" alt="Plattform: Windows 10 / 11">
  <a href="https://discord.gg/5VZsTk3qjR"><img src="https://img.shields.io/discord/1234564972198236261?style=for-the-badge&labelColor=232323&logo=discord&logoColor=5865F2&label=Discord&color=5865F2" alt="Discord Mitglieder"></a>
  <a href="https://www.sc-deutsch-launcher.de"><img src="https://img.shields.io/badge/sc--deutsch--launcher.de-232323?style=for-the-badge&logo=googlechrome&logoColor=f97316" alt="Webseite"></a>
  <a href="https://ko-fi.com/scdeutsch"><img src="https://img.shields.io/badge/Ko--fi%20unterst%C3%BCtzen-232323?style=for-the-badge&logo=kofi&logoColor=FF5E5B" alt="Auf Ko-fi unterstützen"></a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Electron-28-47848F?style=for-the-badge&labelColor=232323&logo=electron&logoColor=47848F" alt="Electron 28">
  <img src="https://img.shields.io/badge/Node.js-18-339933?style=for-the-badge&labelColor=232323&logo=nodedotjs&logoColor=339933" alt="Node.js 18">
  <img src="https://img.shields.io/badge/JavaScript-ES2022-F7DF1E?style=for-the-badge&labelColor=232323&logo=javascript&logoColor=F7DF1E" alt="JavaScript ES2022">
</p>

<p align="center">
  Der inoffizielle Launcher für Star Citizen: installiert und pflegt Community-Übersetzungen automatisch, patcht Baupläne in die Missionstexte und hält alles ohne manuelles Zutun aktuell.
</p>

<p align="center">
  <a href="https://www.sc-deutsch-launcher.de">Webseite</a> ·
  <a href="https://github.com/rjcncpt/scdl-releases/releases/latest">Download</a> ·
  <a href="docs/Features.md">Alle Features</a>
</p>

<p align="center">
  <img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/f6c308b8-b271-4a57-b3f2-2594423122da" />
</p>

---

## Was ist der SCDL?

Star Citizen kommt ohne offizielle deutsche Übersetzung. Das bringt das Community-Projekt **StarCitizen-Deutsch** bei: Spieltexte, Missionen, Item-Beschreibungen, alles übersetzt. Der **SCDL** sorgt dafür, dass diese Übersetzung auch tatsächlich in der Installation landet, aktuell bleibt und bei jedem neuen Bauplan automatisch nachgepatcht wird. Neben Deutsch stehen weitere Community-Übersetzungen zur Wahl, etwa Français, Italiano, Português oder 日本語.

Er läuft neben dem RSI Launcher her, findet die Installation von selbst und behandelt **LIVE**, **HOTFIX**, **PTU** und **TECH-PREVIEW** als getrennte Baustellen. Einmal eingerichtet, merkt man vom Launcher im Alltag kaum noch etwas. Er hält die Übersetzung im Hintergrund am Laufen.

## Herkunft des Namens

Der SCDL ist seit dem 25. Dezember 2025 als deutsches Community-Projekt aktiv und hat zunächst ausschließlich die deutsche Übersetzung für Star Citizen installiert und aktuell gehalten. Später kamen die Baupläne hinzu und ab diesem Zeitpunkt war der Wunsch groß, den SCDL für internationale Nutzer zu öffnen. Der App-Name "SCDL" hieß ursprünglich "SC Deutsch Launcher". Mittlerweile deckt das Programm viele Sprachen und weit mehr als nur die Übersetzung ab, weshalb der ursprüngliche Name nicht mehr zum heutigen Funktionsumfang passt. Geblieben ist vorerst die Abkürzung SCDL.

## Für wen ist das?

Für alle, die die Spieltexte in Star Citizen mit sinnvollen Informationen wie Baupläne, Item-Zusatzangaben und mit einer Community-Übersetzung spielen wollen. Technisches Vorwissen braucht es dafür nicht: Der Ersteinrichtungs-Assistent findet die Installation, schlägt den passenden Kanal vor und richtet den Rest von selbst ein.

## Kernfunktionen im Überblick

Reihenfolge nach dem, was man im Launcher zuerst sieht bzw. benutzt.

| | |
|---|---|
| **Dashboard** | Info-Spalte und Kacheln im Hauptfenster: Kanal-Status, Spielzeit, Bauplan-Fortschritt und mehr auf einen Blick, frei zusammenstellbar. |
| **Automatische Übersetzung** | Findet die Star-Citizen-Installation, installiert eine Übersetzung aus dem Katalog oder einer eigenen Quelle und hält sie über einen Hintergrund-Takt aktuell. |
| **Mehrkanalunterstützung** | LIVE, HOTFIX, PTU und TECH-PREVIEW laufen getrennt, jeweils mit eigener Sprachquelle. Ampelstatus im Fenster und im Tray-Icon zeigt, was aktuell, veraltet oder nicht eingerichtet ist. |
| **Baupläne-Patching** | Baut Bauplan- und Missionsdetails automatisch in die Missionstexte ein, inklusive Fortschrittsliste für bereits erspielte Baupläne aus der `Game.log`. |
| **Leiser Hintergrundbetrieb** | Prüft und installiert Updates automatisch, ohne das laufende Spiel zu stören, und zieht sich bei Serverausfällen sauber zurück. |
| **Profil-Backup** | Sichert Tastenbelegungen und weitere Nutzerdaten je Kanal als ZIP, mit eigener Rotation und Wiederherstellung. |
| **Spielzeit-Statistik** | Wertet die `Game.log` aus und zeigt Spielzeit, Schiffe, Missionen und weitere Kennzahlen. |
| **Problembehandlung** | Read-only Systemscan, Pfad-Reparatur und Fehlerbericht als ZIP für den Support. |
| **SC-Einstellungen** | Grafik-, Anzeige- und Upscaling-Optionen je Kanal, ohne das Spiel zu starten. |
| **Startprogramme** | Startet eigene Programme oder Skripte zusammen mit dem RSI Launcher oder mit Star Citizen. |
| **Cache Cleaner** | Löscht veraltete Shader- und Grafiktreiber-Caches mit einem Klick. |
| **Systeminfo** | Zeigt Hardware- und Grafikwerte übersichtlich an, exportierbar als Bericht. |
| **Mehrsprachige Oberfläche** | Die Launcher-Oberfläche selbst gibt es auf Deutsch und Englisch. |

Die vollständige Liste mit Screenshots und Erklärung steht in **[docs/Features.md](docs/Features.md)**.

## Installation

1. Neuestes Setup von der [Release-Seite](https://github.com/rjcncpt/scdl-releases/releases/latest) herunterladen.
2. `scdlauncher_setup.exe` ausführen.
3. Beim ersten Start führt der Einrichtungs-Assistent durch Installationspfad, Kanal und Sprachauswahl.

Der Launcher aktualisiert sich danach selbst, ein erneuter manueller Download ist normalerweise nicht nötig.

## Unterstützte Kanäle

| Kanal | Beschreibung |
|---|---|
| **LIVE** | Der öffentliche Live-Server |
| **HOTFIX** | Kurzfristige Patches des Live-Servers, nutzt dieselbe Sprachquelle wie LIVE |
| **PTU** | Public Test Universe |
| **TECH-PREVIEW** | Technische Vorschau |

Jeder Kanal wird getrennt erkannt, übersetzt und aktualisiert.

## Verwendete Fremdressourcen

Der SCDL selbst übersetzt nichts. Er lädt und installiert nur, was diese Projekte pflegen.

| Ressource | Anbieter |
|---|---|
| Icons | [Lucide](https://lucide.dev) (ISC-Lizenz) |
| Deutsche Übersetzung, Deutsch+, Schwiizerdütsch | [StarCitizen-Deutsch-INI](https://github.com/rjcncpt/StarCitizen-Deutsch-INI), Schwiizerdütsch von **Doesewicht** |
| Französische & italienische Übersetzung | [Dymerz/StarCitizen-Localization](https://github.com/Dymerz/StarCitizen-Localization) |
| Portugiesische Übersetzung | [yucatan/StarCitizen-PT-BR](https://github.com/yucatan/StarCitizen-PT-BR) |
| Japanische Übersetzung | [stdblue/StarCitizenJapaneseResources](https://github.com/stdblue/StarCitizenJapaneseResources) |
| Bauplan-Daten | [scmdb.net](https://scmdb.net/?page=fab) |

## Disclaimer

Der SCDL ist ein inoffizielles, von der Community erstelltes Werkzeug. Es besteht keine Verbindung zu und keine Unterstützung durch Cloud Imperium Games oder Roberts Space Industries. Star Citizen und alle zugehörigen Namen und Marken sind Eigentum ihrer jeweiligen Rechteinhaber. Die Nutzung des Launchers erfolgt auf eigene Verantwortung.

## Lizenz

Kein offizielles Cloud-Imperium-Games-Produkt. Star Citizen und alle zugehörigen Marken sind Eigentum von Cloud Imperium Games.
