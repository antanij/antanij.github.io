# Jyot Antani: personal website

Source code for my academic website, **https://antanij.github.io**.
Built with [Hugo](https://gohugo.io) and the [Hugo Blox](https://hugoblox.com) Academic CV template
(the successor of Wowchemy). Every push to `master` is built and published automatically by
GitHub Actions (`.github/workflows/deploy.yml`) to GitHub Pages.

---

## Preview the site on my computer (before committing)

### One-time setup

1. **Go**: `winget install GoLang.Go` (already installed).
2. **Node.js 22 or newer**: `winget install OpenJS.NodeJS.LTS`
3. **Hugo 0.161.1 extended**: download
   [hugo_extended_0.161.1_windows-amd64.zip](https://github.com/gohugoio/hugo/releases/download/v0.161.1/hugo_extended_0.161.1_windows-amd64.zip)
   and unzip `hugo.exe` to `C:\Users\jyota\Hugo161\hugo.exe`.
   (Keep the old `C:\Users\jyota\Hugo\hugo.exe` only if you still need the old Wowchemy site.)
4. Quit GitHub Desktop completely (File → Exit) and reopen it, so it sees the new programs.
5. In GitHub Desktop: **Repository → Open in Command Prompt**, then run once:

   ```
   npm install
   ```

   (Creates a `node_modules` folder for the Tailwind CSS styling. It's ignored by git.)

### Each time

1. In GitHub Desktop: **Repository → Open in Command Prompt**.
2. Run:

   ```
   C:\Users\jyota\Hugo161\hugo.exe server
   ```

3. Open **http://localhost:1313**. The page refreshes on every file save.
4. Press **Ctrl+C** to stop.

Note: the search box only works on the published site (its index is built during deployment).

---

## Where things live

| What | File / folder |
|---|---|
| Name, role, social links, interests, education | `data/authors/me.yaml` |
| Profile photo | `assets/media/authors/me.jpg` |
| Homepage layout + the long "About" text | `content/_index.md` |
| Key Publications (one folder per paper, with `featured.png`) | `content/project/<paper>/index.md` |
| Science Outreach posts | `content/post/<post>/index.md` |
| Experimental Protocols | `content/protocols/` (see below) |
| PDFs (CV, papers) | `static/media/` → served at `/media/<FileName>.pdf` |
| Images used inside the About text | `assets/media/` (write `![alt](file.jpg)`) |
| Top menu | `config/_default/menus.yaml` |
| Site name, description, colours, footer | `config/_default/params.yaml` |
| Hugo version used for publishing | `hugoblox.yaml` |

## Experimental Protocols

Drop a Markdown (`.md`) file into `content/protocols/` and commit. That's it.

- Each file gets its own page: `phage_growth.md` → `/protocols/phage_growth/` (share this link).
- Each page also gets a **printer-friendly copy** (always light, no menu) at
  `/print/protocols/<file-name>/`, linked as "Printer-friendly version" on the page.
- An optional header sets the title; without it the title comes from the file name:

  ```
  ---
  title: Phage growth (for beginners)
  ---
  ```

- The intro text (and the agarose-pad video link) is in `content/protocols/_index.md`.
- `.txt` files also work (shown as expandable plain text on the list page), but Markdown is recommended.
- Templates: `layouts/protocols/` (`single.print.html` is the printable version).

## Gallery

Each image or movie is one small `.md` file in `content/gallery/` and gets its own page
(`/gallery/<file-name>/`). Put the media file in `static/media/`, then copy an existing gallery file and edit:

```
---
title: Bacterial monolayer
media: /media/bacteria_monolayer.jpg     # image (.jpg/.png) or movie (.mp4)
poster: /media/some_still_frame.jpg      # movies only: frame shown before playing
alt: Short description for screen readers
weight: 30                               # order on the Gallery page
---
Caption text (Markdown).
```

Browsers can't play `.avi`. Convert movies to `.mp4` (and optionally `.webm`, used automatically when
a file with the same name exists), e.g. with ffmpeg:
`ffmpeg -i movie.avi -vf "scale=trunc(iw/2)*2:trunc(ih/2)*2,format=yuv420p" -c:v libx264 -crf 20 -an movie.mp4`

## Homepage animation

The animated figure in the About text is `static/media/feature_with_bacBurst.mp4`/`.webm`
(made from `feature_with_bacBurst.gif`, ~30x smaller, and it scales to phone screens).
It is a `<video>` tag inside `text:` in `content/_index.md`.

## Adding a paper

1. Copy an existing folder in `content/project/`, rename it, and edit `index.md` (title, date, summary text, links).
2. Replace `featured.png` with an image for the paper.
3. Put the PDF in `static/media/` and link it as `/media/Exact_File_Name.pdf`.
   **Capitalisation must match exactly**: GitHub Pages treats `CV.pdf` and `cv.pdf` as different files.

Link icons: `academicons/doi`, `hero/document-text` (PDF), `hero/newspaper`, `hero/beaker`,
`hero/user`, `brands/bluesky`, `brands/youtube`, `brands/github`, `brands/x`.

## The old Netlify address

`antanij.netlify.app` forwards to this site through the redirects in `netlify.toml`
(see `netlify.redirect.toml`). Keep the Netlify site in place so links shared in the past keep working.
