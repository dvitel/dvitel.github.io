# Research homepage on GitHub Pages

Status: live at https://dvitel.github.io since 2026-09-07 (repo dvitel/dvitel.github.io, commit 6b22598, Pages build_type=legacy from main root).

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
  Article links (added 2026-09-07, resolved via Crossref / OpenReview API): ICLR → OpenReview `Dkgw08Z4sj`
  (ICLR 2026 poster) + arXiv 2511.04715; GECCO → doi:10.1145/3712256.3726464; EvoStar →
  doi:10.1007/978-3-031-90065-5_33 (LNCS, EvoApplications 2025 Part II, pp. 541-556).
- Contact email is `dvitel@usf.edu` (replaced Gmail 2026-09-07). It is stored as `data-u`/`data-d` attributes
  and assembled into the `mailto:` by a few lines of JS, with `dvitel [at] usf [dot] edu` as the no-JS text,
  so the address never appears as a plain `mailto:` in the HTML source. Gmail remains only inside the CV PDF.

## To update

Edit `index.html` directly, bump the "Last updated" footer, replace `assets/Dmytro_Vitel_CV.pdf`.
