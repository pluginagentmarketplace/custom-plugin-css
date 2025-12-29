---
name: css-fundamentals
description: Master CSS selectors, box model, typography, colors, and positioning. Build strong CSS foundations with practical examples and best practices.
sasmp_version: "1.3.0"
bonded_agent: 01-css-fundamentals
bond_type: PRIMARY_BOND
---

# CSS Fundamentals Skill

## Quick Start

### Basic Selector Examples
```css
/* Element selector */
p { color: blue; }

/* Class selector */
.primary { font-weight: bold; }

/* ID selector */
#header { background: navy; }

/* Attribute selector */
input[type="text"] { border: 1px solid gray; }

/* Pseudo-class */
a:hover { color: red; }

/* Pseudo-element */
p::first-line { font-weight: bold; }
```

### Box Model
```css
.box {
  width: 300px;
  padding: 20px;
  border: 2px solid black;
  margin: 30px;
  box-sizing: border-box; /* Include padding & border in width */
}
```

### Typography
```css
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  letter-spacing: 0.5px;
  text-align: center;
}

h1 { font-size: 2rem; }
p { font-weight: normal; }
```

### Colors
```css
/* Different color formats */
.color1 { color: #FF5733; }           /* Hex */
.color2 { color: rgb(255, 87, 51); }  /* RGB */
.color3 { color: hsl(10, 100%, 60%); }/* HSL */
.color4 { color: rgba(255, 87, 51, 0.8); } /* Transparency */
```

### Positioning
```css
/* Static (default) */
.static { position: static; }

/* Relative */
.relative { position: relative; top: 10px; left: 20px; }

/* Absolute */
.absolute { position: absolute; top: 50px; right: 20px; }

/* Fixed */
.fixed { position: fixed; bottom: 0; left: 0; }

/* Sticky */
.sticky { position: sticky; top: 0; }
```

## Key Concepts

### Selector Specificity
- Element: 1 point
- Class/Attribute: 10 points
- ID: 100 points
- Inline: 1000 points

### Box Model Calculation
```
Total Width = width + padding + border + margin
```

### Text Properties
- **font-family** - Font type
- **font-size** - Text size
- **font-weight** - Boldness
- **text-align** - Horizontal alignment
- **line-height** - Vertical spacing

### Common Colors
- Named: red, blue, green
- Hex: #FF0000
- RGB: rgb(255, 0, 0)
- HSL: hsl(0, 100%, 50%)

## Best Practices

✓ Use classes for styling (avoid IDs)
✓ Keep specificity low
✓ Use semantic HTML
✓ Organize CSS logically
✓ Comment complex styles
✓ Maintain consistent naming

## When to Use

- Starting CSS journey
- Learning core concepts
- Building web foundations
- Understanding design principles
