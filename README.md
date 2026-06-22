# webpage-jnca-bc-iot-slr

Public landing page for the JNCA paper "Integrating blockchain and Internet of Things systems: A Systematic Review on Objectives and Designs" (Tran, Babar & Boan, JNCA Vol. 173, Article 102844, 2021).

Hosted via GitHub Pages at: `https://nguyentran0212.github.io/webpage-jnca-bc-iot-slr/`

## Layout

- `index.md` — page content (Markdown, processed by Jekyll)
- `_layouts/default.html` — base HTML template
- `assets/css/style.css` — single stylesheet
- `assets/pdf/BC_IoT_Survey.pdf` — downloadable copy of the paper
- `_config.yml` — site config (`baseurl` set to `/webpage-jnca-bc-iot-slr`)
- `Gemfile` — Jekyll dependency pinned to `~> 4.3`

## Local preview

Requires Ruby + Bundler.

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000/webpage-jnca-bc-iot-slr/
```

## Editing content

The page is one Markdown file. Sections (in order):
Hero → TL;DR → Key numbers → Abstract → Contributions → Cite → Source repos.

`baseurl` in `_config.yml` is set to `/webpage-jnca-bc-iot-slr`. If you ever move this to a custom domain or root, set `baseurl: ""` and `url: "https://yourdomain.com"`.

## Source

The canonical manuscript LaTeX source lives in the private repositories:
- `github.com/nguyentran0212/jnca_bc_iot_slr`
- `github.cs.adelaide.edu.au/CREST/jnca_bc_iot_slr`