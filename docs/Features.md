# Features

Vollständige Übersicht aller Funktionen des SC Deutsch Launcher (SCDL), mit Erklärung und Fundstelle in der Oberfläche. Screenshots sind Platzhalter und werden vor Veröffentlichung durch echte Aufnahmen ersetzt.

Zurück zu: [README](../README.md)

Reihenfolge nach dem, was man im Launcher zuerst sieht bzw. benutzt, nicht nach technischer Wichtigkeit. Alle Module sind gleich gewichtet.

## Inhalt

- [Ersteinrichtung](#ersteinrichtung)
- [Dashboard](#dashboard)
- [Übersetzung](#übersetzung)
- [Kanäle und Status](#kanäle-und-status)
- [Baupläne](#baupläne)
- [Strings und Item-Werte](#strings-und-item-werte)
- [Hintergrund-Updates](#hintergrund-updates)
- [Profil-Backup](#profil-backup)
- [Spielzeit-Statistik](#spielzeit-statistik)
- [Problembehandlung](#problembehandlung)
- [SC-Einstellungen](#sc-einstellungen)
- [Startprogramme](#startprogramme)
- [Cache Cleaner](#cache-cleaner)
- [Systeminfo](#systeminfo)
- [Was ist neu](#was-ist-neu)
- [Oberfläche und Fenster](#oberfläche-und-fenster)
- [Kommandozeile und Diagnose](#kommandozeile-und-diagnose)

---

## Ersteinrichtung

### Erststart-Wizard

Beim allerersten Start führt ein Assistent Schritt für Schritt durch die Einrichtung: Installationspfad finden oder von Hand angeben, Kanal auswählen, Übersetzungsvariante wählen. Kein technisches Vorwissen nötig.

**Wie erreichen:** Startet automatisch beim ersten Programmstart. Danach über „Einstellungen zurücksetzen" erneut auslösbar.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/029ce231-aa35-49ce-ad68-6a4fb98b9af2" />

---

## Dashboard

### Kachel-Übersicht

Info-Spalte und Kacheln im Hauptfenster, das Erste, was man nach dem Start sieht. Zeigt auf einen Blick die wichtigsten Kennzahlen: Kanal-Status, letzte Backups, Spielzeit, Bauplan-Fortschritt und weitere frei wählbare Kacheln.

**Wie erreichen:** Hauptfenster → Reiter „Dashboard". Welche Kacheln erscheinen und in welcher Reihenfolge, legt „Dashboard einrichten" per Drag-and-drop fest.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/18a14b93-0f47-4436-8044-cc4c7e812715" />

---

## Übersetzung

### Automatische Pfaderkennung

Findet die Star-Citizen-Installation selbstständig, ohne dass man Ordner suchen muss.

**Wie erreichen:** Läuft automatisch beim Start und im Ersteinrichtungs-Assistenten.

### Manuelle Pfadeinstellung

Wer eine ungewöhnliche Installation hat (z. B. auf einem Zweitlaufwerk oder über einen Symlink), kann den Pfad je Kanal von Hand setzen.

**Wie erreichen:** Einstellungen → Reiter „Installationen" → Pfad bearbeiten.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/7abdd069-1763-47fb-94fa-1beabb7dfa90" />

### Sprachvarianten

Jeder Kanal hat zwei frei benennbare Sprachknöpfe. Dahinter steht entweder eine Übersetzung aus dem Katalog (Deutsch, Deutsch+, Schwiizerdütsch, Français, Italiano, Português, 日本語, Englisch direkt aus der `Data.p4k`) oder eine selbst eingetragene Quell-URL. Bereits installierte Sprachdateien hält der Launcher per Versionsabgleich (ETag) automatisch aktuell.

**Wie erreichen:** Einstellungen → Reiter „Sprachen" → Quelle je Kanal wählen, oder im Hauptfenster über „Sprache wählen" aus dem Katalog übernehmen.

### Übersetzung reparieren

Setzt die Übersetzung eines Kanals zurück und installiert sie neu. Hilfreich, wenn ein Spiel-Update die `global.ini` überschrieben hat.

**Wie erreichen:** Hauptfenster → Kanal-Kachel → „Reparieren".

---

## Kanäle und Status

### Mehrkanal-Verwaltung

LIVE, HOTFIX, PTU und TECH-PREVIEW werden getrennt behandelt: eigener Pfad, eigene Sprachquelle, eigener Ampelstatus, eigenes Backup. HOTFIX teilt sich die Sprachquelle mit LIVE. PTU und TECH-PREVIEW starten ohne eigene Quelle (Englisch aus der `Data.p4k`), eine eigene lässt sich eintragen.

**Wie erreichen:** Kanal-Kacheln im Hauptfenster, ein Reiter je Kanal.

### Ampelstatus je Kanal

Grün, Gelb, Rot oder Grau zeigt je Kanal getrennt auf einen Blick, ob eine Übersetzung aktuell, veraltet, fehlerhaft oder nicht eingerichtet ist.

**Wie erreichen:** Sichtbar direkt an jeder Kanal-Kachel im Hauptfenster und am Tray-Icon.

### Kanal-Schnellschalter (experimentell)

Ein Power-Schalter direkt am Kanal-Header, um eine Übersetzung schnell an- oder abzuschalten, ohne die Einstellungen zu öffnen.

**Wie erreichen:** Einstellungen → Modul-Schalter „Kanal-Schnellschalter" aktivieren (standardmäßig aus), danach Schalter am Kanal-Header.

---

## Baupläne

### Bauplan-Patching in Missionstexte

Neue Fahrzeuge und Waffen bringen oft Baupläne mit, deren Vorlagen-Texte noch nicht übersetzt sind. Der SCDL baut Bauplan- und Missionsdetails automatisch in die `global.ini` ein. Die Daten stammen von scmdb.net und werden automatisch aktualisiert.

**Wie erreichen:** Läuft automatisch nach jedem Übersetzungs-Update. Manuell anstoßbar über Hauptfenster → „Baupläne" → „Neu einbauen".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/1f26b60a-fe59-469a-a1f7-52f514fce9e6" />

### Erspielte Baupläne-Übersicht

Hält fest, welche Baupläne bereits erspielt wurden, damit deren Vorlagen-Texte nicht mehr als „fehlend" markiert werden. Lässt sich ansehen, durchsuchen und von Hand anpassen.

**Wie erreichen:** Hauptfenster → „Baupläne" → Reiter „Erledigt".

### Erspielte Baupläne aus der Game.log einlesen

Scannt die `Game.log` nach Hinweisen auf erspielte Baupläne und trägt sie automatisch in die Erledigt-Liste ein, auch als Live-Mitschnitt während des Spielens.

**Wie erreichen:** Automatisch im Hintergrund, solange Star Citizen läuft. Manueller Scan über „Baupläne" → „Log durchsuchen".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/a657a098-846f-4fda-89b2-394e8c1162a6" />

### Erspielte Baupläne-Datei sichern und wiederherstellen

Die Erledigt-Liste lässt sich exportieren, importieren oder zurücksetzen, ohne den restlichen Bauplan-Fortschritt zu verlieren.

**Wie erreichen:** „Baupläne" → Reiter „Erledigt" → Menü „Sichern/Importieren".

---

## Strings und Item-Werte

### Waffen- und Komponenten-Texte

Ergänzt StarStrings-Texte für Waffen, Schilde und weitere Komponenten um die deutsche Übersetzung, aufgeteilt in vier Kategorien.

**Wie erreichen:** Läuft automatisch mit dem Übersetzungs-Update. Einstellung unter Einstellungen → „Baupläne & Strings".

### Item-Werte in Beschreibungen

Trägt echte Zahlenwerte (Schaden, Reichweite usw.) aus den Item-Stats-Daten in die deutschen Item-Beschreibungen ein, statt Platzhaltertexte stehen zu lassen.

**Wie erreichen:** Automatisch aktiv, abschaltbar über Einstellungen → Modul-Schalter „Item-Werte".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/4bd4abea-1b35-4aa5-a208-21e0bbe3f8a0" />

---

## Hintergrund-Updates

### Automatischer Update-Takt

Prüft in einem festen Takt im Hintergrund, ob eine neue Übersetzung oder neue Baupläne vorliegen, und installiert sie leise, ohne das laufende Spiel zu unterbrechen.

**Wie erreichen:** Läuft automatisch, keine Interaktion nötig. Takt einsehbar in den Einstellungen.

### Rückzug bei Serverausfall

Ist der Übersetzungsserver nicht erreichbar, meldet der Launcher das klar und arbeitet mit dem zuletzt bekannten Stand weiter, statt Fehler zu häufen.

**Wie erreichen:** Erscheint automatisch als Hinweisbanner, sobald ein Ausfall erkannt wird.

### Update nach Spielende

Erkennt automatisch, wenn Star Citizen beendet wurde, und holt dann liegen gebliebene Updates nach.

**Wie erreichen:** Automatisch, basiert auf der Prozess-Überwachung.

### Launcher-Selbstupdate

Der Launcher aktualisiert sich selbst über GitHub Releases, inklusive Prüfsummen-Abgleich vor der Installation.

**Wie erreichen:** Automatisch beim Start, mit Hinweis vor der Installation.

---

## Profil-Backup

### ZIP-Sicherung der Nutzerdaten

Sichert Tastenbelegungen und weitere Nutzerdaten je Kanal als ZIP-Archiv, mit automatischer Rotation älterer Stände.

**Wie erreichen:** Hauptfenster → Reiter „Profil-Backup" → geführter Ablauf: Profil wählen → Auswahl, was gesichert wird → Sicherung erstellen.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/9ebe50b4-deae-4888-8836-96f3934619b1" />

### Wiederherstellung

Spielt eine vorhandene Sicherung zurück, ohne danach dazugekommene Dateien zu verlieren oder die Sicherung selbst zu überschreiben.

**Wie erreichen:** Reiter „Profil-Backup" → Sicherung auswählen → „Wiederherstellen".

---

## Spielstatistik

### Auswertung aus der Game.log

Liest die Logdateien aus und zeigt Spielzeit je Sitzung, erspielte Baupläne und weitere Kennzahlen, ohne dass Star Citizen selbst dafür laufen muss.

**Wie erreichen:** Hauptfenster → Reiter „Spielzeit".

### Export der Statistik

Die gesammelten Daten lassen sich exportieren, etwa für eigene Auswertungen.

**Wie erreichen:** Reiter „Spielzeit" → „Exportieren".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/65211b5c-ebc5-44a0-9dd2-9125c35011b2" />

---

## Problembehandlung

### Read-only Systemscan

Prüft Installation, Pfade und Konfiguration, ohne etwas zu verändern, und zeigt gefundene Probleme verständlich an.

**Wie erreichen:** Hauptfenster → Reiter „Problembehandlung" → „Scan starten".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/8888639a-5dde-41b5-a004-f5485f5a790c" />

### Pfad-Reparatur

Behebt erkannte Pfadprobleme automatisch, sofern eindeutig möglich.

**Wie erreichen:** Nach dem Scan → „Reparieren" bei betroffenen Einträgen.

### Fehlerbericht als ZIP

Bündelt relevante Logs und Diagnosedaten in einer ZIP-Datei für den Support, ohne Zugangsdaten oder persönliche Inhalte.

**Wie erreichen:** Reiter „Problembehandlung" → „Fehlerbericht erstellen".

---

## SC-Einstellungen

### Grafik- und Anzeigeeinstellungen

Zeigt und ändert ausgewählte Star-Citizen-Einstellungen (Anzeige, Upscaling) direkt aus dem Launcher, je Kanal getrennt, ohne das Spiel starten zu müssen.

**Wie erreichen:** Hauptfenster → Reiter „SC-Einstellungen".

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/10978bee-465a-4e22-b7ca-425fbe5066a7" />

### user.cfg-Verwaltung

Bearbeitet die `user.cfg` der Installation komfortabel über die Oberfläche.

**Wie erreichen:** Reiter „SC-Einstellungen" → „user.cfg".

---

## Startprogramme

### Eigene Programme mitstarten

Startet festgelegte Programme oder Skripte automatisch beim RSI-Launcher- oder Star-Citizen-Start, etwa Voice-Tools oder Overlays (`.exe` als Ziel eines Skripts ausgeschlossen, Opt-in erforderlich). Fenstermodus und Wartezeit lassen sich je Eintrag festlegen.

**Wie erreichen:** Einstellungen → Modul-Schalter „Startprogramme" aktivieren (standardmäßig aus), danach Reiter „Startprogramme" → Eintrag hinzufügen.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/97ec9a79-0d30-45ae-adfd-62ca32977bba" />

---

## Cache Cleaner

### Shader-Cache leeren

Löscht den Shader-Cache von Star Citizen mit einem Klick. Hilft bei Grafikfehlern nach Updates.

**Wie erreichen:** Cache-Cleaner-Knopf in der Titelleiste, Dashboard-Kachel „Cache" oder Tray → „Cache bereinigen". Öffnet ein Modal im Hauptfenster.

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/00d68527-422e-4ba6-8dd8-5522a8433062" />

---

## Systeminfo

### Systemdaten auf einen Blick

Zeigt relevante Systeminformationen (Hardware, Treiber, Pfade) übersichtlich an, hilfreich für Fehlerberichte.

**Wie erreichen:** Titelleiste → Symbol „Systeminfo" (oder Klick auf die Grafik- bzw. Leistungskachel im Dashboard).

<img width="1254" height="776" alt="image" src="https://github.com/user-attachments/assets/08f9f9c7-64a3-422f-b38b-d07188b33e5b" />

---

## Was ist neu

### Release-Notizen der installierten Fassung

Zeigt die mitgelieferte Seite mit den Neuerungen dieser Version. Liegt im Programm selbst, es wird nichts aus dem Netz geladen.

**Wie erreichen:** Erscheint nach einem Update einmal von selbst; jederzeit über die Glocke in der Titelleiste.

---

## Oberfläche und Fenster

### Tray-Icon mit Ampelpunkt

Zeigt den Gesamtstatus aller Kanäle direkt im Tray, auch wenn das Fenster geschlossen ist.

**Wie erreichen:** Immer sichtbar in der Windows-Taskleiste, sobald der Launcher läuft.

### Mehrsprachige Oberfläche

Die Launcher-Oberfläche selbst (nicht die Spielübersetzung) gibt es auf Deutsch und Englisch.

**Wie erreichen:** Einstellungen → „Oberflächensprache".

### Farbschema

Helles oder dunkles Erscheinungsbild, folgt wahlweise dem System.

**Wie erreichen:** Einstellungen → „Erscheinungsbild".

### Fenstergröße und Skalierung

Merkt sich Fensterposition und -größe, unterstützt Zoom-Stufen für unterschiedliche Bildschirme.

**Wie erreichen:** Fenster wie gewohnt ziehen/skalieren, wird automatisch gemerkt. Zoom über Strg + Mausrad oder Einstellungen.

---

## Kommandozeile und Diagnose

### Kommandozeilen-Modi

Der Launcher lässt sich ohne Fenster und ohne Tray-Symbol per Kommandozeile steuern, etwa aus Batch-Skripten oder der Windows-Aufgabenplanung: `--update`, `--check`, `--bp-reinject` und `--log-scan` je Kanal (`live`/`hotfix`/`ptu`/`tech-preview`/`all`), außerdem `--version` und `--export-log`.

**Wie erreichen:** z. B. `scdlauncher_setup.exe --update=live,hotfix` oder `scdlauncher_setup.exe --check=all` in einer Konsole. Läuft der SCDL bereits, bricht der Aufruf ab statt in dieselben Dateien zu schreiben.

### Debug Console

Mit F12 im Hauptfenster öffnet sich ein Selbsttest für System, Konfiguration, Pfade und Server-Erreichbarkeit. Hilfreich für Bug-Reports.

**Wie erreichen:** Hauptfenster → F12 → „Checks ausführen" → „Exportieren".

### Aktivitätsprotokoll

Zeigt ein laufendes Protokoll der Launcher-Aktivitäten zur Fehlersuche.

**Wie erreichen:** Debug-Fenster öffnen (siehe Problembehandlung / Support-Hinweise).
