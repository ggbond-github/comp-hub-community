<div align="center">

# comp-hub

**The component hub for teams — Vue and React.**

Share, preview, and manage components across your team, without asking anyone to set up a local environment.

[![GitHub stars](https://img.shields.io/github/stars/ggbond-github/comp-hub-community?style=social)](https://github.com/ggbond-github/comp-hub-community/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/ggbond-github/comp-hub-community)](https://github.com/ggbond-github/comp-hub-community/issues)
[![License](https://img.shields.io/github/license/ggbond-github/comp-hub-community)](LICENSE)

[English](README.md) · [简体中文](README.zh-CN.md)

🌐 **[Website](https://www.comphub.cn)** · 📖 **[Documentation](https://docs.comphub.cn/)** · 🚀 **[Live platform](https://intranet.comphub.cn/main/)**

</div>

---

> ### 📌 This repository is an issue tracker — not a source repository.
>
> The comp-hub source code is **not** public. This repository exists to collect bug reports, feature requests, and general feedback, and to act as the public front door for the project.
>
> There is nothing to clone or build here. If you are looking for the project itself, start with [What is comp-hub](#what-is-comp-hub) below.

---

## What is comp-hub

**comp-hub** is a team-level platform for sharing and managing front-end components.

Most teams end up with the same problem: a growing pile of components scattered across repositories, half of them duplicated, none of them easy to find, and no way to see what one looks like without pulling a branch and running it locally. comp-hub fixes that.

It gives your team a central place to publish components, browse them, preview them live in the browser, and drop them into any project — across **Vue 2, Vue 3, React 17, and React 18**.

## See it for yourself

You don't need to install anything to look around:

**🌐 <https://www.comphub.cn>** — browse, search, preview, and download components without signing in.

The full platform — teams, publishing, favorites, and management — lives at **[intranet.comphub.cn/main/](https://intranet.comphub.cn/main/)**.

<!-- TODO: real screenshots convert far better than a link. Drop them in ./docs/images/ and put a small table here. -->

## Links

|                                |                                                              |
| ------------------------------ | ------------------------------------------------------------ |
| 🌐 **Website**                 | <https://www.comphub.cn>                                      |
| 📖 **Documentation**           | <https://docs.comphub.cn/> (also available in 简体中文, 繁體中文, Français, Nederlands) |
| 🚀 **Full platform**           | <https://intranet.comphub.cn/main/>                           |
| 🐛 **Issue tracker**           | <https://github.com/ggbond-github/comp-hub-community/issues>     |
| 💬 **Discussions**             | <https://github.com/ggbond-github/comp-hub-community/discussions> |

## Why teams use it

- **Stop re-writing the same component.** Publish once, and everyone finds it in the shared library.
- **Preview before you install.** Components render live in the browser — each preview isolated, so one broken component can't take down the page. No local setup, no branch switching.
- **Vue and React side by side.** Vue 2, Vue 3, React 17, and React 18 components all live in the same hub. Migrating gradually? Nothing has to move at once.
- **Keep the team's work inside the team.** Team spaces and permissions keep each group's components separate and controlled.

## Supported frameworks

The framework is detected automatically from the component's own imports — there is nothing to declare. Import `vue` and it's treated as Vue; import `react` and it's treated as React.

| Framework    | Entry file                            | Notes                                                                    |
| ------------ | ------------------------------------- | ------------------------------------------------------------------------ |
| **Vue 3**    | `index.vue`                           | Add a `main.js` when a third-party UI library is needed (`Vue.app.use()`) |
| **Vue 2**    | `index.vue`                           | Add a `main.js` when a third-party UI library is needed (`Vue.use()`)     |
| **React 18** | `index.jsx` / `index.js` / `index.tsx` | No `main.js` needed — just import. A default export is required.          |
| **React 17** | `index.jsx` / `index.js` / `index.tsx` | No `main.js` needed — just import. A default export is required.          |

Styles work as you'd expect: SCSS and Less for Vue (scoped recommended), and relative CSS/SCSS/Less imports for React.

## Features

| Area                 | What you get                                                                                                                     |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **No-install start** | `npx comp-hub` — one command wires your existing project into the hub. Configurable port, directory, and log level.              |
| **Local server**     | Component management with version history, module-based organization, a built-in file browser, a web terminal, and dependency pre-compilation. |
| **Cloud platform**   | Accounts and sign-in (including GitHub OAuth), multi-team collaboration with permissions, the component library with search and keywords, comments and discussion, and version diffing. |
| **Web app**          | Library, My Components, Favorites, Local Components, Upload, online preview (with side-by-side comparison of similar components), web terminal, settings, and team spaces. |
| **Authoring help**   | Four-level dependency matching, similar-component detection so near-duplicates rank lower, a scale API for fitting fixed-size designs into the preview panel, and one-click open in VS Code. |

### Upload limits

A component can contain up to **30 files**, **3 MB per file**, and **10 MB in total**.

## Getting started

Pick whichever fits:

```bash
# Try it without installing anything, from your existing project
npx comp-hub
```

Or browse the hosted library first — no account required — at <https://www.comphub.cn>.

<!-- TODO: if the CLI needs flags or a follow-up step for a first run, document them here. -->

## Documentation

Full documentation lives at **<https://docs.comphub.cn/>**, available in English, 简体中文, 繁體中文, Français, and Nederlands.

Chinese readers: <https://docs.comphub.cn/zh/>

## Status

comp-hub is under active development. The current release is **0.46.x**.

<!-- TODO: replace the above with a short, honest roadmap. A "what's next" list gives visitors a reason to watch the repo. -->

## Reporting bugs and requesting features

Use the [issue tracker](https://github.com/ggbond-github/comp-hub-community/issues) — it is the whole point of this repository.

- 🐛 **[Report a bug](https://github.com/ggbond-github/comp-hub-community/issues/new?template=bug_report.yml)**
- ✨ **[Request a feature](https://github.com/ggbond-github/comp-hub-community/issues/new?template=feature_request.yml)**
- 💬 **Have a question instead?** Use [Discussions](https://github.com/ggbond-github/comp-hub-community/discussions) — it is not an issue.

Before filing, please [search existing issues](https://github.com/ggbond-github/comp-hub-community/issues?q=is%3Aissue) first. Good reports include versions, reproduction steps, and what you expected to happen — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contributing

This repository accepts contributions to its **documentation and issue templates** only — there is no product source code here. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Security

Please do **not** report security vulnerabilities through public issues. See [SECURITY.md](SECURITY.md) for the private reporting process.

## License

The contents of **this repository** (documentation, issue templates, and configuration) are released under the [MIT License](LICENSE).

That license covers **only this repository**. It does not apply to the comp-hub software itself, which is proprietary and is not distributed here.
