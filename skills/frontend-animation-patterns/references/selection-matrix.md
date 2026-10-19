# Element Style and Motion Selection Matrix

Read this file before choosing a component style or animation. Start from the element's role and the user's interaction goal, not from the most visually impressive demo.

## Element Styling and Composition

| User need | First choice | Alternatives | Avoid |
|---|---|---|---|
| Determinate upload, export, or long-running task progress | COSS UI **Progress** with label and textual value | Existing project progress primitive styled to the same anatomy | Fake progress, color-only meaning, or a bar without status text |
| Work is running but completion percentage is unknown | Spinner or explicitly indeterminate status | Skeleton when content shape is known | A determinate progress bar with invented percentages |
| Neutral product component needs clear anatomy and accessible states | COSS UI pattern adapted to project tokens | Existing Base UI/Radix/headless primitive | Copying the COSS site theme or replacing an established design system |
| Hero headline needs an expressive media-filled treatment | React Bits **Masked Heading** | Static gradient/image-clipped text; Magic UI Text Animate | Dense dashboards, forms, long reading text, or unreadable media contrast |
| Premium headline needs a slow continuous color sweep | Rewamp UI **Gradient Reveal Text** | React Bits Gradient Text; Magic UI Animated Gradient Text | Body copy, several competing gradient headings, or no solid-color fallback |
| Decorative heading must remain semantic and resilient | Native `h1`/`h2` with static text fallback | Masked Heading with missing-media fallback | Rendering essential copy only in canvas/video or hiding it from assistive tech |
| Product form needs consistent labels, validation, grouping, and controls | COSS UI **Field / Fieldset / Form** plus the matching input primitive | Existing accessible design-system form components | Styling standalone inputs without error, disabled, and focus states |
| Searchable choice among many options | COSS UI **Combobox / Autocomplete** | Select for a short fixed list; Command for command/search palettes | A custom dropdown without keyboard navigation |
| Measured status is not task completion | COSS UI **Meter** | Progress only for completion; textual value | Reporting a score or capacity as task progress |
| Empty, loading, and loaded states need one visual system | COSS UI **Empty / Skeleton / Spinner** | Existing project status primitives | Showing a spinner forever or using skeletons with the wrong content shape |
| Dense data needs neutral presentation | COSS UI **Table / Pagination / Scroll Area** | Existing data-grid primitives | Decorative motion on every row or hiding horizontal overflow |
| Audit/telemetry events need filters, trace IDs, and expandable payloads | EasyUI **Activity Feed** | Existing log view; EasyUI Interactive Timeline for milestones | Enabled live simulation in production, exposed secrets, or treating a retained viewport as the full audit history |
| Dense records need inspectable details and mobile card presentation | EasyUI **Expandable Data Row / Advanced Data Table** | COSS Table; existing data grid | No virtualization for large data, fake row actions, or hidden keyboard access |
| Selected items need a contextual batch toolbar | EasyUI **Selection Basket / Batch Gesture Tray** | Existing bulk-action bar | Applying to unselected records, hidden partial failures, or drag-only actions |
| Version history needs diff inspection and explicit restoration | EasyUI **Recovery Ledger** | Existing version timeline plus confirmation | Restore animation without a real backend operation, authorization, or error recovery |
| API documentation needs language switching and parameterized examples | EasyUI **Code Snippet Deck** | Existing accessible code tabs | Calling it a code runner, leaking credentials, or executing generated snippets automatically |
| Technical dashboard needs inspectable time-series metrics | EasyUI **Metric HUD** | Existing chart; beUI chart primitives | Demo series presented as telemetry, pointer-only inspection, or unreadable units |
| Related nodes or dependencies need inspectable connection tracing | EasyUI **Dependency Trace** | Magic UI Animated Beam for a simple illustrative relationship | Drawing a diagram as evidence of actual execution or no textual relationship alternative |
| Plans/products need a searchable, difference-focused feature matrix | EasyUI **Smart Comparison** | Static semantic comparison table | Invented plan features or mobile views that hide important differences |
| Transaction result needs confirmation, receipt, and recovery actions | EasyUI **Payment Status / Payment Receipt Printer** | Existing order confirmation | Receipt animation used as payment proof or unconnected download/retry buttons |
| Hero copy needs a static expressive treatment | React Bits **Gradient Text / Shiny Text / Stroke Text** | Masked Heading; native gradient text | Multiple simultaneous text effects or weak contrast |
| Hero or section copy needs an entrance | React Bits **Split Text / Blur Text / Fold Text / Scroll Reveal** | Magic UI Text Animate; Transitions.dev Texts reveal | Per-character animation on long body copy |
| Short phrases rotate or loop | React Bits **Text Loop / Rotating Text** | Magic UI Word Rotate / Morphing Text | Large layout shifts between phrases |
| Highlighted KPI needs animated counting | React Bits **Count Up** | Magic UI Number Ticker; Transitions.dev Spinning counter | Animating every number in a dense dashboard |
| Media needs one strong reveal or transition | React Bits **Pixel Transition / Halftone Reveal / Scroll Expand** | Fade Content; Animated Content | Stacking several reveal effects on the same media |
| Showcase card or gallery needs spatial interaction | React Bits **Tilted Card / Magic Bento / Circular Gallery / Depth Carousel** | Magic UI Magic Card; Transitions.dev 3D tilt | Using pointer-dependent interaction without touch/keyboard fallback |
| Small editorial collection needs a theatrical spatial browser | Rewamp UI **Perspective Flip Deck / Editorial 3D Orbit Carousel / Arch Card Carousel** | React Bits Depth Carousel; static responsive grid | Essential content available only through drag/3D motion or automatic rotation |
| Branded navigation needs an expressive presentation | React Bits **Pill Nav / Card Nav / Gooey Nav / Staggered Menu** | COSS Tabs/Menu/Toolbar for product UI | Replacing clear product navigation with novelty motion |
| Hero needs a quiet animated background | React Bits **Aurora / Silk / Threads / Dot Grid / Gradient Waves** | Magic UI grid/light backgrounds | Reducing text contrast or running multiple canvas backgrounds |
| Hero needs a pointer-reactive technical backdrop | Rewamp UI **Elastic Line Grid / Spotlight Grid / Ripple Grid** | React Bits Dot Grid; static grid with radial hover | Touch-only experiences, blocked clicks, or pointer work running offscreen |
| Hero needs a cinematic WebGL material or atmosphere | Rewamp UI **Soft Aurora / Water Caustics / Silk Waves / Singularity Flare** | CSS gradient or static image fallback | Dense product screens, uncapped DPR, no renderer cleanup, or no unsupported-browser fallback |
| Showcase needs a high-energy background | React Bits **Hyperspeed / Lightning / Ballpit / Liquid Chrome** | Lower-energy React Bits background | Dense product pages, forms, low-power devices, or no unsupported-browser fallback |
| Action needs idle, loading, success, and error continuity | beUI **Stateful Button** | MicroInteractions UI Button5; Transitions.dev spinner-to-check | Decorative timers or reporting success before the operation completes |
| Select or popover should visibly grow from its trigger | beUI **Select Morph / Popover Morph** | Transitions.dev Dropdown menu morph | Losing focus management or making the morph slower than selection |
| Mobile workflow needs a draggable edge surface | beUI **Bottom Sheet** | COSS Drawer/Sheet; beUI Drawer | Desktop-only assumptions, missing snap semantics, or trapping scroll incorrectly |
| Mobile content refresh needs physical threshold feedback | beUI **Pull to Refresh** | Native refresh behavior | Triggering refresh before threshold or lacking async/error state |
| App navigation needs desktop rail and mobile panel continuity | beUI **Animated Sidebar** | Preview Rail; COSS navigation primitives | Hover-only labels or a mobile panel without focus management |
| Status notifications need a compact stack and readable expansion | beUI **Animated Toast Stack / Notification Stack** | Transitions.dev Toast; COSS Toast | Hiding actions, auto-dismissing critical errors, or motion-only status |
| Dense interactive data needs virtualization and restrained motion | beUI **Table** | COSS Table; project data grid | Animating every row or rendering 10k rows without virtualization |
| Upload workflow needs queue, retry, delete, and real progress | beUI **File Upload block** | COSS Progress plus project uploader | Fake progress or missing failure/retry states |
| AI product needs one coherent workspace reference | Beautiful UI **Ice Cream Harness** composition | Existing app shell plus selected Beautiful UI primitives | Shipping the scripted demo data or copying the whole visual theme unchanged |
| AI work has no reliable percentage but elapsed time is useful | Beautiful UI **Loading State** | beUI Loading States; textual indeterminate status | Invented progress, endless animation after completion, or no cancel/error path |
| AI activity needs expandable steps, searches, coding, and tool events | Beautiful UI **Thinking + Tool Chips** | EasyUI AI Agent Activity; beUI Agent Activity | Exposing private chain-of-thought, fabricated steps, or treating animation as proof of work |
| AI answer streams with sources, actions, and follow-ups | Beautiful UI **Streaming Text** | EasyUI AI Response; beUI Streaming Response / Message Scroller | Layout shift, forced autoscroll, or decorative citations without resolvable sources |
| AI task contains several independently verifiable stages | Beautiful UI **Task Rows** | beUI Todo List / Agent Activity | Marking the parent complete from one successful child step |
| AI tool needs a structured multi-question permission gate | Beautiful UI **Approval Card** | beUI Tool Approval / Approval Card | Preselected consent, unclear action scope, or executing on option selection |
| AI recommendation needs confidence and alternatives | Beautiful UI **Recommendation Card** | Existing decision card | Unexplained confidence, hiding “needs review,” or auto-accepting the recommendation |
| AI answer needs inspectable retrieval or memory chunks | Beautiful UI **Context Cards** | beUI Citations; existing evidence drawer | Source-looking badges that cannot open or be verified |
| AI proposes structured record changes | Beautiful UI **Diff Table** | Code Block diff for text/code | Applying generation immediately, hiding add/remove counts, or unclear selected rows |
| AI augments a data grid with model-generated properties | Beautiful UI **Records Table** | Existing data grid with an explicit AI column | Untraceable values, missing grounding/input configuration, or animating thousands of rows |
| AI composer needs files, sources, commands, model choice, and dictation | Beautiful UI **Prompt Bar** | Existing accessible composer | Showing unavailable integrations as connected or hiding selected model/source state |
| User edits content by selecting a passage | Beautiful UI **Selection Actions** | Native selection toolbar plus explicit apply/revert | Replacing text without preview, recovery, or selection context |
| User watches or teaches a remote agent | Beautiful UI **Agent Screen** | Existing remote-view surface | Hidden recording, no stop control, placeholder media presented as live, or relying on its unavailable registry endpoint |
| AI response streams without layout shift | beUI **Streaming Response / Message Scroller** | Existing chat primitives | Forcing autoscroll after the reader moves away |
| AI task execution needs visible structured progress | beUI **Agent Activity / Todo List / Loading States** | Existing job timeline | Fabricated reasoning text or stale completion states |
| AI tool use requires an explicit permission decision | beUI **Tool Approval / Approval Card** | Existing confirmation dialog | Animating past consent, preselecting approval, or hiding scope |
| AI answer needs inspectable source support | beUI **Citations** | Existing citation list | Decorative source badges without resolvable references |

## Charts and Visual Data

| User need | First choice | Alternatives | Avoid |
|---|---|---|---|
| Daily activity or streaks over months/year | UIArc **Activity heatmap** (Free) | Existing calendar heatmap | Treating missing dates as zero without a data contract; confusing this with a category × hour matrix |
| Inspectable multi-series time trend | UIArc **Line chart** (Free) | Existing chart stack; EasyUI Metric HUD | Missing series values silently rendered as zero, unclear units, or too many points |
| Long history needs a draggable overview window | UIArc **Brush chart** (Free) | Existing zoomable time-series chart | Unsorted times, negative/log-scale data unsupported by the recipe, or brush state disconnected from filters |
| One metric across discrete periods | UIArc **Bar chart** (Free) | Existing column/bar chart | Copying a single-series recipe as though it supports every grouped/stacked chart |
| Part-to-whole composition | UIArc **Donut chart / Waffle chart** (Free) | Existing semantic chart; Bar chart for exact comparisons | Non-positive values discarded silently, unclear denominator, or relying on rounded cell counts as raw data |
| Exactly two moments need a change comparison | UIArc **Slope chart** (Free) | Existing grouped bar chart | Using it for three or more time points or overcrowding item labels |
| Many groups need distribution-shape comparison | UIArc **Ridgeline** (Free) | Existing box plot/histogram | Inventing observations from averages or changing domains without explanation |
| Hierarchical quantities need drilldown | UIArc **Treemap** (Free) | Existing hierarchy table; Sunburst (Pro) with licensed access | Negative leaf values clamped silently, unstable ids, or missing way back up |
| Real-time, flow, funnel, or rank replay needs advanced data interaction | UIArc **Realtime stream / Sankey flow / Funnel chart / Race bar chart** (Pro) | Existing licensed chart stack; free Line/Bar/Treemap for an appropriate simpler view | Copying Pro source without access or presenting simulated animation as real execution/telemetry |
| Image edit/redesign needs before-and-after inspection | UIArc **Image compare** (Free) | Existing accessible comparison slider | Different image crops, drag-only operation, or implying the slider processes images |

## Product UI and State Changes

| User need | First choice | Alternatives | Avoid |
|---|---|---|---|
| Card expands, collapses, or changes content size | Transitions.dev **Card resize** | panel reveal; CSS grid-row transition | Animating fixed height guesses |
| Dropdown/menu appears | **Menu dropdown** | Dropdown menu morph for a strong spatial transformation | Long bounce or background particles |
| Modal/dialog appears | **Modal open/close** | panel reveal for side sheets | Large travel distance; slow exit |
| Side panel/drawer opens | **Panel reveal** | page side-by-side | Hiding focus or moving the entire app unnecessarily |
| Tabs switch | **Tabs sliding** | MicroInteractions UI Tabs1–5 for a complete React/shadcn control | Crossfading all page content on every tab |
| Tooltip appears | **Tooltip open/close** | short opacity/translate transition | Delayed exit; motion-only explanation |
| Toast/notification appears | **Toast open/close** | Notification badge for count changes | Confetti for ordinary status updates |
| Loading resolves to content | **Skeleton loader and reveal** | spinner-to-check morph (Pro) for a single action | Infinite shimmer after content is ready |
| Success feedback | **Success check** | checkbox check; Magic UI Confetti for a rare milestone | Celebration for routine autosave |
| Error feedback | **Error state shake** | color/message transition | Repeated shaking or motion without error text |
| Checkbox/toggle changes | **Checkbox check** / **Toggle** | icon swap | Custom control without native semantics |
| Metric/value changes | **Number pop-in** or **Spinning counter** | Magic UI Number Ticker; MicroInteractions UI Input2 for user-controlled increments | Animating every refresh in a dense table |
| Icon changes state | **Icon swap** | success check | Rotating the whole button when only the glyph changes |
| Input is cleared | **Input clear with dissolve** | immediate clear when app motion is explicitly off | Per-character motion in high-frequency forms |
| Page/step navigation | **Page side-by-side** | MicroInteractions UI Stepper1/2 for a React multi-step form; View Transitions API | Losing scroll/focus or faking navigation state |
| High-consequence action benefits from a deliberate slide gesture | Rewamp UI **Slide To Confirm Button** | Native confirmation dialog plus ordinary button | Using drag as the only keyboard/assistive-tech path or implying consent before completion |
| Accordion expands | **Accordion** | Card resize | Fixed-duration clipping for long dynamic content |
| Destructive action completes | native fade/collapse | Delete with smoky dissolve (Pro) only for expressive contexts | Making the user wait for deletion animation |
| Social login button needs hover continuity | MicroInteractions UI **Button1** (Google) / **Button8** (Apple) | restrained icon swap | Replacing provider branding or hiding the label |
| Primary action needs in-button progress | MicroInteractions UI **Button5** | spinner-to-check morph (Pro); success check | Reporting completion before the real operation succeeds |
| CTA label/background should swap on hover | MicroInteractions UI **Button2–4** | Transitions.dev Learn more hover | Making essential text unavailable to keyboard/touch users |
| Inline value/tag switches between view and edit | MicroInteractions UI **Input1** | icon swap plus native input | Disabled-looking controls without an accessible edit action |
| Quantity/input stepper changes | MicroInteractions UI **Input2** | immediate numeric update | Motion without announced value changes or min/max handling |
| Theme icon/toggle changes | MicroInteractions UI **Theme Toggle1/2** | Magic UI Animated Theme Toggler; immediate swap | Visual icon swap without updating the actual theme state |
| Compact vertical icon navigation | MicroInteractions UI **Navbar1** | native active-indicator transition | Tooltip-only labels without accessible names |
| Compact search should morph from icon to input | Rewamp UI **Morph Search Capsule** | native expandable search field | Losing input focus, obscuring the label, or hiding result/loading states |
| AI assistant needs an ambient visual presence | Rewamp UI **Marbled / Particle Dot / Fluid Morph / Wireframe Ring / Particle Morph Orb** | Static branded avatar plus textual status | Treating the orb as the only status channel or fabricating agent activity |

## Marketing, Content, and Brand Motion

| User need | First choice | Alternatives | Guidance |
|---|---|---|---|
| Quiet section/hero entrance | Magic UI **Blur Fade** | Transitions.dev Texts reveal | Use one direction and a small stagger |
| Rich headline entrance | **Text Animate** | Text Reveal, Dia Text Reveal, Hyper Text | Preserve readable text when app motion is explicitly off |
| Rotating value proposition | **Word Rotate** / **Morphing Text** | Typing Animation | Keep phrases similar in length to limit layout shift |
| KPI count-up | **Number Ticker** | Transitions.dev Spinning counter | Trigger once in view; render the final number accessibly |
| Customer logos/testimonials | **Marquee** | Avatar Circles | Pause or simplify when app motion is explicitly off; do not hide essential content |
| Integration/data-flow diagram | **Animated Beam** | Orbiting Circles, Icon Cloud | Use only when relationships are meaningful |
| Premium card hover | **Magic Card** / **Glare Hover** | Border Beam, Shine Border, 3D tilt | Provide focus-visible feedback and a static touch state |
| Branded navigation needs one highly tactile signature | Rewamp UI **Hero Morph / Pill Expand / Liquid Underline Navbar** | React Bits Pill Nav; COSS navigation primitive | Novelty motion that obscures routes, focus, active state, or mobile close behavior |
| Primary CTA emphasis | **Interactive Hover Button** | Shimmer Button, Ripple Button, Pulsating Button | Choose one CTA effect, not several |
| Rare success/launch moment | **Confetti** | Transitions.dev Confetti burst (Pro) | User-triggered, brief, and never required for comprehension |
| Theme change | **Animated Theme Toggler** | immediate theme swap | Use View Transitions fallback; preserve controlled theme state |
| Long article/page progress | **Scroll Progress** | Text Reveal for selected sections | Avoid scroll hijacking |
| Scrollable list edge cue | **Progressive Blur** | static gradient mask | Keep content readable and pointer-accessible |
| Hero background ambience | Particles, Meteors, Light Rays, Animated Grid Pattern | Flickering Grid, Ripple, Warp Background | Decorative only; reduce/stop continuous motion |
| Showcase cursor | Smooth Cursor | Pointer | Restrict to fine pointers and brand/showcase pages, not forms or dashboards |
| Media/product inspection | Lens | 3D tilt / Image open tilt (Pro) | Provide touch and keyboard alternatives |

## Visual and Motion Intensity Ladder

1. **Foundation:** legible typography, spacing, component anatomy, focus, disabled, loading, success, and error states.
2. **Supportive:** state transitions, section reveal, count-up, content sequencing, and subtle hover lift.
3. **Signature:** one hero text treatment, integration diagram, or branded card interaction.
4. **Celebratory:** confetti or particles after a rare user achievement.

Always complete level 1. Then use the lowest additional level that solves the communication problem. Dense product surfaces should usually stay at levels 1–2; marketing heroes may use one level-3 effect.

## Framework Routing

- Plain HTML/CSS/vanilla: favor Transitions.dev recipes and native CSS/View Transitions.
- React 19 + TypeScript + CSS Modules + Motion: UIArc is a candidate for controls, charts, image comparison, and business blocks; inspect registry files, foundation/global-style impact, data semantics, and Free/Pro access. Tailwind is not required.
- React + Base UI + Tailwind: COSS UI components are candidates after checking the exact component API and license path.
- React + Tailwind + Framer Motion + shadcn GitHub registry: EasyUI is a candidate for tactile controls and developer/product blocks; inspect its shared utility targets, actual callback behavior, and per-component accessibility before copying.
- React/Next + Tailwind + Motion + shadcn registry: beUI components are candidates for complete animated controls, application blocks, and AI agent surfaces.
- React hero/editorial surfaces: React Bits patterns are candidates after checking dependencies, semantics, media fallbacks, and license terms.
- React/Next + Tailwind + shadcn conventions: Magic UI components are candidates after checking current docs and dependencies.
- React + Tailwind + shadcn + Motion: MicroInteractions UI registry recipes are candidates for complete interactive controls; inspect each recipe rather than assuming uniform dependencies.
- React/Next + Tailwind v4 AI products: Beautiful UI primitives are candidates after installing or mapping the shared foundation and inspecting each registry dependency; use the Harness as composition guidance, not production state.
- React 19 + Tailwind v4 + Framer Motion showcase surfaces: Rewamp UI is a candidate for one signature effect; inspect the component registry, verify reuse terms, and add Three.js only when the selected recipe requires it.
- Existing Motion/Framer Motion: adapt the chosen pattern to existing primitives rather than adding duplicate animation infrastructure.
- Existing GSAP or complex timelines/scroll choreography: use a relevant GSAP skill when available; otherwise use the project's library and official documentation. Keep this catalog as the visual recipe selector.
- Vue/Svelte: reproduce behavior with native CSS or the project's animation stack; do not paste React-only Magic UI code.
