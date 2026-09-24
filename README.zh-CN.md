<div align="center">

# comp-hub

**面向团队的组件中心 —— 同时支持 Vue 与 React。**

在团队内共享、预览和管理组件,不需要任何人先搭好本地环境。

[![GitHub stars](https://img.shields.io/github/stars/ggbond-github/comp-hub-community?style=social)](https://github.com/ggbond-github/comp-hub-community/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/ggbond-github/comp-hub-community)](https://github.com/ggbond-github/comp-hub-community/issues)
[![License](https://img.shields.io/github/license/ggbond-github/comp-hub-community)](LICENSE)

[English](README.md) · [简体中文](README.zh-CN.md)

🌐 **[官网](https://www.comphub.cn)** · 📖 **[文档](https://docs.comphub.cn/zh/)** · 🚀 **[完整平台](https://intranet.comphub.cn/main/)**

</div>

---

> ### 📌 本仓库是问题反馈中心,不是源码仓库。
>
> comp-hub 的源代码**不公开**。本仓库存在的意义是收集 bug 反馈、功能建议和一般性意见,并作为项目的对外入口。
>
> 这里没有可以 clone 或构建的东西。想了解项目本身,请从下面的「comp-hub 是什么」读起。

---

## comp-hub 是什么

**comp-hub** 是一个团队级的前端组件共享与管理平台。

大多数团队最后都会撞上同一个问题:散落在各个仓库里的组件越堆越多,一半是重复的,没人找得到,想看某个组件长什么样还得切分支、起本地服务。comp-hub 就是来解决这件事的。

它给团队一个集中的地方来发布组件、浏览组件、在浏览器里直接实时预览,然后接入任何项目 —— 同时覆盖 **Vue 2、Vue 3、React 17、React 18**。

## 先看看效果

不用装任何东西就能逛:

**🌐 <https://www.comphub.cn>** —— 免登录浏览、搜索、预览、下载组件。

包含团队空间、组件发布、收藏与管理的完整平台在 **[intranet.comphub.cn/main/](https://intranet.comphub.cn/main/)**。

<!-- TODO: 真实截图的转化率远高于一个链接。把图放进 ./docs/images/ 后在这里加一张小表格。 -->

## 相关链接

|                        |                                                              |
| ---------------------- | ------------------------------------------------------------ |
| 🌐 **官网**            | <https://www.comphub.cn>                                      |
| 📖 **文档**            | <https://docs.comphub.cn/zh/>(另有 English / 繁體中文 / Français / Nederlands) |
| 🚀 **完整平台**        | <https://intranet.comphub.cn/main/>                           |
| 📋 **版本日志**        | <https://intranet.comphub.cn/main/#/upgrade>                  |
| 🐛 **问题追踪**        | <https://github.com/ggbond-github/comp-hub-community/issues>     |
| 💬 **讨论区**          | <https://github.com/ggbond-github/comp-hub-community/discussions> |

## 团队为什么用它

- **不再重复造轮子。** 发布一次,全团队都能在共享组件库里找到。
- **装之前先看效果。** 组件在浏览器里直接实时渲染 —— 每个预览互相隔离,一个坏组件拖不垮整个页面。不用配环境,不用切分支。
- **Vue 和 React 并存。** Vue 2、Vue 3、React 17、React 18 的组件都在同一个中心里。正在渐进式迁移?不需要一次性搬完。
- **团队的成果留在团队内。** 团队空间加权限控制,各组组件互不干扰。

## 框架支持

框架由组件自己的引入**自动判定**,无需任何声明。引入 `vue` 即按 Vue 处理,引入 `react` 即按 React 处理。

| 框架         | 入口文件                              | 说明                                                                    |
| ------------ | ------------------------------------- | ----------------------------------------------------------------------- |
| **Vue 3**    | `index.vue`                           | 需要第三方 UI 库时新增 `main.js`(`Vue.app.use()`)                        |
| **Vue 2**    | `index.vue`                           | 需要第三方 UI 库时新增 `main.js`(`Vue.use()`)                            |
| **React 18** | `index.jsx` / `index.js` / `index.tsx` | 无需 `main.js`,直接 import 即可;必须有 default export                    |
| **React 17** | `index.jsx` / `index.js` / `index.tsx` | 无需 `main.js`,直接 import 即可;必须有 default export                    |

样式按各自习惯写即可:Vue 支持 SCSS / Less(建议始终加 scoped),React 直接 import 相对路径的 css / scss / less。

## 功能

| 模块             | 能力                                                                                                                            |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **免安装启动**   | `npx comp-hub` —— 一条命令把现有项目接入组件中心。端口、目录、日志等级均可配置。                                                 |
| **本地服务端**   | 组件管理与版本记录、按模块组织、内置文件浏览器、Web 终端,以及依赖预编译。                                                        |
| **云端平台**     | 账号体系与登录(支持 GitHub OAuth)、多团队协作与权限、带搜索和关键词的组件库、评论讨论,以及版本 Diff。                            |
| **Web 主应用**   | 组件库、我的组件、收藏、本地组件、上传、在线预览(支持相似组件并排对比)、Web 终端、设置,以及团队空间。                            |
| **开发辅助**     | 四级依赖匹配、相似组件检测降权(近似重复的组件排序靠后)、让固定尺寸设计自适应预览面板的缩放 API,以及一键用 VS Code 打开组件。      |

### 上传限制

单个组件最多 **30 个文件**、**单文件 3MB**、**总计 10MB**。

## 快速开始

随你选:

```bash
# 不装任何东西,在现有项目里直接试
npx comp-hub
```

或者先去线上组件库逛逛 —— 无需注册:<https://www.comphub.cn>。

<!-- TODO: 如果 CLI 首次运行还需要别的参数或后续步骤,在这里补上。 -->

## 文档

完整文档在 **<https://docs.comphub.cn/zh/>**,提供 English、简体中文、繁體中文、Français、Nederlands 五种语言。

## 项目状态

comp-hub 仍在活跃开发中,当前版本为 **0.46.x** —— 各版本的具体变更见[版本日志](https://intranet.comphub.cn/main/#/upgrade)。

<!-- TODO: 把上面这段换成一份简短的、真实的路线图。「接下来做什么」能让访客有理由 watch 这个仓库。 -->

## 反馈 Bug 与提需求

请使用[问题追踪](https://github.com/ggbond-github/comp-hub-community/issues) —— 这正是本仓库存在的意义。

- 🐛 **[反馈 Bug](https://github.com/ggbond-github/comp-hub-community/issues/new?template=bug_report.yml)**
- ✨ **[提功能需求](https://github.com/ggbond-github/comp-hub-community/issues/new?template=feature_request.yml)**
- 📋 **先看[版本日志](https://intranet.comphub.cn/main/#/upgrade)** —— 你要反馈的问题可能已在新版本中修复。
- 💬 **只是想提问?** 请用 [Discussions](https://github.com/ggbond-github/comp-hub-community/discussions) —— 提问不算 issue。

提交前请先[搜索已有 issue](https://github.com/ggbond-github/comp-hub-community/issues?q=is%3Aissue)。一份好的反馈应包含版本信息、复现步骤和期望结果 —— 详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 参与贡献

本仓库只接受**文档和 issue 模板**方面的贡献 —— 这里没有产品源码。详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 安全

请**不要**通过公开 issue 报告安全漏洞。私有上报流程见 [SECURITY.md](SECURITY.md)。

## 许可

**本仓库的内容**(文档、issue 模板和配置)基于 [MIT License](LICENSE) 发布。

该许可**仅覆盖本仓库**,不适用于 comp-hub 软件本身 —— 该软件为专有软件,不在此分发。
