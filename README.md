# Ayon Ghosh — academic website

A research-led personal website based on [al-folio](https://github.com/alshedivat/al-folio), using its versioned Jekyll core. Prepared for https://ayon8181.github.io.

## Edit content

- `_pages/about.md`: homepage and introduction
- `_pages/research.md`: research overview
- `_projects/*.md`: individual project pages, ordered by `importance`
- `_bibliography/papers.bib`: publications, rendered using jekyll-scholar
- `_pages/cv.md`: background, teaching, and service
- `_pages/contact.md` and `_data/socials.yml`: contact details
- `_sass/_themes.scss`: teal / ivory / copper palette and project-card styling

Project pages use `topic`, `status`, and `importance` in their YAML front matter. Keep ongoing work labelled accurately and add real figures with descriptive captions when ready. No illustrative plot should be presented as a research result.

## Local preview

Requires Ruby 3.3 or later and Bundler:

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. Node is needed only for formatting: `npm ci`, then `npm run lint:prettier`.

## Review and publishing

The redesign branch is for review. The workflow builds pull requests without deploying. Publication happens only after merging to `master`, through GitHub Pages' official Actions workflow. In repository Settings → Pages, select GitHub Actions before deploying. The existing live website remains unchanged while the redesign is on its own branch.

Before publication: review all project descriptions and statuses, verify publication metadata, and add a portrait and a current CV PDF if desired. Publication metadata and full author lists were retrieved from Crossref; the training contribution is updated to its 2025 journal publication.

## Theme maintenance

`_sass/_themes.scss` intentionally overrides al-folio's theme tokens for this personal site. The original light/dark behaviour is retained; site-specific palette and research components are appended. `.al-folio-overrides.yml` tracks the override against the pinned gem version. Run `bundle exec al-folio upgrade overrides audit` after updating core dependencies.

The template is MIT licensed; see `LICENSE`.
