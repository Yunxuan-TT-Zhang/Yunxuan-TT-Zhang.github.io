# Personal research website

A minimal, fast, static personal website — plain HTML/CSS/JS, no build step.
Designed to be published for free on **GitHub Pages**.

```
personal-website/
├── index.html     ← all your content
├── styles.css     ← design (change --accent at the top to recolor)
├── script.js      ← mobile menu + auto year
└── README.md      ← this file
```

---

## 1. Personalize it (10 minutes)

Open `index.html` and search for **`EDIT:`** — every comment marked that way
points to something you should change. The main ones:

- **Your name** — the site currently says `Y. Zhang` (from your preprint).
  Replace it everywhere with your full name. Quick find-and-replace `Y. Zhang`.
- **Profile links** — the Email / Google Scholar / GitHub / LinkedIn / X links
  use `href="#"` placeholders. Paste your real URLs.
- **Photo** — the round avatar is currently your initials on a gradient. To use
  a real photo, drop e.g. `profile.jpg` in this folder and replace the
  `<div class="hero__photo">…</div>` with `<img src="profile.jpg" class="hero__photo" alt="Y. Zhang" />`.
- **About / Interests** — rewrite in your own voice.
- **More publications** — copy the commented `<article class="pub">…</article>`
  block for each additional paper.

To change the accent color for the whole site, edit `--accent` (and
`--accent-strong`) at the top of `styles.css`.

## 2. Preview locally

Just double-click `index.html` — it opens in your browser. No server needed.
(Optional live server: `python3 -m http.server` then visit
`http://localhost:8000`.)

## 3. Publish on GitHub Pages

This will live at **https://yunxuan-tt-zhang.github.io** — for that URL the repo
must be named **exactly** `Yunxuan-TT-Zhang.github.io`.

### Fastest way (you already have the `gh` CLI signed in)

```bash
cd ~/Desktop/personal-website
git init
git add .
git commit -m "Personal website"
git branch -M main
gh repo create Yunxuan-TT-Zhang.github.io --public --source=. --remote=origin --push
```

For a `username.github.io` repo, GitHub Pages turns on automatically from the
`main` branch — wait ~1 minute and visit https://yunxuan-tt-zhang.github.io.
(If it isn't live, go to **Settings → Pages** and set Source =
**Deploy from a branch**, branch **main**, folder **/ (root)**.)

### Every later update

```bash
cd ~/Desktop/personal-website
git add .
git commit -m "Update site"
git push
```

The live site refreshes automatically within a minute.

> Note: `.gitignore` keeps the huge original uploads (`IMG_9229.jpg`,
> `website cartoon.png`) out of the repo — the optimized `profile.jpg` and
> `research-figure.png` are what get published.

---

Built as a starting point — make it yours.
