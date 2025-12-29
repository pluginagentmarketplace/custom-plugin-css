---
name: css-frameworks
description: Master Tailwind CSS, Bootstrap, SASS, and CSS frameworks. Accelerate development with proven CSS tools and preprocessors.
sasmp_version: "1.3.0"
bonded_agent: 01-css-fundamentals
bond_type: PRIMARY_BOND
---

# CSS Frameworks & Preprocessors Skill

## Quick Start

### Tailwind CSS
```html
<!-- Utility-first approach -->
<div class="flex justify-center items-center bg-blue-500 p-4 rounded-lg">
  <button class="bg-white text-blue-500 px-6 py-2 rounded hover:bg-gray-100">
    Click me
  </button>
</div>
```

```js
// tailwind.config.js
module.exports = {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {
      colors: { primary: '#3B82F6' },
      spacing: { 'xs': '2px' }
    }
  }
}
```

### Bootstrap
```html
<!-- Component-based approach -->
<div class="container mt-5">
  <div class="row">
    <div class="col-md-6">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">Card Title</h5>
          <p class="card-text">Card content here</p>
        </div>
      </div>
    </div>
  </div>
</div>
```

### SASS/SCSS
```scss
// Variables
$primary-color: #3498db;
$spacing-unit: 8px;

// Nesting
.button {
  background-color: $primary-color;
  padding: $spacing-unit * 2;

  &:hover {
    background-color: darken($primary-color, 10%);
  }

  &.secondary {
    background-color: lightgray;
  }
}

// Mixin
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container { @include flex-center; }
```

## Framework Comparison

| Framework | Approach | Best For |
|-----------|----------|----------|
| Tailwind | Utility-first | Custom designs |
| Bootstrap | Component-based | Quick prototypes |
| SASS | Preprocessor | Code organization |

## Common Utilities

### Tailwind Classes
- `flex`, `grid` - Layouts
- `p-4`, `m-2` - Spacing
- `bg-blue-500`, `text-white` - Colors
- `rounded-lg`, `shadow-md` - Effects
- `hover:`, `focus:` - States

### Bootstrap Classes
- `.container`, `.row`, `.col-*` - Grid
- `.btn`, `.btn-primary` - Components
- `.mt-3`, `.p-4` - Spacing
- `.text-center`, `.d-flex` - Utilities

## SCSS Features

✓ Variables
✓ Nesting
✓ Mixins & functions
✓ Imports & partials
✓ Color functions
✓ Extends & inheritance

## Best Practices

✓ Choose one framework (don't mix)
✓ Understand framework principles
✓ Customize when needed
✓ Follow naming conventions
✓ Optimize for production
✓ Document custom styles

## When to Use

- Accelerating development
- Maintaining consistency
- Learning CSS organization
- Building design systems
- Custom component libraries
