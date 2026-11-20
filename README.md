# Adaptive Robotics Lab website

Source for https://adaptiveroboticslab.github.io, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll template.

## How to update

Edit files on the `main` branch; GitHub Actions rebuilds and deploys the site to the `gh-pages` branch in a few minutes.

| What | Where |
| --- | --- |
| Home page text | `_pages/about.md` |
| Research areas | `_pages/research.md` |
| People | `_pages/people.md` |
| Publications | `_bibliography/papers.bib` (add `selected = {true}` to show on the home page) |
| News | one file per item in `_news/` (copy an existing one) |
| Teaching, Join us | `_pages/teaching.md`, `_pages/join.md` |
| Code page | `_data/repositories.yml` |
| Site title, URL, settings | `_config.yml` |
| Images | `assets/img/` |

Template documentation: `docs/` and `docs/AL_FOLIO_README.md`.
