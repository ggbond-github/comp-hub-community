# Contributing to comp-hub

Thanks for your interest in comp-hub.

## Read this first: there is no source code here

This repository is a **public issue tracker**, not the comp-hub codebase. The comp-hub source code is proprietary and is not published here — you will not find anything to clone, build, or run in this repository.

That shapes what "contributing" means here.

## What we welcome

| Contribution                        | How                                                                     |
| ----------------------------------- | ----------------------------------------------------------------------- |
| 🐛 **Bug reports**                  | [Open an issue](https://github.com/ggbond-github/comp-hub-community/issues/new?template=bug_report.yml) |
| ✨ **Feature requests**             | [Open an issue](https://github.com/ggbond-github/comp-hub-community/issues/new?template=feature_request.yml) |
| 💬 **Questions, ideas, showcases**  | [Start a discussion](https://github.com/ggbond-github/comp-hub-community/discussions) |
| 📝 **Fixes to this repo's docs**    | Pull request — README, CONTRIBUTING, SECURITY, issue templates          |
| 🔒 **Security reports**             | Privately, per [SECURITY.md](SECURITY.md) — never a public issue        |

## What we can't accept

- **Pull requests against the product source.** There is no product source in this repository, so there is nothing to patch. A PR containing a "fix" for the software itself cannot be merged, however good it is.
- **Issues that are actually questions.** Those belong in Discussions. An issue is for something concretely broken or concretely missing.

## Writing a good bug report

The single highest-leverage thing you can do is make the bug **reproducible**. A short, precise report beats a long, vague one every time.

Please include:

1. **Where** — which part of comp-hub (CLI, local server, remote server, web app, preview).
2. **Versions** — comp-hub, Node.js, pnpm, browser, OS. Check the [changelog](https://intranet.comphub.cn/main/#/upgrade) first to confirm you're on the current release.
3. **Framework** — Vue 2 or Vue 3 host project.
4. **Steps to reproduce** — numbered, starting from a clean state.
5. **Actual behaviour** — including the full error message, not a paraphrase of it.
6. **Expected behaviour** — what should have happened instead.

Logs, screenshots, and screen recordings are all welcome and usually speed things up considerably.

### Before you paste anything

Please strip confidential information from logs, screenshots, and code samples:

- Company names, internal URLs, hostnames, and IP addresses
- Credentials, tokens, API keys, connection strings
- Customer data or anything personally identifying
- Proprietary component source you don't have permission to share

If a bug genuinely can't be described without internal context, say so in the issue and we'll find another route — do not paste it publicly.

## What to expect from us

- **Triage.** We aim to label new issues within a few working days.
- **Honesty over speed.** If something isn't going to be fixed, or isn't a priority, we'll say so and close the issue with an explanation rather than leaving it open indefinitely.
- **No fixed timelines.** comp-hub is developed by a small team. We can't promise dates, and we'd rather not pretend otherwise.

Issues that go quiet for a long time and can't be reproduced may be closed. That isn't a judgement on the report — you're welcome to reopen with more detail.

## Pull requests against this repository

Small and focused, please. One concern per PR.

Because this repository holds no code, PRs here are limited to documentation, issue templates, and configuration. For those:

- Keep the change narrow and explain the motivation in the description.
- Match the existing tone and formatting.
- Note that `README.md` and `README.zh-CN.md` are translations of each other — if you change one, change both.

## Code of conduct

Be decent to each other. Assume good faith, criticise the work and not the person, and remember that most people here are volunteering their time to make the product better.
