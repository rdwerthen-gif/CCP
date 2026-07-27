# Cloud+ CV0-004 Study Desk — Website Files

This folder contains the full source for the Cloud+ Study Desk, split into standard
web files instead of one combined HTML file.

## Folder structure

```
cloudplus-study-desk/
├── index.html          Main page — open this file in a browser to run the site
├── css/
│   └── styles.css      All visual styling (themes, layouts, components)
└── js/
    └── app.js          All application logic and data (questions, flashcards,
                         acronyms, PBQs) — everything runs client-side
```

## How to use it

- **Just want to study?** Double-click `index.html` to open it in your browser.
  Works completely offline — no server, install, or internet connection required.
- **Want to host it online?** Upload the whole folder (keeping the structure intact)
  to any static web host (GitHub Pages, Netlify, S3, your own server, etc.). No
  build step is needed — these are plain HTML/CSS/JS files.
- **Want to edit it?** `app.js` contains the question bank, flashcards, acronym
  list, and all the app's logic. `styles.css` contains every theme and layout.
  Both are plain text and safe to open in any code editor.

## Data & privacy

The site saves your quiz progress and settings locally in your browser
(`localStorage`). Nothing is ever sent to a server — there isn't one. Clearing
your browser data or switching browsers/devices will reset your saved progress.

## Note on file:// vs a local server

Opening `index.html` directly by double-clicking (`file://...`) works fine for
this site, since everything is plain HTML/CSS/JS with no server-side dependency.
If your browser ever blocks local file access for any reason, you can also run
a simple local server from this folder, e.g.:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000` in your browser.
