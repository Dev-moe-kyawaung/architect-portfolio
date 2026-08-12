<div align="center">

# Moe Kyaw Aung — Senior Android Architect Portfolio

**Dark-glass · 3D floating UI · Bilingual (Burmese/English) · Cinematic scroll**

[![Deploy GitHub Pages](https://github.com/Dev-moe-kyawaung/architect-portfolio/actions/workflows/deploy.yml/badge.svg)](https://github.com/Dev-moe-kyawaung/architect-portfolio/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-00d9c0.svg)](LICENSE)
[![Made with](https://img.shields.io/badge/stack-HTML%20%7C%20CSS%20%7C%20JS-7b6ef6)](#tech-stack)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-ffb627.svg)](CONTRIBUTING.md)

[Live Demo](#) · [Report Bug](.github/ISSUE_TEMPLATE/bug_report.md) · [Request Feature](.github/ISSUE_TEMPLATE/feature_request.md)

</div>

---

## Overview

A single-page, self-contained portfolio for a Senior Mobile/Android App Architect. Built with plain HTML/CSS/JS (no build step), it renders a dark-glass aesthetic with 3D floating hero cards, an animated skills radar, a Clean Architecture diagram, performance benchmark charts, an animated CI/CD pipeline visual, and a live English ⇄ Burmese (မြန်မာ) language toggle.

## Sections

| # | Section | Description |
|---|---------|-------------|
| 1 | Hero | 3D floating tech cards, gradient headline, key stats |
| 2 | Skills Matrix | Canvas-drawn animated radar chart + skill bars |
| 3 | Android Roadmap | 12-year vertical timeline across four eras |
| 4 | Compose UI Gallery | Reusable Jetpack Compose component cards |
| 5 | Architecture Lab | Clean Architecture layer diagram |
| 6 | Performance Benchmarks | Mini sparkline charts per metric |
| 7 | CI/CD Pipelines | Animated commit → Play Store pipeline |
| 8 | Project Showcase | Flagship projects (MoekyawTranslator, Portfolio V8, etc.) |
| 9 | GitHub Network | Multi-account / persona stats |
| 10 | Certifications | 80+ credentials across 9 domains |
| 11 | Testimonials | Collaborator quotes |
| 12 | Contact | Links + closing CTA |

## Tech Stack

- **HTML5 / CSS3** — glassmorphism (`backdrop-filter`), CSS 3D transforms, custom properties
- **Vanilla JavaScript** — Canvas 2D (particles, radar chart, sparkline charts), IntersectionObserver scroll reveals
- **Fonts** — Space Grotesk, Inter, JetBrains Mono, Noto Sans Myanmar
- No frameworks, no build tools, no dependencies — deploys as static files.

## Getting Started

```bash
git clone https://github.com/Dev-moe-kyawaung/architect-portfolio.git
cd architect-portfolio
# just open it — no build step required
open index.html        # macOS
xdg-open index.html    # Linux
start index.html        # Windows
```

Or serve locally:

```bash
python3 -m http.server 8080
# visit http://localhost:8080
```

## Deployment

This repo ships ready-to-deploy configs for both platforms:

### GitHub Pages (automatic)
Push to `main` and [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) publishes automatically via GitHub Actions. Enable **Settings → Pages → Source: GitHub Actions** once, and every push redeploys.

### GitLab Pages (automatic)
Push to `main`/`master` and [`.gitlab-ci.yml`](.gitlab-ci.yml) publishes via the built-in `pages` job. No extra setup needed — GitLab CI/CD picks it up automatically.

See [DEPLOYMENT.md](DEPLOYMENT.md) for step-by-step instructions for both.

## Customizing

- **Content data** lives in plain JS arrays near the bottom of `index.html` (`skills`, `roadmap`, `galleryItems`, `benchData`, `projects`, `netStats`, `certDomains`, `testimonials`) — edit the arrays, the UI regenerates itself.
- **Colors / type** are CSS custom properties at the top of the `<style>` block (`:root`).
- **Language strings** use `data-lang="en"` / `data-lang="my"` pairs — add a new pair anywhere to extend bilingual coverage.

## Contributing

Contributions, issue reports, and design suggestions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Security

To report a vulnerability, see [SECURITY.md](SECURITY.md).

## License

Released under the [MIT License](LICENSE).

## Author

**Moe Kyaw Aung (မိုးကျော်အောင်)** — Senior Android Developer
Tachileik, Myanmar · Bangkok, Thailand
[GitHub](https://github.com/Dev-moe-kyawaung) · Open to freelance, consulting, and mentoring engagements.

<div align="center">Crafted in dark glass, rooted in Bagan. 🇲🇲</div>
