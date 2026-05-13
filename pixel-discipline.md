# Pixel Discipline

Audit and fix mobile app UI/UX using clean design rules. Every element must earn its place.

## Activate When

User asks to: audit, revamp, clean up, fix spacing, fix padding, fix colors, fix typography, fix icons, apply theme, or improve any mobile screen or component.

## Step 2 — Load Relevant Rules

Read only the rule files needed for the task.

| Task | Load |
|---|---|
| Colors, theme, palette | `rules/colors.md` |
| Fonts, text, hierarchy | `rules/typography.md` |
| Spacing, padding, layout | `rules/spacing.md` |
| Cards, shadows, borders, backgrounds | `rules/surfaces.md` |
| Icons, tinting | `rules/icons.md` |
| Full revamp / audit | Load all rule files |

Always load `rules/element-audit.md` when a specific screen or component is named.

## Step 3 — Element Audit (when a screen or component is named)

Read `rules/element-audit.md` and run a full element inventory before touching any code.
For every element found: question existence, then question appearance.
Do not skip this step. Do not write code before the audit is complete.

## Step 4 — Fix and Deliver

Apply every loaded rule file. Then deliver:
1. **Element audit results** — existence verdict + appearance verdict per element
2. **Violations found** — grouped by rule
3. **Code** — fixed, production-ready, platform-specific
4. **Checklist** — confirm every loaded rule was applied
