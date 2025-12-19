# Elevation System

## Overview

The elevation system creates visual depth through layered shadows. Higher elevation values indicate elements that are "closer" to the user, creating a clear visual hierarchy.

## Shadow Scale

### CSS Custom Properties

```css
--shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.1)
--shadow-md: 0 4px 8px rgba(0, 0, 0, 0.15)
--shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.2)
--shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.25)
--shadow-2xl: 0 16px 32px rgba(0, 0, 0, 0.3)
```

### Light Mode Adjustments

In light mode, shadows are more subtle:

```css
@media (prefers-color-scheme: light) {
    --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.05)
    --shadow-md: 0 4px 8px rgba(0, 0, 0, 0.08)
    --shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.1)
    --shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.12)
    --shadow-2xl: 0 16px 32px rgba(0, 0, 0, 0.15)
}
```

## Elevation Levels

### Level 0: Base (No Shadow)
**Usage**: Page background, flat elements
**Shadow**: none
**Examples**: Body background

### Level 1: Subtle Elevation
**Usage**: Slightly raised elements, hover states
**Shadow**: `var(--shadow-sm)`
**Examples**: 
- Badge hover state
- Subtle text shadows

### Level 2: Card Elevation
**Usage**: Content cards, grouped information
**Shadow**: `var(--shadow-md)`
**Examples**:
- Bio card/container
- Badge default state (optional)

### Level 3: Floating Elements
**Usage**: Elements that float above content
**Shadow**: `var(--shadow-lg)`
**Examples**:
- Badge hover state (enhanced)
- Dropdown menus (future)

### Level 4: Primary Actions
**Usage**: Important interactive elements
**Shadow**: `var(--shadow-xl)`
**Examples**:
- CTA button default state
- Modal dialogs (future)

### Level 5: Maximum Elevation
**Usage**: Critical actions, hover states for primary elements
**Shadow**: `var(--shadow-2xl)`
**Examples**:
- CTA button hover state
- Tooltips (future)

## Component Application

### Headline (h1)
```css
text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3)
```
Subtle text shadow for depth without overwhelming the text.

### Bio Card
```css
box-shadow: var(--shadow-md)
```
Elevated card to separate content from background.

### Badges

**Default State**:
```css
box-shadow: var(--shadow-sm)
```

**Hover State**:
```css
box-shadow: 0 4px 8px rgba(255, 185, 0, 0.3)
```
Accent-colored shadow for interactive feedback.

### CTA Button

**Default State**:
```css
box-shadow: var(--shadow-xl)
```

**Hover State**:
```css
box-shadow: var(--shadow-2xl)
```

**Active State**:
```css
box-shadow: var(--shadow-lg)
```
Reduced shadow to simulate "pressing down" the button.

## Transitions

All shadow changes should be animated for smooth interactions:

```css
transition: box-shadow 0.3s ease, transform 0.3s ease
```

### Accessibility: Reduced Motion

Respect user preferences for reduced motion:

```css
@media (prefers-reduced-motion: reduce) {
    * {
        transition: none !important;
    }
}
```

## Best Practices

### Do's ✅
- Use elevation to establish visual hierarchy
- Animate shadow changes for smooth interactions
- Combine elevation with subtle transforms (scale, translateY)
- Use accent-colored shadows for interactive elements

### Don'ts ❌
- Don't use too many elevation levels on one page
- Don't animate shadows without respecting `prefers-reduced-motion`
- Don't use heavy shadows on small elements
- Don't mix elevation levels inconsistently

## Examples

### Badge with Elevation
```css
.badge {
    box-shadow: var(--shadow-sm);
    transition: all 0.2s ease;
}

.badge:hover {
    box-shadow: 0 4px 8px rgba(255, 185, 0, 0.3);
    transform: translateY(-2px);
}
```

### CTA Button with Elevation
```css
.cta-button {
    box-shadow: var(--shadow-xl);
    transition: all 0.3s ease;
}

.cta-button:hover {
    box-shadow: var(--shadow-2xl);
    transform: scale(1.05);
}

.cta-button:active {
    box-shadow: var(--shadow-lg);
    transform: scale(1.02);
}
```

### Bio Card with Elevation
```css
.bio {
    background: var(--color-surface);
    padding: var(--space-lg);
    border-radius: 16px;
    box-shadow: var(--shadow-md);
}
```

## Performance Considerations

- Shadows are GPU-accelerated in modern browsers
- Use `will-change: box-shadow` sparingly for elements that frequently animate
- Avoid animating shadows on scroll (performance impact)
- Combine with `transform` for smoother animations
