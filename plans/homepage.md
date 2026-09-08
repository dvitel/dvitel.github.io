# Research homepage on GitHub Pages

Status: page built locally 2026-09-07, not yet pushed. Owner creates the `dvitel.github.io` repo and pushes.

## Goal

A single-page academic homepage at `https://dvitel.github.io`: photo, short bio, research interests,
three most recent publications, education, links (Scholar, ORCID, GitHub, LinkedIn, email), CV download.

## Decisions

- Plain static HTML + CSS, no build step, no framework, no external requests. Chosen over al-folio /
  academicpages because the content is a CV's worth and the page must stay easy to update by hand.
- Repo name `dvitel.github.io`, served from the `main` branch root. `.nojekyll` disables Jekyll processing.
- No custom domain.
- Photo: `~/Downloads/IMG_4342.JPG` (iPhone, 4032x3024) cropped to a 2300 px square at x=770,y=0 and scaled to
  640x640 with ffmpeg lanczos, q=3 → `assets/photo.jpg` (33 KB). Rendered as a 168 px circle.
- CV: copied from `~/Documents/CVs/Dmytro_Vitel_CV__PostDoc_.pdf` to `assets/Dmytro_Vitel_CV.pdf`.
  Replace the copy whenever the CV changes.
- Selected publications = three most recent from the CV (ICLR 2026, GECCO 2025, EvoStar 2025). Code links
  taken from the CV's own hyperlinks: `nn-infl` + `nn-infl-data` (ICLR), `cde-search` (GECCO and EvoStar).

## To update

Edit `index.html` directly, bump the "Last updated" footer, replace `assets/Dmytro_Vitel_CV.pdf`.
