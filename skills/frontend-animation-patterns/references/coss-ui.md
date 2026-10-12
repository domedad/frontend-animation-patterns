# COSS UI Catalog

- Official catalog: [COSS UI Components](https://coss.com/ui/docs/components/accordion)
- Official repository: [cosscom/coss](https://github.com/cosscom/coss)
- Last reviewed: 2026-08-16
- Public components indexed: 54

## Contents

- [Role and routing](#role-and-routing)
- [Disclosure and overlays](#disclosure-and-overlays)
- [Forms and selection](#forms-and-selection)
- [Navigation and actions](#navigation-and-actions)
- [Status, content, and data](#status-content-and-data)
- [Implementation guidance](#implementation-guidance)
- [Access and license](#access-and-license)

## Role and routing

COSS UI is the Cal.com design system: composable React product primitives built with Base UI and Tailwind CSS. Use it for restrained element styling, accessible component anatomy, complete interaction states, and dense product surfaces. Adapt components to the host project's tokens instead of copying the documentation site's brand theme.

Use the groups below to find a candidate, then open the exact official page before implementation to confirm its current API, dependencies, examples, and installation command.

## Disclosure and overlays

- [Accordion](https://coss.com/ui/docs/components/accordion) — collapsible content with rotating chevron and animated height.
- [Alert Dialog](https://coss.com/ui/docs/components/alert-dialog) — blocking confirmation for consequential actions.
- [Collapsible](https://coss.com/ui/docs/components/collapsible) — compact show/hide region without accordion grouping.
- [Context Menu](https://coss.com/ui/docs/components/context-menu) — pointer or keyboard-invoked contextual actions.
- [Dialog](https://coss.com/ui/docs/components/dialog) — modal task or focused content.
- [Drawer](https://coss.com/ui/docs/components/drawer) — edge-originating, often touch-friendly overlay.
- [Menu](https://coss.com/ui/docs/components/menu) — grouped action menu.
- [Popover](https://coss.com/ui/docs/components/popover) — anchored non-modal content.
- [Preview Card](https://coss.com/ui/docs/components/preview-card) — anchored preview for a referenced item.
- [Sheet](https://coss.com/ui/docs/components/sheet) — side-panel workflow or supporting detail.
- [Toast](https://coss.com/ui/docs/components/toast) — transient status feedback.
- [Tooltip](https://coss.com/ui/docs/components/tooltip) — short supplementary explanation, never the only accessible label.

## Forms and selection

- [Autocomplete](https://coss.com/ui/docs/components/autocomplete)
- [Calendar](https://coss.com/ui/docs/components/calendar)
- [Checkbox](https://coss.com/ui/docs/components/checkbox)
- [Checkbox Group](https://coss.com/ui/docs/components/checkbox-group)
- [Combobox](https://coss.com/ui/docs/components/combobox)
- [Date Picker](https://coss.com/ui/docs/components/date-picker)
- [Field](https://coss.com/ui/docs/components/field)
- [Fieldset](https://coss.com/ui/docs/components/fieldset)
- [Form](https://coss.com/ui/docs/components/form)
- [Group](https://coss.com/ui/docs/components/group)
- [Input](https://coss.com/ui/docs/components/input)
- [Input Group](https://coss.com/ui/docs/components/input-group)
- [Label](https://coss.com/ui/docs/components/label)
- [Number Field](https://coss.com/ui/docs/components/number-field)
- [OTP Field](https://coss.com/ui/docs/components/otp-field)
- [Radio Group](https://coss.com/ui/docs/components/radio-group)
- [Select](https://coss.com/ui/docs/components/select)
- [Slider](https://coss.com/ui/docs/components/slider)
- [Switch](https://coss.com/ui/docs/components/switch)
- [Textarea](https://coss.com/ui/docs/components/textarea)
- [Toggle](https://coss.com/ui/docs/components/toggle)
- [Toggle Group](https://coss.com/ui/docs/components/toggle-group)

## Navigation and actions

- [Breadcrumb](https://coss.com/ui/docs/components/breadcrumb)
- [Button](https://coss.com/ui/docs/components/button)
- [Command](https://coss.com/ui/docs/components/command)
- [Pagination](https://coss.com/ui/docs/components/pagination)
- [Tabs](https://coss.com/ui/docs/components/tabs)
- [Toolbar](https://coss.com/ui/docs/components/toolbar)

## Status, content, and data

- [Alert](https://coss.com/ui/docs/components/alert)
- [Avatar](https://coss.com/ui/docs/components/avatar)
- [Badge](https://coss.com/ui/docs/components/badge)
- [Card](https://coss.com/ui/docs/components/card)
- [Empty](https://coss.com/ui/docs/components/empty)
- [Frame](https://coss.com/ui/docs/components/frame)
- [Kbd](https://coss.com/ui/docs/components/kbd)
- [Meter](https://coss.com/ui/docs/components/meter)
- [Progress](https://coss.com/ui/docs/components/progress)
- [Scroll Area](https://coss.com/ui/docs/components/scroll-area)
- [Separator](https://coss.com/ui/docs/components/separator)
- [Skeleton](https://coss.com/ui/docs/components/skeleton)
- [Spinner](https://coss.com/ui/docs/components/spinner)
- [Table](https://coss.com/ui/docs/components/table)

## Implementation guidance

- Prefer COSS when a product primitive needs complete anatomy and state behavior, not merely a visual effect.
- Reuse the project's spacing, color, type, radius, and shadow tokens. Treat the COSS appearance as a structural reference.
- Preserve Base UI semantics, focus management, keyboard behavior, accessible names, and controlled/uncontrolled state contracts.
- Use Accordion for grouped disclosure and Collapsible for one independent region. Do not substitute either for navigation.
- Use Dialog or Alert Dialog for modal work, Sheet or Drawer for edge panels, Popover for anchored non-modal content, and Tooltip only for supplementary help.
- Use Skeleton for known content shape, Spinner for unknown-duration work, Progress for measurable completion, and Meter for a bounded reading that is not task completion.
- Bind loading, progress, success, and error visuals to real application state.
- Verify custom children required by compound components. For example, custom Progress content must retain its track and indicator.

Most recipes install through the shadcn CLI using `@coss/<slug>`, but confirm the current command on the component page rather than deriving it blindly.

## Access and license

The repository uses mixed licensing. Its README identifies `apps/ui/` and `apps/origin/` as MIT while other repository areas use AGPLv3. Confirm the exact source path and current license before copying code outside the registry workflow.
