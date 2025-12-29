# 🎨 Custom Plugin CSS

[![Version](https://img.shields.io/badge/Version-1.0.0-blue?style=flat-square)](https://github.com/pluginagentmarketplace/custom-plugin-css)
[![Status](https://img.shields.io/badge/Status-Development-brightgreen?style=flat-square)](https://github.com/pluginagentmarketplace/custom-plugin-css)
[![Agents](https://img.shields.io/badge/Agents-0-orange?style=flat-square)](#agents-overview)
[![Skills](https://img.shields.io/badge/Skills-5-purple?style=flat-square)](#skills-reference)
[![License](https://img.shields.io/badge/License-Custom-yellow?style=flat-square)](LICENSE)
[![SASMP](https://img.shields.io/badge/SASMP-v1.3.0-green.svg)](docs/SASMP.md)

[Quick Start](#quick-start) | [Agents](#agents-overview) | [Skills](#skills-reference) | [Commands](#commands)

The ultimate CSS mastery plugin for Claude Code. Master CSS from fundamentals to advanced techniques with **5 specialized agents**, **5 comprehensive skills**, **4 interactive commands**, and **50+ hands-on projects**.

---

---

## 🚀 Quick Start

### Option 1: Install from GitHub (Recommended)

```bash
# Step 1: Add the marketplace from GitHub
/plugin add marketplace pluginagentmarketplace/custom-plugin-css

# Step 2: Install the plugin
/plugin install css-assistant@pluginagentmarketplace-css

# Step 3: Restart Claude Code to load new plugins
```

### Option 2: Clone and Load Locally

```bash
# Clone the repository
git clone https://github.com/pluginagentmarketplace/custom-plugin-css.git

# Navigate to the directory in Claude Code
cd custom-plugin-css

# Load the plugin
/plugin load .
```

After loading, restart Claude Code.

### Verify Installation

After restarting Claude Code, verify the plugin is loaded by checking available agents:

```
css-assistant:agent-name
```
## ✨ Key Features

### 🎓 5 Specialized Agents

| Agent | Focus | Duration |
|-------|-------|----------|
| **#1: Fundamentals** | Selectors, box model, typography, colors, positioning | 20-40h |
| **#2: Layouts** | Flexbox, CSS Grid, responsive design | 30-50h |
| **#3: Frameworks** | Tailwind, Bootstrap, SASS, CSS architecture | 35-55h |
| **#4: CSS-in-JS** | styled-components, Emotion, CSS Modules | 40-60h |
| **#5: Advanced** | Animations, transforms, performance, accessibility | 50-80h |

### 📚 5 Comprehensive Skills

Each skill includes:
- 🎯 Quick start guide
- 💻 Real code examples
- 📖 Best practices
- 🔧 Tools & resources
- 🚀 Performance tips

**Skills:**
1. **css-fundamentals** - Selectors, box model, typography
2. **css-layouts** - Flexbox & CSS Grid
3. **css-frameworks** - Tailwind, Bootstrap, SASS
4. **css-in-js** - styled-components, Emotion
5. **css-advanced** - Animations, transforms, optimization

### 🛠️ 4 Interactive Commands

```bash
/learn-css [topic]       # Learn CSS topics with structured paths
/css-playground [cat]    # Interactive CSS examples & playground
/css-inspector [action]  # Analyze, debug & optimize CSS
/css-projects [level]    # 50+ hands-on projects
```

### 🎯 50+ Projects

- **10 Beginner** (20-40 hours each)
- **10 Intermediate** (40-80 hours each)
- **10 Advanced** (80-150 hours each)
- **20+ Specialized** (frameworks, animations, systems)

## 📊 Plugin Overview

```
Custom Plugin CSS/
├── .claude-plugin/
│   └── plugin.json ........................ Plugin manifest
├── agents/ .............................. 5 Agent files
│   ├── 01-css-fundamentals.md
│   ├── 02-css-layouts.md
│   ├── 03-css-frameworks.md
│   ├── 04-css-in-js.md
│   └── 05-css-advanced.md
├── commands/ ........................... 4 Commands
│   ├── learn-css.md
│   ├── css-playground.md
│   ├── css-inspector.md
│   └── css-projects.md
├── skills/ ............................. 5 Skills
│   ├── fundamentals/SKILL.md
│   ├── layouts/SKILL.md
│   ├── frameworks/SKILL.md
│   ├── css-in-js/SKILL.md
│   └── advanced/SKILL.md
├── hooks/
│   └── hooks.json ...................... Automation hooks
└── README.md
```

## 🎯 Learning Paths

### Path 1: Complete Beginner → Expert
1. `/learn-css fundamentals` (20-40h)
2. `/learn-css layouts` (30-50h)
3. `/learn-css responsive` (20-30h)
4. `/learn-css animations` (25-40h)
5. `/learn-css frameworks` (35-55h)
**Total: 130-215 hours**

### Path 2: Intermediate → Expert
1. `/learn-css layouts`
2. `/learn-css frameworks`
3. `/learn-css css-in-js`
4. `/learn-css performance`
**Total: 100-180 hours**

### Path 3: Advanced Focus
1. `/learn-css animations`
2. `/learn-css transforms`
3. `/learn-css performance`
4. `/learn-css design-systems`
**Total: 80-150 hours**

## 💡 Usage Examples

### Learn a Topic
```bash
/learn-css fundamentals
```
Get structured lessons with examples and best practices.

### Practice Interactively
```bash
/css-playground flexbox-intro beginner
```
Explore interactive examples with live code editor.

### Debug Your CSS
```bash
/css-inspector optimize
```
Get optimization suggestions and performance tips.

### Build Projects
```bash
/css-projects intermediate
```
Find engaging projects matching your skill level.

## 🎓 Topics Covered

### Fundamentals ✓
- Selectors & specificity
- Box model & margins
- Typography & colors
- Display & positioning
- Units & values

### Layouts ✓
- Flexbox (flex-direction, justify-content, align-items)
- CSS Grid (grid-template, areas, auto-fit)
- Responsive design & media queries
- Mobile-first approach
- Layout patterns & techniques

### Frameworks ✓
- **Tailwind CSS** - Utility-first approach
- **Bootstrap** - Component framework
- **SASS/SCSS** - CSS preprocessing
- **LESS** - Dynamic styles
- **PostCSS** - CSS transformations

### CSS-in-JS ✓
- **styled-components** - CSS-in-JS library
- **Emotion** - Lightweight CSS-in-JS
- **CSS Modules** - Local scoping
- **BEM Methodology** - Scalable architecture
- **Atomic CSS** - Utility patterns

### Advanced ✓
- Keyframe animations & transitions
- 2D & 3D transforms
- Performance optimization
- CSS accessibility (WCAG)
- Advanced selectors (:has, :is, :where)
- Container queries & cutting-edge CSS

## 📈 Progression Map

```
Beginner Projects (Simple Forms, Cards, Layouts)
            ↓
Master Fundamentals & Layouts
            ↓
Intermediate Projects (Components, Animations)
            ↓
Learn Frameworks & Advanced Techniques
            ↓
Advanced Projects (Design Systems, Optimization)
            ↓
Expert Portfolio (Production-Ready Code)
```

## 🌟 Plugin Highlights

✅ **5 Agents** - Specialized expertise
✅ **5 Skills** - Comprehensive guides with code
✅ **4 Commands** - Interactive learning tools
✅ **50+ Projects** - Real portfolio pieces
✅ **100+ Examples** - Practical code snippets
✅ **250+ Hours** - Complete learning content
✅ **Production Ready** - Professional quality
✅ **Free & Open** - Accessible to all

## 🎯 For Different Users

### 🔰 Complete Beginners
- Start: `/learn-css fundamentals`
- Follow: Beginner projects
- Time: 130-215 hours to expert

### 🚀 Experienced Developers
- Start: `/learn-css layouts`
- Jump to: Intermediate/advanced
- Time: 80-150 hours to mastery

### 🎨 Designers Learning Code
- Start: `/learn-css fundamentals`
- Focus: Responsive design & frameworks
- Time: 100-150 hours

### 💼 Interview Preparation
- Study: All 5 agents systematically
- Practice: CSS projects portfolio
- Time: 150-200 hours

## 📚 Resources Included

Each topic includes:
- **Core Concepts** - Explained clearly
- **Code Examples** - Practical snippets
- **Best Practices** - Industry standards
- **Common Mistakes** - What to avoid
- **Projects** - Hands-on practice
- **Performance Tips** - Optimization
- **Tools** - Recommended resources

## 🔧 Agent Tools

### CSS Inspector Features
- 📊 Performance analysis
- 🔍 Accessibility checking
- 🐛 Debugging assistance
- ⚡ Optimization suggestions
- 📈 Metrics & metrics

### CSS Playground Features
- 💻 Live code editor
- 👁️ Real-time preview
- 📚 Explanations
- 🔗 Variation examples
- 💾 Save & share

### Project Builder
- 📋 Project descriptions
- ✅ Feature checklist
- 🎯 Learning outcomes
- 🚀 Deployment guide
- 📝 Code review guide

## 🚀 Getting Started Now

1. **Install Plugin**
   ```bash
   claude add custom-plugin-css
   ```

2. **Choose Your Path**
   ```bash
   /learn-css fundamentals    # Beginner
   /learn-css layouts         # Intermediate
   /learn-css advanced        # Advanced
   ```

3. **Practice**
   ```bash
   /css-playground [category] [difficulty]
   /css-projects [difficulty]
   ```

4. **Optimize**
   ```bash
   /css-inspector optimize
   /css-inspector performance
   ```

## 📊 Statistics

- **5 Agents** - Specialized expertise
- **5 Skills** - Comprehensive guides
- **4 Commands** - Interactive tools
- **50+ Projects** - Real practice
- **100+ Code Examples** - Practical reference
- **250+ Hours** - Complete content
- **All Skill Levels** - Beginner to expert

## 🎓 Certifications & Goals

After completing this plugin, you'll be able to:

✓ Master CSS fundamentals
✓ Create responsive layouts
✓ Use modern frameworks
✓ Optimize CSS performance
✓ Ensure accessibility
✓ Build design systems
✓ Write production-ready CSS
✓ Mentor others in CSS

## 📄 License

MIT License - Free for personal and commercial use

## 🔗 Resources

- **GitHub:** https://github.com/pluginagentmarketplace/custom-plugin-css
- **Claude Docs:** https://docs.claude.com

## 💬 Support

Need help? Check:
- Agent guides (detailed expertise)
- Skill files (how-to guides)
- Command documentation (quick reference)
- Project descriptions (requirements)

---

**Master CSS. Build beautiful web experiences. Start now! 🎨**

**Version:** 1.0.0 | **Status:** Production Ready ✅ | **License:** MIT


---

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Quick Start

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


---

<div align="center">

**Style beautiful interfaces with AI!**

[![Made for Css](https://img.shields.io/badge/Made%20for-Css-1572B6?style=for-the-badge&logo=css3)](https://github.com/pluginagentmarketplace/custom-plugin-css)

**Built by Dr. Umit Kacar & Muhsin Elcicek**

</div>

---

## ⚠️ Security Notice

> **Important:** This repository contains third-party code and dependencies.
> - Always review code before using in production
> - Check dependencies for known vulnerabilities
> - Follow security best practices
> - Report security issues privately

---

## 📅 Metadata

| Field | Value |
|-------|-------|
| **Last Updated** | 2025-12-29 |
| **Maintenance Status** | Active |
| **SASMP Version** | 1.3.0 |
| **Support** | [Issues](../../issues) |
