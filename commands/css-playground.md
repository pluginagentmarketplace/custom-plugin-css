---
name: css-playground
description: Interactive CSS Examples & Practice
allowed-tools: Read
version: "2.0.0"
updated: "2025-12-30"
---

# /css-playground - Interactive CSS Examples

Explore CSS with interactive examples, live code, and hands-on practice.

## Synopsis

```
/css-playground <category> [difficulty]
```

## Input Validation

```yaml
parameters:
  category:
    required: true
    type: string
    enum: [selectors, box-model, flexbox, grid, responsive, colors, typography, animations, transforms, components]
    error: "Category must be one of the available topics"

  difficulty:
    required: false
    type: string
    default: beginner
    enum: [beginner, intermediate, advanced, expert]
    error: "Difficulty must be: beginner, intermediate, advanced, or expert"
```

## Exit Codes

| Code | Meaning |
|------|---------|
| 0 | Playground loaded successfully |
| 1 | Invalid category |
| 2 | Invalid difficulty |
| 3 | Resource not found |

## Categories

### Fundamentals
| Category | Description | Levels |
|----------|-------------|--------|
| `selectors` | CSS selectors mastery | All |
| `box-model` | Content, padding, border, margin | Beginner-Intermediate |
| `colors` | Color systems & palettes | All |
| `typography` | Font styling & text | All |

### Layout
| Category | Description | Levels |
|----------|-------------|--------|
| `flexbox` | Flex container & items | All |
| `grid` | CSS Grid layouts | All |
| `responsive` | Mobile-first patterns | Intermediate+ |

### Effects
| Category | Description | Levels |
|----------|-------------|--------|
| `animations` | Keyframes & timing | Intermediate+ |
| `transforms` | 2D & 3D transforms | All |

### Components
| Category | Description | Levels |
|----------|-------------|--------|
| `components` | Buttons, cards, navs | All |

## Usage Examples

```bash
# Basic flexbox examples
/css-playground flexbox beginner

# Advanced grid techniques
/css-playground grid advanced

# Animation patterns
/css-playground animations intermediate

# Component library examples
/css-playground components
```

## Difficulty Levels

### Beginner
- Core concepts explained
- Simple, isolated examples
- Step-by-step guidance
- Common patterns only

### Intermediate
- Real-world patterns
- Combined techniques
- Responsive variations
- Best practices focus

### Advanced
- Complex compositions
- Edge cases covered
- Performance optimized
- Browser considerations

### Expert
- Cutting-edge features
- Optimization tricks
- Architecture patterns
- Production patterns

## What Each Playground Includes

```
Each playground provides:
├─ Live code editor
├─ Real-time preview
├─ Concept explanation
├─ Property reference
├─ Common mistakes
├─ Variations to try
└─ Related patterns
```

## Quick Reference

### Flexbox

```css
.container {
  display: flex;
  justify-content: center;  /* Main axis */
  align-items: center;      /* Cross axis */
  gap: 1rem;
}
```

### Grid

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
}
```

### Animations

```css
@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

.element {
  animation: fade-in 0.3s ease-out forwards;
}
```

## Learning Path

```
1. selectors beginner
   └─ Learn CSS selection
       ↓
2. box-model beginner
   └─ Understand spacing
       ↓
3. flexbox beginner → intermediate
   └─ 1D layouts
       ↓
4. grid beginner → intermediate
   └─ 2D layouts
       ↓
5. responsive intermediate
   └─ Mobile-first
       ↓
6. animations intermediate → advanced
   └─ Motion design
       ↓
7. components advanced
   └─ Build real UI
```

## Featured Playgrounds

### Most Used
- `flexbox beginner` - Start here for layouts
- `grid intermediate` - Responsive grids
- `animations intermediate` - Smooth transitions

### Modern CSS
- `grid expert` - Container queries
- `selectors advanced` - :has() patterns
- `responsive expert` - Fluid typography

## Related Commands

- `/css-inspector` - Debug issues
- `/css-projects` - Build projects
- `/learn-css` - Structured learning
