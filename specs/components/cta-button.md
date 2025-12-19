# CTA Button Component

## Content
```
Talk AI and Cloud Optimization
```

## Link Destination
```
mailto:mattasmall@gmail.com?subject=Consultation%20Request
```

## HTML Structure

```html
<div class="cta-container">
    <a href="mailto:mattasmall@gmail.com?subject=Consultation%20Request"
       class="cta-button"
       role="button"
       aria-label="Contact Matt Small to discuss AI and Cloud Optimization">
        Talk AI and Cloud Optimization
    </a>
</div>
```

## Button Styling

### Default State

**Dimensions (Desktop)**:
```css
width: 300px
height: 100px
border-radius: 50px  /* Oval shape */
```

**Colors & Background**:
```css
background: linear-gradient(
    135deg,
    var(--color-accent) 0%,
    hsl(var(--color-accent-h), var(--color-accent-s), calc(var(--color-accent-l) + 10%)) 100%
)
color: var(--color-primary)
```

**Typography**:
```css
font-size: 18px
font-weight: 600
text-decoration: none
```

**Layout**:
```css
display: inline-flex
align-items: center
justify-content: center
```

**Elevation**:
```css
box-shadow: var(--shadow-xl)  /* Strong elevation for primary action */
```

**Transition**:
```css
transition: transform 0.3s ease, box-shadow 0.3s ease
cursor: pointer
```

### Hover State
```css
background: linear-gradient(
    135deg,
    var(--color-accent-hover) 0%,
    hsl(var(--color-accent-h), var(--color-accent-s), calc(var(--color-accent-l) + 15%)) 100%
)
transform: scale(1.05)
box-shadow: var(--shadow-2xl)  /* Maximum elevation */
```

### Active State (Click/Press)
```css
transform: scale(1.02)  /* Slight press effect */
box-shadow: var(--shadow-lg)  /* Reduced shadow */
```

### Focus State (Keyboard Navigation)
```css
outline: 3px solid var(--color-accent)
outline-offset: 4px
```

## Container Styling

```css
.cta-container {
    margin-top: var(--space-lg)  /* 32px */
    display: flex
    justify-content: center
}
```

## Responsive Sizing

### Tablet (≤768px)
```css
width: 280px
height: 90px
font-size: 18px  /* Consistent across breakpoints */
```

### Mobile (≤480px)
```css
width: 100%
max-width: 280px
min-height: 56px  /* iOS recommended minimum */
padding: 0 24px
```

## Accessibility

### Semantic HTML
- Use `<a>` element (not `<button>`) since it navigates to mailto link
- Include `role="button"` for screen reader context
- Descriptive `aria-label` for full context

### Keyboard Navigation
- Focusable via Tab key
- Activatable via Enter or Space key
- Clear focus indicator (3px outline, 4px offset)

### Touch Targets
- Desktop: 300x100px (well above 44x44px minimum)
- Mobile: 56px minimum height (exceeds 44px minimum)

### Color Contrast
- Text on button: 7.2:1 (exceeds WCAG AA 4.5:1) ✅
- Focus outline: High contrast accent color

### Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
    .cta-button {
        transition: none !important
    }
}
```

## Interaction States Summary

| State | Transform | Shadow | Background |
|-------|-----------|--------|------------|
| Default | none | `--shadow-xl` | Accent gradient |
| Hover | `scale(1.05)` | `--shadow-2xl` | Lighter gradient |
| Active | `scale(1.02)` | `--shadow-lg` | Accent gradient |
| Focus | none | `--shadow-xl` | Accent gradient + outline |

## Design Tokens Used

- `--color-accent`: Button background
- `--color-accent-hover`: Hover state background
- `--color-primary`: Button text color
- `--shadow-xl`: Default elevation
- `--shadow-2xl`: Hover elevation
- `--shadow-lg`: Active elevation
- `--space-lg`: Top margin

## Related Specifications

- [colors.md](../design-system/colors.md) - Color tokens and gradients
- [elevation.md](../design-system/elevation.md) - Shadow system
- [spacing.md](../design-system/spacing.md) - Dimensions and spacing
- [typography.md](../design-system/typography.md) - Font specifications
