# talks

Presentations by Jing Sun, written in [Quarto](https://quarto.org) as reveal.js decks and published by GitHub Pages at
<https://teresajingsun.github.io/talks/> (served from the `docs/` directory of the `main` branch).

## Layout

- `index.qmd`: the list of decks (date, title, link).
- `<yyyy-mm-topic>/index.qmd`: one directory per deck, with its figures under `figs/` and its theme file next to it.
- `docs/`: the rendered site, committed so that GitHub Pages can serve it without a build step.

## Adding a deck

1. Create `<yyyy-mm-topic>/index.qmd` with `format: revealjs` and copy the figures it uses into `<yyyy-mm-topic>/figs/`.
2. Add a row to the table in `index.qmd`.
3. `quarto render` at the repository root, then commit the sources and `docs/` together and push.

The deck is then at `https://teresajingsun.github.io/talks/<yyyy-mm-topic>/`. A self-contained copy for offline use is
made with `quarto render <yyyy-mm-topic>/index.qmd -M embed-resources:true --output <file>.html` from a copy of the
deck directory outside this project.
