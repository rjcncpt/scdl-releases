# SCDL interface languages

This folder holds the interface texts of the **SC Desktop Launcher (SCDL)**.
Each language is a set of JSON files. If you want SCDL in your language, you can
translate these files and send them to us. No programming is needed.

> This is about the launcher's own interface (buttons, settings, reports).
> The Star Citizen game translation (`global.ini`) is a separate thing.

## Files of a language

Every language uses the same file name in four places. `xx` stands for the
language code.

| File | Content | Required |
|---|---|---|
| `xx.json` | The whole interface | **yes** |
| `debug/xx.json` | Debug window | no |
| `log/xx.json` | Activity log (dashboard, error report) | no |
| `bericht/xx.json` | Reports: game statistics, error report, joystick report | no |

Once your `xx.json` is part of an SCDL release, the language shows up in the
language selection of SCDL. The other three files are loaded automatically in
the same language.

Missing files or missing entries are no problem: SCDL falls back to English,
then to German. A half-finished translation works as well.

## Start a new language

1. Pick the language code: two letters after ISO 639-1 (`pl`, `nl`, `pt`),
   optionally with a region (`pt-br`). Lowercase.
2. Copy the English files and rename them:
   `en.json` → `xx.json`, `debug/en.json` → `debug/xx.json`, and so on.
3. Set name and flag at the top of `xx.json` (see below).
4. Translate the **values** – the text to the right of the colon.

```json
"settings.opt.windowsStart": "Start SCDL with Windows in system tray",
```

Only `Start SCDL with Windows in system tray` gets translated. The key
on the left (`settings.opt.windowsStart`) stays exactly as it is.

## Name and flag

```json
"meta.name": "Polski",
"meta.flag": "h:#ffffff,#dc143c",
```

- `meta.name`: the language name in the language itself (`Polski`, not `Polish`).
- `meta.flag`: the flag as colour stripes. Windows cannot show flag emoji, so
  SCDL draws simple stripes.
  - `h:` horizontal stripes from top to bottom, `v:` vertical stripes from left to right
  - 2 to 5 colours as hex values (`#ffffff` or `#fff`), separated by commas

| Example | Flag |
|---|---|
| `h:#000000,#dd0000,#ffce00` | Germany |
| `v:#009246,#ffffff,#ce2b37` | Italy |
| `h:#ffffff,#0039a6,#d52b1e` | Russia |

For flags with symbols or crosses, pick the main colours as stripes.

## Rules for translating

**Keep placeholders.** `{0}`, `{1}` … are replaced by values (numbers, names,
paths). Every placeholder in the English text must also be in your text. The
order may change.

```json
"log.gt.fertig": "Scan finished: {0} files, {1} MB, {2} s",
```

**Keep HTML tags.** Some texts contain tags such as `<b>`, `<code>`, `<br>` or
`<strong>`. Translate the text between the tags, leave the tags themselves
unchanged. `&lt;` and `&gt;` stay as they are.

**Line breaks.** `\n` or `<br>` start a new line. Keep them where they are.

**Do not translate:**
- Names: Star Citizen, SCDL, RSI Launcher, HidHide, Discord, GitHub
- Channels: LIVE, PTU, HOTFIX, TECH-PREVIEW
- File names and technical terms: `global.ini`, `actionmaps.xml`, `Game.log`,
  `user.cfg`, `Data.p4k`, `settings.json`, ETag, optionsVersion

**Lists keep their format.** `gt.bericht.tage` holds the seven weekdays as short
names, starting with Sunday, separated by commas without spaces
(`Sun,Mon,Tue,Wed,Thu,Fri,Sat`). Translate the names, keep seven entries and the
commas.

**Keep the JSON valid.**
- Every line except the last one ends with a comma.
- A double quote inside a text must be written as `\"`, a backslash as `\\`.
  Typographic quotes such as „…“, «…» or “…” need no escaping.
- Save the files as UTF-8.

You can check a file with any JSON validator, for example by pasting it into
https://jsonlint.com.

**Form of address.** Use one form throughout your language (for example "du"
or "Sie" in German, "tu" or "vous" in French). The existing languages use:
German/Italian/Spanish informal, French/Russian formal.

## Update an existing translation

New SCDL versions add new entries to `en.json`. A missing entry in your file is
shown in English, so nothing breaks. To complete your translation:

1. Open `en.json` and your `xx.json` side by side.
2. Find the entries that are in `en.json` but not in your file. Each entry has
   a key on the left (for example `"settings.lang.hint"`) and a text on the right.
3. Copy the missing lines into your file. Translate only the text on the right
   and keep the key exactly as it is. The order of the lines does not matter.
4. Check the file again: valid JSON, all placeholders `{0}`, `{1}` … still there.

Example. The English file has this entry, your file does not:

```json
"settings.lang.hint": "Preview shown immediately – applied on Save.",
```

Your translation:

```json
"settings.lang.hint": "Vorschau sofort sichtbar – wird beim Speichern übernommen.",
```

Every line except the last one in a file ends with a comma. Keep that in mind
when you add lines.

## Testing your translation

You can test your language in SCDL before you send it. This needs a current SCDL
version; older versions do not have the button.

1. Open SCDL: **Settings → Appearance → Language**. Click
   **Test your own language: open folder**.
2. Put your `xx.json` in that folder. If you have them, copy the `debug/`,
   `log/` and `bericht/` files too, in the same subfolders.
3. Restart SCDL. Your language appears in the language selection.

Notes:
- Only new language codes work. A file called `de.json` or `en.json` does not
  change the existing languages, so improvements to a language that SCDL already
  ships cannot be tested this way – just send them.
- Use lowercase file names (`pl.json`, not `PL.json`).
- Check the file first: valid JSON, and all placeholders `{0}`, `{1}` … still there.
- Long texts can make buttons and tables wider than planned. Tell us if something
  does not fit.

We test the new file in a development build before it goes into a release.

## Send your translation

- Open an issue at https://github.com/rjcncpt/scdl-releases/issues and attach
  your files (zip them if GitHub refuses `.json`), or
- post them in our Discord: https://discord.gg/5VZsTk3qjR

Once your language is part of an SCDL release, it appears in the standard language
selection for everyone.

Thank you for helping!
