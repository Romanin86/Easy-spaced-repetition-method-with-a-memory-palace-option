# Palais Mental

[Français](README.md) · **English**

A memory-palace study tool contained in **a single HTML file**. No installation, no account, no server, no connection required.

Version 6.0

> **The interface is in French.** Button and menu names in this document are translations; the original French label is given in brackets where it helps you find it on screen.

---

## Quick start

1. Download `palais-mental.html`
2. Open it in a recent browser — Firefox, Chrome, Edge
3. That's it

For your students, the application produces a standalone **reader file**, distributed like any other file.

---

## Privacy and offline use

**Everything stays on your device.** The application contacts no server on startup: no Google, no analytics, no downloaded fonts, no external libraries. Everything it needs is inside the file.

**Everything works offline**, application and reader file alike: creating content, reviewing, reminders, spreadsheet import and export, backups, ZIP archives.

Only two features use the internet — both **optional**, and only when you trigger them:

- **AI image generation**
- **Free-licence photo search**

---

## Two forms

| | **The application** | **The reader file** |
|---|---|---|
| Who it's for | The teacher | The students |
| Create, edit, delete | Yes | No |
| Review, walk through, schedule reminders | Yes | Yes |
| Where progress is saved | On your device | On the student's device, never touching your copy |

---

# Part one — The application

## 1. How content is organised

Three levels, from broad to precise:

- **Palace** — a subject, a syllabus, a theme. *"Year 11 History & Geography"*
- **Room** — a chapter, a topic. *"The Second World War"*
- **Object** — one thing to remember. *"Battle of Stalingrad"*

An object holds a **title** (what must be recalled), the **information to remember**, and optionally an **image**, a **mnemonic phrase**, **tags** and an **attached document**.

The sort order chosen on the home screen — creation order, alphabetical, most recent, largest — applies to **every** palace list in the application.

## 2. Creating content

**From a spreadsheet — fastest for large volumes.** Export the blank template from Settings, fill it in, import it back. One row = one object. The `palais`, `salle` and `objet` columns build the structure; missing rooms are created for you.

> The column names stay in French: they are the headers the application actually expects.

A prompt is supplied so an AI can generate that spreadsheet. One warning: language models fill the `favori` column very generously — see the Favourites section.

**By hand**, palace by palace.

**By importing** a backup or an archive, JSON or ZIP.

## 3. Refining content

Generated content is broadly right, never perfect. **Walk-through** mode steps through objects with no questioning: it is the proofreading mode. Two buttons matter there:

- **Edit** — fixes the card and returns you to exactly the same card
- **Favourite** — the star marks what deserves to be kept

**The curation workflow**, to extract the best from a large generated palace:

1. Duplicate the palace ("More" menu)
2. Walk through the copy, starring what you keep
3. Inside a room, click **Favourites** until it reads **"Non favourites"** [*Non favoris*]
4. Select all, delete

Bulk deletion stays undoable for twelve seconds, and a snapshot is taken beforehand.

> Duplicating a palace doubles its weight, images included.

## 4. Images

For a single object or a whole batch:

- **Import** from your device
- **AI generation** — Pollinations service, free, key optional
- **Real photograph** — Openverse, Wikimedia Commons and other free services

**The generation style matters more than anything.** The supplied styles deliberately produce absurd images: effective for anchoring an isolated word, useless for illustrating a concept. The **"True to subject"** [*Fidèle au sujet*] style draws on the content and the room.

In batch generation the style is fixed once for the whole run, so images within a palace look consistent.

## 5. Attached documents

Each object can carry a PDF, a Word, Excel or LibreOffice document.

- **PDF** → opens in a window during review, offline included
- **Other formats** → open in the student's own software, since no browser can display them

**Batch import**: each file joins the object whose title matches its filename, extension removed. A summary lists whatever found no match.

## 6. Reviewing

Review is spaced: an object you knew comes back later, one you missed comes back soon.

During a review, the top bar lets you **edit** the object, **star** it, **set the session aside**, show the mnemonic phrase, or hide images.

An interrupted session is resumed automatically: a banner offers it on your return.

## 7. Favourites

The star marks an object — in a room, during review or during a walk-through. The **Favourites** entry in the side menu reviews them all, across every palace.

A room's filter has three states: **all**, **favourites**, **non favourites**.

**Bulk removal** in Settings: palace by palace or all at once, undoable. Essential after importing an AI-generated spreadsheet.

## 8. Reminders

A reminder series schedules reviews on specific dates: **what to revisit** (whole palaces or rooms), a **starting point**, and a **series of intervals** — D+1, D+3, D+7, D+14, D+30, or your own.

Ready-made series: **Forgetting curve**, **Progressive**, **Weekly**, **Exam run-up**. All editable.

In the target list, each palace folds and unfolds; **Unfold all** [*Tout déplier*] and **Fold all** [*Tout replier*] act on every palace at once.

The **Agenda** shows a monthly calendar with colour dots and the list of active series.

## 9. Backing up, archiving

**Full backup**, JSON or ZIP: every palace, image, document, progress record, reminder, the wallpaper, custom services, set-aside sessions. ZIP is lighter as soon as there are images.

**Archive of selected palaces**, JSON or ZIP: only the ticked palaces, with their full content. It contains **no settings** — re-importing it leaves your styles, wallpaper and reminders untouched. This is the tool for slimming the application down or handing over a subject.

**Snapshots**: taken automatically before every risky operation, restorable from Settings.

**Diagnostics**: checks integrity and reports orphaned images, without exposing your content.

> Service access keys are **never** exported.

## 10. Importing a large base

During an import, a window shows the current step, progress palace by palace, elapsed time and an estimate of the time remaining.

Once finished, if the base is large, a summary places it on a scale:

| Level | Number of objects |
|---|---|
| Comfortable | under 3,000 |
| Loaded | 3,000 to 8,000 |
| Heavy | over 8,000 |

These thresholds are **estimated guidelines**, not technical limits: beyond them everything still works, more slowly on a phone. The advice is then to archive subjects you are not currently using, and remove them.

## 11. Exporting for students

Settings [*Paramètres*] → **Read-only export** [*Exporter en lecture seule*].

1. Unfold **Choose palaces** [*Choisir les palais*] and tick those to distribute
2. Check the **estimated size** and the comfort indicator
3. Choose a name, or one of the three suggestions
4. Tick **"Reset review statistics"** [*Réinitialiser les statistiques*] if the file is for someone else
5. Generate

| Size | What to expect |
|---|---|
| under 8 MB | Comfortable everywhere, modest phones included |
| 8 to 25 MB | Slightly slow to open on older devices |
| 25 to 60 MB | Email attachment often refused |
| over 60 MB | Risk of failure on a phone |

The same foldable **Choose palaces** panel serves all three exports: read-only, archive, spreadsheet.

## 12. Wallpaper

Settings [*Paramètres*] → **Wallpaper** [*Fond d'écran*], three tabs: **Generate (AI)** [*Générer (IA)*], **Free photo** [*Photo libre*], **Import** [*Importer*].

Suggestions accumulate in a gallery. A click places an image **in preview**: your current wallpaper stays in place until you click **Apply this wallpaper** [*Appliquer ce fond*]. Once applied, **Back to previous wallpaper** [*Revenir au fond précédent*] undoes the change.

---

# Part two — The reader file

*Hand this section to students.*

## Opening it

Double-click the file. It opens in your browser. **No connection required**, and nothing is sent anywhere.

## What you can do

**Browse** palaces, rooms and objects.

**Review**: a question appears, you think, you reveal, you say whether you knew it. Later reviews are spaced accordingly.

**Schedule your own reminders**: what to revisit, a starting date, a series of intervals, or a ready-made pattern.

**Sort palaces**: original order, alphabetical, most recent, largest.

## What you cannot do

Create, edit or delete anything. The content is what your teacher approved.

## Your progress

It is saved **in your browser, on your device**, and reported to no one.

You pick up where you left off when reopening the file on the same device and browser. It does not follow you to another device, and clearing your browser data clears it too.

---

# Part three — Technical reference

## Accepted formats

| Use | Formats |
|---|---|
| Content import | `.xlsx`, `.csv`, `.ods`, `.json`, `.zip` |
| Images | `.jpg`, `.png`, `.webp`, `.gif` |
| Attached documents | `.pdf`, `.docx`, `.doc`, `.odt`, `.xlsx`, `.xls`, `.ods`, `.csv`, `.rtf`, `.txt` |

## Limits

- **Attached document**: warning above 2 MB, refused above 12 MB
- **Images**: resized to 640 px; wallpaper to 1600 px
- **Reader file**: above 25 MB, email attachment is often refused

## Where the data lives

In the browser's local storage. It survives closing the browser, but **not** clearing browser data, and it does not move to another device.

Browsers store data **per address**, not per file: two copies of the application opened from the same address share the same base.

**Export regularly.** That is the only real backup.

## Image services

Two families of services, **free and optional**:

- **Pollinations** — AI generation. Without a key, expect roughly 23 seconds between images; with one, about 9.
- **Real photographs** — Openverse, Wikimedia Commons, and others you can declare.

In Settings you can declare your own services, test them, remove them, and choose which one is used by default.

## Troubleshooting

| Symptom | What to check |
|---|---|
| The reader file shows nothing | It was generated from an old version: regenerate it |
| Image generation fails | VPNs are often blocked by the service; so is a key whose account has run out of credits — remove it to fall back on anonymous access |
| The reader file is too heavy | Fewer images, lighter PDFs, or one file per subject |
| A deletion you regret | The undo banner (twelve seconds), otherwise a snapshot |
| Favourites you never set | They came from the imported spreadsheet: bulk removal in Settings |
| The application is slow on a phone | See the volume summary: archive inactive subjects |

## Known limitations

- **iPad and Safari**: a malfunction of the reader file has been reported and is not yet diagnosed.
- **SheetJS 0.18.5**, embedded to read spreadsheets, has known vulnerabilities when importing crafted files. The risk is low as long as you only import your own spreadsheets. Do not import spreadsheets of unknown origin.

## Third-party libraries

Embedded in the file, under their respective licences:

| Library | Version | Licence |
|---|---|---|
| Vue | 3 | MIT |
| SheetJS | 0.18.5 | Apache-2.0 |
| PapaParse | 5.3.0 | MIT |
| JSZip | 3.10.1 | MIT or GPLv3, at your choice |

## Licence

See the `LICENSE` file.
