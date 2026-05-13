# Colors

## The Rule: 60-30-10

- **60%** background / surface (neutral, low contrast)
- **30%** secondary surface / container (slightly elevated)
- **10%** accent / primary action (brand color, used sparingly)

Never use more than 3 named colors in one screen. Every additional color is a violation.

## Required Tokens

```
background       — page/scaffold background
surface          — card, sheet, dialog background
surfaceVariant   — input fill, chip background, subtle containers
onSurface        — primary text on surface
onSurfaceVar     — secondary text, placeholders, captions
primary          — CTA buttons, active states, links
onPrimary        — text/icons on primary color
outline          — borders, dividers
error            — destructive actions, validation errors
```

## Violations

- More than one accent color active on the same screen
- Using `primary` for decorative elements (it must always signal action)
- `onSurface` text placed directly on `background` without a surface container
- Hard-coded hex values instead of tokens
- Pure black (#000) for text — use `onSurface` (e.g. #1C1B1F or equivalent)
- Using opacity hacks instead of proper semantic tokens

## Checklist

- [ ] Exactly one accent/primary color in use
- [ ] Text always on correct surface token (not raw background)
- [ ] No hard-coded colors in component code
- [ ] Error color used only for actual errors
- [ ] Disabled states use `onSurfaceVar` at reduced opacity, not a new color
