# Surfaces

## The Rule: Border XOR Shadow — Never Both

A surface communicates elevation through either a border or a shadow. Never both.

- **Border** → flat, same-level surfaces (cards on white bg, inputs, outlined buttons)
- **Shadow** → elevated surfaces (FAB, modals, bottom sheets, elevated cards)
- **Neither** → surface color alone provides enough separation (filled cards, colored containers)

## Card Rules

- Border: 1dp, `outline` token color, radius per brand profile
- No shadow on flat cards
- Background: `surface` token (never raw white unless `surface` = white in your theme)
- Inner padding: 16dp minimum, 24dp preferred

## Radius Scale

```
none  =  0dp   — data tables, full-width banners
sm    =  4dp   — chips, badges, small tags
md    =  8dp   — buttons, input fields
lg    = 12dp   — cards, containers
xl    = 16dp   — bottom sheets, large cards
pill  = 9999dp — FAB, avatar, toggle chips
```

Use one radius value per component type. Never mix radii on the same component.

## Background Shapes — Banned

Do not place colored/filled background shapes behind UI elements for decoration.
No blobs, no gradient circles, no decorative panels. If content needs separation, use a surface token.

## Violations

- Card has both a border and a shadow
- Drop shadow on a flat list item
- Multiple different radius values on sibling cards
- Decorative colored shapes behind content
- Card background is hard-coded white instead of `surface` token
- Input field has a shadow

## Checklist

- [ ] Border OR shadow, never both
- [ ] Consistent radius per component type
- [ ] Card background uses `surface` token
- [ ] No decorative background shapes
- [ ] Modals / bottom sheets use shadow only
