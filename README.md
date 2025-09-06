
# QR Wrongbook

> A local-first “wrong question notebook” for quant & QR interview prep.
> Single-file, privacy-friendly, no backend, runs anywhere.

* 🗃️ **Local-first** — data stored entirely in your browser (IndexedDB), works offline
* 🧠 **Rich metadata** — category (Code / Math / Behavior question / Machine Learning), difficulty (Easy → Deadly), mastery (Not at all → Mastered)
* 🖼️ **Screenshot support** — drag & drop, file picker, or paste (Ctrl/Cmd+V)
* 🧪 **Focus practice mode** — full-screen single question view with collapsible Hint/Solution, timer, and practice log
* 💬 **Comments** — add & delete (with confirmation)
* 📊 **Stats dashboard** — total study time, sessions, practiced days, last 30 days daily chart
* 🔎 **Search & filter** — full-text, multi-select filters, sorting
* 🎨 **Themes** — Light / Dark / Green + soft translucent gradient header
* 🔐 **Backup/restore** — one-click Export / Import (JSON)

---

## 1. Quick start

```bash
# Clone
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# Or: create a new GitHub repo → upload index.html + README.md

# Local use
# Just double-click index.html and open it in Chrome/Firefox/Edge/Safari
```

> No Node.js, no backend, no build tools. It’s a **single static file**.

---

## 2. Deploy on GitHub Pages

1. Push `index.html` and `README.md` to the `main` branch of your repo.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**:

   * Source: `Deploy from a branch`
   * Branch: `main` / root (`/`)
4. Save. After a short while, your site will be live at:
   `https://<your-username>.github.io/<your-repo>/`

---

## 3. Usage

### Add Problem

* Top navigation → **Add Problem**
* Required:

  * **Title**
  * **Category**: Code / Math / Behavior question / Machine Learning
  * **Difficulty**: Easy / Medium / Hard / Deadly
  * **Mastery**: Not at all / A bit / Slightly unsure / Calculation error / Mastered
* Optional: Source, tags, Hint, Solution, screenshots

### Grid View

* Search box: full-text (title, body, tags)
* Filters: category / difficulty / mastery (multi-select)
* Sorting: newest, oldest, difficulty, mastery, category
* Cards show title, metadata, preview images
* Buttons: **Practice** (focus mode), **Edit**, **Mark Mastered / Unmark**, **Delete**

### Focus View

* Title, metadata, full question, images (click to enlarge)
* **Hint / Solution** sections are collapsible
* **Solution editor**: edit / save / clear
* **Comments**: add or delete (with confirmation)
* **Practice & Time**: start/pause/reset/log, sessions recorded per question

**Image viewer:** zoom, pan, fit, 100%, close

### Stats View

* Summary: total study time, total sessions, distinct days
* Last 30 days: bar chart (minutes/day, problems/day) + table

### Theme

* Right-hand dropdown: Light / Dark / Green
* Soft pastel gradient header (blue → aqua → mint, 92% opacity)
* Theme preference stored in localStorage

---

## 4. Data & Backup

### Storage

* All problems, screenshots, comments, and sessions live in **IndexedDB**
* 100% local, offline-friendly

### Export / Import

* **Export**: download `qr-wrongbook-backup.json`
* **Import**: upload the JSON to restore/merge
* Compatible with both `{"items": [...]}` and plain array format

### Backup file structure (excerpt)

```json
{
  "v": 2,
  "exportedAt": "2025-09-05T12:34:56.000Z",
  "items": [
    {
      "id": "uuid",
      "title": "Clan Size",
      "category": "Math",
      "difficulty": "Deadly",
      "mastery": "A bit",
      "tags": ["dp","expected value"],
      "hint": "…",
      "solution": "…",
      "images": [{ "name": "img1", "dataUrl": "data:image/png;base64,..." }],
      "comments": [{ "ts": 1711111111111, "text": "watch edge case" }],
      "sessions": [{ "start": 1711111111111, "end": 1711111211111, "durationSec": 100 }],
      "createdAt": 1711111111111,
      "updatedAt": 1711111211111
    }
  ]
}
```

---

## 5. Browser support & privacy

* Works in latest **Chrome / Edge / Firefox / Safari** (desktop preferred)
* Privacy: **no backend, no tracking, no third-party code**
* To clear all data: browser settings → privacy → clear site data / IndexedDB

---

## 6. FAQ

**Q: Import doesn’t work?**

* Make sure you’re importing the exported JSON.
* Check DevTools Console for error messages.
* Worst case: export your current data, clear site data, then re-import.

**Q: Images too small?**

* Click to open viewer → zoom with mouse wheel → drag to pan.

**Q: Comments won’t delete?**

* Each comment has a ✕ button. Deletion asks for confirmation.

**Q: Export file is huge?**

* Screenshots are base64-encoded. Consider removing unnecessary images before exporting.

---

## 7. Customization

Want a different header gradient? Edit in `index.html`:

```css
header {
  background: linear-gradient(
    90deg,
    rgba(165,216,255,0.92) 0%,
    rgba(153,246,228,0.92) 50%,
    rgba(185,251,192,0.92) 100%
  );
}
```

Lower the `0.92` to `0.88` for more transparency.
Themes live in `:root` variables.

---

## 8. Contributing

PRs and issues welcome! Ideas include:

* Spaced repetition scheduler
* Keyboard shortcuts
* Additional charting
* UI polish (keeping the single-file, offline-only spirit)

---

## 9. License

MIT License — free to use, share, hack on.

---

## 10. Project structure

```
.
├─ index.html      # Entire app in one file
└─ README.md       # This documentation
```

---

✨ Simple by design: just two files. Clone, open, start practicing.

---

Would you like me to also draft a **short GitHub repo tagline + topics** (so your repo shows up in search/discovery for “quant interview prep”, “local-first”, “wrongbook”)?
