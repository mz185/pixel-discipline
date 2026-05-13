# Spacing

## The Rule: 8dp Grid

Every spacing value must be a multiple of 8dp.
Allowed: 4, 8, 12, 16, 24, 32, 40, 48, 64
Never use: 5, 6, 7, 9, 10, 11, 13, 15, 17, 18, 20, 22, 25, 28, 30, etc.

4dp is allowed only for micro-spacing (icon-to-label gap, badge offset).

## Standard Values

```
xs   =  4dp   — icon-to-label gap, badge offset
sm   =  8dp   — tight grouping within a component
md   = 16dp   — standard inner padding (cards, list items)
lg   = 24dp   — section spacing, generous card padding
xl   = 32dp   — between major sections
xxl  = 48dp   — top/bottom page breathing room
```

## Touch Targets

- Every tappable element: minimum 48dp height
- Icon buttons: 48×48dp minimum (icon inside can be 24dp)
- Bottom navigation items: 56dp height minimum
- FAB: 56dp diameter (mini: 40dp)

## Screen Padding

- Horizontal screen edge padding: 16dp minimum, 24dp preferred
- Never let content touch the screen edge
- Safe area insets: always respect top (status bar) and bottom (home indicator / nav bar)

## Violations

- Any spacing value not on the 8dp grid
- Interactive element under 48dp tall
- Content touching screen edge (0 horizontal padding)
- Inconsistent padding between sibling components (e.g. one card has 16dp, another has 20dp)
- Ignoring safe area insets

## Checklist

- [ ] All spacing values on 8dp grid
- [ ] All interactive elements ≥ 48dp tall
- [ ] Horizontal screen padding ≥ 16dp
- [ ] Safe area insets respected
- [ ] Sibling components have identical padding
