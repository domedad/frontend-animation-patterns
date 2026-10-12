---
name: frontend-animation-patterns
license: MIT for original guidance; see LICENSE and THIRD_PARTY_NOTICES.md for scope.
description: Select, design, implement, audit, or refine frontend element styling, component appearance, interaction states, and motion using a maintained UI catalog. Use when a user asks how buttons, cards, inputs, progress bars, headings, typography, navigation, dialogs, forms, AI agent interfaces, or page sections should look or behave; requests AI chat/tool surfaces, streaming answers, thinking and tool-call states, approval flows, animated backgrounds, custom cursors, AI companion orbs, component variants, visual hierarchy, polish, hover/focus/press/loading/success/error states, micro-interactions, transitions, animated text, scroll effects, hero effects, 元素样式, 组件样式, 按钮样式, 卡片样式, 表单样式, 标题样式, 进度条样式, AI聊天页面, AI工具页面, 智能体界面, 流式回答, 思考状态, 工具调用, 审批卡, 动态背景, 自定义光标, AI状态球, 页面美化, 前端样式搭配, 动效, 交互动效, 页面动画, 过渡动画, 微交互, 悬停效果, 入场动画, or 滚动动画; or wants a suitable pattern from EasyUI, Beautiful UI, Rewamp UI, beUI, COSS UI, React Bits, Transitions.dev, Magic UI, MicroInteractions UI, or later cataloged frontend UI sources.
---

# Frontend Element and Interaction Patterns

Choose the element style, state treatment, and motion together from the interface's product intent. Treat the source sites as pattern libraries, not as permission to copy their whole visual theme or decorate every surface.

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
7. Verify the real interface in a browser, including visual consistency, keyboard use, responsive layout, reduced motion, and entering/exiting states when animated.

## Selection Rules

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
- **Fallback:** reduced-motion, missing-media, and unsupported-browser behavior.
- **Acceptance:** observable appearance, state behavior, responsive behavior, and interaction path.

## Implementation Guardrails

- Reuse the project's color, spacing, radius, typography, shadow, and density tokens. Do not transplant a source site's brand theme wholesale.
- Cover every state the component can actually enter; do not design only the attractive default and hover states.
- Preserve semantic HTML and accessible names. Keep labels, values, error text, and progress meaning available without color or motion.
- Keep typography readable at the actual breakpoint and content length. Decorative text treatments must degrade to ordinary text.
- Keep semantics and state in the DOM. Never communicate success, failure, selection, or progress through motion alone.
- Honor `prefers-reduced-motion: reduce`; remove movement, blur, parallax, rotation, and continuous loops while preserving the final state.
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
- Verify `prefers-reduced-motion` produces an immediate or low-motion equivalent.
- Check for clipping, unexpected scrollbars, layout shift, blocked pointer events, lost focus, and stale hidden content.
- Confirm animation cleanup on component unmount and no new console errors.

## Maintaining the Catalog

When the user supplies another frontend UI, component, style, or animation source, follow [source-registry.md](references/source-registry.md). Add a source-specific reference file, merge only useful new scenario mappings into the selection matrix, and revalidate the skill. Keep source access limits and license terms explicit.
