# Onboarding and activation

First-run and licensing flows must be clearer than the rest of the product — people are not in a session yet.

**Code:** Matrix activation card / Quadra Guard flows · Site `/activate`, `/login`, TermsAcceptModal · `brand.messaging.ts`

---

## Messaging

Lead with outcomes:

- 14-day full trial
- Perpetual license
- Seats / Mac activation as specified in product copy
- Offline work after authorization (Quadra Guard)

Avoid dumping HAL/engine jargon before the person knows what MATRIX is.

---

## Structure

1. Brand mark + product name
2. One sentence value
3. Primary CTA (Start free trial / Sign in / Activate)
4. Secondary path (Buy, Support)
5. Legal acceptance when required (scroll + accept)

Use `radiusLG` activation surfaces, accent primary button, hairline card — not a dashboard.

---

## Do

- Keep the path linear.
- Surface HWID / offline key tools in Account after identity exists.
- Announce status (“Signed in”, “Trial started”) to assistive tech.

## Don’t

- Don’t force a tour overlay that blocks the patch field on every launch.
- Don’t hide pricing honesty — match store and marketing license terms.
