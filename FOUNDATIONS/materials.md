# Materials

Materials express depth without turning the UI into glass for its own sake. Follow Apple’s idea of deference: materials serve navigation and panel structure; content stays readable.

**Code:** Matrix `LiquidGlass.swift`, `QuadraPillChrome.swift`, `StudioAtmosphere` · Site nav blur + hydra shell

---

## Surfaces

| Surface | Light | Dark | Use |
|---------|-------|------|-----|
| Page / window | snow | fascia / ink | Root background |
| Raised | paper | fasciaRaised | Cards, bays, empty states |
| Inverse / storytelling | ink | — | Marketing inverse bands, MATRIX microsite |

Studio atmosphere: cool gray / ink washes with a soft teal radial bloom — atmosphere, not a second brand color.

---

## Glass and blur

### Native panels (MATRIX)

- **Panel** (`liquidGlassPanel`): radius 28 — patch field host
- **Bay** (`liquidGlassBay`): radius 16 — Monitor / Crosspoint
- macOS 26+: `NSGlassEffectView` backdrop (Liquid Glass family)
- Older macOS: `raised` fill — **not** flat system gray Material on panels
- Rim: hairline ~65%, 1pt, continuous corner

Pills may use ultra-thin material + accent wash. Panels do **not** use SwiftUI `.glassEffect` on AppKit hosts.

### Web chrome

- Quadra GlobalNav: translucent bg + `backdrop-filter` blur (~16px)
- MATRIX HydraChrome: dark translucent bar + saturate/blur
- Content heroes are full-bleed visuals, not glass cards

---

## Shadows

Soft elevation only:

- Web: `--shadow-soft: 0 18px 50px rgba(14, 18, 24, 0.08)`
- Native activation card: soft ink shadow (~r 18, y 6)
- Primary pills: small accent-tinted shadow when selected

**Don’t** stack multi-layer neon glow shadows.

---

## Rules

### Do

- Reserve heavier glass for navigation chrome and major panels.
- Keep text on solid or high-legibility fills when contrast would suffer.
- Match window background to semantic surface.

### Don’t

- Don’t apply Liquid Glass / blur to every control and content row.
- Don’t use purple frosted glass trends.
- Don’t paint opaque fills that hide macOS traffic lights in windowed mode.
