---
name: learn-css
description: CSS Learning Path Command
allowed-tools: Read
version: "2.0.0"
updated: "2025-12-30"
---

# /learn-css - CSS Learning Path

Structured CSS learning paths from beginner to expert.

## Synopsis

```
/learn-css <topic> [options]
```

## Input Validation

```yaml
parameters:
  topic:
    required: true
    type: string
    enum: [fundamentals, colors, positioning, layouts, responsive, accessibility, animations, transforms, frameworks, css-in-js, performance, design-systems, cutting-edge]
    error: "Topic must be a valid CSS learning topic"

  depth:
    required: false
    type: string
    default: standard
    enum: [quick, standard, deep]
    description: "Level of detail"
```

## Exit Codes

| Code | Meaning |
|------|---------|
| 0 | Topic loaded successfully |
| 1 | Invalid topic |
| 2 | Prerequisites not met |

## Topics Reference

### Beginner Topics

| Topic | Description | Prerequisites | Est. Time |
|-------|-------------|---------------|-----------|
| `fundamentals` | Selectors, box model, typography | HTML | 20-40h |
| `colors` | Color theory, CSS colors, palettes | None | 8-12h |
| `positioning` | Position properties, z-index | fundamentals | 12-20h |

### Intermediate Topics

| Topic | Description | Prerequisites | Est. Time |
|-------|-------------|---------------|-----------|
| `layouts` | Flexbox & CSS Grid mastery | fundamentals | 30-50h |
| `responsive` | Mobile-first, media queries | layouts | 20-30h |
| `accessibility` | WCAG, contrast, focus | fundamentals | 16-24h |

### Advanced Topics

| Topic | Description | Prerequisites | Est. Time |
|-------|-------------|---------------|-----------|
| `animations` | Keyframes, timing, performance | fundamentals | 25-40h |
| `transforms` | 2D/3D transforms, perspective | fundamentals | 16-24h |
| `frameworks` | Tailwind, Bootstrap, Sass | layouts | 35-55h |
| `css-in-js` | styled-components, Emotion | frameworks | 24-40h |

### Expert Topics

| Topic | Description | Prerequisites | Est. Time |
|-------|-------------|---------------|-----------|
| `performance` | Critical CSS, optimization | All basics | 20-30h |
| `design-systems` | Tokens, architecture, theming | frameworks | 40-60h |
| `cutting-edge` | Container queries, @layer, :has() | layouts | 16-24h |

## Usage Examples

```bash
# Start with fundamentals
/learn-css fundamentals

# Quick overview of layouts
/learn-css layouts quick

# Deep dive into animations
/learn-css animations deep

# Learn modern CSS features
/learn-css cutting-edge
```

## Learning Paths

### Path 1: Complete Beginner → Expert

```
fundamentals (20-40h)
    ↓
colors (8-12h)
    ↓
positioning (12-20h)
    ↓
layouts (30-50h)
    ↓
responsive (20-30h)
    ↓
animations (25-40h)
    ↓
frameworks (35-55h)
    ↓
performance (20-30h)

Total: 170-277 hours
```

### Path 2: Developer Fast Track

```
layouts (30-50h)
    ↓
responsive (20-30h)
    ↓
frameworks (35-55h)
    ↓
performance (20-30h)

Total: 105-165 hours
```

### Path 3: Design Focus

```
fundamentals (20-40h)
    ↓
colors (8-12h)
    ↓
animations (25-40h)
    ↓
design-systems (40-60h)

Total: 93-152 hours
```

## Topic Content

Each topic includes:

```
Topic Package:
├─ Core Concepts
│   └─ Theory & principles
├─ Code Examples
│   └─ Practical snippets
├─ Best Practices
│   └─ Industry standards
├─ Common Mistakes
│   └─ What to avoid
├─ Practice Projects
│   └─ Hands-on exercises
├─ Debug Guide
│   └─ Troubleshooting
└─ Resources
    └─ Further reading
```

## Depth Options

### Quick (30-50% time)
- Core concepts only
- Essential examples
- Key takeaways

### Standard (default)
- Complete coverage
- Multiple examples
- Practice exercises

### Deep (150-200% time)
- Advanced concepts
- Edge cases
- Performance considerations
- Architecture patterns

## Progress Tracking

```yaml
Recommended Study Pattern:
  - daily_time: 1-2 hours
  - weekly_project: 1 small project
  - monthly_review: Revisit earlier topics
  - practice_ratio: 60% hands-on, 40% theory
```

## Skill Verification

After each topic:
- [ ] Can explain core concepts
- [ ] Built practice project
- [ ] Reviewed common mistakes
- [ ] Applied best practices
- [ ] Debugged issues independently

## Topic Dependencies

```
fundamentals ─┬─→ positioning
              ├─→ colors
              ├─→ layouts ─┬─→ responsive
              │            ├─→ frameworks ─→ css-in-js
              │            └─→ cutting-edge
              ├─→ animations
              ├─→ transforms
              └─→ accessibility

All topics ─→ performance
           ─→ design-systems
```

## Related Commands

- `/css-playground` - Practice interactively
- `/css-projects` - Build projects
- `/css-inspector` - Debug & optimize
