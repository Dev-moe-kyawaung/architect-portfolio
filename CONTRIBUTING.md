# Contributing

Thanks for considering a contribution to this portfolio project.

## Ground rules

- This is a **single-file, no-build** static site (`index.html`). Keep it that way unless a change specifically requires otherwise — discuss build-tooling additions in an issue first.
- Preserve the bilingual pattern: every user-facing string needs both an `data-lang="en"` element and a matching `.my[data-lang="my"]` element.
- Keep new sections consistent with the existing design tokens (see `:root` CSS variables) rather than introducing new colors/fonts ad hoc.

## Workflow

1. Fork the repo and create a branch: `git checkout -b feature/short-description`
2. Make your changes directly in `index.html` (or add a new static asset).
3. Test locally by opening `index.html` in a browser, or run:
   ```bash
   python3 -m http.server 8080
   ```
4. Check both language modes (EN/MY toggle) and at least one mobile viewport width before submitting.
5. Commit with a clear message (e.g. `feat: add case-study subpage`, `fix: radar chart mobile overflow`).
6. Open a pull request using the provided template, describing what changed and why.

## Reporting issues

Use the [bug report](.github/ISSUE_TEMPLATE/bug_report.md) or [feature request](.github/ISSUE_TEMPLATE/feature_request.md) templates. Include browser/OS and a screenshot or screen recording where relevant — most issues here are visual.

## Code style

- Vanilla JS, no semicolon-omission style changes to existing code.
- CSS: keep new component styles scoped under a clearly named class rather than adding global selectors.
- Avoid adding external dependencies; this project intentionally has none.

## Security

Do not open a public issue for security concerns — see [SECURITY.md](SECURITY.md).
