# Faders and meters

Gain and level are studio-critical. Readouts must be precise and accessible.

**Code:** Matrix `QuadraFader` (AppKit), `DockMeterView`, axis presence rails · Site Three.js meters (storytelling)

---

## Faders

- Default range −60…12 dB, step 0.5 (product may specialize)
- Track ~6pt capsule; thumb circle with accentDeep stroke
- VoiceOver: label + `"%.1f dB"`
- Prefer QuadraFader for ops; system `Slider` + tint is OK for non-audio settings (zoom)

## Meters

- Dock L/R wells with footnote labels
- Axis rails show presence along patch axes
- Fill uses accent opacity mapped to level; danger/warm only with clear meaning

---

## Do

- Use monospaced numerals for dB and percent.
- Provide textual accessibility values (“Silent”, percent signal).
- Gate decorative breathe/shimmer on Reduce Motion (required for future work).

## Don’t

- Don’t animate meter geometry in ways that fight performance or a11y clocks without need.
- Don’t show clipping only as a red pixel with no label elsewhere.
