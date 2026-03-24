# ARVO Topic Arranger

A browser-based drag-and-drop tool for reordering curriculum topic tags across grades and chapters. Built for [ARVO Schools](https://arvoschools.com) to manage **SNC-aligned FET & Topic Repository mappings** across K–12 subjects.

**[▶ Launch Live Tool](https://arvoai-03-cloud.github.io/arvo-topic-arranger/)**

---

## What It Does

| Feature | Description |
|---|---|
| **Upload** | Drop any `.csv`, `.xlsx`, or `.xls` file with topic metadata |
| **Smart Header Detection** | Auto-detects the header row — handles title rows, metadata rows, and merged cells |
| **Column Mapping** | Maps columns automatically (Grade, Chapter, FET Main Topic, etc.) with manual override |
| **Drag & Drop Reorder** | Grab any row and drag it to a new position within a chapter |
| **FET Main ↔ Sub Swap** | One-click to move a topic from FET Main Topic to FET Sub Topic column (and back) |
| **Undo** | Tracks up to 50 actions with full undo support |
| **Export** | Downloads a clean `.xlsx` file with your reordered data and original column names preserved |

## Getting Started

### Option 1: Use Online (GitHub Pages)

1. Go to the [live tool link](https://arvoai-03-cloud.github.io/arvo-topic-arranger/)
2. Upload your file
3. Map columns → Arrange → Export

### Option 2: Run Locally

1. Clone this repo:
   ```bash
   git clone https://github.com/YOUR_USERNAME/arvo-topic-arranger.git
   ```
2. Open `index.html` in any browser — no server required.

## Expected File Format

Your file should have these columns (names are flexible — you map them in Step 2):

| Column | Required | Example |
|---|---|---|
| Grade | ✅ | `1`, `2`, `3` |
| Chapter | ✅ | `1`, `2`, `10` |
| Chapter Name | ✅ | `Living and Non-Living Things` |
| FET - Main Topic | ✅ | `Breathe`, `Growth`, `Photosynthesis` |
| FET - Sub Topic | Optional | *(often empty — you can move Main → Sub in the tool)* |
| Topic Repository | Optional | `Characteristics of living things` |
| Subject | Optional | `Science`, `Math` |

Title rows and metadata rows above the headers are handled automatically.

## Use Cases

- **Curriculum teams** reordering topic tags to match textbook sequence
- **Content managers** fixing FET Main vs Sub Topic classifications
- **QA reviewers** verifying topic alignment across grades and chapters
- Works with any subject — Science, Math, Urdu, English, ICT, Social Studies

## Tech Stack

Zero build step. Single HTML file. Runs entirely in the browser.

- **[SheetJS (xlsx)](https://sheetjs.com/)** — Excel read/write
- **[PapaParse](https://www.papaparse.com/)** — CSV parsing
- **Vanilla JS** — No framework dependencies
- **Plus Jakarta Sans** — Typography via Google Fonts

## Screenshots

| Upload | Column Mapper | Arranger |
|---|---|---|
| ![Upload](screenshots/upload.png) | ![Mapper](screenshots/mapper.png) | ![Arranger](screenshots/arranger.png) |

> Add your own screenshots to a `screenshots/` folder.

## License

MIT — free to use, modify, and distribute.

---

Built with ☕ at **ARVO Schools** for Pakistan's K–12 education ecosystem.
