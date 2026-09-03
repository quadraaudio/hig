# Inputs

Text and value entry should look like Quadra surfaces and behave like platform fields.

**Code:** Matrix text fields in Settings/Account · Site support search, checkout promo, HWID fields

---

## Visual

- Radius `radiusSM` (10) or pill for search
- Light: snow/paper fills, line border
- Dark: fascia raised fills, fasciaLine border
- Focus: accent border and/or **2px accent outline** with offset (required on web)

## Behavior

- Labels visible (or `aria-label` when icon-only search)
- Errors adjacent with `role="alert"`
- Mono font for technical strings (HWID, keys) on web

---

## Do

- Keep hit targets comfortable (≥28–36 native; 48 web primary).
- Preserve paste and password-manager behavior on auth fields.

## Don’t

- Don’t remove focus outlines without a visible replacement.
- Don’t style fields like inert cards.
