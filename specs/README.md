# Specifications

Modular specifications for Matt Small's landing page, optimized for implementation with enhanced design system.

## Version
**Specification Version**: 2.0.0 (Enhanced Design System)
**Last Updated**: 2025-12-19

## Structure

```
specs/
├── project.md              # Project overview and goals
├── design-system/          # Design tokens and system
│   ├── colors.md          # CSS custom properties, light/dark themes
│   ├── typography.md      # Enhanced font hierarchy
│   ├── spacing.md         # Spacing scale and responsive grid
│   └── elevation.md       # Shadow system for depth ✨ NEW
├── components/             # Component specifications
│   ├── headline.md        # Headline with text shadow
│   ├── bio.md            # Biography with card styling
│   ├── badges.md         # Badges with hover effects and variants
│   └── cta-button.md     # CTA button with enhanced interactions
├── layouts/               # Page layout and composition
│   └── landing-page.md   # Responsive grid system, HTML structure
└── requirements/          # Cross-cutting requirements
    ├── technical.md      # Technical constraints
    └── accessibility.md  # WCAG 2.1 Level AA standards
```

## What's New in v2.0.0

### Enhanced Design System
- **CSS Custom Properties**: Dynamic theming with CSS variables
- **Light/Dark Mode**: Automatic theme switching based on user preference
- **Elevation System**: Layered shadows for visual hierarchy
- **Responsive Grid**: Asymmetric layout on desktop (≥1025px)

### Visual Enhancements
- **Typography Hierarchy**: Bolder headlines (800 weight), larger sizes
- **Card Styling**: Elevated bio container with shadows
- **Badge Interactions**: Hover effects with accent-colored shadows
- **Primary Badge Variants**: Enhanced styling for top credentials
- **Gradient Backgrounds**: Subtle gradients for depth

### Improved Interactions
- **Micro-animations**: Smooth hover transitions
- **Transform Effects**: Scale and translateY on interactive elements
- **Enhanced CTA**: Gradient background with maximum elevation
- **Staggered Animations**: Optional badge entrance animations

## Implementation Order

### Phase 1: Foundation
1. Read [`project.md`](project.md) for business context and goals
2. Read [`layouts/landing-page.md`](layouts/landing-page.md) for HTML structure and responsive strategy

### Phase 2: Design System
3. Read [`design-system/colors.md`](design-system/colors.md) for color tokens and theming
4. Read [`design-system/typography.md`](design-system/typography.md) for font specifications
5. Read [`design-system/spacing.md`](design-system/spacing.md) for spacing scale and grid
6. Read [`design-system/elevation.md`](design-system/elevation.md) for shadow system

### Phase 3: Components
7. Read [`components/headline.md`](components/headline.md) for headline specifications
8. Read [`components/bio.md`](components/bio.md) for bio paragraph with card styling
9. Read [`components/badges.md`](components/badges.md) for badge list with interactions
10. Read [`components/cta-button.md`](components/cta-button.md) for CTA button

### Phase 4: Requirements
11. Read [`requirements/technical.md`](requirements/technical.md) for technical constraints
12. Read [`requirements/accessibility.md`](requirements/accessibility.md) for WCAG compliance

## Design System Features

### CSS Custom Properties
All design tokens are defined as CSS variables for:
- Easy theme switching (light/dark mode)
- Consistent values across components
- Maintainable and scalable styling
- Dynamic color calculations

### Responsive Strategy
- **Mobile First**: Base styles for ≤1024px
- **Tablet**: 481px - 768px (centered, single column)
- **Desktop**: ≥1025px (asymmetric grid layout)
- **Touch Targets**: 44x44px minimum on mobile

### Theming Support
- **Dark Theme**: Default (professional, high contrast)
- **Light Theme**: Automatic via `prefers-color-scheme: light`
- **Reduced Motion**: Respects `prefers-reduced-motion` preference

## Component Highlights

### Headline
- Enhanced typography (36px, weight 800)
- Text shadow for depth
- Responsive alignment (left on desktop, center on mobile)

### Bio
- Card styling with elevation
- Emphasized text with accent color
- Responsive padding and alignment

### Badges
- Primary variants for top credentials
- Hover effects with accent shadows
- Optional staggered entrance animations
- Responsive touch targets

### CTA Button
- Gradient background
- Maximum elevation (shadow-xl)
- Enhanced hover state (scale + shadow)
- Keyboard accessible with clear focus indicator

## Testing

See [`../tests/validation.md`](../tests/validation.md) for:
- Performance targets (<50KB, <3s load time)
- Core Web Vitals thresholds
- Accessibility testing checklist
- Browser compatibility matrix

## Planning Documents

- [Architecture Improvements](../plans/architecture-improvements.md) - System-level enhancements
- [Frontend Design Improvements](../plans/frontend-design-improvements.md) - Visual design enhancements
- [Modular Spec Structure](../plans/modular-spec-structure.md) - Specification organization

## Related Files

- **Main Documentation**: [`../README.md`](../README.md)
- **Safety Protocols**: [`../SAFETY.md`](../SAFETY.md)
- **Source Code**: [`../src/index.html`](../src/index.html)
- **Production**: [`../docs/index.html`](../docs/index.html)
- **Archived Specs**: [`page-spec-ARCHIVED.md`](page-spec-ARCHIVED.md)

## Migration Notes

### From v1.0.0 to v2.0.0

**Breaking Changes**:
- Color values now use CSS custom properties
- Layout changes to grid system on desktop
- Typography sizes increased for better hierarchy

**New Features**:
- Light/dark mode support
- Elevation system with shadows
- Enhanced component interactions
- Responsive grid layout

**Backward Compatibility**:
- Mobile/tablet layouts remain centered
- Core content and structure unchanged
- Accessibility standards maintained

## Quick Reference

### Design Tokens
- **Colors**: `var(--color-primary)`, `var(--color-accent)`, `var(--color-text-primary)`
- **Spacing**: `var(--space-xs)` through `var(--space-2xl)` (8px - 64px)
- **Shadows**: `var(--shadow-sm)` through `var(--shadow-2xl)`

### Breakpoints
- Mobile: ≤480px
- Tablet: 481px - 768px
- Desktop (Small): 769px - 1024px
- Desktop (Large): ≥1025px

### Key Measurements
- Max width (mobile): 800px
- Max width (desktop grid): 1200px
- Bio max width (mobile): 700px
- CTA button: 300x100px (desktop), 280x90px (tablet)

## Contributing

When updating specifications:
1. Maintain cross-references between related specs
2. Update version number and changelog
3. Test changes with agent generation
4. Verify accessibility compliance
5. Document breaking changes
