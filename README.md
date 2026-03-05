# Braintree BC Widgets

Documentation for Braintree BigCommerce Widgets, published via [GitHub Pages](https://braintree-by-vox.github.io/Braintree-BC-Widgets/).

## Site Structure

| Path | Description |
|------|-------------|
| `index.md` | Home page |
| `docs/getting-started.md` | Installation and initial setup guide |
| `docs/configuration.md` | Widget configuration reference |
| `docs/widgets.md` | Detailed widget API documentation |
| `_config.yml` | Jekyll site configuration |
| `.github/workflows/deploy-pages.yml` | GitHub Pages deployment workflow |

## Publishing

The documentation site is built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

### Automatic Publishing

The site is automatically built and deployed whenever changes are merged into the `main` branch.

### Manual Publishing (Agent)

The deployment workflow supports manual triggering via the GitHub Actions `workflow_dispatch` event. This allows an automated agent or administrator to publish the site on demand without a code change:

- **Via GitHub UI:** Go to **Actions → Deploy GitHub Pages → Run workflow**
- **Via GitHub API / agent:**

```bash
curl -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <YOUR_TOKEN>" \
  https://api.github.com/repos/Braintree-by-Vox/Braintree-BC-Widgets/actions/workflows/deploy-pages.yml/dispatches \
  -d '{"ref":"main","inputs":{"reason":"Scheduled agent publish"}}'
```

## Local Development

```bash
gem install bundler jekyll
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000/Braintree-BC-Widgets/`.
