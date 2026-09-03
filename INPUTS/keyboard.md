# Keyboard

Keyboard access is part of professional audio workflows and accessibility.

**Code:** Matrix key handlers (Monitor, scenes, zoom, Settings) · Web focusable controls and shortcuts where present

---

## Principles (Apple HIG → Quadra)

- Offer keyboard equivalents for frequent actions.
- Never make keyboard the *only* way without on-screen affordances.
- Document shortcuts in UI help / footnotes where density allows (e.g. ⌘± zoom hints).
- Focus must be visible — see [Accessibility](../FOUNDATIONS/accessibility.md).

---

## MATRIX reference shortcuts

| Key | Action |
|-----|--------|
| `D` `M` `O` `T` `C` | Dim / Mute / Mono / Talk / Cue |
| `1` `2` `3` | Recall scenes A/B/C |
| `⌥1/2/3` | Capture scene |
| `⌘,` | Settings |
| `⌘⇧D` | Deep Room |
| `⌘=` `⌘+` `⌘-` `⌘0` | Grid zoom / reset |
| `⌘Q` | Quit |
| Return | Default action (Done / Subscribe) |

Windows ports should map to familiar modifiers (`Ctrl` instead of `⌘`) while keeping letter mnemonics when safe.

---

## Do

- Keep shortcut letters stable across releases when possible.
- Ensure list/table type-select and arrow navigation work in AppKit/WinUI lists.
- Provide a non-canvas list mode for patch routing.

## Don’t

- Don’t capture keys needed by text fields while typing.
- Don’t disable focus rings as a shortcut for “clean UI” in new apps.
