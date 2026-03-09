# Security Policy

## Supported Versions

We provide security fixes for the latest release on the `main` branch of each repository.

| Repository | Supported |
|------------|-----------|
| iu-alumni-backend | ✅ latest `main` |
| iu-alumni-frontend | ✅ latest `main` |
| iu-alumni-mobile | ✅ latest `main` |
| iu-alumni-infra | ✅ latest `main` |
| iu-alumni-bot | ✅ latest `main` |

---

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security vulnerabilities.**

Report security issues privately via one of these channels:

1. **GitHub Private Advisory** — use the [Security tab](https://github.com/iu-alumni/iu-alumni-backend/security/advisories/new) of the affected repository → *Report a vulnerability*
2. **Telegram (direct message)** — contact a maintainer via [t.me/+8hrAOuObPXQzZGRi](https://t.me/+8hrAOuObPXQzZGRi)

### What to include

- A clear description of the vulnerability
- Steps to reproduce or a proof-of-concept
- Potential impact and affected versions
- Any suggested mitigations (optional)

---

## Response Timeline

| Step | Target |
|------|--------|
| Acknowledgement | Within 3 business days |
| Initial triage | Within 7 business days |
| Fix or mitigation | Depends on severity |
| Public disclosure | After fix is released |

We follow responsible disclosure — we will coordinate with you on the disclosure timeline.

---

## Scope

The following are **in scope**:

- Authentication and authorization bypasses
- Data exposure or injection vulnerabilities (SQLi, XSS, SSRF, etc.)
- Insecure direct object references
- Infrastructure misconfiguration leading to data exposure

The following are **out of scope**:

- Denial-of-service attacks
- Social engineering
- Issues in third-party dependencies (report upstream)
- Theoretical vulnerabilities without proof of exploitability
