# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| 1.x     | ✅ |
| < 1.0   | ❌ |

## Reporting a Vulnerability

This is a static, client-side-only portfolio site (no backend, no database, no user data collection, no authentication), so its attack surface is intentionally small. That said, if you find something — e.g. a dependency-free XSS vector, an unsafe `innerHTML` injection point, or a misconfigured deploy workflow with excessive permissions:

1. **Do not** open a public GitHub/GitLab issue.
2. Email the maintainer directly (see contact links in [README.md](README.md)) with:
   - A description of the issue and its potential impact
   - Steps to reproduce
   - Any suggested fix, if you have one
3. Expect an initial response within **5 business days**.

## Scope

In scope:
- The static site itself (`index.html`, assets)
- The GitHub Actions / GitLab CI deploy configurations

Out of scope:
- Third-party font/CDN providers (Google Fonts) — report to the respective vendor
- Issues requiring physical access to the maintainer's infrastructure

## Disclosure

We prefer coordinated disclosure. Once a fix is deployed, credit is given to the reporter (unless anonymity is requested) in the [CHANGELOG.md](CHANGELOG.md).
