<div align="center">

<!-- Animated Typing Banner -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=2E9EF7&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=100&lines=Css+Assistant;7+Agents+%7C+8+Skills;Claude+Code+Plugin" alt="Css Assistant" />

<br/>

<!-- Badge Row 1: Status Badges -->
[![Version](https://img.shields.io/badge/Version-2.0.0-blue?style=for-the-badge)](https://github.com/pluginagentmarketplace/custom-plugin-css/releases)
[![License](https://img.shields.io/badge/License-Custom-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production-brightgreen?style=for-the-badge)](#)
[![SASMP](https://img.shields.io/badge/SASMP-v1.3.0-blueviolet?style=for-the-badge)](#)

<!-- Badge Row 2: Content Badges -->
[![Agents](https://img.shields.io/badge/Agents-7-orange?style=flat-square&logo=robot)](#-agents)
[![Skills](https://img.shields.io/badge/Skills-8-purple?style=flat-square&logo=lightning)](#-skills)
[![Commands](https://img.shields.io/badge/Commands-4-green?style=flat-square&logo=terminal)](#-commands)

<br/>

<!-- Quick CTA Row -->
[📦 **Install Now**](#-quick-start) · [🤖 **Explore Agents**](#-agents) · [📖 **Documentation**](#-documentation) · [⭐ **Star this repo**](https://github.com/pluginagentmarketplace/custom-plugin-css)

---

### What is this?

> **Css Assistant** is a Claude Code plugin with **7 agents** and **8 skills** for css development.

</div>

---

## 📑 Table of Contents

<details>
<summary>Click to expand</summary>

- [Quick Start](#-quick-start)
- [Features](#-features)
- [Agents](#-agents)
- [Skills](#-skills)
- [Commands](#-commands)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [License](#-license)

</details>

---

## 🚀 Quick Start

### Prerequisites

- Claude Code CLI v2.0.27+
- Active Claude subscription

### Installation (Choose One)

<details open>
<summary><strong>Option 1: From Marketplace (Recommended)</strong></summary>

```bash
# Step 1️⃣ Add the marketplace
/plugin marketplace add pluginagentmarketplace/custom-plugin-css

# Step 2️⃣ Install the plugin
/plugin install css-development-assistant@pluginagentmarketplace-css

# Step 3️⃣ Restart Claude Code
# Close and reopen your terminal/IDE
```

</details>

<details>
<summary><strong>Option 2: Local Installation</strong></summary>

```bash
# Clone the repository
git clone https://github.com/pluginagentmarketplace/custom-plugin-css.git
cd custom-plugin-css

# Load locally
/plugin load .

# Restart Claude Code
```

</details>

### ✅ Verify Installation

After restart, you should see these agents:

```
css-development-assistant:01-css-fundamentals
css-development-assistant:02-css-layout-master
css-development-assistant:03-css-animations
css-development-assistant:04-css-architecture
css-development-assistant:05-css-preprocessors
... and 2 more
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🤖 **7 Agents** | Specialized AI agents for css tasks |
| 🛠️ **8 Skills** | Reusable capabilities with Golden Format |
| ⌨️ **4 Commands** | Quick slash commands |
| 🔄 **SASMP v1.3.0** | Full protocol compliance |

---

## 🤖 Agents

### 7 Specialized Agents

| # | Agent | Purpose |
|---|-------|---------|
| 1 | **01-css-fundamentals** | Master CSS basics including selectors, specificity, box model, typography |
| 2 | **02-css-layout-master** | Flexbox, CSS Grid, responsive design, layout patterns |
| 3 | **03-css-animations** | Keyframes, transitions, performance optimization |
| 4 | **04-css-architecture** | BEM, SMACSS, design systems, scalability |
| 5 | **05-css-preprocessors** | Sass, PostCSS, Tailwind, CSS Modules |
| 6 | **06-css-performance** | Critical CSS, code splitting, optimization |
| 7 | **07-css-modern-features** | Custom properties, :has(), @layer, container queries |

---

## 🛠️ Skills

### Available Skills

| Skill | Description | Invoke |
|-------|-------------|--------|
| `css-fundamentals` | Selectors, specificity, box model | `Skill("css-development-assistant:css-fundamentals")` |
| `css-flexbox-grid` | Flexbox & CSS Grid layouts | `Skill("css-development-assistant:css-flexbox-grid")` |
| `css-animations` | Keyframes, transitions, motion | `Skill("css-development-assistant:css-animations")` |
| `css-architecture` | BEM, SMACSS, design systems | `Skill("css-development-assistant:css-architecture")` |
| `css-sass` | Sass/SCSS preprocessing | `Skill("css-development-assistant:css-sass")` |
| `css-tailwind` | Utility-first CSS framework | `Skill("css-development-assistant:css-tailwind")` |
| `css-performance` | Critical CSS, optimization | `Skill("css-development-assistant:css-performance")` |
| `css-modern` | Custom properties, container queries | `Skill("css-development-assistant:css-modern")` |

---

## ⌨️ Commands

| Command | Description |
|---------|-------------|
| `/learn-css` | Learn CSS topics with structured paths |
| `/css-playground` | Interactive CSS examples & playground |
| `/css-inspector` | Analyze, debug & optimize CSS |
| `/css-projects` | 50+ hands-on projects |

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |
| [LICENSE](LICENSE) | License information |

---

## 📁 Project Structure

<details>
<summary>Click to expand</summary>

```
custom-plugin-css/
├── 📁 .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── 📁 agents/              # 7 agents
├── 📁 skills/              # 8 skills (Golden Format)
├── 📁 commands/            # 4 commands
├── 📁 hooks/
├── 📄 README.md
├── 📄 CHANGELOG.md
└── 📄 LICENSE
```

</details>

---

## 📅 Metadata

| Field | Value |
|-------|-------|
| **Version** | 2.0.0 |
| **Last Updated** | 2025-12-31 |
| **Status** | Production Ready |
| **SASMP** | v1.3.0 |
| **Agents** | 7 |
| **Skills** | 8 |
| **Commands** | 4 |

---

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

1. Fork the repository
2. Create your feature branch
3. Follow the Golden Format for new skills
4. Submit a pull request

---

## ⚠️ Security

> **Important:** This repository contains third-party code and dependencies.
>
> - ✅ Always review code before using in production
> - ✅ Check dependencies for known vulnerabilities
> - ✅ Follow security best practices
> - ✅ Report security issues privately via [Issues](../../issues)

---

## 📝 License

Copyright © 2025 **Dr. Umit Kacar** & **Muhsin Elcicek**

Custom License - See [LICENSE](LICENSE) for details.

---

## 👥 Contributors

<table>
<tr>
<td align="center">
<strong>Dr. Umit Kacar</strong><br/>
Senior AI Researcher & Engineer
</td>
<td align="center">
<strong>Muhsin Elcicek</strong><br/>
Senior Software Architect
</td>
</tr>
</table>

---

<div align="center">

**Made with ❤️ for the Claude Code Community**

[![GitHub](https://img.shields.io/badge/GitHub-pluginagentmarketplace-black?style=for-the-badge&logo=github)](https://github.com/pluginagentmarketplace)

</div>
