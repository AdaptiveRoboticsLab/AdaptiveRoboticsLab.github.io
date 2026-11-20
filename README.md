# Adaptive Robotics Lab website

Source for https://adaptiveroboticslab.github.io, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll template.

## How to update

Edit files on the `main` branch; GitHub Actions rebuilds and deploys the site to the `gh-pages` branch in a few minutes.

| What | Where |
| --- | --- |
| Home page (hero, research cards, join us) | `_pages/about.md` |
| Research areas | `_pages/research.md` |
| People | `_pages/people.md` |
| Publications | `_bibliography/papers.bib` (add `selected = {true}` to show on the home page) |
| News | one file per item in `_news/` (copy an existing one) |
| Site title, URL, settings | `_config.yml` |
| Images | `assets/img/` |
| Colors and styling (CSU branding) | bottom of `assets/css/main.scss` |

Template documentation: `docs/` and `docs/AL_FOLIO_README.md`.
