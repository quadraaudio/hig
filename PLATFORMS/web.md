# Web

The Quadra site is a light studio marketing and commerce surface. The MATRIX microsite is a dark product story. Both share tokens.

**Code:** `quadraaudio.github.io` — `tokens.scss`, `globals.scss`, `(site)` vs `(hydra)` layouts, motion components

---

## Two atmospheres, one brand

| Surface | Ground | CTAs | Motion |
|---------|--------|------|--------|
| Quadra site | snow / paper | Teal pills | Reveal, particles, typed header |
| MATRIX `/products/matrix` | ink / fascia | Text + › (hero); compact pill in chrome | Pin scrub, patch field, MatrixFade |

Remap `--theme-*` on the hydra shell so shared chrome inherits dark product semantics.

---

## Layout rules

- First viewport: brand, one headline, one lede, one CTA group, one dominant full-bleed visual
- No hero card grids, floating badges, or promo stickers on media
- Cards only when they contain interaction (store product, account session)
- Sticky nav clearance via `scroll-padding-top`

---

## Accessibility on web

- Landmarks, skip-friendly structure, `sr-only` where needed
- `prefers-reduced-motion` kills Lenis/GSAP/WebGL storytelling
- Focus-visible accent outlines on interactive tiles and search
- Dialogs: modal semantics + focus management

---

## Do

- Pull colors from CSS variables — no one-off Tailwind-ish reds for brand UI.
- Keep IBM Plex Mono for technical strings.
- Match license/trial claims to `brand.messaging.ts`.

## Don’t

- Don’t force dark mode site-wide with `prefers-color-scheme` unless product asks — today the site is intentionally light with scoped dark product pages.
- Don’t reuse MATRIX hot teal as a native app fill token.
