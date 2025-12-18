# Specifications

Modular specifications for Matt Small's landing page, optimized for implementation.

## Structure

```
specs/
├── project.md              # Project overview
├── design-system/          # Design tokens
│   ├── colors.md          # Color values
│   ├── typography.md      # Font specifications
│   └── spacing.md         # Spacing and layout
├── components/             # Component specs
│   ├── headline.md        # Headline
│   ├── bio.md            # Biography
│   ├── badges.md         # Badges list
│   └── cta-button.md     # CTA button
├── layouts/               # Page layout
│   └── landing-page.md   # HTML structure
└── requirements/          # Requirements
    ├── technical.md      # Technical constraints
    └── accessibility.md  # Accessibility standards
```

## Implementation Order

1. Read [`project.md`](project.md) for context
2. Read [`layouts/landing-page.md`](layouts/landing-page.md) for HTML structure
3. Read [`design-system/`](design-system/) for design tokens
4. Read [`components/`](components/) for each component
5. Read [`requirements/`](requirements/) for constraints

## Testing

See [`../tests/validation.md`](../tests/validation.md) for performance targets, testing checklist, and validation criteria.

## Related

- Main: [`../README.md`](../README.md)
- Safety: [`../SAFETY.md`](../SAFETY.md)
- Source: [`../src/index.html`](../src/index.html)
- Production: [`../docs/index.html`](../docs/index.html)
- Archived: [`page-spec-ARCHIVED.md`](page-spec-ARCHIVED.md)
