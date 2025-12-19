# Typography

## Font Family
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif
```

System font stack for optimal performance and native appearance across platforms.

## Enhanced Typography Scale

### Desktop (Default)

#### Headline (h1)
```css
font-size: 36px  /* Increased from 32px for better hierarchy */
font-weight: 800  /* Bolder for more impact */
letter-spacing: -0.5px  /* Tighter tracking for large text */
line-height: 1.3
color: var(--color-text-primary)  /* Brighter than body text */
text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3)  /* Subtle depth */
```

#### Bio Paragraph
```css
font-size: 18px  /* Increased from 16px for better readability */
font-weight: 400
line-height: 1.8
color: var(--color-text-secondary)
```

#### Bio Emphasized Text (strong)
```css
font-weight: 600
color: var(--color-accent)  /* Highlight key terms */
```

#### Badges
```css
font-size: 12px
font-weight: 400
color: var(--color-text-secondary)
```

#### CTA Button
```css
font-size: 18px
font-weight: 600
color: var(--color-primary)
```

### Tablet (≤768px)

#### Headline
```css
font-size: 28px  /* Increased from 26px */
font-weight: 800
letter-spacing: -0.3px
line-height: 1.3
```

#### Bio
```css
font-size: 16px  /* Increased from 14px */
font-weight: 400
line-height: 1.8
```

#### Badges
```css
font-size: 13px  /* Slightly larger for better touch targets */
font-weight: 400
```

#### CTA Button
```css
font-size: 18px  /* Consistent across breakpoints */
font-weight: 600
```

### Mobile (≤480px)

Same as tablet, with additional touch target optimizations in spacing.

## Line Heights

```css
--line-height-tight: 1.3  /* Headlines */
--line-height-normal: 1.6  /* Default */
--line-height-relaxed: 1.8  /* Body text, bio */
```

## Text Alignment

### Desktop (≥1025px)
```css
h1: text-align: left  /* Left-aligned in grid layout */
.bio: text-align: left  /* Better readability for long text */
.badges-container: justify-content: flex-start
.cta-container: justify-content: center
```

### Tablet and Mobile (≤1024px)
```css
h1: text-align: center
.bio: text-align: center
.badges-container: justify-content: center
.cta-container: justify-content: center
```

## Typography Hierarchy

### Visual Weight Distribution
1. **Headline (h1)**: Heaviest weight (800), largest size (36px), brightest color
2. **Bio Emphasized**: Medium weight (600), accent color for key terms
3. **Bio Text**: Regular weight (400), secondary color
4. **Badges**: Small size (12px), secondary color
5. **CTA Button**: Semi-bold (600), high contrast

### Content Emphasis

**In Bio Paragraph**, emphasize key expertise areas:
```html
<p class="bio">
    I specialize in <strong>FinOps</strong>,
    <strong>Enterprise AI adoption and governance</strong>,
    and <strong>Cloud strategy</strong>.
</p>
```

This creates visual hierarchy and draws attention to core competencies.

## Accessibility

### Minimum Font Sizes
- Body text: 16px minimum (18px on desktop)
- Small text (badges): 12px minimum
- All text maintains 4.5:1 contrast ratio

### Responsive Scaling
Font sizes scale proportionally across breakpoints to maintain readability without requiring zoom on mobile devices.

### Text Shadow Accessibility
Text shadows are subtle (0 2px 4px) and do not interfere with readability or contrast ratios.
