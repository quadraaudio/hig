# Writing

Voice and naming are part of the interface. Plain language first; technical detail after the reader understands the value.

**Code:** `quadraaudio.github.io` → `src/data/brand.messaging.ts` · Matrix `QuadraBrand.swift` · guidance copy in-app

---

## Brand constants

| Constant | Value |
|----------|-------|
| Company | Quadra |
| Product | MATRIX (always uppercase in UI lockups) |
| Tagline | Designed in Italy |
| Purpose | Professional audio software for Mac. |
| Forbidden product names | Hydra, Matrice, Soundcard, Quadra Soundcard |

Sub-brands used in product copy: Quadra ID, Quadra Guard, Quadra Deep Room, Matrix Bridges.

---

## Tone

- Direct, calm, studio-literate — not hype.
- Prefer short sentences.
- Explain jargon once (patch field, Matrix Bridge, control room) then use the term consistently.
- CTAs are concrete: Explore MATRIX, Buy MATRIX, Start free trial.

### Do

- Lead with what the person can do (“Route everything.”) before architecture.
- Match button labels to the outcome (“Start free trial”, “Done”).
- Keep sidebar rows short; put teaching copy in info popovers, help tags, or support articles.

### Don’t

- Don’t invent playful marketing voice inside the native ops UI.
- Don’t use forbidden names in UI, filenames shown to users, or window titles.
- Don’t write walls of instructional text into list rows.

---

## Capitalization

| Context | Style |
|---------|-------|
| Product lockup | MATRIX |
| Company lockup | QUADRA (tracked Syne) or Quadra in prose |
| Section labels | Uppercase micro labels (MONITOR, SCENES) via `label()` / eyebrow |
| Buttons | Sentence case (“Clear all”) unless matching a proper noun |

---

## Accessibility writing

- Accessibility labels describe **purpose**, not appearance (“Mute monitors”, not “Red button”).
- Errors say what failed and what to do next.
- Status text stays short enough to announce without fatigue.
