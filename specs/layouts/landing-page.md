# Landing Page Layout

## Component Order
1. [headline.md](../components/headline.md)
2. [bio.md](../components/bio.md)
3. [badges.md](../components/badges.md)
4. [cta-button.md](../components/cta-button.md)

## HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Matt Small - Principal Consultant specializing in FinOps, Enterprise AI adoption, and Cloud strategy. 15+ years driving transformation at Fortune 500 companies and startups.">
    <title>Matt Small - Principal Consultant</title>
    <style>
        /* CSS Custom Properties */
        :root {
            /* Color tokens from colors.md */
            /* Spacing tokens from spacing.md */
            /* Shadow tokens from elevation.md */
        }
        
        /* CSS Reset */
        /* Body styles */
        /* Main container styles */
        /* Component styles */
        
        /* Responsive breakpoints */
        @media (max-width: 768px) { /* Tablet */ }
        @media (max-width: 480px) { /* Mobile */ }
        @media (min-width: 1025px) { /* Desktop Grid */ }
        
        /* Light mode support */
        @media (prefers-color-scheme: light) { }
        
        /* Reduced motion support */
        @media (prefers-reduced-motion: reduce) { }
    </style>
</head>
<body>
    <main role="main">
        <h1><!-- Headline --></h1>
        <p class="bio"><!-- Bio with <strong> tags --></p>
        <div class="badges-container" role="list" aria-label="Professional credentials and expertise">
            <!-- Badge spans -->
        </div>
        <div class="cta-container">
            <a href="mailto:..." class="cta-button" role="button" aria-label="...">
                <!-- CTA text -->
            </a>
        </div>
    </main>
</body>
</html>
```

## CSS Architecture

### 1. CSS Custom Properties (Root)

Define all design tokens at the root level:

```css
:root {
    /* Colors - see colors.md */
    --color-primary-h: 240;
    --color-primary-s: 20%;
    --color-primary-l: 27%;
    --color-primary: hsl(240, 20%, 27%);
    --color-accent: hsl(45, 100%, 50%);
    /* ... all color tokens */
    
    /* Spacing - see spacing.md */
    --space-xs: 8px;
    --space-sm: 16px;
    --space-md: 24px;
    --space-lg: 32px;
    --space-xl: 48px;
    --space-2xl: 64px;
    
    /* Shadows - see elevation.md */
    --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.1);
    --shadow-md: 0 4px 8px rgba(0, 0, 0, 0.15);
    --shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.2);
    --shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.25);
    --shadow-2xl: 0 16px 32px rgba(0, 0, 0, 0.3);
}
```

### 2. CSS Reset

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

### 3. Body Styles

```css
body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    background: linear-gradient(
        135deg,
        var(--color-background) 0%,
        hsl(var(--color-primary-h), calc(var(--color-primary-s) + 5%), calc(var(--color-primary-l) - 3%)) 100%
    );
    color: var(--color-text-primary);
    line-height: 1.6;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px;
}
```

## Responsive Layout System

### Mobile First (Default: ≤1024px)

**Single Column, Centered Layout**:

```css
main {
    max-width: 800px;
    width: 100%;
    text-align: center;
    padding: 40px 20px;
}

/* Tablet adjustments */
@media (max-width: 768px) {
    main {
        padding: 20px 15px;
    }
}
```

### Desktop Grid Layout (≥1025px)

**Asymmetric Grid with Sidebar**:

```css
@media (min-width: 1025px) {
    main {
        display: grid;
        grid-template-columns: 300px 1fr;
        grid-template-areas:
            "sidebar header"
            "sidebar bio"
            "badges badges"
            "cta cta";
        gap: var(--space-xl);  /* 48px */
        max-width: 1200px;
        text-align: left;  /* Left-align for better readability */
    }
    
    /* Future: Profile sidebar area */
    .profile-sidebar {
        grid-area: sidebar;
        /* Reserved for future profile image, social links */
    }
    
    h1 {
        grid-area: header;
        text-align: left;
    }
    
    .bio {
        grid-area: bio;
        text-align: left;
        max-width: 100%;  /* Full width in grid */
    }
    
    .badges-container {
        grid-area: badges;
        justify-content: flex-start;  /* Left-aligned */
    }
    
    .cta-container {
        grid-area: cta;
        justify-content: center;  /* Centered */
    }
}
```

## Breakpoint Strategy

| Breakpoint | Range | Layout | Alignment |
|------------|-------|--------|-----------|
| Mobile | ≤480px | Single column | Center |
| Tablet | 481px - 768px | Single column | Center |
| Desktop (Small) | 769px - 1024px | Single column | Center |
| Desktop (Large) | ≥1025px | Asymmetric grid | Left (except CTA) |

## Component Integration

### Headline
- Mobile/Tablet: Centered
- Desktop Grid: Left-aligned in header area
- See [headline.md](../components/headline.md)

### Bio
- Mobile/Tablet: Centered, max-width 700px
- Desktop Grid: Left-aligned, full width with card styling
- See [bio.md](../components/bio.md)

### Badges
- Mobile/Tablet: Centered, flex-wrap
- Desktop Grid: Left-aligned, grid layout
- See [badges.md](../components/badges.md)

### CTA Button
- All breakpoints: Centered
- Responsive sizing per breakpoint
- See [cta-button.md](../components/cta-button.md)

## Theme Support

### Light Mode
```css
@media (prefers-color-scheme: light) {
    :root {
        --color-primary-l: 95%;
        --color-background: hsl(240, 15%, 95%);
        --color-surface: hsl(240, 15%, 98%);
        --color-surface-elevated: hsl(0, 0%, 100%);
        --color-text-primary: hsl(240, 20%, 15%);
        --color-text-secondary: hsl(240, 15%, 30%);
        /* Adjust shadows for light mode */
        --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.05);
        --shadow-md: 0 4px 8px rgba(0, 0, 0, 0.08);
        --shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.1);
        --shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.12);
        --shadow-2xl: 0 16px 32px rgba(0, 0, 0, 0.15);
    }
}
```

### Dark Mode (Default)
Uses default CSS custom property values.

## Accessibility

### Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
    }
}
```

### Semantic Structure
- `<main role="main">` for main content
- Proper heading hierarchy (single `<h1>`)
- ARIA labels for non-semantic elements
- Keyboard navigation support

### Focus Management
- Visible focus indicators on all interactive elements
- Logical tab order
- Skip links (future enhancement)

## Performance Considerations

### Single File Architecture
- All CSS inline in `<style>` tag
- No external requests
- Target file size: <50KB
- Load time: <3 seconds

### CSS Optimization
- Use CSS custom properties for maintainability
- Minimize selector complexity
- Leverage GPU acceleration (transform, opacity)
- Avoid expensive properties (box-shadow on scroll)

## Future Enhancements

### Profile Sidebar (Desktop Grid)
Reserved grid area for:
- Profile image
- Social media links
- Contact information
- Theme toggle button

### Grid Template (Future)
```css
grid-template-areas:
    "sidebar header"
    "sidebar bio"
    "sidebar badges"
    "cta cta";
```

## Design System References

- [colors.md](../design-system/colors.md) - Color tokens and theming
- [typography.md](../design-system/typography.md) - Font specifications
- [spacing.md](../design-system/spacing.md) - Spacing and layout
- [elevation.md](../design-system/elevation.md) - Shadow system

## Component References

- [headline.md](../components/headline.md) - Headline component
- [bio.md](../components/bio.md) - Bio paragraph component
- [badges.md](../components/badges.md) - Badges component
- [cta-button.md](../components/cta-button.md) - CTA button component

## Requirements References

- [technical.md](../requirements/technical.md) - Technical constraints
- [accessibility.md](../requirements/accessibility.md) - WCAG compliance
