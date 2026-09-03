# Feedback

Feedback tells people what happened — visually, textually, and for assistive technologies.

**Code:** Matrix status LEDs, meters, confirmation dialogs · Site `role="status"` / `role="alert"` notices

---

## Levels

| Level | Use | Examples |
|-------|-----|----------|
| Silent visual | Continuous state | Signal rails, selection highlight, chip selected fill |
| Soft notice | Non-blocking info | Trial banner, “promo applied” |
| Alert | Error / must act | PayPal failure, validation errors |
| Confirmation | Destructive commit | Clear all routes, overwrite scene |

---

## Do

- Pair color with text or value (see [Accessibility](../FOUNDATIONS/accessibility.md)).
- Announce errors with `role="alert"` (web) or equivalent native announcement.
- Keep success notices dismissible or auto-clear without stealing focus unnecessarily.
- Use danger styling only for destructive or critical latched states.

## Don’t

- Don’t flash the entire window for routine patch changes.
- Don’t rely on toast spam for every toggle.
- Don’t leave failed checkouts without an alert role.
