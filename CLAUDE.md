# CLAUDE.md

Quarto static website for the "Responsible Modelling" workshop (epidemiological modelling, LSHTM, March 2026).

## Workshop background
Epidemiological modelling is expanding in capacity and visibility (e.g. COVID-19), but professional norms for evaluation and ethical conduct are still forming. This workshop asks: what does responsible modelling look like in practice?

The day is structured around two complementary angles:
1. **Scientific responsibility** — technical evaluation of models (validity, assumptions, reproducibility). How do we assess model quality across contexts, from endemic disease programmes to real-time outbreak response?
2. **Social responsibility** — the role of values, expertise, and judgement when models inform public health decisions. Modelling choices are value-laden (parameter selection, objective functions, uncertainty quantification, ensemble interpretation). Who counts as an expert, and what are modellers' ethical duties?

Key intellectual threads (from organisers Kath Sherratt, Seb Funk, Erica Thompson):
- Evaluation is central: both of model outputs (predictions, forecasts) and modelling processes
- Expert judgement is unavoidable — the question is how to apply it well
- Communication alone is not the answer; responsibility starts upstream in model designs
- The goal is practical: identify what responsible practice looks like and how to embed it in training and workflows

Intended outcomes: shared resources/examples for good practice, a network of interest, and groundwork toward integrating responsible modelling into training (e.g. MSc modules, short courses, UKHSA-specific development).

Background references: Zotero library at https://www.zotero.org/groups/6153593/responsible_id_modelling

### Workshop style
Collaborative, ~50 participants, in a single room. Facilitation aims to use appropriate Liberating Structures techniques where relevant: https://www.liberatingstructures.com/ls/

## Commands
- `quarto preview` — local dev server with live reload
- `quarto render` — build the site to `_site/`

## Structure
- Root `.qmd` files — public website pages (index, schedule, register, about, resources)
- `admin/` — internal planning docs (agenda, logistics, TODOs); excluded from rendering
- `_quarto.yml` — site config, navbar, theme settings
- `styles.css` — custom CSS
- `_site/` — build output (gitignored)

## Conventions
- Pages are Quarto Markdown (`.qmd`), not plain `.md`
- Navbar defined in `_quarto.yml` under `website.navbar.left`
- Admin/planning files go in `admin/`, never rendered to the site
- MIT License (Epiforecasts)

## Deployment
GitHub Actions (`.github/workflows/publish.yml`) auto-renders and publishes to GitHub Pages on push to `main`. Site URL: https://epiforecasts.io/responsible-modelling/
