# Research Notes

A personal research blog built with Hugo and PaperMod, with automatic deployment to GitHub Pages through GitHub Actions.

## Included

- A PaperMod Profile homepage
- A split black-and-white research cover
- About, publications, projects, posts, archives, and search pages
- Tables of contents, reading time, code-copy controls, breadcrumbs, and RSS
- A post archetype designed for research and experiment notes
- Automatic GitHub Pages builds and deployments

## Local preview

A portable Hugo binary is available in the current workspace:

```powershell
.\work\tools\hugo-0.164.0\hugo.exe server -D
```

Open `http://localhost:1313/` in a browser.

On another computer, install Hugo 0.146.0 or later and run:

```powershell
hugo server -D
```

## Create a new post

```powershell
hugo new content posts/my-new-note/index.md
```

Edit the generated Markdown file and change `draft: true` to `draft: false` when it is ready to publish.

## Personalization

The main profile settings are in `hugo.yaml`:

- `title`: site title
- `params.author`: author name
- `params.profileMode`: homepage title, subtitle, and buttons
- `params.socialIcons`: GitHub, Scholar, ORCID, and other links
- `menu.main`: top navigation

The central `R` mark is generated in `assets/css/extended/custom.css`. It can later be replaced with a taijitu symbol.

## Publishing

The repository is published at `aspirationer/aspirationer.github.io`. Every push to the `main` branch automatically rebuilds and deploys the site through GitHub Actions.
