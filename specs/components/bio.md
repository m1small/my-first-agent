# Bio Component

## Content Requirements

### Tone
Confident, results-focused, transformational

### Length
~150 words

### Key Themes
- "Catalyst" for systemic and cultural change
- 15+ years experience
- Fortune 500 and startups
- Core expertise: FinOps, Enterprise AI adoption and governance, Cloud strategy

## HTML Structure

```html
<p class="bio">
    I'm a catalyst for systemic and cultural change, driving transformation
    that improves companies from the inside out. With over 15 years of
    experience spanning Fortune 500 enterprises and innovative startups,
    I specialize in <strong>FinOps</strong>, <strong>Enterprise AI adoption
    and governance</strong>, and <strong>Cloud strategy</strong>. My approach
    focuses on delivering measurable results through strategic alignment,
    operational excellence, and cultural transformation. Whether you're
    optimizing cloud costs, implementing AI governance frameworks, or
    architecting scalable cloud solutions, I bring proven expertise and a
    results-focused methodology. Let's work together to unlock your
    organization's full potential and drive sustainable, transformational
    change that delivers real business impact.
</p>
```

## Typography

### Desktop (Default)
```css
font-size: 18px  /* Enhanced from 16px */
font-weight: 400
line-height: 1.8
color: var(--color-text-secondary)
```

### Tablet (≤768px)
```css
font-size: 16px  /* Enhanced from 14px */
font-weight: 400
line-height: 1.8
```

### Emphasized Text (strong tags)
```css
font-weight: 600
color: var(--color-accent)  /* Gold highlight for key expertise */
```

## Card Styling (Enhanced)

### Background & Elevation
```css
background: var(--color-surface)
box-shadow: var(--shadow-md)
border-radius: 16px
```

### Padding

**Desktop**:
```css
padding: var(--space-lg)  /* 32px */
```

**Tablet/Mobile**:
```css
padding: var(--space-md)  /* 24px */
```

### Spacing
```css
margin-bottom: var(--space-sm)  /* 16px */
```

### Max Width

**Desktop Grid (≥1025px)**:
```css
max-width: 100%  /* Full width in grid area */
```

**Tablet/Mobile (≤1024px)**:
```css
max-width: 700px
margin-left: auto
margin-right: auto
```

## Responsive Alignment

### All Breakpoints
```css
text-align: center  /* Centered at all screen sizes */
max-width: 700px  /* Optimal reading length */
margin-left: auto
margin-right: auto
```

## Content Emphasis

Use `<strong>` tags to highlight key expertise areas:
- **FinOps**
- **Enterprise AI adoption and governance**
- **Cloud strategy**

This creates visual hierarchy and draws attention to core competencies using the accent color.

## Accessibility

### Semantic HTML
- Use `<p>` element with `.bio` class
- Use `<strong>` for emphasis (not just visual styling)

### Readability
- Line height: 1.8 (optimal for body text)
- Max width: 700px on mobile (optimal reading length: 50-75 characters per line)
- Font size: 18px desktop, 16px mobile (meets WCAG minimum)

### Color Contrast
- Body text: 4.5:1 minimum ✅
- Emphasized text (accent): 7.2:1 ✅

## Design Tokens Used

- `--color-surface`: Card background
- `--color-text-secondary`: Body text color
- `--color-accent`: Emphasized text color
- `--shadow-md`: Card elevation
- `--space-lg`: Desktop padding
- `--space-md`: Mobile padding
- `--space-sm`: Bottom margin

## Related Specifications

- [typography.md](../design-system/typography.md) - Font specifications
- [colors.md](../design-system/colors.md) - Color tokens
- [spacing.md](../design-system/spacing.md) - Spacing and padding
- [elevation.md](../design-system/elevation.md) - Shadow system
