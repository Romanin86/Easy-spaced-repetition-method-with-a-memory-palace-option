# Palais Mental

[Français](README.md) · **English**

A memory-palace and spaced-repetition study tool contained in **a single HTML file**. No installation, no account, no server, no connection required.

Version 7.0

> **The interface is in French.** Button and menu names in this document are translations; the original French label is given in brackets where it helps you find it on screen.

---

## Quick start

1. Download `palais-mental.html`
2. Open it in Firefox — or in Chrome and Edge, see "Platforms and browsers"
3. That's it

For your students, the application produces a standalone **reader file**, distributed like any other file.

**A word you don't know?** The **Glossary** [*Glossaire*], in the side menu, defines every term of the application in one sentence and tells you where to find it.

---

## Privacy, offline use, security

**Everything stays on your device.** The application contacts no server on startup: no Google, no analytics, no downloaded fonts, no external libraries. Everything it needs is inside the file.

**Everything works offline**, application and reader file alike: creating content, reviewing, reminders, spreadsheet import and export, backups, ZIP archives.

Only a few **optional** features use the internet, and only when you trigger them: image generation, free-licence photo and definition search, and the buttons that open an AI from the prompt generator.

**Imported content is treated as untrusted.** A crafted spreadsheet or backup cannot execute code: text is neutralised before display, and only `https://` or `http://` web addresses can be opened.

---

## Platforms and browsers

| Platform | File opened from disk | File served from a web address |
|---|---|---|
| **Windows, macOS, Linux — Firefox** | Full | Full |
| **Windows, macOS, Linux — Chrome, Edge** | Reduced capacity, see below | Full |
| **Android — Firefox, Chrome** | Full | Full |
| **iPad, iPhone** | Not supported | Not supported |

**Chrome and Edge** refuse full storage to files opened from disk. The application then switches to fallback storage and says so with a banner: everything works, but capacity drops to a few megabytes, quickly insufficient with images. Two solutions: open the file in **Firefox**, or serve it from a web address — a small local server is enough.

**The reader file** does not have this limit: a student's progress weighs a few kilobytes, which fallback storage handles easily.

**On a network drive**, use a drive letter (`Z:`) or a web address rather than a `\\server\share` path, which some browsers block. Data is never written to the share: each user has their own, on their own machine, and twenty students can open the same file at once.

**On iPad and iPhone**, the Files app preview does not execute JavaScript: the application cannot start from a local file. A message explains this instead of showing a blank page.

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

- **Palace** — a subject, a syllabus, a theme. *"Year 10 History"*
- **Room** — a chapter, a topic. *"The Second World War"*
- **Object** — a card, one thing to remember. *"D-Day landings"*

An object holds a **title** (the question), the **information to remember** (the answer), and optionally an **image**, a **mnemonic phrase**, **tags** and an **attached document**.

The sort order chosen on the home screen applies to every palace list in the application.

## 2. Creating content

Four routes:

- **The prompt generator** — the easiest way to start, see the next section.
- **A spreadsheet**, filled in by hand or by an AI. Download the blank template from Settings → Create and organise content → Spreadsheet import/export [*Paramètres → Créer et organiser le contenu → Import / export tableur*]. One row = one card; missing palaces and rooms are created on import.
- **By hand**, palace by palace.
- **Importing** a backup or an archive, JSON or ZIP.

> The spreadsheet column names stay in French — `palais`, `salle`, `objet`… — because they are the headers the application expects.

**After an import**, a summary [*Import terminé*] confirms everything is saved — number of cards, details per palace — and offers, **as an option**, to add images, with an estimate of the time needed. This can also be done later.

## 3. The prompt generator

It writes the request to give an AI for you. Side menu → **Prompt generator** [*Générateur de prompt*].

**Three levels of customisation:**

| Level | What you fill in |
|---|---|
| **Express** | The subject, the audience, the number of cards. The AI proposes the rest. |
| **Guided** [*Guidé*] — *default* | + palace name, rooms, content types, images, favourites |
| **Expert** | + "Method" and "Trap" lines, mnemonics, answer length, image style, reference to follow, exclusions |

**The rules of a good spaced-repetition card are added automatically**, at every level: atomic facts, a title that never contains the answer, answers that are all different for reverse review, a ban on inventing, no maps or distressing subjects in images.

**Adapt for** [*Adapter pour*], at every level:
- five boxes that combine: **dyslexia and dysorthographia, dyscalculia, dyspraxia, dysphasia, attention disorders**;
- **students learning French as a second language (FLS)**: 35 home languages to choose from, plus a free field, and a French level from A1 to B1. The AI adds a translation and, where needed, a transliteration into the Latin alphabet. Have it checked by a speaker when possible.

**The result** updates live. "Copy the prompt" [*Copier le prompt*], "Download the blank template" [*Télécharger le modèle vierge*], then six AIs — ChatGPT, Claude, Gemini, Le Chat, DeepSeek, Copilot: each button copies the prompt, then opens the site. Attach the blank template and paste. **"+ Add an AI"** [*+ Ajouter une IA*] adds any other AI by its address.

**For free AIs** that cannot produce a file, the prompt asks them for a semicolon-separated CSV table, which the application also imports.

**The library** keeps your prompts: reload them into the form, rename, edit, copy, delete.

## 4. Refining content

Generated content is broadly right, never perfect. **Walk-through** mode [*Parcourir*] steps through cards with no questioning: it is the proofreading mode.

- **Edit** fixes the card and returns you to the same card.
- **The star** marks what deserves to be kept.

**The curation workflow**, to extract the best from a large generated palace:

1. Duplicate the palace ("More" menu)
2. Walk through the copy, starring what you keep
3. Inside a room, click **Favourites** until it reads **"Non favourites"** [*Non favoris*]
4. Select all, delete

Deletion stays undoable for twelve seconds, and a snapshot is taken beforehand.

## 5. Images

Three sources, for one card or a batch:

- **AI generation** — Pollinations.ai, free, no account, key optional
- **Free photo** [*Photo libre*] — Openverse, Wikimedia Commons; author, source and licence are kept
- **Import** from your device

**Style matters more than anything.** "True to subject" [*Fidèle au sujet*] illustrates the concept; the other styles create offbeat scenes, effective for an isolated word. In a batch, the style is fixed for the whole run.

**Batch images** [*Images en lot*]: Settings → Images and online services, or a palace's "More" menu.

## 6. Attached documents

Each card can carry a PDF or an office document. The PDF opens during review, even offline; other formats open in the student's own software. A batch import attaches each file to the card whose title matches its name.

## 7. Reviewing

Review is spaced: a card you knew comes back later, one you missed comes back soon.

**Above each question**, a line shows where the card comes from — *● Year 10 History › The Second World War* — in the palace's colour. You always know where you are, even in a review that mixes several rooms.

During a review: edit the card, star it, **set it aside** to resume later, show the mnemonic phrase, hide images. An interrupted session is offered for resumption on your return.

**Position mode** asks you to recall a card from its room and its rank, as in a real memory palace.

## 8. Favourites

The star marks a card — in a room, during review or walk-through. Side menu → **Favourites** [*Favoris*] reviews them all, across palaces; **"Walk through favourites"** [*Parcourir les favoris*] rereads them without questioning.

A room's filter has three states: all, favourites, non favourites. **Bulk removal** in Settings → Create and organise content → Favourites.

## 9. Reminders

A reminder series schedules reviews on specific dates: what to revisit, a starting point, intervals — D+1, D+3, D+7…

Ready-made series: **Forgetting curve**, **Progressive**, **Weekly**, **Exam run-up**. All editable. The **Agenda** shows a calendar with colour dots.

## 10. Backing up, archiving

Settings → Export and back up [*Exporter et sauvegarder*]:

- **Backup & transfer** [*Sauvegarde & transfert*] — the **full backup**, JSON or ZIP: palaces, images, documents, progress, reminders, wallpaper, services, prompt library, added AIs. And the **archive of selected palaces** [*Archiver certains palais*], with no settings at all: re-importing it touches nothing else.
- **Automatic backups** [*Sauvegardes automatiques*] — snapshots taken before every risky operation, restorable.

> Service access keys are **never** exported.

## 11. Importing a large base

During an import, a window shows the current step, progress and an estimate of the time remaining. At the end, a summary places the base: **comfortable** under 3,000 cards, **loaded** up to 8,000, **heavy** beyond. These are estimated guidelines, not limits: beyond them everything works, more slowly on a phone. Archive inactive subjects at that point.

## 12. Exporting for students

Settings → Export and back up → **Read-only export** [*Exporter en lecture seule*]:

1. Unfold **"Choose palaces"** [*Choisir les palais*] and tick those to distribute
2. Check the **estimated size** and the comfort indicator
3. Choose a name, or one of the suggestions
4. Tick **"Reset review statistics"** [*Réinitialiser les statistiques*] if the file is for someone else
5. Generate

| Size | What to expect |
|---|---|
| under 8 MB | Comfortable everywhere |
| 8 to 25 MB | Slightly slow to open on older devices |
| 25 to 60 MB | Email attachment often refused |
| over 60 MB | Risk of failure on a phone |

**After a correction, regenerate and redistribute**: a file already handed out does not update itself.

## 13. Wallpaper

Settings → Appearance → Wallpaper [*Apparence → Fond d'écran*], three tabs: **Generate (AI)**, **Free photo**, **Import**. A click places an image in preview; your current wallpaper stays until **"Apply this wallpaper"** [*Appliquer ce fond*], and **"Back to previous wallpaper"** [*Revenir au fond précédent*] undoes it.

## 14. Settings, explanations and glossary

Settings are organised under **five themes**, each with its colour: create and organise content, images and online services, export and back up, appearance, advanced. Each section shows **a one-line summary**, even when folded.

**Detailed explanations are hidden** and open section by section with the **"?"**. To show them everywhere: Appearance → **"Always show explanations"** [*Toujours afficher les explications*].

**The Glossary** [*Glossaire*] — side menu — defines about forty terms in five families, with a search and, for each word, where to find it.

---

# Part two — The reader file

*Hand this section to students.*

## Opening it

Double-click the file. It opens in your browser. **No connection required**, and nothing is sent anywhere.

If a message says the file cannot open here, it is being shown in a simple preview: open it in Firefox, Chrome or Edge.

## What you can do

**Browse** palaces, rooms and cards. **Review**: a question appears, you think, you reveal, you say whether you knew it — the line above the question always shows the palace and the room. **Schedule your own reminders**. **Sort palaces**.

## What you cannot do

Create, edit or delete anything. The content is what your teacher approved.

## Your progress

It is saved **in your browser, on your device**, and reported to no one. You pick up where you left off on the same device and browser; it does not follow you to another computer.

If the browser refuses all storage, a banner warns you **before** you review for nothing.

---

# Part three — Technical reference

## Accepted formats

| Use | Formats |
|---|---|
| Content import | `.xlsx`, `.ods`, `.csv` (commas or semicolons), `.json`, `.zip` |
| Images | `.jpg`, `.png`, `.webp`, `.gif` |
| Attached documents | `.pdf`, `.docx`, `.doc`, `.odt`, `.xlsx`, `.xls`, `.ods`, `.csv`, `.rtf`, `.txt` |

## Limits

- **Attached document**: warning above 2 MB, refused above 12 MB
- **Images**: resized to 640 px; wallpaper to 1600 px
- **Reader file**: above 25 MB, email attachment is often refused

## Where the data lives

In the browser's storage, **per address** and not per file: two copies of the application opened from the same address share the same base. Data survives closing the browser, but not clearing browser data or changing device.

**Export regularly.** That is the only real backup.

## Image services

- **Pollinations** — AI generation. Delay imposed by the free service: about **16 seconds** for one image, **23 per image in a batch**. With a key: 6 and 9 seconds.
- **Free photos** — Openverse, Wikimedia Commons, and other services you can declare in Settings → Images and online services → Service access keys [*Clés d'accès aux services*].

## Troubleshooting

| Symptom | What to check |
|---|---|
| "Reduced storage in this browser" banner [*Stockage réduit dans ce navigateur*] | Chrome or Edge on a local file: open it in Firefox, or from a web address |
| "Cannot open here" message | The file is shown in a preview: open it in Firefox, Chrome or Edge |
| The reader file shows nothing | It comes from an old version: regenerate it |
| Image generation fails | VPNs are often blocked by the service, as is a key whose account has run out of credits |
| Favourites you never set | They came from the imported spreadsheet: bulk removal in Settings → Favourites |
| The application is slow on a phone | See the volume summary: archive inactive subjects |
| A deletion you regret | The undo banner (twelve seconds), otherwise a snapshot |

## Known limitations

- **iPad and iPhone**: not supported.
- **Chrome and Edge on a local file**: reduced storage capacity, see "Platforms and browsers".
- **SheetJS 0.18.5**, embedded to read spreadsheets, has known vulnerabilities when importing crafted files. Do not import spreadsheets of unknown origin.

## Resources supplied with the project

| File | Content |
|---|---|
| `TUTORIELS.md` | Six step-by-step walkthroughs, from the express route to backups (in French) |
| `GUIDE-ELEVE.md` | A one-page guide for students, to print or attach (in French) |
| `PROMPT-UNIVERSEL.md` | The prompt to copy to have an AI fill in a spreadsheet (in French) |
| `Palais-Mental-Prompts` (`.xlsx`, `.ods`) | 24 ready-made prompts by domain, and a questionnaire |
| `Palais-Mental-Schemas.drawio` | Five diagrams, editable in draw.io |

## Third-party libraries

Embedded in the file, under their respective licences:

| Library | Version | Licence |
|---|---|---|
| Vue | 3.4 | MIT |
| SheetJS | 0.18.5 | Apache-2.0 |
| PapaParse | 5.3.0 | MIT |
| JSZip | 3.10.1 | MIT or GPLv3, at your choice |

## Licence

See the `LICENSE` file.
