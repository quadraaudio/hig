# Modality

Use modality sparingly. Prefer sheets and dialogs for focused tasks that interrupt the session briefly.

**Code:** Matrix Settings / About / Monitor sheets · Site `TermsAcceptModal` and checkout flows

---

## When to use a modal / sheet

- Account and licensing decisions
- Settings that apply globally
- Confirming destructive actions (clear routes, overwrite scene, clear license)
- Legal acceptance that must complete before continuing

## When not to

- Frequent monitor tweaks that belong in a persistent bay
- Teaching copy (use popover / help)
- Multi-step browsing that deserves a full page

---

## Behavior

### Do

- Title the sheet with Syne/brand or clear Manrope title.
- Provide an obvious dismiss (Done / Close) as ghost or secondary.
- Use platform confirmation dialogs for destructive commits.
- On web: `role="dialog"`, `aria-modal="true"`, `aria-labelledby`, focus the dialog, restore focus on close; stop smooth-scroll traps while open.

### Don’t

- Don’t stack multiple modals.
- Don’t use modality to paper over unclear navigation.
- Don’t allow background interaction while a blocking legal/terms dialog is open.
