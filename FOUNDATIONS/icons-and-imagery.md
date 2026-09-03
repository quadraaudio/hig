# Icons and imagery

**Code:** Matrix `BrandMark.swift`, AppIcon, menu bar assets · Site `LogoMark`, `public/icon.svg`, `public/matrix/*`, hydra media

---

## Brand marks

| Surface | Mark |
|---------|------|
| In-app chrome / About | Teal waveform (“M” wave) + Syne product wordmark |
| Menu bar / OS template | Company **Q** (template image) — not the wave |
| Web favicon / app icon plate | Snow plate + ink **Q** (`#FBFCFD` / `#0E1218`) |
| MATRIX app icon | Dark squircle + teal waveform |

**Rules:**

- Never show the company Q as the in-window product lockup.
- Never rename the product UI to forbidden names (Hydra, Matrice, etc.) — see [Writing](writing.md).
- Prefer flat, minimal marks — no bevels or purple gradients.

---

## System symbols

On macOS, SF Symbols are appropriate for tool actions (refresh, info, speakers) at theme micro sizes. Tint with primary/secondary/accent semantics — not multicolor rainbow glyphs.

On Windows, use Segoe Fluent Icons or WinUI symbol fonts with the same restraint: one weight, accent only for selected/active.

---

## Product imagery

### Web / marketing

- Heroes are **full-bleed** visual planes (photo or live field), not inset rounded media cards.
- MATRIX chapters: the scene *is* the section — WebGL or static chapter art behind type with an ink veil for legibility.
- No floating promo stickers or badge clusters on hero media.

### App window captures

- Show real chrome (traffic lights, teal controls, patch grid) for honesty.
- Prefer dark fascia screenshots for MATRIX product truth; light site screenshots for Quadra marketing.

---

## Decorative layers

Particles, atmospheres, grid drifts, and canvas effects are decorative:

- Mark `aria-hidden` / `.accessibilityHidden`
- Provide static fallbacks when motion or WebGL is unavailable

---

## Do / Don’t

### Do

- Keep icons optically aligned to text caps height.
- Use waveform / Q marks consistently per surface table above.

### Don’t

- Don’t invent a second illustrative mascot style.
- Don’t place emoji in product chrome.
- Don’t overlay detached labels or chips on hero media.
