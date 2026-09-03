# Typography

Typography follows Apple HIG **roles** (Large Title → Caption), implemented with Quadra faces.

**Code:** Matrix `QuadraTheme.swift` + `FontRegistration.swift` · Site `layout.tsx` (next/font) + `globals.scss`

---

## Faces

| Face | Role | Platforms |
|------|------|-----------|
| **Syne** (Bold / 700–800) | Brand display — company and product names only | macOS, web |
| **Manrope** | All operational UI and marketing body | macOS, web |
| **IBM Plex Mono** | Technical indices, HWID, code-like fields | web |
| **SF / Segoe** | Fallback and micro system glyphs | macOS / Windows |

Fallbacks on web: `"Avenir Next", "Segoe UI", sans-serif`.

---

## Brand moments (Syne)

Use Syne only when the brand or product is the signal:

- `QUADRA` / `MATRIX` wordmarks
- Sheet titles that are product moments (“Settings”, “About”) when matching MATRIX
- Marketing display headlines (`.display`, `.display-xl`)

**Tracking (native):** company `QUADRA` ~4; product `MATRIX` ~1.5–2; section labels uppercase +1.1.

**Web MATRIX hero:** product name `letter-spacing: 0.3em` in hot teal; headlines tightly tracked (−0.03 to −0.045em).

---

## Operational type (Manrope) — macOS HIG sizes

MATRIX copies default macOS `NSFont` text-style sizes into Manrope. Prefer **role**, not raw point size.

| HIG role | Approx size | Weight cue | Use |
|----------|-------------|------------|-----|
| Large Title | 26 | regular / brand | Rare display |
| Title 1 | 22 | regular / brand | Major headings |
| Title 2 | 17 | regular / brand SM | Secondary display |
| Title 3 | 15 | semibold | Settings card titles |
| Headline | 13 | **bold** | Section headers (same size as body — hierarchy is weight) |
| Body | 13 | regular / medium / semibold | Primary UI, rows, buttons |
| Callout | 12 | regular / semibold | Details, compact controls |
| Subheadline | 11 | regular | Supporting line |
| Footnote / Caption / Label | 10 | regular / semibold | Annotations, uppercase meta |
| Numeral | = body semibold + monospaced digits | dB, %, zoom |

### Do

- Pick the HIG role first (`headline` / `body` / `callout`…).
- Keep Headline and Body at the same size; emphasize with weight.
- Use numerals with monospaced digits for meters and readouts.

### Don’t

- Don’t invent a parallel “designer size scale” that disagrees with roles.
- Don’t use Syne for list rows, buttons, or form labels.
- Don’t hardcode `.system(size: N)` for UI text when a theme role exists.

---

## Web marketing scale

Utilities in `globals.scss`:

| Class | Behavior |
|-------|----------|
| `.eyebrow` | 0.8125rem, 600, uppercase, 0.08em tracking, muted |
| `.display` | Syne 700, −0.03em, line-height 1.05 |
| `.display-xl` | `clamp(2.75rem, 7vw, 5.5rem)` |
| `.display-lg` | `clamp(2.1rem, 4.5vw, 3.75rem)` |
| `.display-md` | `clamp(1.6rem, 3vw, 2.4rem)` |
| `.lede` | muted, clamp ~1.05–1.25rem, max-width 34rem |

---

## Dynamic Type and Windows text scale

Apple HIG expects text to scale with user settings. MATRIX branded fonts are currently **fixed** sizes.

**Requirement for future apps:** bind custom fonts to Dynamic Type (macOS) and system text scaling (Windows) so large accessibility sizes remain readable. See [Accessibility](accessibility.md).
