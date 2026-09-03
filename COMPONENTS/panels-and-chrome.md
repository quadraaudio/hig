# Panels and chrome

Panels frame work areas. Chrome moves the window and product identity without stealing focus from content.

**Code:** Matrix `liquidGlassPanel` / `liquidGlassBay`, `TopBar`, window chrome · Site shells and footers

---

## Native panels

| Kind | Radius | Use |
|------|--------|-----|
| Panel | 28 | Patch field host |
| Bay | 16 | Monitor, Crosspoint |
| Activation card | 28 | Licensing |

Rim hairline; glass backdrop on macOS 26+; raised fill on older systems.

## Window chrome (macOS)

- Transparent titlebar + fullSizeContentView
- Traffic lights visible
- Drag from TopBar region only (not entire content)
- Close does not quit if menu-bar presence is intended
- Product lockup in TopBar — system title hidden

## Web chrome

- Quadra sticky header / MATRIX product chrome
- Footer as secondary destinations — not a second hero

---

## Do

- Match horizontal insets across TopBar, grid, and bays.
- Keep one primary panel focus per region.

## Don’t

- Don’t wrap every paragraph in a card.
- Don’t hide window controls.
- Don’t apply glass to content lists end-to-end.
