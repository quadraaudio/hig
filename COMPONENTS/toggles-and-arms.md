# Toggles and arms

Binary state should be obvious at a glance and correctly announced.

**Code:** Matrix `QuadraArm`, system `Toggle` with `.quadraTint()`, Monitor `SoftPad`

---

## Patterns

| Control | When |
|---------|------|
| **QuadraArm** | Emphasized binary arm (login, feedback, crosspoint on/off) — custom capsule track 36×20, thumb 14 |
| **System Toggle (switch)** | Sidebar device enable, dense lists |
| **System Toggle (checkbox)** | Deep Room options (“Mute Sub”) |
| **SoftPad** | Monitor CR latches: Dim, Mono, Mute, Talk, Cue — pill chrome; Mute uses danger when on |

Arm on: primary fill + white thumb. Off: secondary glass + mist thumb.

---

## Do

- Announce On/Off via accessibility value.
- Respect Reduce Motion on SoftPad (instant state, no flourish).
- Tint system switches with accent.

## Don’t

- Don’t build a second custom switch style besides Arm/SoftPad/system.
- Don’t use color-only state without label.
