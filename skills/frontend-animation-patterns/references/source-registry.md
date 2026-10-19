# Source Registry and Update Procedure

Use this file when the user provides another frontend UI, component, style, interaction, or animation website and asks to extend the Skill.

## Registered Sources

| Source | Role | Reference | Last reviewed |
|---|---|---|---|
| [UIArc / Arc UI](https://uiarc.dev/llms.txt) | 262 indexed entries: 168 components (including 44 special) + 94 blocks; 134 Free, 128 Pro; 21 chart-family entries | `uiarc.md` | 2026-10-19 |
| [EasyUI](https://www.easyui.site/components/activity-feed) | 108 React/Tailwind/Framer Motion components across feedback, forms, motion, navigation, overlays, buttons, and authentication | `easy-ui.md` | 2026-10-07 |
| [Rewamp UI](https://www.rewampui.com/components/gradient-reveal-text) | 70 expressive React/Framer Motion/Three.js components across backgrounds, buttons, text, toggles, cursors, navigation, search, sidebars, cards, and AI orbs | `rewamp-ui.md` | 2026-09-23 |
| [Beautiful UI](https://www.beautifului.dev/) | 21 AI-native interface components for streaming, tools, approvals, evidence, tasks, data edits, and agent workspaces | `beautiful-ui.md` | 2026-09-03 |
| [beUI](https://beui.dev/components/motion) | 76 public Motion controls, application blocks, and AI agent interface patterns | `beui.md` | 2026-08-17 |
| [Transitions.dev](https://transitions.dev/) | Product transitions and micro-interactions | `transitions-dev.md` | 2026-08-13 |
| [Magic UI](https://magicui.design/docs/components) | React/Tailwind showcase components and visual effects | `magic-ui.md` | 2026-08-13 |
| [MicroInteractions UI](https://www.microinteractionsui.com/) | React/Tailwind/shadcn animated controls | `microinteractions-ui.md` | 2026-08-15 |
| [COSS UI](https://coss.com/ui/docs/components/accordion) | 54 accessible, composable React product primitives and element styles | `coss-ui.md` | 2026-08-16 |
| [React Bits](https://reactbits.dev/get-started/index) | 166 public text animations, general effects, components, and backgrounds | `react-bits.md` | 2026-08-16 |

Current indexed catalog: **879 reference entries across 10 sources** (including Free and restricted/Pro items). Counts represent source entries, not deduplicated concepts; the selection matrix resolves overlap by scenario. Each source count is its own last-reviewed snapshot, not a claim that all sites were refreshed together.

## Update Procedure

1. Browse the new source's official catalog, installation guide, representative component pages, visual anatomy, interaction states, accessibility guidance, and license/access notes when available.
2. Record the source's intended stack and delivery model: plain CSS, Web API, React/Vue/Svelte component, animation library, paid recipe, or visual inspiration only.
3. Create `references/<source-slug>.md` containing:
   - official URLs and review date;
   - concise component, style, and effect names grouped by element role and interaction purpose;
   - exact component/detail links;
   - stack/dependency constraints;
   - free, paid, Pro, experimental, or browser-support limits;
   - element anatomy, visual/state guidance, and accessibility/performance cautions specific to that source.
4. Add only genuinely useful new mappings to `selection-matrix.md`. Prefer the strongest existing recipe when the source merely duplicates it.
5. Link the new reference from `SKILL.md` and add it to the registry table.
6. Update the description when the new source introduces trigger phrases or a materially new class of styling, component, interaction, or animation tasks.
7. Regenerate `agents/openai.yaml` if the Skill's user-facing purpose changed.
8. Run the host's `quick_validate.py` when available; otherwise validate the frontmatter, relative reference links, catalog coverage, and unfinished placeholders directly. Check every newly added official URL.

Do not copy entire external documentation pages into the Skill. Summarize selection knowledge and link to the current official implementation source.
