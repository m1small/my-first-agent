# Badges Component

## Badge List

All badges now use the gold gradient styling for visual consistency.

### Row 1 (3 badges)
1. AWS Solutions Architect
2. FinOps Certified
3. Kwaai.ai Board Member

### Row 2 (4 badges)
4. 15+ Years Cloud Platforms
5. RightScale Pioneer
6. Infrastructure-as-Code Expert
7. Enterprise AI Governance

### Row 3 (3 badges)
8. Pulumi Alumni
9. Customer Success Leader
10. Strategic GTM Advisor

## HTML Structure

```html
<div class="badges-container" role="list" aria-label="Professional credentials and expertise">
    <!-- Row 1: 3 badges -->
    <span class="badge" role="listitem">AWS Solutions Architect</span>
    <span class="badge" role="listitem">FinOps Certified</span>
    <span class="badge" role="listitem">Kwaai.ai Board Member</span>
    
    <!-- Row 2: 4 badges -->
    <span class="badge" role="listitem">15+ Years Cloud Platforms</span>
    <span class="badge" role="listitem">RightScale Pioneer</span>
    <span class="badge" role="listitem">Infrastructure-as-Code Expert</span>
    <span class="badge" role="listitem">Enterprise AI Governance</span>
    
    <!-- Row 3: 3 badges -->
    <span class="badge" role="listitem">Pulumi Alumni</span>
    <span class="badge" role="listitem">Customer Success Leader</span>
    <span class="badge" role="listitem">Strategic GTM Advisor</span>
</div>
```

## Container Layout

### All Breakpoints (Centered)
```css
display: flex
flex-wrap: wrap
justify-content: center  /* Always centered */
gap: var(--space-xs)  /* 8px */
margin-top: var(--space-md)  /* 24px */
margin-bottom: var(--space-md)  /* 24px */
max-width: 800px  /* Constrain width for 3-4-3 layout */
margin-left: auto
margin-right: auto
```

## Badge Styling

### All Badges - Default State (Gold Gradient)
All badges now use the gold gradient styling:

```css
background: linear-gradient(
    135deg,
    var(--color-surface) 0%,
    hsl(var(--color-accent-h), 30%, 25%) 100%
)
border-color: var(--color-accent)
color: var(--color-text-secondary)
font-size: 12px
font-weight: 400
padding: var(--space-xs) var(--space-sm)  /* 8px 16px */
border-radius: 20px  /* Pill shape */
box-shadow: var(--shadow-sm)
display: inline-block
white-space: nowrap
transition: all 0.2s ease
```

### All Badges - Hover State
```css
border-color: var(--color-accent)
box-shadow: 0 4px 8px rgba(255, 185, 0, 0.4)  /* Accent-colored shadow */
transform: translateY(-2px)
```

## Mobile Optimization (≤768px)

### Enhanced Touch Targets
```css
padding: 12px 20px  /* Larger for better touch targets */
font-size: 13px  /* Slightly larger */
```

## Staggered Animation (Optional Enhancement)

On page load, badges can animate in with a staggered delay:

```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.badge {
    animation: fadeInUp 0.5s ease forwards;
    opacity: 0;
}

.badge:nth-child(1) { animation-delay: 0.1s; }
.badge:nth-child(2) { animation-delay: 0.15s; }
.badge:nth-child(3) { animation-delay: 0.2s; }
.badge:nth-child(4) { animation-delay: 0.25s; }
.badge:nth-child(5) { animation-delay: 0.3s; }
.badge:nth-child(6) { animation-delay: 0.35s; }
.badge:nth-child(7) { animation-delay: 0.4s; }
.badge:nth-child(8) { animation-delay: 0.45s; }
.badge:nth-child(9) { animation-delay: 0.5s; }
.badge:nth-child(10) { animation-delay: 0.55s; }
```

**Note**: Must respect `prefers-reduced-motion`:
```css
@media (prefers-reduced-motion: reduce) {
    .badge {
        animation: none;
        opacity: 1;
    }
}
```

## Accessibility

### Semantic HTML
- Container: `role="list"` with descriptive `aria-label`
- Individual badges: `role="listitem"`

### Interactive Elements
- Badges are not interactive (no click/tap behavior)
- Hover effects are visual enhancements only
- Cursor remains default (not pointer)

### Touch Targets
- Mobile: 44x44px minimum (achieved with 13px font + 12px vertical padding + 20px horizontal padding)

### Color Contrast
- Text on badge background: 4.5:1 minimum ✅
- Border visibility: Sufficient contrast in both themes

## Design Tokens Used

- `--color-surface-elevated`: Badge background
- `--color-surface`: Primary badge gradient start
- `--color-text-secondary`: Badge text
- `--color-accent`: Primary badge border, hover shadows
- `--shadow-sm`: Default elevation
- `--space-xs`: Vertical padding, container gap
- `--space-sm`: Horizontal padding
- `--space-md`: Container margins

## Related Specifications

- [colors.md](../design-system/colors.md) - Color tokens and gradients
- [spacing.md](../design-system/spacing.md) - Padding and gaps
- [elevation.md](../design-system/elevation.md) - Shadow system
- [typography.md](../design-system/typography.md) - Font specifications
