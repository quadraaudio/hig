# Buttons

Buttons are the primary affordance for actions. Native apps use the Quadra pill catalog; the marketing site uses pill CTAs; MATRIX storytelling heroes prefer text links.

**Code:** Matrix `QuadraButton` / `QuadraPillChrome` · Site `.btn` / `.btn-primary` in `globals.scss`

---

## Roles (native)

| Role | Style | Visual |
|------|-------|--------|
| Primary / selected | `.primary` | Solid accent + soft teal shadow; label `onAccent` |
| Secondary / idle | `.secondary` | Glass + accent wash + teal rim; secondary text |
| Danger (on) | `.danger` | Solid danger; white label |
| Ghost | `.ghost` | Accent text only — tertiary (Done beside chrome) |

Heights: **36** default, **28** compact. Manrope semibold.

## Web marketing

| Class | Visual |
|-------|--------|
| `.btn-primary` | Teal fill, white text, hover accentDeep |
| `.btn-secondary` | Transparent + border → ink on hover |
| `.btn-inverse` | Inverse on ink bands |
| `.btn-ghost` | No border |

Min-height **48px**, pill radius, hover `translateY(-1px)`.

## MATRIX microsite heroes

Text CTAs with `›` suffix (teal → hot on hover) — not pills — so the full-bleed composition stays calm. Compact pill allowed in the 48px product chrome (“Buy MATRIX”).

---

## Do

- Use primary for the single most important action in a region.
- Keep destructive actions visually danger when latched or confirming.
- Include `.accessibilityAddTraits(.isButton)` / native button semantics.

## Don’t

- Don’t ship borderless accent `Text` as a lone primary action in native apps.
- Don’t use `.borderedProminent` system blue for MATRIX chrome.
- Don’t invent a fifth pill style.
