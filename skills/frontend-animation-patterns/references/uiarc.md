# Arc UI / UIArc Catalog

Official sources: [catalog](https://uiarc.dev/llms.txt), [installation](https://uiarc.dev/docs/installation), [license](https://uiarc.dev/license), [free source repository](https://github.com/kuratlielia/arc-library).
Last reviewed: **2026-10-19**.

## Snapshot and scope

The live machine-readable index lists **262 unique component/block entries**: **168 components** (124 standard + 44 special) and **94 blocks**. Of these, **134 are Free** (112 components + 22 blocks), and **128 are Pro** (56 components + 72 blocks). These are reference entries, not 262 installed, independently tested, or freely redistributable implementations.

Use the live `llms.txt` listing for this dated snapshot. Some rendered sidebars still show older totals (121 standard components / 87 blocks). Do not add the 44 special components to 168 again. Templates, guides, official AI skills, and variants inside a page are not additional component/block entries in this count.

The chart/data-visualization family below contains **21 entries: 13 Free + 8 Pro**, matching the site's Charts and Advanced charts groupings. Animated counter and Data grid belong to that navigation family but are not separate statistical chart types.

## Role, stack, and access

- Prefer Arc for React product controls, cohesive chart cards, image comparison, business blocks, and scenario-specific data interaction. Preserve an existing chart/component stack if it already solves the task.
- Installation targets React 19 + TypeScript. Components use CSS Modules, CSS custom properties, and `motion`; Tailwind is not required. Inspect each registry item's exact dependencies and file targets.
- Free installation example: `npx shadcn@latest add https://uiarc.dev/r/activity-heatmap.json`. Add `https://uiarc.dev/r/arc-foundation.json` once and import the installed `foundation.css` once when needed. The optional `@uiarc` namespace maps to `https://uiarc.dev/r/{name}.json`.
- The foundation includes global selectors as well as tokens: review impact on existing forms/focus styles before importing it. Adapt to project tokens; do not replace an established application's entire design system for one chart.
- Registry TSX and CSS are installed together under the configured components alias, typically `components/arc/<slug>/`; internal relative imports and shared motion tokens matter. Do not paste one TSX file and assume it is standalone.
- Upstream uses `data-theme="dark"` and accent/chart tokens. Map these to the app's real theme state, not a disconnected demo theme.
- Source implementations contain system-driven reduced-motion hooks/CSS. Apply this Skill's **Default Motion Policy** when adapting selected components: animations stay on regardless of system settings; only an explicit app/user choice turns them off. Keep keyboard behavior, performance budgets, offscreen pausing, and readable final values.
- Free implementations are MIT according to the official license; retain their notices if copied. Pro has a separate license and authenticated registry. Indexing public names and scenarios is not authorization to fetch, reconstruct, bundle, or redistribute Pro implementation source. Offer a free alternative or the official purchase path when access is absent.
- This catalog does not install Arc's official skills/MCP, buy Pro, set tokens, or copy paid source. Check current component Markdown at `<page>/markdown` and registry metadata only for the selected implementation.

## Charts and advanced data controls — 21

All descriptions here are selection guidance, not a replacement for current props or live testing.

| Reference | Access | Choose for | Interaction / boundary |
|---|---|---|---|
| [Line chart](https://uiarc.dev/components/line-chart) | Free | 趋势与多序列对比 | 首次描线、区间变形、十字线读值、图例显隐；优先用于需要读准确趋势的看板。 |
| [Bar chart](https://uiarc.dev/components/bar-chart) | Free | 离散周期或类别的单指标比较 | 柱体入场、稳定 key 驱动的区间切换、均值参考线；不是多系列通用柱图。 |
| [Donut chart](https://uiarc.dev/components/donut-chart) | Free | 一个整体的构成 | 分段弧形变换、中心数字滚动、图例筛选；类别多或差异很小时改用条形图。 |
| [Streamgraph](https://uiarc.dev/components/streamgraph) | Free | 多类别随时间变化的构成与节奏 | 流层变形、图层聚焦、时间读值；精确比较优先折线，负值不适用，需固定基线可核对 offset=zero。 |
| [Brush chart](https://uiarc.dev/components/brush-chart) | Free | 长时间序列的局部放大 | 总览窗拖动/缩放、预设范围平滑移动、事件标记；日期升序、毫秒时间窗，默认最小跨度需适配业务。 |
| [Waffle chart](https://uiarc.dev/components/waffle-chart) | Free | 单位格表示整体占比 | 格子按类别迁移、图例与百分比联动；显示真实百分比及舍入规则，不能把格数误当原始数量。 |
| [Slope chart](https://uiarc.dev/components/slope-chart) | Free | 恰好两个时点的变化 | 端点和连线变形、名次变化；约 3–10 项可读，多时点改用折线。 |
| [Sparkline](https://uiarc.dev/components/sparkline) | Free | 指标卡或表格行内的小趋势 | 短线描绘、可选滑动读值；密集表格关闭逐个交互，避免大量焦点与监听器。 |
| [Gauge](https://uiarc.dev/components/gauge) | Free | 已知上下限的单值指标 | 弧线和读数随值变化、阈值文字提示；容量/评分不是任务完成进度。 |
| [Activity heatmap](https://uiarc.dev/components/activity-heatmap) | Free | 按日活跃度、连续记录与空闲周期 | 按周列排布、色阶、格子入场、日期选择与提示；不是任意行列的业务矩阵。 |
| [Animated counter](https://uiarc.dev/components/animated-counter) | Free | 独立的总数、价格和指标 | 数字逐位上下滚动、位数增减过渡、可选入视从零播放；少量重点指标使用。 |
| [Ridgeline](https://uiarc.dev/components/ridgeline) | Free | 多个分组的分布形状 | 分布曲线变形、聚焦分组与分位数读值；提供原始观测值，不用均值伪造分布。 |
| [Treemap](https://uiarc.dev/components/treemap) | Free | 多层分类的数量构成 | 矩形面积重排、层级下钻与面包屑返回；稳定节点 id，面积与颜色的指标分别说明。 |
| [Split bar](https://uiarc.dev/components/split-bar) | Pro | 紧凑的整体占比条 | 分段聚焦、图例重排；须有 Pro 授权，不将被放大的悬停面积当作新的真实占比。 |
| [Sunburst](https://uiarc.dev/components/sunburst) | Pro | 探索层级构成 | 同心层级与下钻；Pro。免费替代参考 Treemap 或层级表。 |
| [Sankey flow](https://uiarc.dev/components/sankey-flow) | Pro | 跨阶段的分流、合流 | 路径追踪与流量关系；Pro。数值须来自实际节点和连边，不是执行成功的证据。 |
| [Funnel chart](https://uiarc.dev/components/funnel-chart) | Pro | 有序步骤的转化与流失 | 步骤聚焦、分组切换；Pro。先定义人数/事件口径、分母与去重窗口。 |
| [Radar chart](https://uiarc.dev/components/radar-chart) | Pro | 少量对象的多维画像 | 轮廓切换与逐轴比较；Pro。量纲/上限需可比，精确比较可改用柱图。 |
| [Realtime stream](https://uiarc.dev/components/realtime-stream) | Pro | 实时监控数据 | 持续时间窗与异常标记；Pro。没有真实数据源时不得把示例波动当实时遥测。 |
| [Race bar chart](https://uiarc.dev/components/race-bar-chart) | Pro | 历史名次变化的回放 | 时间轴播放/暂停和排名重排；Pro。稳定对象 id 与完整时间帧，回放不冒充直播数据。 |
| [Data grid](https://uiarc.dev/components/data-grid) | Pro | 类似电子表格的结构化编辑 | 选区、编辑、填充与表格操作；Pro。这是高级数据控件，不应计为独立统计图类型。 |

## Chart contracts and source-specific traps

- **Business data first:** specify metric, unit, grouping, time zone/business date, range, ordering, aggregation, unique identity, missing-data policy, and interaction callbacks before rendering. Demo data, playback, particle flow, and animation are not live operational facts.
- **Missing is not zero:** the reviewed Line chart substitutes zero for a missing series value. Activity heatmap fills missing dates with zero; its implementation sums duplicate dates and clamps negative counts. Validate and aggregate upstream; if absent/unknown days must remain distinct, adapt the selected component or choose another chart instead of silently treating them as no activity.
- **Heatmap contract:** pass `days: { date: "YYYY-MM-DD", count: number }[]`, with explicit calendar-day interpretation. Review UTC conversion against the application's business time zone. Fix comparable thresholds across periods when comparison matters; default data-relative levels can make equal colors mean different counts. Use `onSelectDate` to open genuine date details. A date picker, geographic heatmap, and category × hour matrix are different patterns.
- **Scale and sign:** Donut excludes non-positive values; the reviewed Treemap clamps leaf size below zero to zero. Do not use these to hide losses or negative balances. Brush chart documentation excludes negative/log-scale use cases; Streamgraph is for non-negative magnitudes. Surface a clear unsupported-data state or use the existing chart stack.
- **Identity and totals:** stable keys/ids preserve correspondence during range and dataset changes. Explain whether hiding a series recomputes the visible total. Keep formatted units, decimals, rates, legend totals, tooltip values, and downloadable/table values consistent.
- **Interaction:** use pointer and keyboard paths, visible focus, named chart regions, and text/table alternatives. Readout, selection, range, and drilldown callbacks do not load data or persist edits automatically; wire them to the real application with loading/empty/error states.
- **Volume:** the Line chart is intended for a few hundred points per series; Brush chart is the long-history option with a summary strip. A year of heatmap cells is not virtualized. Dense Sparkline tables should avoid hundreds of independent focusable scrubbers; test actual volume rather than adopting demo performance claims.
- **Motion:** retain selected first-view reveals, digit rolls, crosshair movement, and data transitions by default. Stop offscreen/hidden-tab loops and clean up observers/canvas/listeners on unmount. Range changes must not obscure the final data or present interpolated values as new measurements.
- **Pro analytical blocks:** Revenue explorer, Cohort retention, MRR waterfall, Usage forecast, Metric explorer, KPI drilldown, Budget variance, Small multiples, Connected scatter, Line replay, Market terminal, Choropleth explorer, and Activity terrain are indexed below. Consult their public descriptions as composition references; use licensed implementations only with confirmed access. Forecasts and illustrative 3D terrain must not replace factual data or uncertainty labels.

## Image comparison

[Image compare](https://uiarc.dev/components/image-compare) is Free: compare two images with a controlled/uncontrolled divider, horizontal or vertical orientation, touch dragging, and keyboard steps. Keep identical crop, dimensions, and meaningful alt text for both images. `position` is a percentage and `onPositionChange` reports a settled divider position, not an image-processing operation. Preserve the focusable slider, arrow/Page/Home/End controls, and vertical page scrolling. Use a carousel for many images and resizable panels for live content.

## Complete remaining component/block index

Each line is one directory entry. **Pro** means licensed/restricted; unmarked items are Free in this snapshot. The 21 chart-family entries above are omitted here to avoid counting them twice. Section labels follow the machine-readable index, not the narrower site sidebar groups.

### Actions — 19

- [Button](https://uiarc.dev/components/button)
- [Action button](https://uiarc.dev/components/action-button)
- [Split button](https://uiarc.dev/components/split-button)
- [Button group](https://uiarc.dev/components/button-group)
- [Floating button group](https://uiarc.dev/components/floating-button-group)
- [Expanding button group](https://uiarc.dev/components/expanding-button-group)
- [Copy button](https://uiarc.dev/components/copy-button)
- [Icon morph](https://uiarc.dev/components/icon-morph)
- [Confirm morph](https://uiarc.dev/components/confirm-morph)
- [Hold to confirm](https://uiarc.dev/components/hold-to-confirm)
- [Swipe actions](https://uiarc.dev/components/swipe-actions)
- [Reactions](https://uiarc.dev/components/reactions)
- [Dropdown menu](https://uiarc.dev/components/dropdown-menu)
- [Context menu](https://uiarc.dev/components/context-menu)
- [User menu](https://uiarc.dev/components/user-menu)
- [Theme switcher](https://uiarc.dev/components/theme-switch)
- [Eclipse](https://uiarc.dev/components/theme-switch-eclipse)
- [Split](https://uiarc.dev/components/theme-switch-split)
- [Rise](https://uiarc.dev/components/theme-switch-rise)

### Inputs — 36

- [Input](https://uiarc.dev/components/input)
- [Textarea](https://uiarc.dev/components/textarea)
- [Password field](https://uiarc.dev/components/password-field)
- [Password strength](https://uiarc.dev/components/password-strength)
- [Search field](https://uiarc.dev/components/search-field)
- [Expanding search](https://uiarc.dev/components/expanding-search)
- [Inline edit](https://uiarc.dev/components/inline-edit)
- [Number field](https://uiarc.dev/components/number-field)
- [Money input](https://uiarc.dev/components/money-input)
- [Phone input](https://uiarc.dev/components/phone-input)
- [Tag input](https://uiarc.dev/components/tag-input)
- [Mention input](https://uiarc.dev/components/mention-input)
- [Shortcut recorder](https://uiarc.dev/components/shortcut-recorder)
- [Select](https://uiarc.dev/components/select)
- [Combobox](https://uiarc.dev/components/combobox)
- [Multi-select](https://uiarc.dev/components/multi-select)
- [Morph select](https://uiarc.dev/components/morph-select)
- [Chip group](https://uiarc.dev/components/chip-group)
- [Radio cards](https://uiarc.dev/components/radio-cards)
- [Billing toggle](https://uiarc.dev/components/billing-toggle)
- [Checkbox](https://uiarc.dev/components/checkbox)
- [Radio group](https://uiarc.dev/components/radio-group)
- [Switch](https://uiarc.dev/components/switch)
- [Segmented control](https://uiarc.dev/components/segmented-control)
- [Slider](https://uiarc.dev/components/slider)
- [Elastic slider](https://uiarc.dev/components/elastic-slider)
- [Calendar](https://uiarc.dev/components/calendar)
- [Date picker](https://uiarc.dev/components/date-picker)
- [Date range picker](https://uiarc.dev/components/date-range-picker)
- [Time picker](https://uiarc.dev/components/time-picker)
- [Color picker](https://uiarc.dev/components/color-picker)
- [Emoji picker](https://uiarc.dev/components/emoji-picker) — **Pro**
- [Rich text editor](https://uiarc.dev/components/rich-text-editor)
- [Signature pad](https://uiarc.dev/components/signature-pad)
- [File dropzone](https://uiarc.dev/components/file-dropzone)
- [Avatar upload](https://uiarc.dev/components/avatar-upload) — **Pro**

### Disclosure — 15

- [Tabs](https://uiarc.dev/components/tabs)
- [Breadcrumb](https://uiarc.dev/components/breadcrumb)
- [Mega menu morph](https://uiarc.dev/components/mega-menu-morph) — **Pro**
- [Scroll area](https://uiarc.dev/components/scroll-area)
- [Accordion](https://uiarc.dev/components/accordion)
- [Expandable card](https://uiarc.dev/components/expandable-card)
- [Resizable panels](https://uiarc.dev/components/resizable-panels)
- [Expandable text](https://uiarc.dev/components/expandable-text)
- [Dialog](https://uiarc.dev/components/dialog)
- [Drawer](https://uiarc.dev/components/drawer)
- [Bottom sheet](https://uiarc.dev/components/bottom-sheet)
- [Popover](https://uiarc.dev/components/popover)
- [Hover card](https://uiarc.dev/components/hover-card)
- [Tooltip](https://uiarc.dev/components/tooltip)
- [Share access](https://uiarc.dev/components/share-access) — **Pro**

### Feedback — 10

- [Alert](https://uiarc.dev/components/alert)
- [Toast](https://uiarc.dev/components/toast)
- [Toast stack](https://uiarc.dev/components/toast-stack)
- [Announcement bar](https://uiarc.dev/components/announcement-bar)
- [Cookie consent](https://uiarc.dev/components/cookie-consent)
- [Progress](https://uiarc.dev/components/progress)
- [Skeleton](https://uiarc.dev/components/skeleton)
- [Stepper](https://uiarc.dev/components/stepper)
- [Countdown](https://uiarc.dev/components/countdown)
- [Usage meter](https://uiarc.dev/components/usage-meter)

### Other data, tables, activity, and media — 19

- [Pagination](https://uiarc.dev/components/pagination)
- [Avatar](https://uiarc.dev/components/avatar)
- [Avatar group](https://uiarc.dev/components/avatar-group)
- [Badge](https://uiarc.dev/components/badge)
- [Presence stack](https://uiarc.dev/components/presence-stack) — **Pro**
- [Card](https://uiarc.dev/components/card)
- [Metric card](https://uiarc.dev/components/metric-card)
- [Empty state](https://uiarc.dev/components/empty-state)
- [Sortable data table](https://uiarc.dev/components/sortable-data-table)
- [Tree view](https://uiarc.dev/components/tree-view)
- [Filter toolbar](https://uiarc.dev/components/filter-toolbar)
- [Code block](https://uiarc.dev/components/code-block)
- [JSON viewer](https://uiarc.dev/components/json-viewer)
- [Timeline](https://uiarc.dev/components/timeline)
- [Comment thread](https://uiarc.dev/components/comment-thread)
- [Chat thread](https://uiarc.dev/components/chat-thread)
- [Image compare](https://uiarc.dev/components/image-compare)
- [Carousel](https://uiarc.dev/components/carousel)
- [Card stack](https://uiarc.dev/components/card-stack)

### Text — 4

- [Text reveal](https://uiarc.dev/components/text-reveal)
- [In-view title](https://uiarc.dev/components/in-view-title)
- [Text morph](https://uiarc.dev/components/text-morph)
- [Text shimmer](https://uiarc.dev/components/text-shimmer)

### Special — 44

- [Share sheet](https://uiarc.dev/components/share-sheet) — **Pro**
- [Action morph](https://uiarc.dev/components/action-morph) — **Pro**
- [Morph nav](https://uiarc.dev/components/morph-nav) — **Pro**
- [Dock](https://uiarc.dev/components/dock) — **Pro**
- [Liquid tab bar](https://uiarc.dev/components/liquid-tab-bar) — **Pro**
- [Orbit menu](https://uiarc.dev/components/orbit-menu) — **Pro**
- [Glass menu](https://uiarc.dev/components/glass-menu) — **Pro**
- [Glass segmented](https://uiarc.dev/components/glass-segmented) — **Pro**
- [Glass card](https://uiarc.dev/components/glass-card) — **Pro**
- [Glass tab bar](https://uiarc.dev/components/glass-tabbar) — **Pro**
- [Sheet stack](https://uiarc.dev/components/sheet-stack) — **Pro**
- [Wallet stack](https://uiarc.dev/components/wallet-stack) — **Pro**
- [Control center](https://uiarc.dev/components/control-center) — **Pro**
- [Holo card](https://uiarc.dev/components/holo-card) — **Pro**
- [Link unfurl](https://uiarc.dev/components/link-unfurl) — **Pro**
- [Product gallery](https://uiarc.dev/components/product-gallery) — **Pro**
- [Lightbox gallery](https://uiarc.dev/components/lightbox-gallery) — **Pro**
- [Photo grid](https://uiarc.dev/components/photo-grid) — **Pro**
- [Cover flow](https://uiarc.dev/components/cover-flow) — **Pro**
- [Voice orb](https://uiarc.dev/components/voice-orb) — **Pro**
- [Now playing](https://uiarc.dev/components/now-playing) — **Pro**
- [Voice recorder](https://uiarc.dev/components/voice-recorder) — **Pro**
- [Booking pill](https://uiarc.dev/components/booking-pill) — **Pro**
- [Activity rings](https://uiarc.dev/components/activity-rings) — **Pro**
- [Time dial](https://uiarc.dev/components/time-dial) — **Pro**
- [Date reel](https://uiarc.dev/components/date-reel) — **Pro**
- [Keycap keyboard](https://uiarc.dev/components/keycap-keyboard) — **Pro**
- [Slot text](https://uiarc.dev/components/slot-text)
- [Sand text](https://uiarc.dev/components/sand-text) — **Pro**
- [Typewriter terminal](https://uiarc.dev/components/typewriter-terminal) — **Pro**
- [Stretch refresh](https://uiarc.dev/components/stretch-refresh) — **Pro**
- [Morph loader](https://uiarc.dev/components/morph-loader) — **Pro**
- [Skeleton morph](https://uiarc.dev/components/skeleton-morph) — **Pro**
- [Black hole](https://uiarc.dev/components/black-hole) — **Pro**
- [Sticker peel](https://uiarc.dev/components/sticker-peel) — **Pro**
- [Page curl](https://uiarc.dev/components/page-curl) — **Pro**
- [Orbit logos](https://uiarc.dev/components/orbit-logos) — **Pro**
- [Dot grid](https://uiarc.dev/components/dot-grid) — **Pro**
- [Gravity well](https://uiarc.dev/components/gravity-well) — **Pro**
- [Ink fluid](https://uiarc.dev/components/ink-fluid) — **Pro**
- [Data flow](https://uiarc.dev/components/data-flow) — **Pro**
- [Payment flow](https://uiarc.dev/components/payment-flow) — **Pro**
- [Multi-region failover](https://uiarc.dev/components/multi-region-failover) — **Pro**
- [Vector search](https://uiarc.dev/components/vector-search) — **Pro**

### Blocks — 94

- [Release readiness](https://uiarc.dev/components/blocks/release-readiness) — **Pro**
- [Sign up form](https://uiarc.dev/components/blocks/signup-form)
- [Wallet card](https://uiarc.dev/components/blocks/wallet-card) — **Pro**
- [Logo marquee](https://uiarc.dev/components/blocks/logo-marquee)
- [Team directory](https://uiarc.dev/components/blocks/team-directory) — **Pro**
- [Project board](https://uiarc.dev/components/blocks/project-board) — **Pro**
- [Invoice studio](https://uiarc.dev/components/blocks/invoice-studio) — **Pro**
- [Plan comparison](https://uiarc.dev/components/blocks/plan-comparison)
- [Availability picker](https://uiarc.dev/components/blocks/availability-picker) — **Pro**
- [Metrics dashboard](https://uiarc.dev/components/blocks/metrics-dashboard) — **Pro**
- [Media player](https://uiarc.dev/components/blocks/media-player) — **Pro**
- [Support conversation](https://uiarc.dev/components/blocks/support-conversation) — **Pro**
- [Inbox triage](https://uiarc.dev/components/blocks/inbox-triage) — **Pro**
- [Command palette](https://uiarc.dev/components/blocks/command-palette)
- [Notification center](https://uiarc.dev/components/blocks/notification-center)
- [File upload](https://uiarc.dev/components/blocks/file-upload)
- [OTP input](https://uiarc.dev/components/blocks/otp-input)
- [Multi-step form](https://uiarc.dev/components/blocks/multi-step-form) — **Pro**
- [Team showcase](https://uiarc.dev/components/blocks/team-showcase) — **Pro**
- [Studio perspectives](https://uiarc.dev/components/blocks/testimonial-stage) — **Pro**
- [Changelog feed](https://uiarc.dev/components/blocks/changelog-feed)
- [Usage pricing](https://uiarc.dev/components/blocks/usage-pricing) — **Pro**
- [AI composer](https://uiarc.dev/components/blocks/ai-composer) — **Pro**
- [Sign in](https://uiarc.dev/components/blocks/sign-in)
- [Workspace sidebar](https://uiarc.dev/components/blocks/workspace-sidebar) — **Pro**
- [Settings page](https://uiarc.dev/components/blocks/settings-page) — **Pro**
- [Sidebar rail](https://uiarc.dev/components/blocks/sidebar-rail) — **Pro**
- [Onboarding illustration](https://uiarc.dev/components/blocks/onboarding-illustration) — **Pro**
- [Docs sidebar](https://uiarc.dev/components/blocks/docs-sidebar) — **Pro**
- [Integrations](https://uiarc.dev/components/blocks/integrations) — **Pro**
- [Billing overview](https://uiarc.dev/components/blocks/billing-overview) — **Pro**
- [API keys](https://uiarc.dev/components/blocks/api-keys) — **Pro**
- [Inbox sidebar](https://uiarc.dev/components/blocks/inbox-sidebar) — **Pro**
- [Team members](https://uiarc.dev/components/blocks/team-members) — **Pro**
- [Page header](https://uiarc.dev/components/blocks/page-header)
- [Revenue explorer](https://uiarc.dev/components/blocks/revenue-explorer) — **Pro**
- [Journey flow](https://uiarc.dev/components/blocks/journey-flow) — **Pro**
- [Empty states](https://uiarc.dev/components/blocks/empty-states)
- [Centered login](https://uiarc.dev/components/blocks/login-centered)
- [Immersive login](https://uiarc.dev/components/blocks/login-immersive) — **Pro**
- [Security settings](https://uiarc.dev/components/blocks/security-settings) — **Pro**
- [Cancel flow](https://uiarc.dev/components/blocks/cancel-flow) — **Pro**
- [Login split](https://uiarc.dev/components/blocks/login-split) — **Pro**
- [Cohort retention](https://uiarc.dev/components/blocks/cohort-retention) — **Pro**
- [Support widget](https://uiarc.dev/components/blocks/support-widget) — **Pro**
- [Usage forecast](https://uiarc.dev/components/blocks/usage-forecast) — **Pro**
- [MRR waterfall](https://uiarc.dev/components/blocks/mrr-waterfall) — **Pro**
- [Webhooks](https://uiarc.dev/components/blocks/webhooks) — **Pro**
- [Roles and permissions](https://uiarc.dev/components/blocks/roles-permissions) — **Pro**
- [Metric explorer](https://uiarc.dev/components/blocks/metric-explorer) — **Pro**
- [Activity terrain](https://uiarc.dev/components/blocks/activity-terrain) — **Pro**
- [Revenue globe](https://uiarc.dev/components/blocks/revenue-globe) — **Pro**
- [Customer galaxy](https://uiarc.dev/components/blocks/customer-galaxy) — **Pro**
- [Semantic zoom](https://uiarc.dev/components/blocks/semantic-zoom) — **Pro**
- [Layout morph](https://uiarc.dev/components/blocks/layout-morph) — **Pro**
- [Agent run](https://uiarc.dev/components/blocks/agent-run) — **Pro**
- [Week calendar](https://uiarc.dev/components/blocks/week-calendar) — **Pro**
- [Scroll story](https://uiarc.dev/components/blocks/scroll-story) — **Pro**
- [Spotlight grid](https://uiarc.dev/components/blocks/spotlight-grid) — **Pro**
- [Invite people](https://uiarc.dev/components/blocks/invite-people) — **Pro**
- [Cart drawer](https://uiarc.dev/components/blocks/cart-drawer) — **Pro**
- [Pricing calculator](https://uiarc.dev/components/blocks/pricing-calculator) — **Pro**
- [AI chat](https://uiarc.dev/components/blocks/ai-chat) — **Pro**
- [Checkout summary](https://uiarc.dev/components/blocks/checkout-summary) — **Pro**
- [Site header](https://uiarc.dev/components/blocks/site-header)
- [Site footer](https://uiarc.dev/components/blocks/site-footer)
- [Hero section](https://uiarc.dev/components/blocks/hero-section)
- [FAQ section](https://uiarc.dev/components/blocks/faq-section)
- [Contact section](https://uiarc.dev/components/blocks/contact-section)
- [Settings command](https://uiarc.dev/components/blocks/settings-command) — **Pro**
- [Live checkout](https://uiarc.dev/components/blocks/checkout-live) — **Pro**
- [Kanban board](https://uiarc.dev/components/blocks/kanban-board) — **Pro**
- [Usage billing](https://uiarc.dev/components/blocks/usage-billing) — **Pro**
- [AI side panel](https://uiarc.dev/components/blocks/ai-side-panel) — **Pro**
- [KPI drilldown](https://uiarc.dev/components/blocks/kpi-drilldown) — **Pro**
- [Blog grid](https://uiarc.dev/components/blocks/blog-grid)
- [Comparison table](https://uiarc.dev/components/blocks/comparison-table)
- [Feature bento](https://uiarc.dev/components/blocks/feature-bento) — **Pro**
- [Stats band](https://uiarc.dev/components/blocks/stats-band)
- [CTA section](https://uiarc.dev/components/blocks/cta-section)
- [Newsletter signup](https://uiarc.dev/components/blocks/newsletter-signup)
- [Product listing](https://uiarc.dev/components/blocks/product-listing) — **Pro**
- [Product detail](https://uiarc.dev/components/blocks/product-detail) — **Pro**
- [Help center](https://uiarc.dev/components/blocks/help-center) — **Pro**
- [Hero signup](https://uiarc.dev/components/blocks/hero-signup) — **Pro**
- [Search results](https://uiarc.dev/components/blocks/search-results) — **Pro**
- [Environment variables](https://uiarc.dev/components/blocks/env-variables) — **Pro**
- [Market terminal](https://uiarc.dev/components/blocks/market-terminal) — **Pro**
- [Budget variance](https://uiarc.dev/components/blocks/budget-variance) — **Pro**
- [Choropleth explorer](https://uiarc.dev/components/blocks/choropleth-explorer) — **Pro**
- [Small multiples](https://uiarc.dev/components/blocks/small-multiples) — **Pro**
- [Connected scatter](https://uiarc.dev/components/blocks/connected-scatter) — **Pro**
- [Line replay](https://uiarc.dev/components/blocks/line-replay) — **Pro**
- [Exploded view](https://uiarc.dev/components/blocks/exploded-view) — **Pro**
