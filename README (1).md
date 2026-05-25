# ICRTACM-2026 — Conference Website

**7th International Conference on Recent Trends in Applied and Computational Mathematics**
School of Applied Science, REVA University, Bangalore
**October 30–31, 2026**

---

## Repository Structure

```
ICRTACM-2026/
├── index.html                  ← Entire website (HTML + CSS + JS in one file)
├── README.md                   ← This file
└── assets/
    ├── img/
    │   ├── banner.jpg          ← Hero section banner image (replace with your image)
    │   ├── reva_logo.png       ← REVA University logo (replace with official logo)
    │   └── speakers/           ← Speaker photos go here
    │       └── speaker1.jpg    ← Name files as speaker1.jpg, speaker2.jpg, etc.
    ├── fonts/                  ← Local fonts if needed (currently using Google Fonts)
    └── docs/
        └── brochure.pdf        ← Conference brochure PDF (replace with actual brochure)
```

---

## How to Use

### 1. Open Locally
Simply open `index.html` in any modern browser. No server required.

### 2. Add Images
- Place the REVA University logo at: `./assets/img/reva_logo.png`
- Place the hero banner at: `./assets/img/banner.jpg`
- Place speaker photos at: `./assets/img/speakers/speakername.jpg`
- Place brochure PDF at: `./assets/docs/brochure.pdf`

### 3. Update Content in index.html
All content is in `index.html`. Search for these placeholders to update:

| Placeholder | What to replace with |
|---|---|
| `[Patron Name]` | Actual patron name |
| `[General Chair]` | Actual general chair name |
| `TBD` in tables | Actual dates once confirmed |
| Speaker cards | Uncomment speaker template, add real data |
| Payment details | Actual bank account details |
| Google Forms link | Update if form URL changes |

### 4. Add Speaker Cards
Find the comment block in the Speakers section and uncomment/duplicate:
```html
<div class="speaker-card">
  <div class="speaker-card__photo-wrap">
    <img src="./assets/img/speakers/speaker1.jpg" alt="Prof. Name" class="speaker-card__photo">
  </div>
  <div class="speaker-card__body">
    <div class="speaker-card__name">Prof. Full Name</div>
    <div class="speaker-card__designation">Designation, University, Country</div>
    <div class="speaker-card__topic">Talk Title</div>
  </div>
</div>
```

### 5. Deploy
Upload the entire folder (`index.html` + `assets/`) to the university web server.
The deployed URL should look like: `https://www1.reva.edu.in/ICRTACM-2026/`

---

## Tech Stack
- **HTML5** — semantic markup
- **CSS3** — custom properties, flexbox, grid, responsive design
- **Vanilla JavaScript** — no frameworks or libraries
- **Google Fonts** — Playfair Display + Lora + Source Sans 3
- **Font Awesome 6** — icons

---

## Contact
📧 icrtacm@reva.edu.in
📞 +91-9980923283
