# pixel-discipline

![version](https://img.shields.io/badge/version-1.1.0-blue)
![platforms](https://img.shields.io/badge/platforms-Flutter%20%7C%20Compose%20%7C%20SwiftUI%20%7C%20RN-green)
![license](https://img.shields.io/badge/license-MIT-brightgreen)

An AI instruction set that audits and fixes mobile app UI/UX using clean design rules.
Works with any AI coding agent that reads markdown.

**Every element must earn its place.**

> Built by [Marinos Zinonos](https://github.com/mz185)

---

## What It Does

Pixel Discipline loads only what it needs for the specified task.
It keeps token usage minimal, while it applies these five rules:

1. **Limit your color palette**: 60-30-10 rule, 3 roles max.
2. **Use fewer fonts & weights**: 2 families max, hierarchy through size and weight.
3. **Add more spacing**: 8dp grid, rewrite every spacing value, not just violations.
4. **Use borders instead of shadows**: 1px border for cards, shadows only for floating elements.
5. **No decorative background shapes**: if it has no purpose, remove it.

Plus: icon tinting hierarchy, 48dp touch targets, and safe area insets.

When a screen or component is named, it enumerates each one of its elements, questions their existence and appearance, including whether loading, empty, and error states are present, fixes what is wrong, and removes what shouldn not be there.

**Supported platforms:** Flutter · Jetpack Compose · SwiftUI · React Native
**Works with:** Claude Code · Cursor · Gemini CLI · Windsurf · Any agent that reads markdown

**Only the relevant files load per session.** e.g. a spacing fix loads one rule file. Nothing else.

---

## Install

### Claude Code

```bash
# Project-level (this project only)
mkdir -p .claude/skills/pixel-discipline
curl -L https://github.com/mz185/pixel-discipline/archive/main.tar.gz \
  | tar xz --strip=1 -C .claude/skills/pixel-discipline

# Global (all projects)
mkdir -p ~/.claude/skills/pixel-discipline
curl -L https://github.com/mz185/pixel-discipline/archive/main.tar.gz \
  | tar xz --strip=1 -C ~/.claude/skills/pixel-discipline
```

### Cursor

Add to `.cursorrules`:
```
When asked to audit, fix, or improve any mobile UI screen or component,
read and follow pixel-discipline.md and load only the relevant rule
and platform files as instructed inside it.
```
Then place the repo files alongside `.cursorrules`.

### Any Other Agent

Copy the content of `pixel-discipline.md` into your agent's system prompt
or context file.

---

## How to Trigger It

Just describe what you want naturally:

| What you type | What loads |
|---|---|
| `"Fix the spacing on this screen"` | `rules/spacing.md` |
| `"Fix icon colors throughout the app"` | `rules/icons.md` |
| `"The colors look off, fix them"` | `rules/colors.md` |
| `"Audit and revamp this screen"` | All rule files |
| `"Apply the brand theme to this card"` | `rules/colors.md` |
| `"This looks cluttered"` | `rules/spacing.md` + `rules/surfaces.md` |

---

## File Structure

```
.claude/skills/pixel-discipline/
├── README.md
├── pixel-discipline.md        ← entry point (~40 lines, always loads)
└── rules/
    ├── element-audit.md       ← enumerate, question existence, question appearance
    ├── colors.md              ← 60-30-10 palette rule
    ├── typography.md          ← fonts, weights, type scale
    ├── spacing.md             ← 8dp grid, touch targets
    ├── surfaces.md            ← borders vs shadows, no bg shapes
    └── icons.md               ← icon tinting hierarchy
```

---

## License

MIT
