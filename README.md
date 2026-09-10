# Nitesh Kumar — Portfolio

Personal portfolio site of **Nitesh Kumar**, Python Backend Developer @ TCS (Kolkata).
Built with [Hugo](https://gohugo.io/) (extended) and a custom white / gold / black luxury theme.

**Live:** https://nitesh009-nc.github.io/portfolio/

## Features

- Sticky glass nav with mobile hamburger menu and scroll-spy
- Hero with availability badge, gradient headline, and gold-ring profile card
- About, Experience timeline, Projects, Skills, Certifications, Education, Languages
- Let's Connect band with LinkedIn / GitHub / HackerRank links
- Floating back-to-top button, scroll-reveal animations
- Downloadable resume (`static/resume.pdf`)

## Local development

Requires Hugo **extended** (v0.165.0).

```bash
# Windows
winget install Hugo.Hugo.Extended

# Serve with live reload
hugo server

# Production build
hugo --minify
```

## Deployment

Every push to `master` auto-deploys via GitHub Actions (`.github/workflows/deploy.yml`):
build with Hugo extended → upload `public/` → deploy to GitHub Pages.

One-time setup in the repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Structure

```
├── .github/workflows/deploy.yml  # Pages auto-deploy
├── archetypes/                   # New-content template
├── assets/
│   ├── css/main.css              # Theme styles
│   ├── images/profile.png        # Profile photo (processed by Hugo)
│   └── js/main.js                # Nav, reveal, back-to-top
├── content/
│   ├── _index.md
│   └── about.md                  # About page
├── layouts/
│   ├── _default/baseof.html      # Shell: nav, floating button, JS pipeline
│   ├── index.html                # Homepage sections
│   └── _default/{list,single}.html
├── static/resume.pdf             # Downloadable resume
└── hugo.toml                     # Site config (params, socials, baseURL)
```

## Customization

- Personal details, socials, and tagline live in `hugo.toml` under `[params]`.
- Edit homepage sections in `layouts/index.html`, styles in `assets/css/main.css`.
- Replace `static/resume.pdf` and `assets/images/profile.png` with your own files.
