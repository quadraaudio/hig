# Pointer

Pointer input (mouse, trackpad, pen) should feel precise and reversible.

**Code:** Matrix patch hover/selection, fader dragging, pinch zoom · Site hover states, Lenis wheel

---

## Behaviors

- Hover affordances: accent wash / rim on cells and chips; web buttons lift slightly
- Click / tap commits; drag on faders updates continuously with accessible value changes
- Pinch or ⌘-scroll zoom on patch grid (MATRIX zooms out to a minimum cell size; document limits in UI)
- Cursor guides on patch row/column hover clarify targets

---

## Do

- Keep hit targets ≥ control height tokens (28–36 native).
- Show hover without relying on color alone when possible (stroke weight, selection ring).
- Cancel drags cleanly on Escape where platform patterns expect it.

## Don’t

- Don’t require hover to reveal the only path to a critical action (touch / keyboard users lose it).
- Don’t attach huge tooltips that fight the pointer on dense grids — prefer fixed inspector panes.
