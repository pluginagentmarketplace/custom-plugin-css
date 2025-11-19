---
name: css-layouts
description: Master Flexbox and CSS Grid for modern responsive layouts. Create flexible, adaptive designs that work on any screen size.
---

# CSS Layouts Skill

## Quick Start

### Flexbox Layout
```css
.container {
  display: flex;
  flex-direction: row; /* row, column, row-reverse, column-reverse */
  justify-content: center; /* flex-start, flex-end, center, space-between */
  align-items: center; /* flex-start, flex-end, center, stretch */
  gap: 20px; /* Space between items */
}

.item {
  flex: 1; /* Equal width */
  flex-grow: 1;
  flex-shrink: 1;
  flex-basis: 0;
}
```

### CSS Grid Layout
```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 equal columns */
  grid-template-rows: auto 200px auto; /* Row heights */
  gap: 20px; /* Space between items */
}

.grid-item {
  grid-column: span 2; /* Span 2 columns */
  grid-row: span 1;
}
```

### Responsive Design
```css
/* Mobile first */
.container {
  display: grid;
  grid-template-columns: 1fr; /* 1 column on mobile */
}

/* Tablet */
@media (min-width: 768px) {
  .container {
    grid-template-columns: repeat(2, 1fr); /* 2 columns */
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .container {
    grid-template-columns: repeat(3, 1fr); /* 3 columns */
  }
}
```

## Flexbox vs Grid

| Feature | Flexbox | Grid |
|---------|---------|------|
| Dimension | 1D (row/col) | 2D (both) |
| Best for | Components | Layouts |
| Item alignment | Center items | Position items |
| Flexibility | Very flexible | Precise control |

## Common Patterns

### Navigation Bar
```css
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}
```

### Card Grid
```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```

### Sidebar Layout
```css
.layout {
  display: grid;
  grid-template-columns: 250px 1fr;
  grid-template-rows: auto 1fr auto;
  height: 100vh;
}
```

## Best Practices

✓ Mobile-first approach
✓ Use semantic HTML
✓ Test on multiple devices
✓ Avoid hardcoded widths
✓ Use gap instead of margins
✓ Consider accessibility

## When to Use

- Building responsive websites
- Creating modern layouts
- Aligning complex components
- Mobile-first development
