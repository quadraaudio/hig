# Layout

Layout creates calm studio hierarchy: consistent spacing, continuous corners, and one job per region.

**Code:** Matrix `QuadraTheme` spacing/radii · Site `tokens.scss` + `.page-shell`

---

## Spacing

### Native (core scale)

| Token | pt |
|-------|-----|
| `spaceXS` | 8 |
| `spaceSM` | 12 |
| `spaceMD` | 16 |
| `spaceLG` | 24 |

Ad-hoc gaps used in dense chrome: 4, 6, 10. Prefer tokens when adding new layout.

### Web (extended scale)

| Token | px |
|-------|-----|
| `--space-2xs` … `--space-6xl` | 4, 8, 12, 16, 24, 32, 48, 72, 96, 128, 180 |
| `--page-margin` | `clamp(20px, 5vw, 72px)` |
| `--page-max` | 1240px |

`.page-shell`: `width: min(100% - 2×margin, 1240px)`, centered.

---

## Radii

| Token | Value | Use |
|-------|-------|-----|
| `radiusSM` | 10 | Fields, small surfaces, patch cells (clamped) |
| `radiusMD` | 16 | Cards, bays, empty pads |
| `radiusLG` | 28 | Large panels, activation card, product cards |
| Pill / capsule | 999 / capsule | Buttons, chips, arms, fader tracks |

**Don’t** invent a fourth radius scale.

---

## Control metrics (native)

| Token | pt |
|-------|-----|
| Default control height | 36 |
| Compact control height | 28 |
| Horizontal pad | 14 (compact 10) |
| Disabled opacity | ~0.45–0.55 |

Web primary buttons: min-height **48px**, pill shape.

---

## Window and page regions

### MATRIX (reference)

- Main window min ~1000×600; default ~1320×860
- Sidebar column ~220–300 wide
- Bottom bays ~148 tall
- One composition per region: sidebar list, patch field, monitor bay, inspector — not a dashboard of competing cards

### Web

- Sticky Quadra nav 64px; MATRIX chrome 48px after hero swap
- First viewport: brand, one headline, one lede, one CTA group, one dominant visual
- No card clutter in heroes; cards only when they contain a real interaction (store, account)

---

## Rules

### Do

- Align gutters — native `spaceLG` insets match across TopBar, grid, and Monitor.
- Use hairline dividers (1pt) at reduced opacity rather than heavy rules.
- Keep scroll padding clear of sticky chrome on web.

### Don’t

- Don’t pack stats, promos, and secondary marketing into the first viewport.
- Don’t nest cards inside cards for decoration.
- Don’t break the spacing scale for one-off “tighter” screens without updating the theme.
