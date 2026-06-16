# Accessibility Compliance Notes

**Project:** BIO 004 Announcements (dated, repo-archivable)
**Files covered:** announcements-BIO-004_2026-06-15.html
**Date:** 2026-06-15
**Brand:** Teaching brand system (see brand-guide.md)

## WCAG version and target level

WCAG 2.2. AA floor; AAA achieved on all text contrast.

Criteria addressed: 1.1.1 (QR images have descriptive alt naming the destination), 1.3.1 (semantic header/main/footer, section landmarks, h1/h2/h3, resources as lists), 1.4.3/1.4.6 (contrast, below), 1.4.11 (focus ring and card borders meet 3:1), 2.1.1 (all interactive elements are native links), 2.4.1 (skip link), 2.4.7 (visible 3px focus, offset 3px), 2.5.8 (buttons exceed 24x24px), 3.2.4 (consistent "Open link" pattern with hidden per-item label), 2.3.3 (prefers-reduced-motion reset).

## Color contrast audit (brand colors)

| Element | Foreground | Background | Ratio | Result |
|---|---|---|---|---|
| Body and headlines (ink) | #0B1530 | #FFFFFF | 18.04:1 | AAA |
| Rust eyebrow / accent / focus | #8B3A2E | #FFFFFF | 7.66:1 | AAA |
| Button label | #FFFFFF | #8B3A2E | 7.66:1 | AAA |
| Button label hover | #FFFFFF | #A0452F | 6.20:1 | AA (AAA large) |
| Footer text (white on dark) | #FFFFFF | #060A18 | 19.73:1 | AAA |
| Footer gold byline / accent | #C9A14A | #060A18 | 8.16:1 | AAA |
| Card border (non-text UI) | #8C90A0 | #FFFFFF | 3.18:1 | Pass (>= 3:1) |
| QR scanner corner (non-text UI) | #8B3A2E | #FFFFFF | 7.66:1 | Pass |

Accent rule honored: rust used only on light, gold only on dark. Rust on dark (2.58:1) is never used for text.

## Keyboard navigation flow verified

Tab order: skip link, logo (course home), then each card's "Open link" button top to bottom (lab gear, skull models, books, community), then footer logo. All activatable with Enter. Skip link jumps to main. No traps. Focus ring visible at every stop.

## Screen reader testing

Verified structurally against the DOM: landmark and heading tree, list semantics, accessible names. Each link reads, for example, "Open link for Lab Coat, opens in a new tab." Each QR image announces its destination. Decorative icons are aria-hidden. Recommend a live VoiceOver/NVDA pass once embedded in the host page.

## Known limitations and remediation plan

- QR codes encode external URLs (Amazon, Audible, Discord); links open in a new tab and are labeled as such.
- Screen reader pass is structural, not yet run in a live AT session. Plan: verify in VoiceOver after embedding.

## Platform compliance

- iframe height-sender present (id "bio004-announcements-2026-06-15", postMessage type "resize", load + resize + ResizeObserver).
- Logo links use target="_top"; all resource links use target="_blank" rel="noopener".
- Teaching brand palette only; no em dashes; byline "Dr. Sharilyn Rennie"; no student PII.

## Reviewer

Dr. Sharilyn Rennie
