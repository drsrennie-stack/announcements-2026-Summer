# Teaching brand rules (BIO 004 and course pages)

Source of truth: the BIO 004 course home page. Apply these to every teaching HTML deliverable unless told otherwise.

## Colors

| Token | Hex | Use |
|---|---|---|
| Ink | #0B1530 | Primary text, headlines, logo figure 1, icon line work |
| Dark | #060A18 | Dark section and footer backgrounds |
| Rust | #8B3A2E | Accents on LIGHT sections: eyebrows, headline accent spans, buttons, focus ring, hover borders |
| Rust hover | #A0452F | Button hover |
| Gold | #C9A14A | Accents on DARK sections: eyebrows, byline, focus ring, current-week flag |
| Terra (secondary) | #C2734D | Headline accent spans on dark sections only |
| White | #FFFFFF | Page background, cards |
| Line gray | #8C90A0 | Card borders |
| Locked gray | #6B7180 | Locked-state text and flag |

Accent rule (load-bearing): rust on light backgrounds, gold on dark backgrounds. Never rust text on dark (fails contrast). 

Cream (#F5F1E8) is not part of the core teaching palette. It appears only as a deliberate, confirmed one-off section treatment on the course home page. Do not add cream to new teaching deliverables unless explicitly confirmed.

## Type

- One family: Plus Jakarta Sans (Variable), system-ui fallback. Loaded via `@import url('https://cdn.jsdelivr.net/npm/@fontsource-variable/plus-jakarta-sans/index.css');`
- Base body: ~17px, line-height 1.6 to 1.65.
- Eyebrows: 12px, weight 700, uppercase, letter-spacing ~0.24 to 0.28em.
- Headlines (h1/h2): weight 800, letter-spacing -0.02 to -0.025em. Use a rust `.accent` span for emphasis on light sections.
- Buttons: 12px, weight 700, uppercase, letter-spacing ~0.16em.

## Components

- Buttons: rust fill, white text, border-radius 4px, hover to #A0452F.
- Cards: white fill, 1px #8C90A0 border, border-radius 8 to 12px, rest shadow `0 1px 3px rgba(11,21,48,0.06)`. On hover: lift `translateY(-3px)`, shadow `0 10px 22px rgba(11,21,48,0.12)`, border-color rust.
- Sections alternate light (white) and dark (#060A18). Vertical padding ~64px, horizontal `max(40px,5vw)`.
- Logo: three-figure SVG (ink, rust, gold) plus "Human Anatomy" wordmark with "Anatomy" in rust, sublabel "BIO 004 · Solano Community College". On dark backgrounds the first figure and wordmark go white, accent stays gold.

## Interactive states (teaching tools)

- Current week: gold flag (#C9A14A) on a gold-bordered card.
- Locked: dashed #8C90A0 border, muted content, gray lock flag, link removed and click/keyboard blocked.

## Platform and accessibility (always)

- WCAG 2.2 AA floor, AAA on text contrast where achievable.
- Skip link, semantic landmarks, heading hierarchy, `.sr-only` helper, visible focus (3px rust on light, gold on dark, offset 3px), `prefers-reduced-motion` reset.
- iframe height-sender before `</body>`: `postMessage({type:'resize', id:<frame-id>, height})` with load + resize listeners and a ResizeObserver.
- Internal and same-domain links: `target="_top"`. External links: `target="_blank" rel="noopener"`.
- No em dashes anywhere.
- Student-facing byline and signature: "Dr. Sharilyn Rennie" (no credential suffix). No student PII stored.

## Note on the saved palette file

The workspace `palettes.md` currently documents a different teaching palette (navy #1E3D4C, DM Sans, Lora). This brand guide reflects the live course pages and should take precedence for teaching work. Worth reconciling `palettes.md` to match.
