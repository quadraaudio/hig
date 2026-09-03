# Accessibility

Accessibility is not a checklist at the end of a sprint. It is how Quadra software respects people in the studio — including people using VoiceOver, Narrator, enlarged text, high contrast, keyboard-only control, or Reduce Motion.

This chapter mirrors Apple HIG accessibility foundations and extends them to **Windows**. Every new Quadra surface must meet the requirements below.

---

## Goals

- People can perceive every meaningful control and status without relying on color alone.
- People can operate primary workflows with keyboard and assistive technologies.
- People who reduce motion still get a complete, readable interface.
- Platform accessibility settings are honored, not overridden.

---

## Do

- Provide accurate **accessibility labels** and values for every interactive control (VoiceOver on macOS, ARIA / accessible names on web, Narrator / AutomationProperties on Windows).
- Use **semantic roles**: buttons are buttons; status updates use live regions (`role="status"` / `role="alert"` on web; equivalent announcements on native).
- Keep **text contrast** at least **4.5:1** for body text against its surface (ink on snow, fasciaText on fascia, mist only for secondary).
- Respect **Reduce Motion** / `prefers-reduced-motion`: skip entrance animations, Lenis/GSAP/WebGL storytelling motion, SoftPad animation, and decorative meter shimmer.
- Show a **visible focus** indicator on keyboard focus (2px accent outline or platform focus ring).
- Hide decorative layers from assistive tech (`aria-hidden`, `.accessibilityHidden`).
- Name navigation landmarks (`Primary`, section nav, breadcrumbs).
- For dialogs: modal role, labelled title, focus trapped in the dialog, restore focus on dismiss.

## Don’t

- Don’t ship tappable plain text as the only affordance for a primary action (native apps).
- Don’t disable focus rings globally without a documented, tested keyboard alternative that still shows focus.
- Don’t encode meaning with color alone (on/off, danger, signal) — pair with label, shape, or value.
- Don’t leave canvas-based UI (patch grids, WebGL) as a single unlabeled blob when the grid is the primary workflow.
- Don’t ignore OS text-size / Dynamic Type settings in future apps.

---

## Labels and traits

### Native (MATRIX reference)

Evidence: `Apps/QuadraMatrix` controls use `.accessibilityLabel`, `.accessibilityValue`, `.accessibilityAddTraits(.isSelected)` on pills, arms, chips, and pads. Faders expose label + dB value. Brand decorative marks are `.accessibilityHidden`; wordmarks combine to `"MATRIX"`.

**Required for future apps:**

| Element | Expose |
|---------|--------|
| Button / chip / pad | Name of the action + selected state |
| Toggle / arm | Name + On/Off |
| Fader | Name + numeric value with unit |
| Meter | Name + level description (e.g. percent / Silent) |
| Icon-only control | Spoken name (never empty) |

### Web

Evidence: GlobalNav, HydraChrome, support search, bag, dialogs, and status notices use `aria-label`, `aria-expanded`, `aria-controls`, `role="dialog"`, `role="status"`, `role="alert"`.

**Required:**

- Every icon button has an accessible name.
- Expandable UI exposes `aria-expanded` / `aria-controls`.
- Errors use `role="alert"`; non-error progress uses `role="status"`.

---

## Reduce Motion

| Platform | Setting | Quadra behavior |
|----------|---------|-----------------|
| macOS | Accessibility → Display → Reduce motion | Skip SoftPad animation; use non-animated state changes; no decorative meter breathe/shimmer |
| Web | `prefers-reduced-motion: reduce` | `--ease-out` becomes linear; kill CSS animations; skip Lenis, GSAP reveals, Three.js fields; show static fallbacks |
| Windows | Settings → Accessibility → Visual effects → Animation effects | Same intent: no entrance choreography, no looping decorative motion |

**Must-fix (known gaps in shipping code):**

- MATRIX meter breathe/shimmer does not currently gate on Reduce Motion — future work must gate it.
- Web forms that set `outline: none` must still provide an equivalent `:focus-visible` style.

---

## Focus and keyboard

- Primary workflows must be reachable without a pointing device where the platform allows it.
- MATRIX product shortcuts (Dim, Mute, Mono, Talk, Cue, scenes, zoom) are documented in [Keyboard](../INPUTS/keyboard.md). Shortcuts never replace accessible names.
- **Focus visibility is mandatory** for web and for future native/Windows apps. MATRIX currently disables focus effects window-wide to keep shortcut focus clean — treat that as a **debt**, not a pattern to copy. New apps must show focus rings (or an equally visible custom focus style).

---

## Contrast and appearance

- Accent `#00A3A0` on white / snow meets interactive contrast for large controls; body text uses ink / fasciaText, not accent.
- Danger `#C44536` and success `#1F8A5B` are status colors — always accompany with text.
- Support **Light (White)** and **Dark** appearances with semantic tokens (`PrimaryText`, `Surface`, `Hairline`, etc.). See [Color](color.md).
- Future: honor **Increase Contrast** / Windows **High Contrast** themes by strengthening hairlines and fills — do not ship a third random palette.

---

## Text size

Apple HIG expects Dynamic Type. MATRIX currently maps Manrope/Syne to **fixed** macOS HIG point sizes (does not scale with Dynamic Type).

**Requirement for future Quadra apps (macOS and Windows):**

- Prefer system text styles or scalable type roles.
- If using custom fonts, bind sizes to Dynamic Type / Windows text scale so accessibility sizes remain usable.
- Layout must reflow — do not clip essential labels at large sizes.

---

## Complex canvases

Patch fields and WebGL storytelling are high-value and hard for assistive tech.

**Do:**

- Provide an alternate **list** mode (MATRIX Grid / List) that is fully keyboard- and VoiceOver-reachable.
- Give the canvas a summary accessibility label (dimensions, selection count).
- Prefer per-cell or per-row accessibility in list mode.

**Don’t:**

- Rely on canvas-only interaction for activation, licensing, or purchase flows.

---

## Windows accessibility mapping

| Apple / Quadra intent | Windows equivalent |
|-----------------------|--------------------|
| VoiceOver labels | Narrator + `AutomationProperties.Name` / accessible WinUI names |
| Reduce Motion | Animation effects off |
| Dynamic Type | Display → Text size / Make text bigger |
| Increase Contrast | High contrast themes / contrast themes |
| Keyboard full access | Full keyboard navigation, visible focus rectangles |
| `.help` tooltips | ToolTipService + accessible descriptions |

Keep **Apple principles** (clarity, deference, perceivable state). Use **native Windows accessibility APIs** — do not reimplement macOS patterns that Narrator cannot read.

---

## Shipping checklist

- [ ] Every interactive control has a spoken name and value
- [ ] Decorative art is hidden from assistive tech
- [ ] Contrast ≥ 4.5:1 for text
- [ ] Reduce Motion verified (no stuck opacity-0, no required motion)
- [ ] Keyboard path exists for primary tasks; focus is visible
- [ ] Errors and status are announced
- [ ] Light and Dark (and High Contrast when targeted) verified
- [ ] Canvas workflows have a non-canvas alternative
