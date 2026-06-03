# Yousra Mohammed — Interactive CV

A single-page, fully responsive personal CV site built with **vanilla HTML, CSS and JavaScript** — no frameworks, no build step required.

## Features
- Top profile photo with accessible `alt` text and semantic markup
- Sections derived from the CV: Summary, Experience, Projects, Skills, Education, Languages, Certifications, Contact
- Smooth-scrolling navigation with active-section highlighting (scroll-spy)
- Collapsible experience entries + an **Expand all / Collapse all** control
- **Download CV** button linking to the original PDF
- **Light / dark theme toggle** (respects system preference, remembers your choice)
- Animated stat counters, scroll-reveal, and language proficiency bars
- Mobile menu, reduced-motion support, and a print-friendly stylesheet
- Accessible: skip link, ARIA states (`aria-expanded`, `aria-current`, `aria-pressed`), keyboard focus styles, landmark elements

## File structure
```
site/
├── index.html                    # the entire app (HTML + CSS + JS inline)
├── README.md
├── package.json                  # optional: local static server script
└── assets/
    ├── profile.png               # headshot (extracted from the CV)
    └── Yousra-Mohammed-Resume.pdf # downloadable resume
```

## Run locally
The site is fully static. The simplest options:

**Option A — just open it**
Open `index.html` in any browser. (Fonts load from Google Fonts, so keep an internet connection.)

**Option B — a local server** (recommended, avoids any file:// quirks)
```bash
# Python (no install needed)
cd site
python3 -m http.server 8080
# → visit http://localhost:8080
```
or, using the included npm script:
```bash
cd site
npm install      # installs the lightweight 'serve' dev dependency
npm start        # serves at http://localhost:3000
```

## Build for production
There is **no build step** — the files in `site/` are the production artifact.
To deploy, upload the contents of `site/` to any static host:
- **Netlify / Vercel / Cloudflare Pages:** drag-and-drop the `site/` folder, or point the project root at it.
- **GitHub Pages:** push `site/` to a repo and enable Pages on the branch/folder.
- **Any web server (S3, Nginx, Apache):** copy `site/` to the web root.

## Customizing
- **Colors / theme:** edit the CSS variables in the `:root` and `html[data-theme="dark"]` blocks at the top of `index.html`.
- **Content:** all copy lives directly in the HTML, organized by `<section>`.
- **Replacing the photo:** drop a new image into `assets/` and update the `<img src>` in the hero.
- **Replacing the PDF:** swap `assets/Yousra-Mohammed-Resume.pdf` (keep the filename, or update the two download links).
