---
name: css-inspector
description: CSS Analysis & Optimization Command
allowed-tools: Read, Glob, Grep
version: "2.0.0"
updated: "2025-12-30"
---

# /css-inspector - CSS Analysis & Optimization

Analyze, debug, and optimize CSS with actionable insights.

## Synopsis

```
/css-inspector <action> [options]
```

## Actions

| Action | Description | Exit Code |
|--------|-------------|-----------|
| `analyze` | Analyze specificity, dead code, performance | 0=clean, 1=issues |
| `optimize` | Get optimization recommendations | 0=success |
| `debug` | Debug CSS issues interactively | 0=resolved |
| `performance` | Audit render performance | 0=good, 1=needs work |
| `accessibility` | Check a11y compliance | 0=pass, 1=warnings, 2=fail |
| `best-practices` | Review code quality | 0=good, 1=improvements |

## Input Validation

```yaml
parameters:
  action:
    required: true
    type: string
    enum: [analyze, optimize, debug, performance, accessibility, best-practices]
    error: "Action must be one of: analyze, optimize, debug, performance, accessibility, best-practices"

  file:
    required: false
    type: string
    pattern: "^.*\\.(css|scss|sass|less)$"
    error: "File must be a CSS, SCSS, Sass, or Less file"

  verbose:
    required: false
    type: boolean
    default: false
```

## Exit Codes

| Code | Meaning |
|------|---------|
| 0 | Success / No issues found |
| 1 | Warnings / Minor issues |
| 2 | Errors / Critical issues |
| 3 | Invalid input |
| 4 | File not found |

## Usage Examples

```bash
# Analyze current project CSS
/css-inspector analyze

# Optimize specific file
/css-inspector optimize styles.css

# Debug layout issues
/css-inspector debug

# Check accessibility
/css-inspector accessibility
```

## Action Details

### analyze

```bash
/css-inspector analyze [file]
```

Analyzes CSS for:
- Specificity issues (over 0,1,0,0 threshold)
- Dead/unused selectors
- Redundant declarations
- Performance anti-patterns
- Accessibility concerns

**Output:**
```
Specificity Report:
├─ [WARN] .header .nav ul li a → 0,0,4,3 (high)
├─ [OK] .nav-link → 0,0,1,0
└─ [WARN] #main .content → 0,1,1,0 (ID used)

Dead Code: 3 unused selectors found
Performance: 2 layout-triggering animations
```

### optimize

```bash
/css-inspector optimize [file]
```

Recommendations for:
- Bundle size reduction
- Critical CSS extraction
- Selector optimization
- Unused style removal

### debug

```bash
/css-inspector debug [issue-type]
```

Interactive debugging for:
- `selector` - Why isn't my selector working?
- `layout` - Box model and positioning issues
- `stacking` - Z-index and stacking context
- `responsive` - Media query problems

### performance

```bash
/css-inspector performance
```

Audits:
- Render-blocking CSS
- Animation performance (compositor-only check)
- will-change usage
- Reflow triggers

### accessibility

```bash
/css-inspector accessibility
```

Checks:
- Color contrast (WCAG AA/AAA)
- Focus visibility
- Motion preferences
- Touch targets

### best-practices

```bash
/css-inspector best-practices
```

Reviews:
- Naming conventions
- Code organization
- Maintainability score
- Documentation coverage

## Quick Reference

### Common Issues & Fixes

| Issue | Fix |
|-------|-----|
| Over-specificity | Use single class selectors |
| Box model overflow | Add `box-sizing: border-box` |
| Animation jank | Use transform, not position |
| Fixed widths | Use `max-width` + percentage |

### Performance Checklist

- [ ] CSS minified in production
- [ ] Unused styles < 20%
- [ ] Critical CSS inlined
- [ ] Animations use transform/opacity
- [ ] No `!important` in components

## Integration

Works with agents:
- 01-css-fundamentals (selector help)
- 06-css-performance (optimization)
- 07-css-modern-features (modern patterns)

## Related Commands

- `/css-playground` - Interactive examples
- `/css-projects` - Practice projects
- `/learn-css` - Learn concepts
