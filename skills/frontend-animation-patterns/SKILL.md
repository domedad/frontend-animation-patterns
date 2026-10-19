---
name: frontend-animation-patterns
license: MIT for original guidance; see LICENSE and THIRD_PARTY_NOTICES.md for scope.
description: Select, style, implement, or refine frontend components, charts, interaction states, and motion from a maintained UI catalog. Use for buttons, cards, inputs, forms, navigation, dialogs, headings, AI chat and agent interfaces, streaming/tool/approval states, chart styling, heatmaps, counters, image comparison, hover/focus/loading feedback, transitions, animated text, scroll and hero effects; or requests for 元素样式、组件样式、页面美化、AI聊天页面、AI工具页面、图表、热力图、数字滚动、图片对比、明暗切换、动效、微交互、入场或滚动动画. Sources include UIArc (Arc UI), EasyUI, Beautiful UI, Rewamp UI, beUI, COSS UI, React Bits, Transitions.dev, Magic UI, MicroInteractions UI, and later cataloged frontend sources.
---

# Frontend Element and Interaction Patterns

Choose the element style, state treatment, and motion together from the interface's product intent. Treat the source sites as pattern libraries, not as permission to copy their whole visual theme or decorate every surface.

## Default Motion Policy

- 默认应用开启动效，不读取或跟随操作系统的“减少动态效果”设置。系统动效关闭时，应用中选定的动效仍正常播放。
- Do not automatically disable, shorten, or replace selected animations because of `prefers-reduced-motion`, `matchMedia`, `useReducedMotion`, or a library's system-driven motion setting. Inspect copied CSS, component hooks, and provider defaults and adapt those gates to this policy within the requested implementation scope.
- Respect an explicit user request or an existing app-level motion-off control. Do not add a new settings screen or motion toggle unless requested. Do not change operating-system settings or unrelated components.
- Source notes about reduced-motion support describe upstream capabilities, not a requirement to follow system settings. Apply this policy when adapting their code. Keep keyboard access, readable status text, performance limits, offscreen pausing, and unsupported-browser fallbacks.

## Workflow

1. Inspect the project before choosing an effect.
   - Read repository instructions and existing design tokens.
   - Identify the framework, styling system, component primitives, installed animation libraries, accessibility conventions, and browser-support constraints.
   - Preserve the project's existing component and animation stacks when they can express the pattern cleanly.
2. Classify the request.
   - **Element styling:** anatomy, shape, spacing, typography, color, border, elevation, and density.
   - **Interaction states:** default, hover, focus-visible, active, selected, disabled, loading, success, and error.
   - **Functional motion:** state, hierarchy, continuity, feedback, and spatial relationships.
   - **Expressive composition:** hero, campaign, brand moment, editorial treatment, or deliberate celebration.
   - If the user did not name a pattern, propose at most three candidates and recommend one with a one-line reason.
3. Read [selection-matrix.md](references/selection-matrix.md) before selecting a recipe.
4. Read the matching source catalog only:
   - [uiarc.md](references/uiarc.md) for React/CSS Modules product controls, the complete UIArc component/block index, chart selection, activity heatmaps, counters, and image comparison; keep Free/Pro boundaries explicit.
   - [easy-ui.md](references/easy-ui.md) for telemetry feeds, inspectable data, batch operations, recovery timelines, AI/chat surfaces, payment feedback, and tactile React controls.
   - [beautiful-ui.md](references/beautiful-ui.md) for AI-native chat and tool interfaces: streaming, thinking, tool calls, approvals, evidence, task progress, proposed edits, and agent workspaces.
   - [rewamp-ui.md](references/rewamp-ui.md) for high-expression Framer Motion and Three.js backgrounds, text, buttons, navigation, cursors, cards, search, toggles, and ambient AI companion orbs.
   - [beui.md](references/beui.md) for copy-in Motion controls, application blocks, and AI agent interface patterns for React/Next.js.
   - [coss-ui.md](references/coss-ui.md) for the full indexed set of restrained, accessible React product primitives and their component anatomy.
   - [react-bits.md](references/react-bits.md) for the full indexed public catalog of expressive React text animations, general effects, components, and backgrounds.
   - [transitions-dev.md](references/transitions-dev.md) for product UI transitions and micro-interactions.
   - [magic-ui.md](references/magic-ui.md) for React/Tailwind marketing components, text effects, backgrounds, and showcase motion.
   - [microinteractions-ui.md](references/microinteractions-ui.md) for React/Tailwind/shadcn control-level motion such as tabs, buttons, inputs, steppers, theme toggles, and compact navigation.
5. Write the element contract below before implementation. Adapt the pattern to existing tokens and components instead of replacing unrelated structure or styling.
6. Implement only the selected pattern and its necessary states.
7. Verify the real interface in a browser, including visual consistency, keyboard use, responsive layout, the default motion policy, and entering/exiting states when animated.

## Selection Rules

- Prefer UIArc for cohesive React chart cards, calendar activity heatmaps, controlled digit rolls, before/after image comparison, and product/data blocks when its CSS Modules and Motion stack fit the project. Read the exact chart's missing-value, scale, date, volume, and license limits before adapting it; do not replace a working chart stack merely for visual similarity.

- Prefer EasyUI for developer/product surfaces needing inspectable telemetry, responsive data details, selection/batch actions, version recovery, API snippets, or AI execution and answer blocks; connect real application state rather than shipping demo simulations.
- Prefer Beautiful UI for data-rich AI-native interfaces where streaming output, agent steps, tool calls, evidence, approvals, recommendations, proposed changes, and human control must form one coherent product surface.
- Prefer Rewamp UI for a React showcase or branded surface that intentionally needs one tactile, kinetic, pointer-reactive, spatial, WebGL, or ambient AI signature effect.
- Prefer beUI for complete copy-in React/Next.js motion controls, application blocks, stateful interaction lifecycles, and AI agent interface patterns.
- Prefer COSS UI for neutral product primitives whose anatomy, labeling, value presentation, and accessible states matter more than visual spectacle.
- Prefer React Bits for expressive headings, hero typography, backgrounds, and branded presentation where the content remains readable without the effect.
- Prefer Transitions.dev for menus, dialogs, panels, tabs, tooltips, toasts, form feedback, loaders, counters, toggles, and other product-state changes.
- Prefer Magic UI for hero reveals, animated typography, social-proof marquees, integration diagrams, decorative card effects, backgrounds, scroll presentation, and celebration.
- Prefer MicroInteractions UI when a compatible React/shadcn project needs a polished, complete interactive control rather than a standalone transition recipe.
- Prefer CSS transitions/keyframes for a contained effect. Reuse an installed Motion/Framer Motion or GSAP stack when the project already depends on it or when orchestration genuinely requires it.
- For scroll-linked sequences, timeline choreography, drag physics, or framework-specific GSAP lifecycle handling, use relevant GSAP skills if the host provides them. Otherwise consult the project's installed library and official documentation; this catalog has no mandatory dependency on another Skill.
- Do not add a library for a single hover, opacity, transform, or state transition that native CSS can handle.
- Do not import a Magic UI component blindly. Confirm React, Tailwind, shadcn-style project structure, required dependencies, and the component's current official documentation first.
- Treat MicroInteractions UI registry recipes the same way: inspect the current JSON, dependencies, semantics, and license status before installation or adaptation.
- Treat Beautiful UI registry recipes the same way: inspect the exact registry JSON and shared foundation before installation; `Agent Screen` may require manual copy while its registry endpoint is unavailable.
- Treat Rewamp UI recipes as visual and implementation references until the exact component, dependency list, registry availability, performance cost, and reuse terms are verified. The CLI metadata alone does not resolve the root repository's licensing ambiguity.
- Do not assume a Transitions.dev Pro recipe is available. Mark Pro candidates and offer a free/native alternative unless the user confirms access.
- Do not combine multiple attention-seeking effects on the same viewport. Default to one signature effect plus quiet supporting micro-interactions.

## Element Contract

For each chosen pattern, state:

- **Role:** what the element helps the user understand or do.
- **Hierarchy:** primary, secondary, supporting, or decorative.
- **Anatomy:** required content and sub-elements.
- **Visual states:** default, hover, focus-visible, active/selected, disabled, loading, success, and error as applicable.
- **Motion:** trigger, purpose, duration/easing, and start/end states, or explicitly none.
- **Recipe/source:** exact catalog name and official URL.
- **Fallback:** missing-media and unsupported-browser behavior; an existing app-level motion-off mode when applicable.
- **Acceptance:** observable appearance, state behavior, responsive behavior, and interaction path.

## Implementation Guardrails

- Reuse the project's color, spacing, radius, typography, shadow, and density tokens. Do not transplant a source site's brand theme wholesale.
- Cover every state the component can actually enter; do not design only the attractive default and hover states.
- Preserve semantic HTML and accessible names. Keep labels, values, error text, and progress meaning available without color or motion.
- Keep typography readable at the actual breakpoint and content length. Decorative text treatments must degrade to ordinary text.
- Keep semantics and state in the DOM. Never communicate success, failure, selection, or progress through motion alone.
- Keep selected animations enabled by default regardless of system motion preferences; apply the Default Motion Policy above.
- Keep keyboard focus visible and ensure hover-only effects have focus-visible or static equivalents.
- Disable fine-pointer-only effects such as custom cursors and 3D tilt on touch-first devices.
- Prefer `transform` and `opacity`. Use `filter` sparingly; avoid animating layout properties when a transform can preserve smoothness.
- Give open and close states separate tuning when needed: entering may be expressive; exiting should usually be quicker and clearer.
- Stop decorative infinite motion when offscreen when practical. Avoid motion behind dense forms, tables, or long reading surfaces.
- Preserve content readability, click targets, scroll position, and focus during transitions.
- Keep animation values in existing design tokens when available. Do not create a new motion-token system for one isolated change.

## Verification

- Run the smallest relevant automated checks for the changed component.
- Exercise the actual page path in a browser at desktop and mobile breakpoints.
- Compare the result with surrounding elements for typography, spacing, radius, borders, elevation, and visual hierarchy.
- Verify every implemented component state, including disabled, loading, success, and error when applicable.
- Verify hover, focus, press, enter, exit, interruption, and repeated triggering as applicable.
- Verify selected animations remain enabled with system reduced motion both on and off. If an app-level motion-off control exists, test it separately; system preferences must not change that application choice.
- Check for clipping, unexpected scrollbars, layout shift, blocked pointer events, lost focus, and stale hidden content.
- Confirm animation cleanup on component unmount and no new console errors.

## Maintaining the Catalog

When the user supplies another frontend UI, component, style, or animation source, follow [source-registry.md](references/source-registry.md). Add a source-specific reference file, merge only useful new scenario mappings into the selection matrix, and revalidate the skill. Keep source access limits and license terms explicit.
