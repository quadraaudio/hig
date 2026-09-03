# macOS

MATRIX is the reference Quadra native app on macOS. Follow Apple HIG platform conventions, then apply Quadra tokens and catalog controls.

**Code:** `Apps/QuadraMatrix` — `RootShell`, window chrome, `QuadraTheme`, `LiquidGlass`, control catalog

---

## Platform baseline

- Target macOS 14+ (capture features may require 14.2+)
- Prefer SwiftUI + AppKit bridges where needed (faders, glass, tables)
- Use `NavigationSplitView`, sidebar `List`, sheets, confirmation dialogs
- Keep traffic lights; support miniaturize/zoom behaviors people expect
- Menu bar extra uses company **Q**; in-window mark uses waveform

---

## Quadra on macOS

| Topic | Rule |
|-------|------|
| Tint | `.quadraTint()` once per scene root — never system blue chrome |
| Type | Manrope HIG roles; Syne for brand moments |
| Appearance | System / White / Dark via semantic Color Sets |
| Panels | `liquidGlassPanel` / `liquidGlassBay` |
| Controls | Compose from catalog only |
| Shortcuts | See [Keyboard](../INPUTS/keyboard.md) |

Implementation playbook inside the app repo: `Docs/Product/DESIGN_SYSTEM.md`. Org SSOT remains this HIG.

---

## Do

- Hide the system window title if TopBar carries the product lockup — keep controls.
- Put long teaching copy in popovers and help tags, not sidebar walls.
- Test VoiceOver on sidebar, monitor pads, faders, and list-mode patching.

## Don’t

- Don’t ship Spaces fullscreen if product policy disables it — document the choice.
- Don’t copy iOS phone patterns into a desktop patchbay.
- Don’t treat focus-ring suppression as a permanent standard (see Accessibility must-fix).
