# Color

Quadra color is a cool graphite studio with an electric teal accent — never purple, never system blue for product chrome.

Tokens are identical across the marketing site and MATRIX native app.

**Code:** `quadraaudio.github.io` → `src/styles/tokens.scss` · `Matrix` → `Colors.xcassets` + `QuadraTheme.swift` · `QuadraBrand.swift`

---

## Brand primitives

| Token | Hex | Role |
|-------|-----|------|
| `ink` | `#0E1218` | Graphite black — dark grounds, primary text on light |
| `inkSoft` | `#1A222D` | Raised dark |
| `slate` | `#3D4756` | Mid gray — secondary text on light |
| `mist` | `#8B95A5` | Steel / muted / secondary on dark |
| `paper` | `#F3F5F7` | Muted light surface |
| `snow` | `#FBFCFD` | Page / light surface |
| `line` | `#D5DAE2` | Light hairlines |
| `accent` | `#00A3A0` | Electric teal — interactive chrome (frozen) |
| `accentDeep` | `#007E7C` | Hover / selected stroke |
| `accentSoft` | `#D7F3F2` | Soft wash / selection on light |
| `warm` | `#E8A54B` | Warning / trial / attention |
| `danger` | `#C44536` | Destructive / clip / mute-on |
| `success` | `#1F8A5B` | Positive / live |
| `onAccent` | `#FFFFFF` | Label on solid accent |
| `fascia` | `#121820` | Dark app surface |
| `fasciaRaised` | `#1C242E` | Dark raised panel |
| `fasciaLine` | `#FFFFFF` @ 10% | Dark hairline |
| `fasciaText` | `#F7F9FB` | Primary text on dark |

### Web storytelling only

| Token | Hex | Role |
|-------|-----|------|
| MATRIX hot | `#5EE0DC` | Microsite wordmark / hover emphasis — **not** a native control fill |

---

## Semantic appearances

| Semantic | Light (White) | Dark |
|----------|---------------|------|
| Primary text | ink `#0E1218` | fasciaText `#F7F9FB` |
| Secondary text | slate `#3D4756` | mist `#8B95A5` |
| Surface | snow `#FBFCFD` | fascia `#121820` |
| Raised | paper `#F3F5F7` | fasciaRaised `#1C242E` |
| Hairline | line `#D5DAE2` | white @ 10% |
| Accent wash | accentSoft @ ~85% | accent @ ~22% |

Accent, accentDeep, danger, success, and warm **do not flip** between appearances.

---

## Rules

### Do

- Use named tokens / Color Sets / CSS variables — never paste a one-off hex in a feature.
- Tint system controls with accent (`#00A3A0`) — MATRIX `.quadraTint()`.
- Keep selection and focus washes on accentSoft / accent wash, not arbitrary blues.
- Use danger only for destructive or critical latched states (e.g. Mute on).

### Don’t

- Don’t use system blue, indigo, or purple for Quadra interactive chrome.
- Don’t use MATRIX hot (`#5EE0DC`) as a native button fill.
- Don’t put body copy in accent color.
- Don’t invent a third “graphite” palette — use ink / fascia tokens.

---

## Web theme mapping

Site default is light:

```
--theme-bg → snow
--theme-text → ink
--theme-accent → accent
```

MATRIX product microsite remaps `--theme-*` to dark graphite on the hydra shell so shared chrome inherits product atmosphere.

---

## Status colors

| Intent | Token | Pair with |
|--------|-------|-----------|
| Destructive | danger | Label (“Mute”, “Clear”, error copy) |
| Success / live | success | Status LED + text |
| Warning | warm | Banner or notice text |

Never rely on color alone — see [Accessibility](accessibility.md).
