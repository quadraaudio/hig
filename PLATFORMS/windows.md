# Windows

Quadra’s north star remains **Apple’s software principles** (Clarity, Deference, Depth) and this HIG’s tokens. Windows apps adapt those principles to Windows platform conventions and accessibility APIs — they do not become Fluent-first clones, and they do not paste macOS chrome onto Win32.

MATRIX is Mac-first today; Windows is a future platform (“business case later” in product docs). Design Windows surfaces from day one of that effort using this chapter.

---

## Principle mapping

| Apple / Quadra principle | Windows adaptation |
|--------------------------|--------------------|
| Clarity | Readable Segoe UI / Manrope body; teal accent `#00A3A0` for interactive chrome — not system accent purple/blue defaults for brand controls |
| Deference | Content layer carries brand; use standard WinUI navigation (NavigationView, title bar) for the UI layer so Windows users feel oriented |
| Depth | Same radii (10 / 16 / 28), snow/paper/fascia surfaces, restrained motion — not Acrylic everywhere |
| Accessibility first | Narrator, High Contrast, text size, animation effects off — see below |

---

## UI layer vs content layer

Mirror Apple’s guidance used in modern HIG thinking:

- **UI layer:** system-familiar navigation, window controls, menus, settings host pages.
- **Content layer:** Quadra patch field, meters, brand typography moments, teal catalog controls.

Do not reinvent window chrome. Do brand the work surface.

---

## Tokens on Windows

Reuse the SSOT in [tokens.md](../references/tokens.md):

- Same hex primitives and semantic light/dark pairs
- Manrope + Syne embedded or packaged; Segoe UI as fallback for system dialogs
- Capsule pills for primary actions; system toggles/sliders tinted to accent when customization is available

**Don’t** introduce Fluent purple, pink acrylic stacks, or Mica-only identity that fights graphite/teal.

---

## Accessibility (required)

| Intent | Windows mechanism |
|--------|-------------------|
| Screen reader names | Narrator + AutomationProperties / WinUI accessible names |
| Keyboard | Full keyboard navigation; visible focus rectangles always on for Quadra apps |
| Reduce motion | Honor Settings → Accessibility → Visual effects → Animation effects |
| Text scale | Honor system text size; reflow layouts |
| High contrast | Ship High Contrast–aware brushes (map semantic tokens to system colors when contrast themes are active) |

Patch/grid workflows must ship a list or tree alternative reachable by Narrator, matching macOS Grid/List expectations.

---

## Inputs and shortcuts

- Map Command-based MATRIX shortcuts to **Ctrl** equivalents where users expect them.
- Keep letter mnemonics (D/M/O/T/C) when they do not conflict with system or text entry.
- Prefer standard WinUI controls for combo boxes and menus with long device catalogs.

---

## Do

- Start from this HIG + tokens — not from a generic Windows dashboard template.
- Test with Narrator and High Contrast before release candidates.
- Keep destructive confirmations in content dialogs with clear primary/safe buttons.

## Don’t

- Don’t port macOS hidden-titlebar aesthetics in ways that break Windows snap layouts or caption buttons.
- Don’t ignore Windows 11 spacing density — adjust padding using the same 8/12/16/24 scale.
- Don’t ship without a Reduce Motion path.
