# Code sources

Evidence base for this HIG. Audited from public repositories (not secondary marketing PDFs).

---

## Repositories

| Repo | Role |
|------|------|
| [quadraaudio/hig](https://github.com/quadraaudio/hig) | This guidelines SSOT |
| [quadraaudio/Matrix](https://github.com/quadraaudio/Matrix) | Native macOS app + engine |
| [quadraaudio/quadraaudio.github.io](https://github.com/quadraaudio/quadraaudio.github.io) | Marketing site, store, MATRIX microsite |

Live site: [https://quadraaudio.com](https://quadraaudio.com)

---

## Matrix (native) paths

| Path | Why it matters |
|------|----------------|
| `Apps/QuadraMatrix/Sources/QuadraMatrix/Resources/Colors.xcassets/` | Color Sets SSOT |
| `Apps/QuadraMatrix/Sources/QuadraMatrix/Theme/QuadraTheme.swift` | Type roles, space, radii, semantic colors, motion |
| `Apps/QuadraMatrix/Sources/QuadraMatrix/Theme/FontRegistration.swift` | Syne / Manrope registration |
| `Apps/QuadraMatrix/Sources/QuadraMatrix/Controls/` | Button, chip, arm, fader, pad catalog |
| `Apps/QuadraMatrix/.../LiquidGlass.swift` | Panel / bay materials |
| `Shared/QuadraCore/Sources/QuadraCore/QuadraBrand.swift` | Brand strings + accent hex |
| `Docs/Product/DESIGN_SYSTEM.md` | App-local implementation playbook |

---

## Website paths

| Path | Why it matters |
|------|----------------|
| `src/styles/tokens.scss` | CSS token SSOT |
| `src/app/globals.scss` | Buttons, type utilities, reduced motion |
| `src/app/layout.tsx` | Font loading (Syne, Manrope, IBM Plex Mono) |
| `src/app/(hydra)/` | MATRIX microsite shell |
| `src/components/hydra/` | Hero, chrome, chapters |
| `src/components/chrome/` | GlobalNav, LogoMark, home |
| `src/components/motion/` | Reveal, MatrixFade, SmoothScroll |
| `src/components/three/` | PatchbayField, chapter visuals |
| `src/data/brand.messaging.ts` | Marketing voice / CTAs |
| `public/matrix/matrix-app-window.png` | Native UI reference capture |
| `public/matrix/brand-mark.png` | App icon style reference |

---

## Relationship to Matrix DESIGN_SYSTEM.md

`Docs/Product/DESIGN_SYSTEM.md` in Matrix describes **how the macOS app composes UI** (layers, checklist, control catalog).  
**This repository** defines **org-wide Human Interface Guidelines** across macOS, web, and future Windows — including accessibility requirements that outrank any single app shortcut.

When they diverge, update both: change tokens in code first, then sync `references/tokens.md` and the Matrix design-system doc.
