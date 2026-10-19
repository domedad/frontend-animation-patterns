# MicroInteractions UI Catalog

Official source: [MicroInteractions UI](https://www.microinteractionsui.com/) · [GitHub repository](https://github.com/mateusmachry/microinteractionsui)

Last reviewed: 2026-08-15.

Use this source for complete animated controls in a compatible React project. The current catalog contains 20 shadcn Registry recipes across Tabs, Button, Input, Theme Toggle, Stepper, and Navbar. The site identifies React, TypeScript, Tailwind CSS, shadcn/ui, and Motion as its stack.

Install a selected recipe through its exact Registry URL, for example:

```bash
npx shadcn@latest add https://microinteractionsui.com/r/button1.json
```

Inspect the JSON before installation because dependencies vary by recipe. Most use `motion`; some also require Radix/shadcn primitives, `react-aria-components`, `next-themes`, `lucide-react`, badges, tooltips, avatars, or scroll areas.

## Animated Tabs

Catalog page: [Tabs](https://www.microinteractionsui.com/tabs)

- [Tabs1](https://microinteractionsui.com/r/tabs1.json) — segmented tabs with an animated active surface and directional panel enter/exit.
- [Tabs2](https://microinteractionsui.com/r/tabs2.json) — Tabs1 behavior with count/status badges.
- [Tabs3](https://microinteractionsui.com/r/tabs3.json) — text tabs with a moving underline and animated content identity.
- [Tabs4](https://microinteractionsui.com/r/tabs4.json) — icon-and-label tabs with an active underline.
- [Tabs5](https://microinteractionsui.com/r/tabs5.json) — compact icon tabs whose selected label expands while inactive labels collapse.

Use these when the entire React/shadcn tab control is in scope. Prefer Transitions.dev Tabs sliding when only an existing indicator transition needs refinement.

## Animated Buttons

Catalog page: [Button](https://www.microinteractionsui.com/button)

- [Button1](https://microinteractionsui.com/r/button1.json) — Google sign-in button; icon and label slide while a directional arrow enters on hover.
- [Button2](https://microinteractionsui.com/r/button2.json) — CTA with a growing icon container and rotating arrow.
- [Button3](https://microinteractionsui.com/r/button3.json) — configurable directional swap between default and hover labels/backgrounds.
- [Button4](https://microinteractionsui.com/r/button4.json) — simple hover fill that expands across the button.
- [Button5](https://microinteractionsui.com/r/button5.json) — payment action with real progress fill, compacting container, and completion check.
- [Button6](https://microinteractionsui.com/r/button6.json) — continuous masked shimmer with a small hover press/scale response.
- [Button7](https://microinteractionsui.com/r/button7.json) — CSS gradient border and hover glow; no Motion dependency in the current recipe.
- [Button8](https://microinteractionsui.com/r/button8.json) — Apple sign-in counterpart to Button1.

Bind Button5 progress and completion to the real operation state; never run a decorative timer that reports false success. Use continuous Button6 shimmer only for a single high-priority action and disable it when app motion is explicitly off, not automatically from system settings.

## Animated Inputs

Catalog page: [Input](https://www.microinteractionsui.com/input)

- [Input1](https://microinteractionsui.com/r/input1.json) — inline value/tag editor with rotating, crossfading edit/save controls.
- [Input2](https://microinteractionsui.com/r/input2.json) — numeric stepper whose value rolls with a direction-aware spring; currently uses `react-aria-components`.

Preserve editable semantics, validation, min/max constraints, keyboard input, and announced value changes. Treat motion as feedback around the control, not as the control's state model.

## Theme Toggles

Catalog page: [Theme Toggle](https://www.microinteractionsui.com/theme-toggle)

- [Theme Toggle1](https://microinteractionsui.com/r/theme-toggle1.json) — spring thumb slide plus sun/moon directional swap; uses `next-themes`.
- [Theme Toggle2](https://microinteractionsui.com/r/theme-toggle2.json) — similar behavior with `lucide-react` icons.

Keep the actual theme state controlled and persistent. Provide an immediate icon/theme change when app motion is explicitly off; otherwise retain the animation regardless of system settings.

## Steppers

Catalog page: [Stepper](https://www.microinteractionsui.com/stepper)

- [Stepper1](https://microinteractionsui.com/r/stepper1.json) — vertical multi-step layout.
- [Stepper2](https://microinteractionsui.com/r/stepper2.json) — horizontal multi-step layout.
- Both depend on the shared [Stepper primitive](https://microinteractionsui.com/r/stepper.json), which animates connector completion with transforms and transitions the indicator to a completed check.

Use for genuine multi-step state. Keep current, completed, inactive, loading, disabled, and validation states derived from the workflow rather than the animation.

## Compact Navigation

Catalog page: [Navbar](https://www.microinteractionsui.com/navbar)

- [Navbar1](https://microinteractionsui.com/r/navbar1.json) — vertical icon rail with a spring-scaled selected background, tooltips, separators, avatar, and settings slot.

Keep accessible names even when the layout is icon-only. Preserve `aria-pressed`, focus-visible styling, and a non-hover path to labels.

## Access and Reuse Notes

- The repository and Registry JSON endpoints were publicly accessible at review time, and the README documents shadcn CLI installation.
- No root `LICENSE` file or `license` package field was observed at review time. Do not infer an open-source reuse license from public access alone; confirm the current repository terms before commercial redistribution or copying substantial implementation code.
- Treat every recipe as source code copied into the project. Review dependencies, styling assumptions, semantics, compliance with the Skill's Default Motion Policy, and cleanup instead of installing the full catalog.
