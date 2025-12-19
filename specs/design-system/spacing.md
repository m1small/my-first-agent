# Spacing

## CSS Custom Properties

```css
--space-xs: 8px
--space-sm: 16px
--space-md: 24px
--space-lg: 32px
--space-xl: 48px
--space-2xl: 64px
```

## Spacing Scale (8px base)

| Token | Value | Usage |
|-------|-------|-------|
| xs | 8px | Small gaps, badge padding vertical |
| sm | 16px | Standard margins, badge padding horizontal |
| md | 24px | Section spacing, badge container margins |
| lg | 32px | Large section spacing, CTA margin-top |
| xl | 48px | Extra large spacing, desktop grid gaps |
| 2xl | 64px | Maximum spacing for major sections |

## Component Spacing

### Headline (h1)
```css
margin-bottom: var(--space-sm)  /* 16px */
```

### Bio Paragraph

**Desktop**:
```css
margin-bottom: var(--space-sm)  /* 16px */
max-width: 100%  /* Full width in grid layout */
padding: var(--space-lg)  /* 32px - card padding */
border-radius: 16px
```

**Tablet/Mobile**:
```css
max-width: 700px
padding: var(--space-md)  /* 24px */
```

### Badges Container
```css
margin-top: var(--space-md)  /* 24px */
margin-bottom: var(--space-md)  /* 24px */
gap: var(--space-xs)  /* 8px */
```

**Desktop (≥1025px)**:
```css
gap: 12px  /* Slightly larger for grid layout */
```

### Individual Badge

**Padding**:
```css
padding: var(--space-xs) var(--space-sm)  /* 8px 16px */
border-radius: 20px  /* Pill shape */
```

**Mobile Touch Targets (≤768px)**:
```css
padding: 12px 20px  /* Larger for better touch targets */
```

**Border**:
```css
border: 1px solid hsla(var(--color-accent-h), var(--color-accent-s), var(--color-accent-l), 0.2)
```

### CTA Button

**Desktop**:
```css
width: 300px
height: 100px
margin-top: var(--space-lg)  /* 32px */
border-radius: 50px  /* Oval shape */
```

**Tablet (≤768px)**:
```css
width: 280px
height: 90px
```

**Mobile (≤480px)**:
```css
width: 100%
max-width: 280px
min-height: 56px  /* iOS recommended minimum */
padding: 0 24px
```

### Main Container

**Desktop**:
```css
padding: 40px 20px
max-width: 800px  /* Centered single column */
```

**Desktop Grid (≥1025px)**:
```css
max-width: 1200px
gap: var(--space-xl)  /* 48px between grid areas */
```

**Tablet/Mobile (≤768px)**:
```css
padding: 20px 15px
```

## Responsive Grid Layout (≥1025px)

### Grid Structure
```css
display: grid
grid-template-columns: 300px 1fr
grid-template-areas:
    "sidebar header"
    "sidebar bio"
    "badges badges"
    "cta cta"
gap: var(--space-xl)  /* 48px */
```

### Grid Areas

**Sidebar** (future profile image area):
```css
grid-area: sidebar
width: 300px
```

**Header**:
```css
grid-area: header
```

**Bio**:
```css
grid-area: bio
```

**Badges**:
```css
grid-area: badges
```

**CTA**:
```css
grid-area: cta
```

## Border Radius Scale

```css
--radius-sm: 8px
--radius-md: 16px  /* Bio card */
--radius-lg: 20px  /* Badges */
--radius-full: 50px  /* CTA button */
--radius-circle: 50%  /* Future: profile image, theme toggle */
```

## Transitions

### Standard Transition
```css
transition: all 0.3s ease
```

### Fast Transition (hover effects)
```css
transition: all 0.2s ease
```

### Properties to Animate
- `transform` (scale, translateY)
- `box-shadow`
- `background-color`
- `border-color`
- `color`

### Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
    * {
        transition: none !important;
        animation: none !important;
    }
}
```

## Touch Targets (Mobile)

All interactive elements must meet minimum touch target sizes:

- **Minimum**: 44x44px (iOS/Android guidelines)
- **Recommended**: 48x48px
- **CTA Button**: 56px minimum height on mobile

## Accessibility

### Focus Indicators
```css
outline: 3px solid var(--color-accent)
outline-offset: 4px
```

### Spacing for Readability
- Line height: 1.8 for body text
- Paragraph max-width: 700px (optimal reading length)
- Adequate spacing between interactive elements (8px minimum)

## Reference

See also:
- [elevation.md](elevation.md) for shadow specifications
- [colors.md](colors.md) for color tokens
- [typography.md](typography.md) for text spacing
