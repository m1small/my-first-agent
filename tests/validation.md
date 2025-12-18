# Validation & Testing

## Performance Targets
load-time-3g: <3s
load-time-4g: <1s
file-size: <50KB
time-to-interactive: <2s

## Core Web Vitals
lcp: <2.5s (Largest Contentful Paint)
fid: <100ms (First Input Delay)
cls: <0.1 (Cumulative Layout Shift)
fcp: <1.5s (First Contentful Paint)

## Lighthouse Scores
performance: 100/100
accessibility: 100/100
best-practices: 100/100
seo: 100/100

## Color Contrast (WCAG AA: 4.5:1 minimum)
text-on-primary: 5.8:1 ✅
primary-on-accent: 7.2:1 ✅

## Browser Testing
chrome: Latest 2 versions
firefox: Latest 2 versions
safari: Latest 2 versions
edge: Latest 2 versions

## Screen Sizes
desktop: 1920px, 1440px, 1280px
tablet: 1024px, 768px
mobile: 414px, 375px

## Accessibility Testing Tools
- WAVE browser extension
- axe DevTools
- Lighthouse
- Screen readers (NVDA, JAWS, VoiceOver, TalkBack)

## Manual Testing Checklist
- [ ] Visual inspection on all target browsers
- [ ] Responsive design at all breakpoints
- [ ] CTA button hover, focus, active states
- [ ] Mailto link opens email client correctly
- [ ] Keyboard navigation (Tab, Enter, Space)
- [ ] Screen reader announces content correctly
- [ ] Color contrast meets WCAG AA
- [ ] No horizontal scrolling at any breakpoint
- [ ] Reduced motion preference respected
