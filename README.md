# Adaptive Robotics Lab website

Source for https://adaptiveroboticslab.github.io, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll template.

## How to update

Edit files on the `main` branch; GitHub Actions rebuilds and deploys the site to the `gh-pages` branch in a few minutes.

| What | Where |
| --- | --- |
| Home page (hero, research cards, join us) | `_pages/about.md` |
| Research areas (overview figure + cards) | `_pages/research.md`; one page per area in `_areas/`; tag papers with `area = {soft}` (or reconfigurable, aerial, multimodal) in `papers.bib` |
| Robots (card grid + one page per robot) | `_pages/robots.md`, one file per robot in `_robots/` |
| People | `_pages/people.md` |
| Publications | `_bibliography/papers.bib` (add `selected = {true}` to show on the home page) |
| News | one file per item in `_news/` (copy an existing one) |
| Site title, URL, settings | `_config.yml` |
| Images | `assets/img/` |
| Colors and styling (CSU branding) | bottom of `assets/css/main.scss` |

Template documentation: `docs/` and `docs/AL_FOLIO_README.md`.

## Adding a robot

1. Copy `_robots/tecobot.md` to `_robots/<name>.md`. The file name becomes the URL (`/robots/<name>/`).
2. In the front matter, set `title`, a one-line `description`, `year`, `venue`, and `order` (smaller numbers show first).
3. Put images in `assets/img/robots/<name>/` and videos in `assets/video/robots/<name>/`.
   - `img`: card picture (16:9 works best; it is also the poster for the card video).
   - `card_video` (optional): a short, muted, looping `.mp4` shown on the card instead of the picture.
   - Keep each video small (under ~2 MB): 640–960 px wide, no audio, H.264. Example:
     `ffmpeg -ss 0:10 -t 8 -i input.mp4 -an -vf "scale=960:-2,fps=24" -c:v libx264 -crf 28 -pix_fmt yuv420p -movflags +faststart out.mp4`
4. Add the paper to `_bibliography/papers.bib` and cite it at the bottom of the robot page with `{% cite key %}` (keep `related_publications: true` in the front matter so the reference list appears).

Building locally on Windows: ImageMagick's `convert` is not available, so build with `imagemagick.enabled: false` in a local override config (`bundle exec jekyll build --config _config.yml,_config.local.yml`).

## Lab logo

The logo files are in `assets/img/logo/` (navbar mark, gold dark-mode mark, iPhone icon, link-preview image) plus `assets/img/favicon.png`. Sources are on the "Logo Concepts" page of the Overview Figma file. To show the logo next to the lab name on every page, `_includes/header.liquid` is a local copy of the theme's header with the brand block changed; if you upgrade the al-folio gems, re-check that file against the new theme version.
