---
name: css-inspector
description: inspector - CSS Analysis & Optimization
allowed-tools: Read
---

# /css-inspector - CSS Analysis & Optimization

Analyze, debug, and optimize your CSS with expert guidance.

## Usage

```
/css-inspector [action]
```

## Actions

### analyze
Analyze CSS for:
- Specificity issues
- Dead code
- Redundant selectors
- Performance problems
- Accessibility concerns

```
/css-inspector analyze
```

### optimize
Get optimization suggestions:
- CSS minification
- Unused styles
- Critical CSS extraction
- Performance metrics
- Bundle size analysis

```
/css-inspector optimize
```

### debug
Debug common CSS issues:
- Selector not working
- Box model problems
- Layout issues
- Z-index stacking
- Specificity conflicts

```
/css-inspector debug
```

### performance
Check performance:
- Rendering speed
- Animation smoothness
- Repaints/reflows
- Will-change usage
- GPU acceleration

```
/css-inspector performance
```

### accessibility
Verify accessibility:
- Color contrast
- Focus management
- Keyboard navigation
- Motion preferences
- WCAG compliance

```
/css-inspector accessibility
```

### best-practices
Review best practices:
- Naming conventions
- Code organization
- Maintainability
- Scalability
- Documentation

```
/css-inspector best-practices
```

## Common Issues & Solutions

### Selector Not Working
✗ `.container .item { }` (overcomplicated)
✓ `.item { }` (simple selector)

→ Lower specificity, easier to override

### Box Model Confusion
✗ `width: 100%; padding: 20px;` (overflow)
✓ `width: 100%; padding: 20px; box-sizing: border-box;`

→ Use box-sizing for predictable layouts

### Animation Performance
✗ `animation: move 1s; @keyframes move { left: 0; }`
✓ `animation: move 1s; @keyframes move { transform: translateX(0); }`

→ Use transform for 60fps animations

### Responsive Issues
✗ `width: 500px;` (fixed width)
✓ `width: 100%; max-width: 500px;`

→ Flexible widths for different screens

## Optimization Techniques

### File Size
- CSS minification: Save 20-30%
- Remove unused: Analyze with PurgeCSS
- Critical CSS: Load above-fold first
- Code splitting: Load when needed

### Performance
- Hardware acceleration: Use will-change
- Reduce repaints: Batch DOM changes
- Optimize selectors: Avoid deep nesting
- Use contain: Limit scope

### Maintainability
- Organize logically: Separate concerns
- Use preprocessors: SASS/LESS
- Follow naming: BEM, OOCSS
- Document code: Comments & guides

## Tools Integration

Recommended tools:
- **PurgeCSS** - Remove unused styles
- **CSSNano** - CSS minification
- **PostCSS** - CSS transformations
- **Stylelint** - CSS linting
- **Chrome DevTools** - CSS debugging

## Common Mistakes

1. **Over-specificity** - Leads to override wars
2. **Nested selectors** - Hard to maintain
3. **Inline styles** - No reusability
4. **Magic numbers** - Unexplained values
5. **Hardcoded widths** - Breaks responsiveness
6. **Animations on position** - Poor performance
7. **No mobile-first** - Harder to scale

## Performance Checklist

- [ ] CSS minified
- [ ] Unused styles removed
- [ ] Critical CSS extracted
- [ ] Animations use transform
- [ ] Colors have contrast
- [ ] Mobile-first approach
- [ ] Semantic selectors
- [ ] Browser support verified

## Quick Wins

1. Add `box-sizing: border-box;`
2. Remove vendor prefixes (autoprefixer)
3. Minify CSS (20-40% reduction)
4. Use CSS variables for consistency
5. Convert animations to transform
6. Mobile-first media queries
7. Optimize images separately

---

**Ready to optimize?** Try `/css-inspector [action]`
