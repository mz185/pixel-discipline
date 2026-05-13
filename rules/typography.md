# Typography

## Type Scale (Material 3 / standard mobile)

| Role | Size | Weight | Use |
|---|---|---|---|
| displayLarge | 57sp | Regular | Hero text only |
| headlineMedium | 28sp | SemiBold | Page titles |
| titleLarge | 22sp | SemiBold | Card titles, section headers |
| titleMedium | 16sp | Medium | List item primary text |
| bodyLarge | 16sp | Regular | Body copy |
| bodyMedium | 14sp | Regular | Secondary body, descriptions |
| labelLarge | 14sp | Medium | Buttons |
| labelSmall | 11sp | Medium | Captions, badges, chips |

Never use more than 3 distinct sizes on one screen.

## Rules

- One font family only. Two maximum (heading + body) if brand requires it.
- Never use Regular weight for interactive elements (buttons, links) — use Medium or SemiBold.
- Never use SemiBold or Bold for body copy — use Regular or Medium only.
- Line height: 1.4–1.5× font size for body, 1.1–1.2× for headings.
- Letter spacing: 0 for body, +0.5–1px for ALL CAPS labels only.
- No ALL CAPS except short labels (≤ 3 words, labelSmall role).

## Violations

- More than 3 font sizes on a single screen
- Using font weight as the only differentiator between hierarchy levels (also vary size)
- Body text smaller than 14sp
- Button label not Medium or SemiBold weight
- Line height less than 1.4× for paragraph text

## Checklist

- [ ] Max 3 font sizes per screen
- [ ] Clear hierarchy: title > body > caption (size AND weight)
- [ ] Buttons use labelLarge (14sp Medium)
- [ ] No body text under 14sp
- [ ] Single font family (two max)
