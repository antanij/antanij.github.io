# Jyot Antani: personal website

Source code for my academic website, live at **https://antanij.netlify.app**.
Built with [Hugo](https://gohugo.io) and the [Wowchemy](https://wowchemy.com) Academic theme; deployed automatically by Netlify whenever I push to `master`.

---

## Preview the site on my computer (before committing)

One-time setup (already done on my laptop): Go installed (`winget install GoLang.Go`) and
Hugo **0.79.1 extended** unzipped to `C:\Users\jyota\Hugo\hugo.exe`
([download](https://github.com/gohugoio/hugo/releases/download/v0.79.1/hugo_extended_0.79.1_Windows-64bit.zip)).
This exact old Hugo version is required by the theme.

Each time:

1. In GitHub Desktop: **Repository → Open in Command Prompt**.
2. Run:

   ```
   C:\Users\jyota\Hugo\hugo.exe server
   ```

3. Open **http://localhost:1313** in the browser. The page refreshes on every file save.
4. Press **Ctrl+C** in the Command Prompt to stop.

If it complains that `go` is not found: fully quit GitHub Desktop (File → Exit) and reopen it.

---

## Where things live

| What | File / folder |
|---|---|
| Bio, education, social icons | `content/authors/admin/_index.md` (photo: `avatar.jpg` in same folder) |
| Key Publications (one folder per paper, with `featured.png`) | `content/project/<paper>/index.md` |
| Science Outreach posts | `content/post/<post>/index.md` |
| Experimental Protocols | `content/protocols/` (see below) |
| PDFs (CV, papers) | `static/media/` → served at `/media/<FileName>.pdf` |
| Top menu | `config/_default/menus.toml` |
| Site title, copyright, base URL | `config/_default/config.toml` |
| Theme, colours, contact info, sharing image | `config/_default/params.toml` |
| Homepage sections (turn on/off with `active:`) | `content/home/*.md` |

## Experimental Protocols

Drop a `.md` or `.txt` file into `content/protocols/` and commit. That's it.

- **`.md` files** get their own page (`/protocols/<file-name>/`). An optional header sets the title;
  without it the title is made from the file name (`phage_growth.md` → "Phage growth"):

  ```
  ---
  title: Phage growth (for beginners)
  ---
  ```

- **`.txt` files** appear on the protocols page as expandable sections, plus a raw-file link at
  `/protocols/<file-name>.txt`. A direct link that opens one: `/protocols/#<title-with-dashes>`,
  e.g. `/protocols/#phage-fluorescent-labeling`.
- The intro text at the top of the page is in `content/protocols/_index.md`.
- The page templates are in `layouts/protocols/` (no need to touch them).

## Adding a PDF and linking it

1. Put the file in `static/media/` (keep the exact capitalisation you'll use in the link).
2. Link it with a path that starts with a slash, e.g. `/media/CV_JAntani.pdf`.

## Other customisations

- `layouts/partials/social_links.html` adds support for custom SVG icons (`icon_pack: custom`);
  the Bluesky logo is `assets/images/icon-pack/bluesky.svg`.
- `netlify.toml` holds the build settings and redirects (e.g. the old protocol link).
