# Design tokens

Single source of truth extracted from shipping code. If code and this table disagree, **update this file** after verifying both repositories.

---

## Brand primitives

| Token | Hex | Web (`tokens.scss`) | Native (`Colors.xcassets` / `QuadraTheme`) |
|-------|-----|---------------------|-----------------------------------------------|
| ink | `#0E1218` | `--quadra-ink` | `ink` |
| inkSoft | `#1A222D` | `--quadra-ink-soft` | `inkSoft` |
| slate | `#3D4756` | `--quadra-slate` | `slate` |
| mist | `#8B95A5` | `--quadra-mist` | `mist` |
| paper | `#F3F5F7` | `--quadra-paper` | `paper` |
| snow | `#FBFCFD` | `--quadra-snow` | `snow` |
| line | `#D5DAE2` | `--quadra-line` | `line` |
| accent | `#00A3A0` | `--quadra-accent` | `accent` / `QuadraBrand.accentHex` |
| accentDeep | `#007E7C` | `--quadra-accent-deep` | `accentDeep` |
| accentSoft | `#D7F3F2` | `--quadra-accent-soft` | `accentSoft` |
| warm | `#E8A54B` | `--quadra-warm` | `warm` |
| danger | `#C44536` | `--quadra-danger` | `danger` |
| success | `#1F8A5B` | `--quadra-success` | `success` |
| onAccent | `#FFFFFF` | (white on buttons) | `onAccent` |
| fascia | `#121820` | hydra / mx panels | `fascia` |
| fasciaRaised | `#1C242E` | — | `fasciaRaised` |
| fasciaText | `#F7F9FB` | `--theme-text-inverse` / mx text | `fasciaText` |
| fasciaLine | `#FFFFFF` @ 10% | `--hydra-line` / mx line | `fasciaLine` |
| MATRIX hot | `#5EE0DC` | `--hydra-hot` / `--mx-hot` | **web storytelling only** |

---

## Semantics

| Role | Light | Dark |
|------|-------|------|
| Primary text | ink | fasciaText |
| Secondary text | slate | mist |
| Surface | snow | fascia |
| Raised | paper | fasciaRaised |
| Hairline | line | fasciaLine |
| Accent wash | accentSoft ~85% | accent ~22% |

---

## Typography

| Role | Face |
|------|------|
| Brand | Syne Bold / 700–800 |
| Body / ops | Manrope |
| Mono (web) | IBM Plex Mono |

Native ops sizes follow macOS HIG roles (body/headline 13, callout 12, footnote/caption 10, title3 15, brand 17/22/26).

---

## Space and radius

| Token | Value |
|-------|-------|
| spaceXS–LG (native) | 8 / 12 / 16 / 24 |
| web space scale | 4 … 180 (`--space-2xs` … `--space-6xl`) |
| page max (web) | 1240px |
| radiusSM / MD / LG | 10 / 16 / 28 |
| pill | capsule / 999px |
| control H | 36 (28 compact) |
| web btn min-height | 48 |

---

## Motion

| Token | Value |
|-------|-------|
| Ease | `cubic-bezier(0.22, 1, 0.36, 1)` |
| Native ease-out | 0.35s |
| Native fade-in | 0.55s |
| Reduced motion | linear / animations off |

---

## Shadow

`--shadow-soft`: `0 18px 50px rgba(14, 18, 24, 0.08)`
