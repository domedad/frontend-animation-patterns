# EasyUI — Tactile Product UI and Developer Surfaces

Reviewed: **2026-10-07**. Indexed **108 public components in 7 official categories**. This is a complete selection index, not 108 locally installed or production-tested implementations. The official [LLM index](https://www.easyui.site/llms.txt), [GitHub registry](https://github.com/Surajmaurya1/easyui/blob/main/registry.json), and [source catalog](https://github.com/Surajmaurya1/easyui/blob/main/src/components/registry/catalog-index.ts) agree on the count. Repository snapshot: `0be45a714208445b4a39e5e9310e9493d74d6640`.

## Routing and Delivery

- Official [component catalog](https://www.easyui.site/components), [introduction](https://www.easyui.site/docs/introduction), [repository](https://github.com/Surajmaurya1/easyui), and [README installation guide](https://github.com/Surajmaurya1/easyui#quick-start).
- Best fit: developer consoles, audit/telemetry streams, inspectable data, batch actions, version history, AI tool execution and responses, and quiet spring-based controls. Use high-energy canvas backgrounds only for intentional showcase surfaces.
- Copy-in TypeScript React components, styled with Tailwind and animated with Framer Motion/CSS/canvas. README targets React 18/19 and Tailwind v3/v4; inspect the selected recipe against the project's actual versions rather than assuming compatibility.
- Add only the selected component through the official GitHub registry, for example:

  ```bash
  npx shadcn@latest add Surajmaurya1/easyui/activity-feed
  ```

  The last URL segment in each table below is the registry component name. Inspect its current GitHub `registry.json` entry first. The reviewed entries declare `framer-motion` and `lucide-react`; shared `utils.ts` also imports `clsx` and `tailwind-merge`, which may already exist in shadcn projects. Do not install the entire documentation app or all components. The site-level `/registry.json` advertised in `llms.txt` returned HTTP 404 during review; use the documented GitHub registry route, not an assumed working site JSON endpoint. The install command was documented, not executed during this catalog update.
- Registry files may target `components/ui/*`, `lib/utils.ts`, and `lib/motion-tokens.ts`. Preserve existing helpers, aliases, tokens, and other users of those files; merge only missing exports instead of overwriting them. Check sibling-component imports as well as package dependencies.
- Reuse terms: the public repository contains an [MIT license](https://github.com/Surajmaurya1/easyui/blob/main/LICENSE), copyright 2026 Suraj Maurya. Keep its copyright and permission notice when redistributing copied code/substantial portions. This source is distinct from other products also called EasyUI.

## Complete Component Index

Categories follow the official catalog even when a component's practical role differs. Search by component name or scenario below; fetch only the selected implementation and props.

### Feedback — 22

| Component / official detail | Selection purpose |
|---|---|
| [Activity Feed](https://www.easyui.site/components/activity-feed) | Filtered audit log with trace and payload inspection |
| [AI Agent Activity](https://www.easyui.site/components/ai-agent-activity) | Expandable tool-event timeline |
| [AI Response](https://www.easyui.site/components/ai-response) | Streaming answer, sources, code, and actions |
| [Batch Gesture Tray](https://www.easyui.site/components/batch-gesture-tray) | Contextual bulk-action tray |
| [Chat](https://www.easyui.site/components/chat) | Conversation history, messages, and composer |
| [FAQ](https://www.easyui.site/components/faq) | Searchable/category-filtered questions |
| [Loader](https://www.easyui.site/components/loader) | Restrained indeterminate loading variants |
| [Morphing Shape Loader](https://www.easyui.site/components/morphing-shape-loader) | SVG path-interpolated loading shapes |
| [Not Found](https://www.easyui.site/components/not-found) | Route-error screen and recovery actions |
| [Notification Bell](https://www.easyui.site/components/notification-bell) | Badge and notification drawer |
| [Notification Stack](https://www.easyui.site/components/notification-stack) | Stacked cards with dismissal gesture |
| [Orbital Loading Ring](https://www.easyui.site/components/orbital-loading-ring) | Layered orbit-style processing indicator |
| [Payment Receipt Printer](https://www.easyui.site/components/payment-receipt-printer) | Paper-extrusion receipt presentation |
| [Payment Status](https://www.easyui.site/components/payment-status) | Transaction result and receipt/recovery actions |
| [Pull to Refresh](https://www.easyui.site/components/pull-to-refresh) | Elastic refresh threshold and async feedback |
| [Recovery Ledger](https://www.easyui.site/components/recovery-ledger) | Snapshots, diffs, and restore callback |
| [Rocket Party Popper](https://www.easyui.site/components/rocket-party-popper) | Rare milestone celebration |
| [Smooth Accordion](https://www.easyui.site/components/smooth-accordion) | Spring-height expandable panels |
| [Stack Unfold Panel](https://www.easyui.site/components/stack-unfold-panel) | Stacked progressive disclosure |
| [Undo Toast](https://www.easyui.site/components/undo-toast) | Timed reversal action with countdown |
| [UnfoldAccordion](https://www.easyui.site/components/unfold-accordion) | Coordinated content, chevron, and spacing |
| [VelocityToast](https://www.easyui.site/components/velocity-toast) | Settling arrival and pausable dismissal |

### Forms — 8

| Component / official detail | Selection purpose |
|---|---|
| [Advanced Data Table](https://www.easyui.site/components/advanced-data-table) | Sort/filter/select, expand rows, and paginate |
| [Animated File Upload](https://www.easyui.site/components/animated-file-upload) | Drop target, file states, and retry presentation |
| [DrawCheckbox](https://www.easyui.site/components/draw-checkbox) | Drawn checkmark feedback |
| [Form](https://www.easyui.site/components/form) | Composable fields and validation states |
| [LockInput](https://www.easyui.site/components/lock-input) | Focus-ring and border continuity |
| [OTP Input](https://www.easyui.site/components/otp-input) | Code entry with digit advancement |
| [SpringSelect](https://www.easyui.site/components/spring-select) | Trigger-anchored spring menu |
| [StretchSwitch](https://www.easyui.site/components/stretch-switch) | Tactile stretch/snap toggle |

### Motion — 40

| Component / official detail | Selection purpose |
|---|---|
| [Airport Matrix Clock](https://www.easyui.site/components/airport-matrix-clock) | World-time display with rolling matrix glyphs |
| [Animated Number Morph](https://www.easyui.site/components/animated-number) | Rolling digits for selected metrics |
| [Car Smoke Page Transition](https://www.easyui.site/components/car-smoke-page-transition) | Deliberate cinematic route transition |
| [Circular Orbit](https://www.easyui.site/components/circular-orbit) | Orbiting image showcase |
| [Cursor Follower](https://www.easyui.site/components/cursor-follower) | Fine-pointer follower with custom content |
| [Density Lens](https://www.easyui.site/components/density-lens) | Pointer-guided detail magnification |
| [Dependency Trace](https://www.easyui.site/components/dependency-trace) | Inspectable SVG relationship graph |
| [Depth Corridor](https://www.easyui.site/components/depth-corridor) | Perspective layer tunnel |
| [Dot Field](https://www.easyui.site/components/dot-field) | Static canvas dot backdrop |
| [Dot Shader](https://www.easyui.site/components/dot-shader) | GPU pointer-reactive dot backdrop |
| [Evil Eye](https://www.easyui.site/components/evil-eye) | Pointer-reactive hanging amulet |
| [Expandable Data Row](https://www.easyui.site/components/expandable-data-row) | Inline record details and mobile cards |
| [Focus Mode](https://www.easyui.site/components/focus-mode) | Isolate a region by dimming its surroundings |
| [Glitch Text](https://www.easyui.site/components/glitch-text) | Short cybernetic headline treatments |
| [Glyph Matrix](https://www.easyui.site/components/glyph-matrix) | Canvas glyph-rain background |
| [Gravity Particle Burst](https://www.easyui.site/components/gravity-particle-burst) | Brief pointer-triggered particle feedback |
| [Interactive Timeline](https://www.easyui.site/components/interactive-timeline) | Milestones, pipeline nodes, and details |
| [macOS Folder Cards](https://www.easyui.site/components/mac-os-folder-cards) | Folder-shaped collection reveal |
| [Meteors](https://www.easyui.site/components/meteors) | Decorative diagonal light trails |
| [Metric HUD](https://www.easyui.site/components/metric-hud) | Time-series summary and point inspection |
| [Morphing Blob](https://www.easyui.site/components/morphing-blob) | Ambient SVG shape with pointer response |
| [Morphing Icon](https://www.easyui.site/components/morphing-icon) | Coordinated glyph-state transition |
| [Nimbu Mirchi](https://www.easyui.site/components/nimbu-mirchi) | Hanging charm with spring response |
| [Particle Delete](https://www.easyui.site/components/particle-delete) | Expressive particle removal feedback |
| [Pricing](https://www.easyui.site/components/pricing) | Quiet two-tier pricing composition |
| [Profile Card](https://www.easyui.site/components/profile-card) | Profile anatomy and expandable details |
| [Rainbow Button](https://www.easyui.site/components/rainbow-button) | Chromatic CTA edge and underglow |
| [Reveal Card](https://www.easyui.site/components/reveal-card) | Tilt/glare showcase card |
| [Scroll Velocity Text](https://www.easyui.site/components/scrollvelocitytext) | Scroll-responsive short typography |
| [Shooting Stars](https://www.easyui.site/components/shooting-stars) | Celestial canvas atmosphere |
| [Sparkles Core](https://www.easyui.site/components/sparkles-core) | Canvas particle sparkle backdrop |
| [Speed Warp](https://www.easyui.site/components/speed-warp) | High-intensity perspective starfield |
| [Spotlight Card](https://www.easyui.site/components/spotlight-card) | Pointer-local surface illumination |
| [Stacked Cards](https://www.easyui.site/components/stacked-cards) | Sticky scroll-stacking collection |
| [Sticky Pages](https://www.easyui.site/components/sticky-pages) | Full-section sticky stacking |
| [Story Cards](https://www.easyui.site/components/story-card) | Responsive story carousel |
| [Text Scramble Decoder](https://www.easyui.site/components/text-scramble-decoder) | Technical reveal resolving to readable copy |
| [Thinking Orb](https://www.easyui.site/components/thinking-orb) | Decorative AI-state companion |
| [Torque Dial](https://www.easyui.site/components/torque-dial) | Rotational control with inertia |
| [Wallet Card](https://www.easyui.site/components/wallet-card) | Balance/actions with local shine |

### Navigation — 14

| Component / official detail | Selection purpose |
|---|---|
| [Animated Tabs](https://www.easyui.site/components/animated-tabs) | Sliding active pill and content transition |
| [Branching Submenu](https://www.easyui.site/components/branching-submenu) | Hierarchical action navigation |
| [Dynamic Island](https://www.easyui.site/components/dynamic-island) | Shared-layout compact-to-expanded surface |
| [Expandable Search](https://www.easyui.site/components/expandable-search) | Focus-expanding search field |
| [Floating Action Dock](https://www.easyui.site/components/floating-action-dock) | Magnifying quick-action dock |
| [Glass Navbar](https://www.easyui.site/components/glass-navbar) | Responsive glass navigation shell |
| [Gooey Menu](https://www.easyui.site/components/gooey-menu) | Expressive liquid dropdown |
| [Hamburger Menu](https://www.easyui.site/components/hamburger-menu) | Menu/close icon morph |
| [iOS-style Search Bar](https://www.easyui.site/components/ios-search-bar) | Search pill with focus and clear states |
| [Pill Navigation](https://www.easyui.site/components/pill-navigation) | Shared active pill and submenus |
| [Scroll Progress Navigation](https://www.easyui.site/components/scroll-progress-nav) | Document outline and active-section progress |
| [SlidePagination](https://www.easyui.site/components/slide-pagination) | Sliding current-page indicator |
| [Small Floating Dock](https://www.easyui.site/components/small-floating-dock) | Compact primary-action dock |
| [Smart Comparison](https://www.easyui.site/components/smart-comparison) | Searchable feature/difference matrix |

### Overlays — 10

| Component / official detail | Selection purpose |
|---|---|
| [Avatar Stack](https://www.easyui.site/components/avatar-stack) | Overlapping participant identities |
| [Command Menu](https://www.easyui.site/components/command-menu) | Keyboard-first grouped command palette |
| [DirectionalTooltip](https://www.easyui.site/components/directional-tooltip) | Origin-aware tooltip entrance |
| [Intro Loader](https://www.easyui.site/components/intro-loader) | Skippable welcome/loading sequence |
| [Morphing Dialog](https://www.easyui.site/components/morphing-dialog) | Card-to-dialog spatial continuity |
| [OriginDropdown](https://www.easyui.site/components/origin-dropdown) | Trigger-origin menu expansion |
| [Peek Card](https://www.easyui.site/components/peek-card) | Edge-aware contextual preview |
| [Selection Basket](https://www.easyui.site/components/selection-basket) | Floating selected-record actions |
| [SettleModal](https://www.easyui.site/components/settle-modal) | Short settling modal entrance |
| [Spotlight Search](https://www.easyui.site/components/spotlight-search) | Global search overlay and active result |

### Buttons — 12

| Component / official detail | Selection purpose |
|---|---|
| [Book Call Button](https://www.easyui.site/components/book-call-button) | Expanding accent CTA |
| [Button](https://www.easyui.site/components/button) | Variants, sizes, loading, and icon slots |
| [Code Snippet Deck](https://www.easyui.site/components/code-snippet-deck) | Language tabs, parameters, and code copying |
| [Drag to Confirm](https://www.easyui.site/components/drag-to-confirm) | Deliberate gesture plus accessible confirmation |
| [Liquid Ripple Button](https://www.easyui.site/components/liquid-ripple-button) | Pointer-origin press ripple |
| [Liquid Toggle](https://www.easyui.site/components/liquid-toggle) | Blob-shaped toggle continuity |
| [Magnetic Button](https://www.easyui.site/components/magnetic-button) | Fine-pointer proximity pull |
| [Morphing Button](https://www.easyui.site/components/morphing-button) | Stable idle/loading/success/error geometry |
| [Neon Edge Button](https://www.easyui.site/components/neon-edge-button) | Travelling edge-light emphasis |
| [PressButton](https://www.easyui.site/components/press-button) | Brief compression and settle |
| [Split Button](https://www.easyui.site/components/split-button) | Primary action with related-action menu |
| [Typewriter Button](https://www.easyui.site/components/typewriter-button) | Short label reveal with optional sound |

### Auth — 2

| Component / official detail | Selection purpose |
|---|---|
| [Login](https://www.easyui.site/components/login) | Authentication form composition |
| [Sign Up](https://www.easyui.site/components/sign-up) | Registration and password-validation presentation |

## Activity Feed: Implementation Contract and Caveats

Anatomy: category/search controls, chronological event rows, type and textual status, actor/time/duration, trace copy, expandable payload, optional replay action. Use restrained insertion and expansion rather than decorative motion on every log refresh.

- `events: ActivityEvent[]`: source requires the prop, though destructuring defaults to `[]`. Stable `id`, `type`, `status`, `title`, and `timestamp` are core fields; optional fields include `isoTimestamp`, `description`, `actor`, `traceId`, `duration`, and `payload`.
- `enableLiveSimulation` defaults to `true`: this exposes a toggle for random demo events, **not a real subscription**. Set it to `false` in production and supply actual API/SSE/WebSocket events. Do not ship demo deployment/security messages as facts.
- `enableFilters` and `enableSearch` default to `true`; adapt the built-in deploy/security/api/system/error vocabulary to the project's real event types if necessary.
- `maxEntries` defaults to `20`, but the reviewed source only applies the cap when inserting **simulated** events. Bound/paginate real incoming data upstream; passing thousands of `events` does not automatically prune or virtualize them. Keep durable audit history in the backend, not this viewport.
- `onEventReplay` receives the selected event but performs no replay itself. A retry/replay is a real external action: implement authorization, deduplication, confirmation where warranted, and observable failure before enabling it. Do not replay automatically when expanding a payload.
- Sanitize/redact secrets and personal data in payloads before display/copy. Check Clipboard API success before showing copied feedback; the reviewed trace-copy handler does not await success.
- The page's accessibility claims are not sufficient proof: the reviewed root uses `role="region"`, not a full feed/log implementation, and this component has no direct reduced-motion branch. Add/verify appropriate semantics, restrained live announcements, compliance with the Skill's Default Motion Policy, focus, and reading-position stability in the actual app.

## Other Source-Specific Decisions

- **AI Agent Activity / AI Response / Chat / Thinking Orb:** drive status, durations, citations, tool inputs/results, and content from real task/message records. Display safe progress summaries, not private chain-of-thought. The orb is decoration, not task evidence. Review streaming cancellation, autoscroll, readable code/source links, and sanitization; a block called “production-ready” is not backend integration.
- **Recovery Ledger:** `onRestore(id)` may return a promise; `currentEntryId` remains application-controlled. The source clears its busy state in `finally` but does not provide a complete failure UI. Handle rejected restore operations and update current/history state only after backend confirmation. **Undo Toast** likewise needs an actual reversal operation, not just the toast's reversal animation.
- **Code Snippet Deck:** renders parameterized code and supports copying/language switching. Despite catalog wording suggesting a runner, its reviewed props do not expose code execution. Do not imply snippets ran or add automatic execution.
- **Advanced Data Table / Expandable Data Row / batch controls:** inspect pagination/large-list cost rather than assuming virtualization. Persist selected IDs across relevant filters, expose batch result/partial failure, keep row expansion keyboard-operable, and prevent mobile cards from hiding essential fields.
- **Payment Status / Receipt Printer / Wallet Card / pricing/auth/upload:** visual blocks are not payment verification, authentication, uploads, durable receipts, or real prices. Wire actual APIs and error/retry/permission states; do not let animation completion set business success.
- **Motion and visual styling:** some recipes contain fixed dark surfaces and tiny text. Map these to project tokens, contrast, density, and actual light/dark themes instead of copying the showcase theme. Shared spring presets are tuning references, not mandatory project-wide constants; reuse existing motion tokens.
- **Pointer/canvas/WebGL/showcase recipes:** preserve static/touch equivalents, semantic text, bounded DPR/particle work, offscreen pause, and listener/RAF/timer/GPU cleanup. Avoid ornamental backgrounds behind dense operational data. Keep Typewriter Button sound opt-in; provide keyboard alternatives to drag confirmation and Torque Dial, and Escape/focus-return for isolation and overlays.

## Refreshing This Source

Compare the live `llms.txt`, `registry.json`, and repository catalog IDs before changing counts. A cached Activity Feed sidebar observed during review listed only 106 entries; the current official index and source registry both list 108, including Airport Matrix Clock and Dynamic Island. Count registry component IDs once, not props, variants, demo presets, or shared utility files. When selecting a recipe later, recheck its exact current source and dependencies; this catalog does not guarantee that future versions retain the reviewed API.
