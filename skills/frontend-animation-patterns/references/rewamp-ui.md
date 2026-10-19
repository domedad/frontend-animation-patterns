# Rewamp UI Catalog

- Official catalog: [Rewamp UI components](https://www.rewampui.com/components/gradient-reveal-text)
- Documentation: [Rewamp UI documentation](https://www.rewampui.com/documentation)
- Source repository: [palakonweb/Rewamp-UI](https://github.com/palakonweb/Rewamp-UI)
- Reviewed: 2026-09-23 at repository commit `45e2460e58c7306abe9fc783fa0584bbadb81086`

Use Rewamp UI for expressive React interfaces that need tactile spring motion, kinetic typography, pointer-reactive backgrounds, spatial navigation, custom cursors, animated cards, or ambient AI companion states. The live sidebar exposes **70 public components across 10 categories**.

## Stack, Installation, and Access

- Stack: React 19, Vite 7, Tailwind CSS 4, Framer Motion, Lucide React, React Router, and Three.js for selected WebGL components.
- Delivery model: copy the component source or use the Node 18+ CLI, for example `npx rewampui@latest add gradient-reveal-text`.
- Registry entries declare per-component dependencies. Inspect the JSON/source before installing; most components use `framer-motion` and `lucide-react`, while several AI orbs use `three`.
- The published `rewampui` CLI package declares MIT, but the reviewed repository root has no `LICENSE` file and states that the designs are inspired by other internet work. Treat component-code licensing and visual originality as **not fully established**; verify before commercial redistribution or close visual replication.
- The live catalog and repository registry are not perfectly synchronized. The visible catalog is the count source of truth. At review time, `Singularity Flare Background` was visible but lacked a matching registry JSON; use manual source inspection instead of assuming the CLI supports it.

## Selection Profile

- **Use for:** marketing heroes, design showcases, portfolios, immersive product launches, high-expression navigation, premium empty/loading states, and AI voice/listening/processing ambience.
- **Use selectively in product UI:** search expansion, tab/navbar active indicators, a deliberate confirmation gesture, or a single tactile card interaction.
- **Avoid by default in:** dense dashboards, long forms, data tables, accessibility-critical flows, low-power/mobile contexts, or pages that already have another signature motion system.
- Prefer one Rewamp signature effect per viewport. Pair it with quiet native transitions instead of combining background, cursor, 3D card, and kinetic text effects together.

## Animated Backgrounds — 20

Use cursor-reactive grid and particle effects for interactive hero surfaces; use ambient gradients, ribbons, dust, snow, caustics, waves, and flares as decorative backdrops only. Canvas/WebGL effects need static imagery or CSS-gradient fallbacks, visibility pausing, device-quality limits, and compliance with the Skill's Default Motion Policy.

- [Liquid Cursor Gradient](https://www.rewampui.com/components/liquid-cursor-gradient)
- [Ascii Matrix Hover](https://www.rewampui.com/components/ascii-matrix-hover)
- [Elastic Line Grid](https://www.rewampui.com/components/elastic-line-grid)
- [Spotlight Grid](https://www.rewampui.com/components/spotlight-grid)
- [Ripple Grid](https://www.rewampui.com/components/ripple-grid)
- [Soft Aurora](https://www.rewampui.com/components/soft-aurora)
- [Plexus Engine](https://www.rewampui.com/components/plexus-engine)
- [Particle Wave](https://www.rewampui.com/components/particle-wave)
- [Hyperspeed Warp](https://www.rewampui.com/components/hyperspeed-warp)
- [Sine Ribbons](https://www.rewampui.com/components/sine-ribbons)
- [Ambient Glow Orbs](https://www.rewampui.com/components/ambient-glow-orbs)
- [Refracted Beams](https://www.rewampui.com/components/refracted-beams)
- [Cosmic Dust](https://www.rewampui.com/components/cosmic-dust)
- [Real Snow Background](https://www.rewampui.com/components/pixel-snow-background)
- [Water Caustics Background](https://www.rewampui.com/components/water-caustics-background)
- [Gradient Wave Background](https://www.rewampui.com/components/gradient-wave-background)
- [Pixel Cloud Background](https://www.rewampui.com/components/pixel-cloud-background)
- [Silk Waves Background](https://www.rewampui.com/components/silk-waves-background)
- [Singularity Flare Background](https://www.rewampui.com/components/singularity-flare-background)
- [Layered Paper Waves Background](https://www.rewampui.com/components/layered-paper-waves-background)

## Buttons — 8

Use tactile buttons when the physical interaction reinforces the action. Retain semantic `<button>` behavior, focus-visible styling, disabled/loading states, and a non-hover equivalent. `Slide To Confirm` is appropriate only when the gesture adds deliberate intent; it must still support keyboard and assistive-technology confirmation.

- [Googly Eyes Button](https://www.rewampui.com/components/googly-eyes-button)
- [Gloss Button](https://www.rewampui.com/components/gloss-button)
- [Neumorphic Download Button](https://www.rewampui.com/components/neumorphic-download-button)
- [Rainbow Button](https://www.rewampui.com/components/rainbow-button)
- [Slide To Confirm Button](https://www.rewampui.com/components/slide-to-confirm-button)
- [Chrome Border Button](https://www.rewampui.com/components/chrome-border-button)
- [Book A Call Button](https://www.rewampui.com/components/book-a-call-button)
- [Shimmer Button](https://www.rewampui.com/components/shimmer-button)

## Text Animations — 9

Use short display copy, hero headings, section labels, or status phrases. Keep real selectable DOM text, preserve the semantic heading, stabilize its layout box, and stop continuous loops when app motion is explicitly off, not automatically from system settings.

- [Kinetic Reel Text](https://www.rewampui.com/components/kinetic-reel-text)
- [Split Text Reveal](https://www.rewampui.com/components/split-text-reveal)
- [Word By Word Text](https://www.rewampui.com/components/word-by-word-text)
- [Character Scramble Text](https://www.rewampui.com/components/character-scramble-text)
- [Gradient Reveal Text](https://www.rewampui.com/components/gradient-reveal-text)
- [Spotlight Text](https://www.rewampui.com/components/spotlight-text)
- [Flip 3D Text](https://www.rewampui.com/components/flip-3-d-text)
- [Typewriter Text](https://www.rewampui.com/components/typewriter-text)
- [Velocity Marquee Text](https://www.rewampui.com/components/velocity-marquee-text)

`Gradient Reveal Text` uses an animated text-clipped gradient with a slow continuous background-position loop. Choose it for one premium headline or AI status phrase, not body text or multiple competing headings. Provide a solid-color text fallback and sufficient contrast in every gradient frame.

## Toggles — 3

These are expressive theme/state toggles. The animation must reflect the actual controlled value rather than becoming the state itself; preserve a visible label or accessible name.

- [Day Night Sky Toggle](https://www.rewampui.com/components/day-night-sky-toggle)
- [Landscape Orb Toggle](https://www.rewampui.com/components/landscape-orb-toggle)
- [Glass Orb Toggle](https://www.rewampui.com/components/glass-orb-toggle)

## Cursors — 2

Restrict custom cursors to fine-pointer showcase pages. Disable them for touch, coarse pointers, explicit app-level motion-off mode, forms, text editing, and accessibility-critical product work. Never hide the native cursor unless the replacement remains precise and visible over every background.

- [Pill Trail Cursor](https://www.rewampui.com/components/pill-trail-cursor)
- [Halftone Dot Cursor](https://www.rewampui.com/components/halftone-dot-cursor)

## Navbars — 12

Use spring, morph, liquid-underline, or radial navigation for a branded shell with a small, stable information architecture. Keep current-page state, keyboard order, labels, focus, mobile escape/close behavior, and route semantics independent of the animation.

- [Hero Morph Navbar](https://www.rewampui.com/components/hero-morph-navbar)
- [Pill Expand Navbar](https://www.rewampui.com/components/pill-expand-navbar)
- [Pixel Dot Navbar](https://www.rewampui.com/components/pixel-dot-navbar)
- [Dark Mode Mobile Navbar](https://www.rewampui.com/components/dark-mode-mobile-navbar)
- [Fluid Wave Navbar](https://www.rewampui.com/components/fluid-wave-navbar)
- [Magnetic Pill Navbar](https://www.rewampui.com/components/magnetic-pill-navbar)
- [Circular Radial Navbar](https://www.rewampui.com/components/circular-radial-navbar)
- [Curtain Reveal Navbar](https://www.rewampui.com/components/curtain-reveal-navbar)
- [Jelly Scoop Navbar](https://www.rewampui.com/components/jelly-scoop-navbar)
- [Liquid Underline Navbar](https://www.rewampui.com/components/liquid-underline-navbar)
- [Morphing Tab Navbar](https://www.rewampui.com/components/morphing-tab-navbar)
- [Orbiting Planets Navbar](https://www.rewampui.com/components/orbiting-planets-navbar)

## Search Bars — 2

Use the capsule morph when saving space matters and the search action remains discoverable. Preserve a real labeled input, focus the input after expansion, return focus after collapse, and expose loading, results, and no-results states.

- [Morph Search Capsule](https://www.rewampui.com/components/morph-search-capsule)
- [Animated Search Demo](https://www.rewampui.com/components/animated-search-demo)

## Sidebars — 3

Use lens, sliding-highlight, or decorative sidebar styles for compact navigation. Labels must remain available without hover, and the active item must not depend on the moving highlight alone.

- [Kinetic Lens Sidebar](https://www.rewampui.com/components/kinetic-lens-sidebar)
- [Sidebar](https://www.rewampui.com/components/sidebar)
- [Flower Sidebar](https://www.rewampui.com/components/flower-sidebar)

## Cards — 6

Use card stacks, flip decks, orbital arches, and carousels for browsing small visual collections or editorial showcases. Provide buttons for previous/next/select, preserve reading order, avoid auto-rotation for essential content, and render a simple list or grid on small screens or when app motion is explicitly off.

- [Diagonal Card Stack](https://www.rewampui.com/components/diagonal-card-stack)
- [Perspective Flip Deck](https://www.rewampui.com/components/perspective-flip-deck)
- [Orbital Card Arch](https://www.rewampui.com/components/orbital-card-arch)
- [Editorial 3D Orbit Carousel](https://www.rewampui.com/components/editorial-3-d-orbit-carousel)
- [Arch Card Carousel](https://www.rewampui.com/components/arch-card-carousel)
- [Folder Tab Card](https://www.rewampui.com/components/folder-tab-card)

## UI for AI — 5

These Three.js companion orbs can communicate ambient AI presence—idle, listening, thinking, speaking, success, or error—when driven by real application state. They do not replace textual status, task steps, tool-call evidence, or approval UI. Define a deterministic state-to-motion/color mapping and a static fallback.

- [Marbled Fluid Orb](https://www.rewampui.com/components/marbled-fluid-orb)
- [Particle Dot Orb](https://www.rewampui.com/components/particle-dot-orb)
- [Fluid Morph Orb](https://www.rewampui.com/components/fluid-morph-orb)
- [Wireframe Ring Orb](https://www.rewampui.com/components/wireframe-ring-orb)
- [Particle Morph Orb](https://www.rewampui.com/components/particle-morph-orb)

## Source-Specific Guardrails

- Rewamp UI is a high-motion library. Start from the product communication need, not from the most spectacular demo.
- Do not combine a continuous WebGL background, custom cursor, kinetic headline, orbiting cards, and elastic navigation in one viewport.
- Pause requestAnimationFrame, canvas, and WebGL work while hidden or offscreen. Dispose Three.js renderers, textures, geometries, materials, listeners, and animation frames on unmount.
- Cap device pixel ratio and reduce particle counts/effect quality on mobile or low-power devices. Avoid using continuous shaders behind forms and dense content.
- Keep selected animations enabled regardless of system motion settings. Map an explicit app-level motion-off choice, if present, to a static final frame, ordinary text, standard cursor, simple grid/list, or immediate state change.
- Keep functional states in DOM text and semantics. Motion, color, glow, and an AI orb can support status but never be the sole status channel.
- Adapt colors, type, radius, and spacing to the existing project. Do not import the whole Rewamp visual language for one component.
- Verify the current registry entry, dependencies, visible behavior, and reuse rights before copying or invoking `npx rewampui@latest add`.
