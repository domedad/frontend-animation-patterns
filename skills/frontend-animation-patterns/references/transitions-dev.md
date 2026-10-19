# Transitions.dev Catalog

Official source: [Transitions.dev](https://transitions.dev/) · [catalog/documentation](https://transitions.dev/detail.html?t=card-resize) · [accessibility](https://transitions.dev/detail.html?doc=accessibility) · [official Skill](https://transitions.dev/skill.html)

Last reviewed: 2026-08-13.

Use this source for production UI transitions. The site presents portable CSS and self-contained React variants; small JavaScript helpers appear only where a demo requires them. Recipes share duration, easing, distance, blur, and scale conventions. Pages may change, so open the exact official recipe before implementing.

## Layout and Navigation

- [Card resize](https://transitions.dev/detail.html?t=card-resize) — smooth size/content changes within a card.
- [Menu dropdown](https://transitions.dev/detail.html?t=menu-dropdown) — source-aware menu open/close.
- [Modal open/close](https://transitions.dev/detail.html?t=modal-open-close) — modal opacity/scale transition.
- [Panel reveal](https://transitions.dev/detail.html?t=panel-reveal) — panels and side sheets.
- [Page side-by-side](https://transitions.dev/detail.html?t=page-side-by-side) — forward/backward page or step movement.
- [Dropdown menu morph](https://transitions.dev/detail.html?t=dropdown-menu-morph) — trigger morphs into menu surface.
- [Accordion](https://transitions.dev/detail.html?t=accordion) — content expansion with chevron transformation.
- [Tabs sliding](https://transitions.dev/detail.html?t=tabs-sliding) — active pill/indicator follows the selected tab.
- [Gooey plus menu](https://transitions.dev/detail.html?t=gooey-plus-menu) — expressive radial action menu. **Pro**.

## Feedback and State

- [Number pop-in](https://transitions.dev/detail.html?t=number-pop-in) — blurred, staggered digit change.
- [Notification badge](https://transitions.dev/detail.html?t=notification-badge) — angled slide with a spring pop.
- [Text states swap](https://transitions.dev/detail.html?t=text-states-swap) — replace short status text with blur/opacity continuity.
- [Icon swap](https://transitions.dev/detail.html?t=icon-swap) — scale/blur between glyph states.
- [Success check](https://transitions.dev/detail.html?t=success-check) — compact success confirmation.
- [Error state shake](https://transitions.dev/detail.html?t=error-state-shake) — short error shake; always pair with text/semantics.
- [Toast open/close](https://transitions.dev/detail.html?t=toast-open-close) — opacity, blur, scale, and staggered toast entry/exit.
- [Checkbox check](https://transitions.dev/detail.html?t=checkbox-check) — draw the check with a stroke path.
- [Toggle](https://transitions.dev/detail.html?t=toggle) — sliding thumb with restrained spring response.
- [Like button](https://transitions.dev/detail.html?t=like-button) — filled heart and particles for explicit likes.
- [Spinner to check morph](https://transitions.dev/detail.html?t=spinner-to-check-morph) — loading spinner becomes completion check. **Pro**.
- [Spinning counter](https://transitions.dev/detail.html?t=spinning-counter) — reel-style value change.
- [Confetti burst](https://transitions.dev/detail.html?t=confetti-burst) — physics confetti for rare achievements. **Pro**.

## Loading and Content Reveal

- [Input clear with dissolve](https://transitions.dev/detail.html?t=input-clear-with-dissolve) — per-character dissolve on explicit clear.
- [Skeleton loader and reveal](https://transitions.dev/detail.html?t=skeleton-loader-and-reveal) — pulse loader crossfades to content.
- [Texts reveal](https://transitions.dev/detail.html?t=texts-reveal) — staggered lines rise into view.
- [Shimmer text](https://transitions.dev/detail.html?t=shimmer-text) — masked gradient scan across text.
- [Organic shimmer](https://transitions.dev/detail.html?t=organic-shimmer) — soft wave/glow surface. **Pro**.
- [Pro gradient text](https://transitions.dev/detail.html?t=pro-gradient-text) — chromatic bloom around lettering. **Pro**.

## Hover, Pointer, and Spatial Effects

- [Avatar group hover](https://transitions.dev/detail.html?t=avatar-group-hover) — distance-decayed lift across a group.
- [Card stack hover](https://transitions.dev/detail.html?t=card-stack-hover) — stacked cards fan out with spring response. **Pro**.
- [Tooltip open/close](https://transitions.dev/detail.html?t=tooltip-open-close) — delayed show and immediate exit.
- [3D tilt](https://transitions.dev/detail.html?t=3d-tilt) — pointer tilt and glare for showcase cards.
- [Learn more hover](https://transitions.dev/detail.html?t=learn-more-hover) — chevron movement and subtle button expansion.
- [Drag & drop with physics](https://transitions.dev/detail.html?t=drag-drop-with-physics) — physical drag feedback and drop-zone transformation. **Pro**.
- [Image open tilt](https://transitions.dev/detail.html?t=image-open-tilt) — image zoom with 3D bend/tilt. **Pro**.
- [Delete with smoky dissolve](https://transitions.dev/detail.html?t=delete-with-smoky-dissolve) — dramatic destructive completion. **Pro**.

## Accessibility and Performance Contract

- Follow the Skill's Default Motion Policy: keep selected animations enabled regardless of system motion settings. If app motion is explicitly off, retain the functional end state without movement, blur, or scale.
- Keep state in DOM text and ARIA; never depend on animation alone.
- Use real controls, correct ARIA states, keyboard access, and visible native focus.
- Prefer compositor-friendly `transform` and `opacity`; use `filter` and `will-change` sparingly.

## Access Notes

Free recipes can be studied and copied from their CSS/React tabs. Entries labeled **Pro** require Transitions Pro; do not represent them as freely available. The source also publishes an official installation command (`npx skills add Jakubantalik/transitions.dev`), but this catalog remains the cross-source selector and should not silently install external Skills.
