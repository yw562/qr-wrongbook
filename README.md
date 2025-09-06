# Wrongbook Suite

> A local-first toolkit for learning from mistakes — from quant interview prep to AI-powered knowledge graphs.

---

## 🌐 Live Demo
Try the apps directly in your browser — no installation needed:

- **[QR Wrongbook (recommended)](https://yw562.github.io/qr-wrongbook/qr_wrongbook_v1.1.html)**  
  A feature-rich, local-first wrong question notebook tailored for quant & QR interview prep.

- **[AI Mistake Notebook (experimental)](https://yw562.github.io/qr-wrongbook/ai-mistake-notebook-v1.1.html)**  
  A lightweight mistake analyzer for code/math/ML with automatic concept extraction and knowledge graph insights.

---

## 📖 Overview
You can use either of the two HTML files included in this repository:
- **`qr_wrongbook_v1.1.html`** → the recommended, feature-rich version for quant & QR interview prep.
- **`ai-mistake-notebook-v1.1.html`** → the experimental version focusing on code/math/ML with knowledge graph insights.

Simply download the file you want, then double‑click it to open in your browser — no installation needed.
This project combines two complementary tools:
- **QR Wrongbook** — a rich, feature-complete wrong question notebook designed for **quant & QR interview preparation**.
- **AI Mistake Notebook** — a lightweight, extensible notebook for **code, math, and ML mistakes**, featuring automatic concept extraction and a knowledge graph.

Both are **single-file, offline-first apps**: no backend, no tracking, just open in your browser.

---

## 🔹 Module A: QR Wrongbook
> A local-first “wrong question notebook” for quant & QR interview prep.

### Features
* 🗃️ **Local-first** — data stored entirely in your browser (IndexedDB), works offline
* 🧠 **Rich metadata** — category (Code / Math / Behavior / Machine Learning), difficulty (Easy → Deadly), mastery (Not at all → Mastered)
* 🖼️ **Screenshot support** — drag & drop, paste, or file picker
* 🧪 **Focus practice mode** — full-screen practice view, collapsible Hint/Solution, timer, and logs
* 💬 **Comments** — add & delete with confirmation
* 📊 **Stats dashboard** — study time, sessions, 30-day charts
* 🔎 **Search & filter** — full-text, multi-select filters, sorting
* 🎨 **Themes** — Light / Dark / Green gradient header
* 🔐 **Backup/restore** — Export/Import JSON

### Quick Start
```bash
# Clone
git clone https://github.com/yw562/qr-wrongbook.git
cd qr-wrongbook

# Local use
# Just double-click index.html in Chrome/Firefox/Edge/Safari
```

### Deploy on GitHub Pages
1. Push `index.html` + `README.md` to the `main` branch.
2. Settings → Pages → Deploy from branch → `main` / root (`/`).
3. Live at `https://yw562.github.io/qr-wrongbook/`.

---

## 🔹 Module B: AI Mistake Notebook
> A lightweight notebook for code, math, and ML mistakes with knowledge graph insights.

### Features
- Input problem + optional answer/attempt.
- Auto/manual type detection (`code`, `math`, `ml`).
- Auto-generate **concepts**, **insight**, **explanation**, **solution sketch**.
- Unlimited storage in `localStorage`.
- Knowledge graph (node frequency & color by type).
- **Import/Export JSON**.
- Optional: integrate local **Ollama LLM** for richer analysis.

### Example Concepts
- *Math*: `size-biased sampling`, `Horvitz–Thompson`, `unbiased estimator`
- *Code*: `enumerate`, `indexing`, `off-by-one`
- *ML*: `overfitting`, `ROC–AUC`, `cross entropy`

### Optional LLM (Ollama)
```bash
# Install Ollama
brew install ollama
ollama pull llama3.1:8b-instruct
ollama serve
```
Check **Use Local LLM (Ollama)** in UI.

---

## 📥 Bulk Import / Export
The QR Wrongbook app supports exporting and importing problems as JSON files, so you can back up your data or add many questions at once.

- **Export** → Use the Export button in the app to download all your problems as a JSON file.  
- **Import** → Use the Import button and select a JSON file in the correct format.

### Ready-to-use helpers
- **BULK_IMPORT.md** — full guide on how to structure import files (schema, examples, and an LLM prompt template for auto-generation).  
- **starter_import.json** — a sample JSON file with one demo problem. You can copy, replace, or expand it to create your own batch of problems.

### Typical workflow
1. Write problems in plain text (Math, Code, ML, Behavioral).  
2. Convert them into the JSON format (see **BULK_IMPORT.md** or generate with an LLM).  
3. Save the JSON as a file.  
4. Click **Import** in the app and select it.  
5. Done 🎉 — all problems are added locally in your browser.

---

## 🔮 Roadmap
- Richer LLM support (more models, better prompts)
- Editable **Hint / Solution / Note** fields
- Graph interactivity: click node → show related problems
- Spaced repetition scheduler based on difficulty
- Progress charts (error frequency over time)

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome!
- Fork and make a PR.
- Open issues for ideas/bugs.
- Suggestions for heuristics, prompts, or visualization especially appreciated.

---

## 📚 Citation
If you use this project, please cite:

**APA:**  
Wang, Y. (2025). *Wrongbook Suite: Local-first mistake notebooks for quant prep and AI error analysis*. GitHub. https://github.com/yw562/qr-wrongbook

**BibTeX:**
```bibtex
@misc{wang2025wrongbook,
  author       = {Yueyi Wang},
  title        = {Wrongbook Suite: Local-first mistake notebooks for quant prep and AI error analysis},
  year         = {2025},
  howpublished = {GitHub},
  url          = {https://github.com/yw562/qr-wrongbook}
}
```

---

## 📜 License
Released under **CC BY-NC 4.0**:
- **Share** — copy & redistribute the material
- **Adapt** — remix, transform, build upon it
- **Attribution** — give credit
- **NonCommercial** — no commercial use without permission

For commercial use, please contact the author.
