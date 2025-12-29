---
name: css-in-js
description: Master CSS-in-JS solutions like styled-components and Emotion. Integrate styles with JavaScript components for modern web apps.
sasmp_version: "1.3.0"
bonded_agent: 01-css-fundamentals
bond_type: PRIMARY_BOND
---

# CSS-in-JS & Modern CSS Skill

## Quick Start

### styled-components
```javascript
import styled from 'styled-components';

const Button = styled.button`
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;

  &:hover {
    background-color: #2980b9;
  }

  ${props => props.primary && css`
    background-color: #e74c3c;
  `}
`;

// Usage
<Button>Click me</Button>
<Button primary>Primary Button</Button>
```

### Emotion
```javascript
import styled from '@emotion/styled';
import { css } from '@emotion/react';

const buttonStyles = css`
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;

  &:hover {
    background-color: #2980b9;
  }
`;

const Button = styled.button`
  ${buttonStyles}
`;
```

### CSS Modules
```css
/* Button.module.css */
.button {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.button:hover {
  background-color: #2980b9;
}

.primary {
  background-color: #e74c3c;
}
```

```javascript
import styles from './Button.module.css';

export function Button({ primary }) {
  return (
    <button className={`${styles.button} ${primary ? styles.primary : ''}`}>
      Click me
    </button>
  );
}
```

## BEM Methodology

```css
/* Block */
.card { }

/* Element */
.card__header { }
.card__body { }
.card__footer { }

/* Modifier */
.card--featured { }
.card__header--dark { }
```

## CSS-in-JS Benefits

✓ Scoped styles (no conflicts)
✓ Dynamic styles from props
✓ Automatic vendor prefixes
✓ Code splitting
✓ Component encapsulation
✓ Type safety (with TypeScript)

## Theming Pattern

```javascript
const theme = {
  colors: {
    primary: '#3498db',
    secondary: '#95a5a6',
    danger: '#e74c3c'
  },
  spacing: {
    xs: '4px',
    sm: '8px',
    md: '16px',
    lg: '24px'
  }
};

const Button = styled.button`
  background-color: ${props => props.theme.colors.primary};
  padding: ${props => props.theme.spacing.md};
`;
```

## Atomic CSS

```javascript
// Utilities as components
const Text = styled.p`
  margin: 0;
  font-family: system-ui;
  line-height: 1.5;
`;

const Flex = styled.div`
  display: flex;
  gap: ${props => props.gap || '0'};
  align-items: ${props => props.align || 'flex-start'};
  justify-content: ${props => props.justify || 'flex-start'};
`;
```

## Best Practices

✓ Keep styles co-located with components
✓ Use theme objects for consistency
✓ Extract common patterns
✓ Avoid deep nesting
✓ Use TypeScript for type safety
✓ Minimize specificity conflicts

## When to Use

- React/Vue component styling
- Creating design systems
- Building scalable applications
- Dynamic style requirements
- Component libraries
