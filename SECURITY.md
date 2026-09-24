# Security Policy

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues, discussions, or pull requests.**

Report them privately through either of these channels:

1. **GitHub private advisory** (preferred) — use the [Security tab](https://github.com/ggbond-github/comp-hub-community/security/advisories/new) to submit a draft advisory. This keeps the report, the discussion, and the fix all in one place.
2. **Email** — `1406059122@qq.com` <!-- TODO: swap for a dedicated security address if you'd rather not use a personal one -->

Please include:

- A description of the vulnerability and its impact
- Steps to reproduce, or a proof of concept
- Affected version(s)
- Any known mitigations or workarounds
- How you'd like to be credited, if at all

## What to expect

| Stage                              | Target                                      |
| ---------------------------------- | ------------------------------------------- |
| Acknowledgement of your report     | Within 3 working days                       |
| Initial assessment and severity    | Within 7 working days                       |
| Fix or mitigation for critical issues | As soon as is practical                  |
| Public disclosure                  | Coordinated with you, after a fix ships     |

We'll keep you updated as the report progresses. If we determine an issue isn't a vulnerability, we'll explain our reasoning rather than just closing it.

We do not operate a paid bounty programme.

## Please give us a chance to fix it first

We ask for a reasonable window to investigate and ship a fix before any public disclosure. We'll work with you on the timing — if you have a deadline or an external obligation, tell us and we'll prioritise accordingly.

## Scope

comp-hub ships as a set of components, and the scope of a report depends on which one is affected:

| Component                                    | In scope                         |
| -------------------------------------------- | -------------------------------- |
| CLI (`npx comp-hub`)                         | Yes                              |
| Local server                                 | Yes                              |
| Cloud platform                               | Yes                              |
| Web app                                      | Yes                              |
| Component preview                            | Yes                              |
| This repository's contents (docs, templates) | Yes, but low severity by nature  |

Out of scope:

- Vulnerabilities in third-party dependencies that are already publicly disclosed and have an available upstream fix. Report those upstream, though do tell us if comp-hub pins an affected version.
- Findings that require an already-compromised host, physical access, or a malicious browser extension.
- Missing security headers or similar hardening suggestions with no demonstrated impact.
- Automated scanner output with no working proof of concept.

## Supported versions

| Version | Supported |
| ------- | --------- |
| `0.46.x` | ✅       |

<!-- TODO: keep this table current as you ship new major versions. -->
