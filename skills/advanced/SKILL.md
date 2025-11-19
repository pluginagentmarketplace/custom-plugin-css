---
name: css-advanced
description: Master animations, transforms, performance optimization, accessibility, and cutting-edge CSS features. Become a CSS expert.
---

# Advanced CSS Techniques Skill

## Quick Start

### Animations & Transitions
```css
/* Transition - smooth property change */
.button {
  background-color: blue;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: darkblue;
}

/* Animation - keyframe sequence */
@keyframes slideIn {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

.element {
  animation: slideIn 0.5s ease forwards;
}
```

### 3D Transforms
```css
.container {
  perspective: 1000px;
}

.card {
  transform: rotateX(10deg) rotateY(20deg) translateZ(50px);
  transform-style: preserve-3d;
}

.card:hover {
  transform: rotateY(360deg);
  transition: transform 0.6s ease;
}
```

### Performance Optimization
```css
/* Use transform & opacity for animations */
.good {
  animation: slideIn 0.5s ease;
}

@keyframes slideIn {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(0); }
}

/* Avoid animating these properties */
.bad {
  animation: position 0.5s ease; /* Don't do this */
}

@keyframes position {
  0% { left: -100px; }
  100% { left: 0; }
}

/* CSS Containment */
.widget {
  contain: layout style paint;
  /* Limits browser reflow to this element */
}
```

### Accessibility
```css
/* Respect user motion preferences */
@media (prefers-reduced-motion: reduce) {
  * {
    animation: none !important;
    transition: none !important;
  }
}

/* Color contrast (check with WCAG) */
.text {
  color: #000000;
  background-color: #FFFFFF;
  /* Contrast ratio: 21:1 (AAA) */
}

/* Focus visible for keyboard navigation */
button:focus-visible {
  outline: 3px solid #4A90E2;
  outline-offset: 2px;
}
```

### Container Queries
```css
@container (min-width: 400px) {
  .card {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
```

## Timing Functions

```css
/* Linear */
.linear { animation: slide 1s linear; }

/* Ease functions */
.ease { animation: slide 1s ease; }
.ease-in { animation: slide 1s ease-in; }
.ease-out { animation: slide 1s ease-out; }
.ease-in-out { animation: slide 1s ease-in-out; }

/* Cubic bezier */
.custom { animation: slide 1s cubic-bezier(0.17, 0.67, 0.83, 0.67); }
```

## Performance Tips

✓ Use `transform` and `opacity` for animations
✓ Enable hardware acceleration (`will-change`)
✓ Minimize repaints and reflows
✓ Use `contain` to limit layout calculations
✓ Optimize images and assets
✓ Critical CSS approach
✓ Lazy load non-critical styles

## Advanced Selectors

```css
/* :has() - Parent selector */
.card:has(img) {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

/* :is() & :where() */
button:is(.primary, .secondary, .danger) {
  padding: 10px 20px;
}

/* Complex combinators */
div > p + span {
  color: red;
}
```

## Cutting-Edge Features

✓ Container Queries
✓ CSS Grid 2 (Subgrid)
✓ Cascade Layers (@layer)
✓ CSS Nesting
✓ View Transitions API
✓ CSS :has() selector

## Best Practices

✓ Plan animations carefully
✓ Test on real devices
✓ Monitor performance metrics
✓ Ensure accessibility
✓ Use hardware acceleration wisely
✓ Document complex animations
✓ Provide fallbacks

## When to Use

- Complex animations
- Interactive designs
- Performance-critical apps
- Accessibility-focused projects
- Cutting-edge modern sites
