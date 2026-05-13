# Element Audit

When a screen or component is named, enumerate every element present.
For each element: ask if it should exist, then ask if it looks correct.
Never skip an element. Never write code before this audit is complete.

## Phase 1 — Inventory

Scan the code or description top to bottom. List every element found:

- Status bar / top bar / navigation bar
- App bar / toolbar (title, leading icon, trailing icons)
- Tab bar / bottom navigation
- Header sections (hero, page title, section labels)
- Search bar / filter bar
- Cards (each card type separately)
- List items / rows
- Buttons (primary, secondary, text, icon buttons — each separately)
- Input fields (each field separately)
- Labels / captions / helper text
- Images / avatars / thumbnails
- Icons (each icon separately)
- Dividers / separators
- Empty states / placeholders
- Loading indicators
- Badges / chips / tags
- Modals / bottom sheets / dialogs
- FAB (floating action button)
- Snackbars / toasts
- Progress indicators
- Any decorative shapes or background elements

## Phase 2 — Existence Check

For each element in the inventory, ask:

1. **Does it belong on this screen?** — Does it serve the user's primary task here?
2. **Is it duplicating another element?** — Is this information already shown elsewhere?
3. **Is it premature?** — Is it showing an action or state that isn't relevant yet?
4. **Is it decorative only?** — Purely decorative elements with no function → remove.

Verdict per element: `KEEP` / `REMOVE` / `QUESTION` (flag for human decision)

## Phase 3 — Appearance Check

For each element marked `KEEP`, ask:

| Property | Question |
|---|---|
| Size | Is it the right size for its importance on this screen? |
| Spacing | Does it have correct padding/margin per the 8dp grid? |
| Color | Does it follow the 60-30-10 rule and brand profile? |
| Typography | Correct weight, size, and hierarchy for its role? |
| Icon | Right tint, right size (24dp interactive / 20dp decorative)? |
| Alignment | Properly aligned to grid and sibling elements? |
| Contrast | Does it meet minimum contrast ratio for its use (text vs bg)? |
| State | Does it handle empty, loading, disabled, error states? |
| Touch target | Interactive elements ≥ 48dp tall? |

Verdict per element: `PASS` / `FIX` (describe what to fix)

## Output Format

```
ELEMENT AUDIT — [Screen Name]

1. [Element name]
   Existence: KEEP — [reason]
   Appearance: FIX — [specific issue]

2. [Element name]
   Existence: REMOVE — [reason]
   Appearance: N/A

3. [Element name]
   Existence: KEEP
   Appearance: PASS
```

After the audit, proceed to fix all `FIX` items and remove all `REMOVE` elements.
