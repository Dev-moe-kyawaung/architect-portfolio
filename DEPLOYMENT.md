# Deployment Guide

This repo can be deployed to **GitHub Pages** and/or **GitLab Pages** with zero build step — the configs are already included.

---

## GitHub Pages

1. Create a new repo (e.g. `architect-portfolio`) under your GitHub account.
2. Push this project to it:
   ```bash
   git init
   git add .
   git commit -m "chore: initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/architect-portfolio.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **GitHub Actions**.
5. That's it — `.github/workflows/deploy.yml` runs automatically on every push to `main` and publishes the site.
6. Your site will be live at:
   ```
   https://<your-username>.github.io/architect-portfolio/
   ```
7. To use a custom domain, add a `CNAME` file at the repo root containing your domain, then configure DNS per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

---

## GitLab Pages

1. Create a new project on GitLab (e.g. `architect-portfolio`).
2. Push this project to it:
   ```bash
   git init
   git add .
   git commit -m "chore: initial commit"
   git branch -M main
   git remote add origin https://gitlab.com/<your-username>/architect-portfolio.git
   git push -u origin main
   ```
3. GitLab detects `.gitlab-ci.yml` automatically and runs the `pages` job on push.
4. Check **CI/CD → Pipelines** to confirm the `pages` job succeeds.
5. Your site will be live at:
   ```
   https://<your-username>.gitlab.io/architect-portfolio/
   ```
6. For a custom domain, go to **Settings → Pages** in your GitLab project and follow the verification steps.

---

## Running both simultaneously

Nothing conflicts — `.github/workflows/deploy.yml` only triggers on GitHub, and `.gitlab-ci.yml` only triggers on GitLab. You can mirror the same repo to both platforms and keep both Pages sites live in parallel (useful as a redundant/backup URL).

## Troubleshooting

| Symptom | Fix |
|---|---|
| GitHub Pages shows 404 | Confirm **Settings → Pages → Source** is set to "GitHub Actions", not "Deploy from a branch" |
| GitLab Pages job fails | Check **CI/CD → Pipelines** logs; ensure branch is `main` or `master` per `.gitlab-ci.yml` rules |
| Fonts not loading | Google Fonts requires outbound network access — shouldn't be blocked on either platform's Pages CDN |
| Changes not appearing | Hard refresh (Pages CDN can cache briefly); confirm the Actions/Pipeline run completed |
