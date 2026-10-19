# Beautiful UI Catalog

- Official gallery: [Beautiful UI](https://www.beautifului.dev/)
- Composed agent demo: [Ice Cream Harness](https://www.beautifului.dev/harness)
- Source and implementation guide: [GitHub repository](https://github.com/slev12397/beautiful-ui)
- Machine-readable registry: [registry.json](https://www.beautifului.dev/r/registry.json)
- License: [MIT](https://www.beautifului.dev/license)
- Last reviewed: 2026-09-03

Use Beautiful UI for AI-native product surfaces where the interface must make model activity, tool use, evidence, approvals, proposed changes, and human control legible. The public gallery currently contains **21 components**. The Harness is a composed reference screen and is not counted as an additional component.

## Stack and Delivery Model

- Built with Next.js App Router, React, TypeScript, and Tailwind CSS v4.
- Components are copy-paste primitives. The recommended path is `npx shadcn add https://www.beautifului.dev/r/<slug>.json`; inspect the component registry entry before installing because dependencies vary.
- Install the shared `app/globals.css` foundation once. It supplies light/dark tokens, Tailwind `@theme` mappings, shadows, keyframes, and `prefers-reduced-motion` fallbacks upstream. Adapt those system-driven fallbacks to the Skill's Default Motion Policy; do not let them disable selected app animations automatically.
- Some components import shared primitives such as `Button`, `GlideMenu`, `EntityChip`, `ValuePill`, `Shimmer`, or `StreamText`; the registry resolves these dependencies.
- Some recipes use packages such as `liveline`, `glimm`, or `iconoir-react`. `Sidebar Nav` uses the commercial `@central-icons-react` package unless those icons are replaced.
- The library is MIT licensed. Preserve the copyright and permission notice when redistributing substantial portions.
- As reviewed, 20 gallery components appear in the top-level registry. `Agent Screen` is visible with copyable code, but its advertised `/r/agent-screen.json` endpoint returns 404; use manual copy and verify dependencies until the registry is corrected.

## Agent Feedback and Execution

| Pattern | Use it for | State and motion guidance | Official link |
|---|---|---|---|
| Loading State | Indeterminate AI work with visible elapsed time | Pixel-grid shimmer; choose one of Drive, Dots, Orbit, or Surfer. Keep a textual status and stop the loop when work completes. | [Loading State](https://www.beautifului.dev/#loading-state) |
| Thinking | Expandable agent traces for steps, reasoning, search, or coding | Collapse by default when detail is secondary; animate disclosure, not fabricated chain-of-thought. Present safe summaries or real tool events. | [Thinking](https://www.beautifului.dev/#thinking-state) |
| Streaming Text | Token/word streaming with inline sources, actions, and follow-up prompts | Append without reflowing previous content, preserve reading position, and reveal citations only when resolvable. | [Streaming Text](https://www.beautifului.dev/#streaming-text) |
| Tool Chips | Compact tool calls, edits, messages, files, and results | Expand a grouped chip into inspectable events; distinguish running, success, and failure with text and iconography. | [Tool Chips](https://www.beautifului.dev/#tool-chips) |
| Task Rows | Multi-step agent execution with running, failed, and completed states | Use expandable rows or compact capsules; derive progress from actual events and never infer completion from animation. | [Task Rows](https://www.beautifului.dev/#task-rows) |

## Conversation and Human Control

| Pattern | Use it for | State and motion guidance | Official link |
|---|---|---|---|
| Approval Card | Human-in-the-loop questions before an agent acts | Support single/multi-select, custom answers, previous/next, skip, and disabled continuation. Show scope and consequence before approval. | [Approval Card](https://www.beautifului.dev/#approval-card) |
| Chat | Tabbed conversations with reasoning summaries and a composer | Keep message order stable, make active thread state explicit, and avoid forced autoscroll after the reader moves upward. | [Chat](https://www.beautifului.dev/#chat-composer) |
| Prompt Bar | Prompt composition with attachments, `@` sources, `/` commands, model selection, dictation, and send state | Treat each control as a real capability with a labeled menu and disabled/loading state; do not present decorative integrations as connected. | [Prompt Bar](https://www.beautifului.dev/#prompt-bar) |
| Selection Actions | Rewrite, explain, shorten, change tone, or fix selected text | Anchor the toolbar to a real selection, keep the original recoverable, and show an explicit pending/apply result. | [Selection Actions](https://www.beautifului.dev/#selection-actions) |

## Recommendations, Evidence, and Proposed Changes

| Pattern | Use it for | State and motion guidance | Official link |
|---|---|---|---|
| Recommendation Card | Agent proposal with confidence, alternatives, and accept action | Explain the evidence behind confidence, separate “needs review” from “no signal,” and require a deliberate accept action. | [Recommendation Card](https://www.beautifului.dev/#recommendation-card) |
| Context Cards | Retrieved knowledge or memory chunks with source metadata | Show document type, source identity, excerpt size, and selection/filter state. Never use source-looking badges without resolvable evidence. | [Context Cards](https://www.beautifului.dev/#context-cards) |
| Diff Table | AI-proposed additions/removals across structured rows | Make changed rows selectable, summarize add/remove counts, and keep “Apply changes” separate from generation. | [Diff Table](https://www.beautifului.dev/#diff-table) |
| Insight Cards | Paged AI insights paired with a compact live chart and follow-up action | Animate the chart only when it clarifies the selected insight; retain exact values and a static view when app motion is explicitly off. | [Insight Cards](https://www.beautifului.dev/#insight-cards) |

## Data, Navigation, and Workflow Surfaces

| Pattern | Use it for | State and motion guidance | Official link |
|---|---|---|---|
| Records Table | CRM/data-grid views with sorting, tags, relationships, and AI-computed properties | Keep column resize, pinning, selection, tool/model configuration, grounding, inputs, prompts, and row-by-row calculation inspectable. Virtualize large real datasets. | [Records Table](https://www.beautifului.dev/#records-table) |
| Filter Table | Reorganizing live rows by status chips | Update counts and rows from the same state source; preserve table context and announce the new result count. | [Filter Table](https://www.beautifului.dev/#filter-table) |
| Sidebar Nav | Collapsible workspaces, chat history, search, and account/upgrade actions | Use the gliding hover highlight as supporting feedback only; retain visible active state, accessible labels, and keyboard focus when collapsed. | [Sidebar Nav](https://www.beautifului.dev/#sidebar-nav) |
| Search | Command/search surface with live filtering and an empty state | Debounce expensive searches, keep keyboard navigation, and render a meaningful no-results state instead of an empty panel. | [Search](https://www.beautifului.dev/#search) |
| Flowchart | Agent or automation triggers and conditional branches | Use connectors and node states to explain real workflow structure; support pan/zoom only when the graph exceeds the viewport. | [Flowchart](https://www.beautifului.dev/#flowchart) |

## Technical and Agent-Operation Surfaces

| Pattern | Use it for | State and motion guidance | Official link |
|---|---|---|---|
| Code Block | Line-numbered code and unified diff output | Preserve copyable text, language/file identity, keyboard selection, and clear code/diff mode state. | [Code Block](https://www.beautifului.dev/#code-block) |
| Fine-tune Card | AI-assisted design/property inspector | Pair sliders with editable numeric values and labels; preview changes continuously but commit destructive or expensive changes explicitly. | [Fine-tune Card](https://www.beautifului.dev/#fine-tune-card) |
| Agent Screen | Live agent screen viewing, expansion, teaching/recording, and status | Accept a real image/video `streamSrc`; make recording unmistakable, preserve it across collapse only when intended, and provide explicit stop controls. The registry endpoint was unavailable at review time. | [Agent Screen](https://www.beautifului.dev/#agent-screen) |

## Composition Recipe

Use the [Ice Cream Harness](https://www.beautifului.dev/harness) as a layout reference when an AI tool needs a collapsible conversation sidebar, multi-tab workspace, prompt composer, suggested prompts, streaming answer area, tools, approvals, context, data views, and task progress in one coherent shell.

Do not copy its scripted ice-cream demo state into production. Map real backend events to the visible contract:

- token/SSE stream → `Streaming Text`;
- safe reasoning or step events → `Thinking`;
- tool calls and results → `Tool Chips`;
- human confirmation → `Approval Card`;
- retrieval or memory → `Context Cards`;
- proposed structured edits → `Diff Table`;
- real task states → `Task Rows`;
- configured models and connected sources → `Prompt Bar`.

## Source-Specific Guardrails

- Treat these as rendering primitives, not an agent runtime. Replace all scripted demo replies, fake progress, fake confidence, and placeholder records with real state.
- Do not expose hidden chain-of-thought. Render concise reasoning summaries, tool events, citations, and verifiable step results.
- Keep approval separate from execution; opening, expanding, or selecting an option must not itself authorize an external action.
- Streaming, thinking, and task status must share one lifecycle so the page cannot show “working” and “completed” simultaneously.
- Preserve user control over autoscroll, expanded traces, recording, cancellation, and applying AI-proposed changes.
- Reuse the target project's tokens where possible. If adopting the foundation, map its cool neutrals, accent, semantic colors, radii, shadows, and fonts deliberately instead of overwriting unrelated global styles.
