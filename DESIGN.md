# Design — Vera Solaro Midnight Ledger

This document is the production design and interaction contract for the Midnight Ledger Vera Solaro template. The local source `/Users/saurabh/Downloads/Vera Solaro Astrology Site/Midnight Ledger.dc.html` is the visual authority for the home composition, typography, palette, rules, celestial geometry, and surface hierarchy. Its `sc-*` prototype directives and demo values are reference material, not production behavior.

## Visual thesis

The site is a night-sky ledger: blue-black ink, off-white register paper, violet annotations, mint status marks, thin monospaced metadata, double rules, archival texture, and deliberately simple celestial geometry. It should feel printed and observant rather than mystical, corporate, or dashboard-like.

The canonical self-hosted type system is:

- Righteous for display statements and wordmarks;
- Spectral 300/400/italic for editorial and long-form copy;
- IBM Plex Mono 400/500 for labels, navigation, prices, metadata, and controls.

`src/styles/vera.css` owns the public system through `--ledger-*` tokens. The source palette anchors are Night `#070A1A`, Ink `#0B1026`, Panel `#171D45`, Violet `#B0A2FF`, Mint `#6FD1A8`, Paper `#E7E9E2`, and Bright Paper `#EDEFF7`.

## Home contract

The home order is header, celestial hero, four-column ledger, facts row, violet ticker, offered-reading register, thirty-minute sitting sequence, one Natal Hour testimonial, three retained deliverables, and footer. Only the currently offered Natal Hour appears. The monthly letter, Year Ahead, Two Charts, warm-home About and Journal sections, and prototype screen-directory links are absent.

Source composition yields to production truth. Duration, price, books-open state, provider availability, privacy, account data, payment status, and delivery status come from the current content/API owners. Missing media remains a truthful `VeraImage` placeholder.

## Shared public surfaces

All visitor routes use the same Ledger tokens and shared Vera frame. Booking, payment, confirmation, account, auth, contact, legal, writing, questions, closed, and error states retain their existing semantic structure and server-owned behavior. EmDash admin and transactional email presentation are outside the public-page theme boundary.

The existing 22 Content Studio entries remain the complete editable boundary. Visible static copy and SEO stay in their canonical entries; runtime facts stay in authoritative APIs. No parallel content registry, asset sidecar, or visual-only business state is allowed.

## Responsive and interaction contract

Desktop follows the source's 1440px composition without fixing the production canvas width. Mobile reflows registers into readable rows, keeps the booking action reachable, retains the celestial identity, provides 44px-class controls, and prevents horizontal overflow at 320–430px.

Motion consists of one hero entrance, one viewport reveal treatment, and focused hover elevation on the primary reading/timeline actions. Every motion has a reduced-motion fallback. Keyboard navigation, visible focus, Escape behavior, pending/disabled/error states, and live regions remain mandatory.

## Architecture boundary

The theme must not change route contracts, generated-site APIs, D1 schemas, Stripe or Calendly authority, account authorization, leads, analytics privacy, content release, Cloudflare bindings, or deployment readiness. Template-specific resource and feature identifiers use `aspt-midnight-ledger-vera-solaro`; neutral capability keys and binding names remain unchanged.
