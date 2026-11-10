# jballesterosc.github.io

A single-page site in the style of [Jon Barron's website](https://jonbarron.info), via [leonidk.github.io](https://github.com/leonidk/leonidk.github.io).

## Editing

- **Bio**: `index.html`
- **Email / Resume / GitHub / LinkedIn links**: `_config.yml`
- **Writing list**: `_data/writing.yml`
- **Styles**: `assets/css/style.css`

Push to `main` and the GitHub Action builds the site and deploys it to the `gh-pages` branch.

## Previewing locally

```sh
bundle install
bundle exec jekyll serve
```
