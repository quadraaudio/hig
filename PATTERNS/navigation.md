# Navigation

Navigation should feel familiar on each platform while carrying Quadra identity in the content layer.

**Code:** Matrix `RootShell`, `DeviceSidebar`, `TopBar` · Site `GlobalNav`, `HydraChrome`, `HydraNavSwap`

---

## Principles

- People should always know where they are and how to move.
- Prefer platform navigation containers (split views, sticky site header) over custom invention.
- Brand lockups belong in predictable chrome — not floating badges.

---

## Native (macOS MATRIX)

| Element | Pattern |
|---------|---------|
| Structure | `NavigationSplitView` + sidebar `List` |
| Sidebar panes | SurfaceChips: Bridges / Devices / Apps |
| TopBar | Product lockup leading; Scenes + Paint trailing |
| System title | Hidden; traffic lights remain |
| Refresh | Toolbar / sidebar action — not buried |

Sidebar rows: **name + control only**. Teaching copy lives in `(i)` popovers, `.help`, and VoiceOver values.

## Web

| Element | Pattern |
|---------|---------|
| Quadra GlobalNav | Sticky 64px, blur glass, Primary landmark |
| MATRIX HydraChrome | 48px product chrome after first viewport |
| Swap | Quadra nav ↔ MATRIX chrome with hysteresis; hide inactive from AT (`aria-hidden`, `tabIndex={-1}`) |
| Mobile | Full-screen menu panel; `aria-expanded` on trigger |

---

## Do

- Use landmarks and selected states.
- Keep primary destinations few (Store, MATRIX, Support on web).
- Preserve scroll position expectations; account for sticky height (`scroll-padding-top`).

## Don’t

- Don’t duplicate competing top bars without a clear swap model.
- Don’t put long paragraphs in sidebar rows.
- Don’t remove traffic lights or expected window controls on macOS.
