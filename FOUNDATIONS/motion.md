# Motion

Motion clarifies change and hierarchy. It never blocks understanding.

**Code:** Matrix `QuadraTheme` easing · Site Lenis / GSAP / CSS `--ease-out` · `prefers-reduced-motion` hooks

---

## Signature easing

```
cubic-bezier(0.22, 1, 0.36, 1)
```

| Token | Duration | Use |
|-------|----------|-----|
| Ease out (native) | 0.35s | Pads, pane changes, session updates |
| Fade in (native) | 0.55s | Activation / reveal |
| Web page enter | ~0.55–0.85s | Shell opacity |
| Web reveal | ~0.7s | Scroll-triggered rise |
| Web button hover | 0.25s | Translate / color |

Under Reduce Motion, web forces `--ease-out: linear` and disables choreography.

---

## Allowed motion

- State change on controls (pad latch, chip selection) with short ease-out
- Panel / page enter fades
- Scroll-authored storytelling on the MATRIX microsite (pin scrub, cable draw) — skipped when reduced motion
- Subtle hover lift on web store cards (`translateY` ~1–3px)

## Disallowed motion

- Infinite decorative loops required to understand UI
- Parallax that moves focus targets unpredictably
- Autoplaying motion that ignores Reduce Motion
- Staggered noise that delays task completion

---

## Reduce Motion requirements

See [Accessibility](accessibility.md).

Minimum:

- No stuck `opacity: 0` content if animation is skipped
- SoftPad and similar controls still toggle instantly
- WebGL / Lenis / GSAP storytelling off → static image or CSS fallback
- Meter cosmetic breathe/shimmer must respect Reduce Motion in future work

---

## Web vs app

| Context | Motion role |
|---------|-------------|
| Marketing site / MATRIX microsite | Presence and story — intentional 2–3 motions, then stop |
| Native app | Feedback on interaction — short, local, interruptible |
| Windows future apps | Same rules; honor OS “Animation effects” |

---

## Do / Don’t

### Do

- Use the shared easing curve.
- Animate transform and opacity, not layout thrash.
- Prefer scroll-driven narrative over looping GIFs on product pages.

### Don’t

- Don’t introduce springy playful motion that fights studio seriousness.
- Don’t animate the patch field layout in ways that break sticky AppKit scroll (MATRIX disables animation transactions on the patch panel for this reason).
