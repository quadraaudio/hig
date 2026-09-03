# Quadra Human Interface Guidelines

Design system and interaction principles for every Quadra surface — native apps, the marketing site, and future Windows software.

These guidelines follow the structure and software-design principles of Apple’s Human Interface Guidelines (Foundations, Patterns, Components, Inputs, Platforms), with **accessibility as a first-class foundation**. Visual tokens and control catalogs are taken from shipping code in [Matrix](https://github.com/quadraaudio/Matrix) and [quadraaudio.github.io](https://github.com/quadraaudio/quadraaudio.github.io) — not invented here.

**Language:** English (canonical).

---

## Principles

Apple’s core principles, adapted for Quadra studio software:

| Principle | Quadra meaning |
|-----------|----------------|
| **Clarity** | One job per region. Text is legible. Interactive chrome uses electric teal (`#00A3A0`), never system blue or purple. Controls look like controls. |
| **Deference** | Content first. Chrome, glass, and motion support the session — they never compete with the patch field, meters, or product story. |
| **Depth** | Hierarchy through surfaces (snow / paper / fascia), continuous radii (10 / 16 / 28), and restrained motion — not stacked cards or glow clutter. |

Additional Quadra rules:

1. **Studio instrument, not SaaS dashboard.** Prefer one composition per viewport or window region.
2. **Compose, don’t restyle.** Use the control catalog and theme API; do not invent a fifth button style or a local hex.
3. **Brand type only for brand moments.** Syne for product/company names; Manrope for all operational UI.
4. **Respect people.** Accessibility settings (Reduce Motion, contrast, text size, assistive tech) are requirements, not polish.

---

## How to use this HIG

1. Read **[Foundations → Accessibility](FOUNDATIONS/accessibility.md)** before shipping any new surface.
2. Pull colors, type, space, and motion from **[references/tokens.md](references/tokens.md)**.
3. Build UI from **[Components](COMPONENTS/buttons.md)** and **[Patterns](PATTERNS/navigation.md)**.
4. Apply platform notes in **[Platforms](PLATFORMS/macos.md)** (macOS, web, Windows).

MATRIX app implementation details live in Matrix `Docs/Product/DESIGN_SYSTEM.md`. That document is the macOS product playbook; **this repository is the org-wide SSOT**.

---

## Contents

### Foundations

- [Accessibility](FOUNDATIONS/accessibility.md)
- [Color](FOUNDATIONS/color.md)
- [Typography](FOUNDATIONS/typography.md)
- [Layout](FOUNDATIONS/layout.md)
- [Materials](FOUNDATIONS/materials.md)
- [Motion](FOUNDATIONS/motion.md)
- [Icons and imagery](FOUNDATIONS/icons-and-imagery.md)
- [Writing](FOUNDATIONS/writing.md)

### Patterns

- [Navigation](PATTERNS/navigation.md)
- [Modality](PATTERNS/modality.md)
- [Feedback](PATTERNS/feedback.md)
- [Settings](PATTERNS/settings.md)
- [Onboarding and activation](PATTERNS/onboarding-activation.md)

### Components

- [Buttons](COMPONENTS/buttons.md)
- [Chips and segments](COMPONENTS/chips-and-segments.md)
- [Toggles and arms](COMPONENTS/toggles-and-arms.md)
- [Faders and meters](COMPONENTS/faders-and-meters.md)
- [Inputs](COMPONENTS/inputs.md)
- [Panels and chrome](COMPONENTS/panels-and-chrome.md)

### Inputs

- [Keyboard](INPUTS/keyboard.md)
- [Pointer](INPUTS/pointer.md)

### Platforms

- [macOS](PLATFORMS/macos.md)
- [Web](PLATFORMS/web.md)
- [Windows](PLATFORMS/windows.md)

### References

- [Design tokens](references/tokens.md)
- [Code sources](references/sources.md)

---

## Source of truth

| Concern | Canonical code |
|---------|----------------|
| Web tokens | `quadraaudio.github.io` → `src/styles/tokens.scss` |
| Native tokens | `Matrix` → `Colors.xcassets` + `QuadraTheme.swift` |
| Brand constants | `Matrix` → `Shared/QuadraCore/.../QuadraBrand.swift` |
| Marketing voice | `quadraaudio.github.io` → `src/data/brand.messaging.ts` |

Accent is frozen: **`#00A3A0`** / deep **`#007E7C`**. Same in light and dark.
