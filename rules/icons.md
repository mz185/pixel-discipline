# Icons

## Tint Hierarchy

| Icon role | Tint token | Size |
|---|---|---|
| Interactive (button, nav, action) | `primary` | 24dp |
| Decorative / informational | `onSurfaceVar` | 20dp |
| On primary background | `onPrimary` | 24dp |
| Disabled | `onSurfaceVar` at 38% opacity | 24dp |
| Destructive action | `error` | 24dp |
| Success / confirmation | `success` or green semantic token | 24dp |

Never use a freeform color for an icon. Always map to a semantic token.

## Style Consistency

Pick one icon style per app and never mix:
- **Outlined** — professional, clean
- **Filled** — warm, bold, consumer
- **Sharp** — efficient, dense
- **Rounded** — friendly, playful

Mixing styles (e.g. some outlined, some filled) is a violation.

## Size Rules

- Navigation bar icons: 24dp
- App bar trailing icons: 24dp
- Inline / decorative icons: 20dp
- FAB icon: 24dp
- Icon inside a filled button: 18dp, 4dp gap to label
- Never scale icons to odd values (17dp, 22dp, 25dp)

## Violations

- Hard-coded color on an icon (e.g. `color: '#FF5722'`)
- Mixing outlined and filled icons in the same app
- Icon size not on the allowed scale (20 / 24dp)
- Interactive icon using `onSurfaceVar` tint (looks inactive)
- Decorative icon using `primary` tint (looks interactive)

## Checklist

- [ ] All icons use semantic token tints
- [ ] Single icon style throughout
- [ ] Interactive icons: `primary`, 24dp
- [ ] Decorative icons: `onSurfaceVar`, 20dp
- [ ] No hard-coded colors on icons
