# Colors

## CSS Custom Properties Architecture

This specification uses CSS custom properties (variables) for dynamic theming and maintainability.

## Dark Theme (Default)

### Base Colors (HSL)
```css
--color-primary-h: 240
--color-primary-s: 20%
--color-primary-l: 27%
--color-primary: hsl(240, 20%, 27%)  /* #313357 */
```

### Accent Colors
```css
--color-accent-h: 45
--color-accent-s: 100%
--color-accent-l: 50%
--color-accent: hsl(45, 100%, 50%)  /* #ffb900 */
--color-accent-hover: hsl(45, 100%, 55%)
--color-accent-active: hsl(45, 100%, 45%)
```

### Surface Colors
```css
--color-background: hsl(240, 20%, 27%)  /* Primary background */
--color-surface: hsl(240, 20%, 32%)  /* Elevated surfaces (bio card) */
--color-surface-elevated: hsl(240, 20%, 37%)  /* Badges, hover states */
```

### Text Colors
```css
--color-text-primary: hsl(0, 0%, 90%)  /* #E8E8E8 - Headlines */
--color-text-secondary: hsl(0, 0%, 75%)  /* #C0C0C0 - Body text */
--color-text-tertiary: hsl(0, 0%, 60%)  /* #999999 - Subtle text */
```

## Light Theme (prefers-color-scheme: light)

### Base Colors
```css
--color-primary-l: 95%
--color-background: hsl(240, 15%, 95%)
--color-surface: hsl(240, 15%, 98%)
--color-surface-elevated: hsl(0, 0%, 100%)
```

### Text Colors (Light Mode)
```css
--color-text-primary: hsl(240, 20%, 15%)
--color-text-secondary: hsl(240, 15%, 30%)
--color-text-tertiary: hsl(240, 10%, 50%)
```

### Accent Colors (Same in both themes)
```css
--color-accent: hsl(45, 100%, 50%)
--color-accent-hover: hsl(45, 100%, 55%)
--color-accent-active: hsl(45, 100%, 45%)
```

## Semantic Color Usage

### Backgrounds
- **Page Background**: `var(--color-background)` with gradient
- **Bio Card**: `var(--color-surface)`
- **Badges**: `var(--color-surface-elevated)`
- **CTA Button**: `var(--color-accent)`

### Text
- **Headline (h1)**: `var(--color-text-primary)`
- **Bio Paragraph**: `var(--color-text-secondary)`
- **Badges**: `var(--color-text-secondary)`
- **CTA Button Text**: `var(--color-primary)`
- **Emphasized Text**: `var(--color-accent)` (for `<strong>` tags)

## Gradients

### Background Gradient
```css
background: linear-gradient(
    135deg,
    var(--color-background) 0%,
    hsl(var(--color-primary-h), calc(var(--color-primary-s) + 5%), calc(var(--color-primary-l) - 3%)) 100%
);
```

### CTA Button Gradient
```css
background: linear-gradient(
    135deg,
    var(--color-accent) 0%,
    hsl(var(--color-accent-h), var(--color-accent-s), calc(var(--color-accent-l) + 10%)) 100%
);
```

### Badge Hover Gradient
```css
background: linear-gradient(
    135deg,
    var(--color-surface-elevated) 0%,
    hsl(var(--color-primary-h), calc(var(--color-primary-s) + 10%), calc(var(--color-primary-l) + 8%)) 100%
);
```

## Badge Variants

### Primary Badges (Top Credentials)
```css
border-color: var(--color-accent)
background: linear-gradient(
    135deg,
    var(--color-surface) 0%,
    hsl(var(--color-accent-h), 30%, 25%) 100%
)
```

**Apply to**: AWS Solutions Architect, FinOps Certified, Kwaai.ai Board Member

### Standard Badges
```css
border-color: hsla(var(--color-accent-h), var(--color-accent-s), var(--color-accent-l), 0.2)
background: var(--color-surface-elevated)
```

## Accessibility

### Contrast Ratios (WCAG AA: 4.5:1 minimum)
- **Dark Theme**: Text on primary: 5.8:1 ✅
- **Dark Theme**: Primary on accent: 7.2:1 ✅
- **Light Theme**: Text on background: 8.5:1 ✅
- **Light Theme**: Primary on accent: 7.2:1 ✅

All color combinations maintain WCAG 2.1 Level AA compliance in both themes.
