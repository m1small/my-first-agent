# Headline Component

## Content
```
Hi, I'm Matt, Principal Consultant of mattasmall.com
```

## HTML Structure
```html
<h1>Hi, I'm Matt, Principal Consultant of mattasmall.com</h1>
```

## Typography

### Desktop (Default)
```css
font-size: 36px  /* Enhanced from 32px */
font-weight: 800  /* Bolder for more impact */
letter-spacing: -0.5px  /* Tighter tracking */
line-height: 1.3
color: var(--color-text-primary)  /* Brighter than body text */
```

### Tablet (≤768px)
```css
font-size: 28px  /* Enhanced from 26px */
font-weight: 800
letter-spacing: -0.3px
line-height: 1.3
```

### Mobile (≤480px)
Same as tablet.

## Visual Enhancements

### Text Shadow
```css
text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3)
```
Adds subtle depth without compromising readability.

### Spacing
```css
margin-bottom: var(--space-sm)  /* 16px */
```

## Responsive Alignment

### Desktop (≥1025px)
```css
text-align: left  /* Left-aligned in grid layout */
```

### Tablet and Mobile (≤1024px)
```css
text-align: center
```

## Accessibility

### Semantic HTML
- Use `<h1>` element (only one per page)
- Proper heading hierarchy

### Color Contrast
- Dark theme: 5.8:1 (exceeds WCAG AA 4.5:1) ✅
- Light theme: 8.5:1 (exceeds WCAG AA) ✅

### Text Shadow
- Shadow does not interfere with contrast ratio
- Enhances readability on gradient backgrounds

## Design Tokens Used

- `--color-text-primary`: Headline color
- `--space-sm`: Bottom margin
- Font family: System font stack (see [typography.md](../design-system/typography.md))

## Related Specifications

- [typography.md](../design-system/typography.md) - Font specifications
- [colors.md](../design-system/colors.md) - Color tokens
- [spacing.md](../design-system/spacing.md) - Spacing values
