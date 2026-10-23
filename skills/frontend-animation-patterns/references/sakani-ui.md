# Sakani UI Catalog

Official sources: [component directory](https://www.sakaniui.com/llms.txt), [API manifest](https://www.sakaniui.com/manifest.json), [installation](https://www.sakaniui.com/docs/installation), [glass guide](https://www.sakaniui.com/docs/glass), [repository and MIT license](https://github.com/samzydd/Sakaniui).
Last reviewed: **2026-10-20**. Reviewed site manifest/package version: **0.8.7**. Source snapshot: [ebc2ca8](https://github.com/samzydd/Sakaniui/tree/ebc2ca8fd1644d7c6ec82a730fdc47ff8f2f8e13).

## Scope and counting

Index **81 documentation groups**: **70 component pages (including 9 chart families)** and **11 block pages**. These are the unique component/block URLs in the official `llms.txt`; starting guides, themes, icon collections, tokens, and variants are not counted again.

The generated manifest separately contains **123 component API entries and 42 block API entries**. All 165 names are listed below for lookup, but compound children, social-icon helpers, and page-level exports are not 165 independent visual designs. Several APIs share a documentation page. The global catalog adds **81**, not 81 + 165, for this source.

Use actual manifest/source contracts rather than headline counts such as “114+ components” or a repository description counting variants. Generated categories can contain preview text (the reviewed NotificationPanelBlock category is malformed); this index groups that block with application blocks without changing its API name.

## Role and implementation stack

- Prefer Sakani for token-driven React product surfaces, coordinated chart styling, light/dark dashboards, and reusable forms/application/commerce/marketing blocks. Keep existing project components and chart libraries when they already meet the need.
- Install `@sakaniui/react` into a compatible React 19 project. Import **both** `@sakaniui/react/tokens.css` and `@sakaniui/react/style.css` once at the app entry. The shorter installation page omits the second import; the machine contract and source package specify both.
- Components import from `@sakaniui/react`; blocks import from `@sakaniui/react/blocks`. This is an npm component package, not a shadcn copy-in registry. Consult the installed version's manifest/types before choosing props.
- The reviewed package depends on Recharts 3.x. Most charts wrap Recharts; **HeatmapChart uses a CSS grid and FunnelChart uses custom SVG**, and some RadialChart treatments are custom. Do not assume all nine expose a generic Recharts API.
- Charts use semantic chart, border, text and surface CSS variables through shared helpers. Preserve the project's metric/series identities when mapping palettes. The first LineChart series deliberately uses chart token 2, the second token 1; the AreaChart palette starts with token 5 and adds token 2. These are source design choices, not data-order errors.
- Use `.dark` on the intended ancestor for the actual theme. Glass/liquid surface selection is separate from light/dark. Keep dense charts/tables/forms on a solid data surface even when surrounding chrome is glass. Read the glass guide for Chromium refraction versus frosted browser fallback.
- Apply this Skill's **Default Motion Policy**: do not automatically disable selected motion based on system settings. Several reviewed chart wrappers explicitly set Recharts `isAnimationActive={false}` for their static treatment; adding the package alone will not create UIArc-like morphs. If motion is requested, adapt the selected implementation or its supported API deliberately; do not invent an unsupported prop on a wrapper.
- Source and package are MIT licensed. Preserve the upstream copyright/license notices when redistributing copied implementation code. “Free” does not remove that obligation or relicense linked Figma/media assets.
- Official manifests and optional MCP tools can help resolve props; this catalog does not install another Skill/MCP, migrate a project wholesale, fetch paid assets, or run demo business actions.

## Chart design and selection — 9 families

| Reference / export | Use for | Styles / variants | Design boundary |
|---|---|---|---|
| [Line Chart](https://www.sakaniui.com/docs/components/line-chart) / `LineChart` | 时间趋势、多指标对比 | default / linear / step / multiple / dots / custom-dots / dots-colors / label / custom-label | 少量点用标记或数值标签；密集序列去掉标记。实际 series 数组控制曲线数量，multiple 本身不生成第二组数据。 |
| [Area Chart](https://www.sakaniui.com/docs/components/area-chart) / `AreaChart` | 强调随时间变化的量级 | default / stacked / step / linear | 通过 value2 增加第二组数据；堆叠看合计与构成，重叠填充不适合多组精确趋势比较。 |
| [Bar Chart](https://www.sakaniui.com/docs/components/bar-chart) / `BarChart` | 分类、周期、正负值对比 | default / active / multiple / stacked / negative / horizontal | 分组比较系列、堆叠比较总量；长类目用横向。negative 以零为中心；active 为强调状态，不是筛选。 |
| [Pie Chart](https://www.sakaniui.com/docs/components/pie-chart) / `PieChart` | 少数类别的整体构成及标签布局 | pie / pie-no-separator / label / custom-label / label-list / donut / donut-active / donut-with-text / stacked / interactive | 外引线、胶囊标签、片内文字、突出切片或光环均有参考；片内文字需要足够面积，类别多改用柱图。 |
| [Donut Chart](https://www.sakaniui.com/docs/components/donut-chart) / `DonutChart` | 总量与占比一起呈现 | 独立 DonutChart，配 centerValue / centerCaption | 中心是应用提供的格式化文字，不会自动保证它与切片之和一致；尾部类别可按业务规则合为其他。 |
| [Radial Chart](https://www.sakaniui.com/docs/components/radial-chart) / `RadialChart` | 容量、配额、目标或多环仪表 | multi / grid / text / shape / gauge-tick / stacked / stacked-3-layers / stacked-label | 区分同心环与角度堆叠圆弧；明确 max 和单位，不能把容量或评分写成任务完成进度。 |
| [Radar Chart](https://www.sakaniui.com/docs/components/radar-chart) / `RadarChart` | 少数对象的多维画像 | default / multiple / dots / custom-label / dots-grid-none / lines-only / circle-grid / circle-grid-no-lines / grid-custom / grid-filled / circle-grid-filled | 可参考多边形／圆形网格、轮廓、填充和标签；先统一各轴量纲及上限，并固定轴顺序。 |
| [Funnel Chart](https://www.sakaniui.com/docs/components/funnel-chart) / `FunnelChart` | 严格嵌套阶段的转化与流失 | 有序阶段、阶段数值／占首阶段比例、聚焦提示 | 后阶段必须是前阶段的子集；可跳步或中途进入的流程，不应用收窄图形暗示嵌套。 |
| [Heatmap Chart](https://www.sakaniui.com/docs/components/heatmap-chart) / `HeatmapChart` | 行 × 列两维的强度与聚集模式 | 矩阵色阶、行列标签、单格聚焦及共享提示 | 适合星期 × 小时、对象 × 日期等矩阵；不是 GitHub 贡献日历。缺失值与真实零值必须先定义。 |

## Source-specific chart contracts and cautions

### Line, area, and bar

- LineChart requires `data` and `series`; default x field is `label`, overridden by `xKey`. Supply real per-series numeric fields, ordered x labels, units, and a known missing-data policy. Do not borrow UIArc's prop names or silently replace absence with zero.
- Use `step` for values held until a change (tiers, capacity, headcount), `linear` for direct joins, and the smooth default only when interpolation is defensible. Showing a smooth curve does not mean intermediate observations exist.
- LineChart's `height` overrides `size`; presets are 180/240/320/420px. A constrained card must set an actual supported height rather than hiding an overflowing SVG with ancestor CSS. BarChart does not expose the same height prop in the reviewed contract.
- `custom-label` reads the field named by `labelKey`; keep labels short and ensure index/data correspondence. Despite the documentation's ring/halo description, the reviewed `custom-dots` source draws a filled dot with short vertical ticks. Check actual installed output when matching a reference.
- AreaChart accepts `{ label, value, value2? }[]`; `seriesLabels` names the fields. In the reviewed source its gradient ids are fixed strings; check for cross-instance collisions when placing several differently themed areas on one page and adapt selected copied source if needed.
- BarChart's second value is used by `multiple` or `stacked`. Its negative treatment uses a symmetric domain around zero; do not remove negatives to fit a decorative recipe. Static active/hover emphasis must not be presented as a user selection or changed data.
- The reviewed Line/Area wrappers do not include a visible numeric YAxis and force every X-axis label through `interval=0`; dense dates can collide. Verify readable ticks and a value/units path before adopting them for exact analytical comparison.

### Matrix heatmap versus activity calendar

- Sakani HeatmapChart takes row-major `number[][]` plus optional `rowLabels`, `colLabels`, `valueLabel`, and `size`. Validate rectangular dimensions and label lengths upstream. The implementation derives its column count from the **first data row**, not the label array.
- This is the **matrix heatmap** recipe. Use UIArc Activity heatmap instead when the job is a dated contribution calendar with streaks. Geographic intensity maps are a third, separate category.
- Official documentation suggests zero padding; only do so for confirmed zero observations. Unknown/uncollected cells require an explicit missing state or another implementation, not fabricated activity. Validate finite values; the reviewed single-hue positive scale is not a signed/diverging metric scale.
- Cell opacity is normalized to the current dataset maximum with a nonzero minimum tint. Equal color in two independently normalized panels does not guarantee equal value. A shared fixed scale needs an adaptation; there is no documented `domain`/`thresholds` prop to invent.
- Hover makes the active cell solid and dims the rest to one constant opacity; this is focus decoration and temporarily stops representing each other cell's original intensity.
- The reviewed cells only handle mouse enter/leave and are not focusable gridcells. Add a real keyboard/touch readout and text/table alternative in the selected implementation; do not claim the source's general accessibility marketing proves this control is accessible.
- No click/date-selection callback is exposed in the reviewed HeatmapChart props. Do not show drilldown as available until implemented and connected to actual data.

### Composition, radial, radar, and funnel

- Pie/Donut take `{ label, value }[]`. Center values/captions are preformatted application text, not automatic aggregates. Tie them to the same rows, currency, period, filters, and rounding as the chart. Use non-negative part-to-whole data and a stated denominator.
- PieChart's rendered docs list the default as pie, while the reviewed source/manifest default to **donut**. Set `variant` explicitly. Its stacked treatment draws two concentric rings from the same data; it is not two independent datasets. Preserve notices and inspect the source before claiming a different comparison.
- A hovering/active/exploded slice is visual emphasis, not a persisted selection. The reviewed public APIs do not provide general controlled selection callbacks for every chart.
- RadialChart data use `{ label, value, max? }`. The reviewed ring scale and arc helpers use `data[0].max` as a shared ceiling; separate per-row maxima are not automatically independent domains. Validate positive ceilings and clarify absolute values versus percentages before use.
- Radar comparisons require compatible units, normalization, fixed spoke order, and an explicitly appropriate domain. The docs say a second series follows `value2`, but the reviewed source only renders it for `multiple`, `custom-label`, or `lines-only`; select one deliberately and verify the installed version.
- FunnelChart uses the first stage for its percentage denominator, not the previous stage. It does not validate the cohort's nesting/non-increasing counts for you. Validate non-negative ordered stages and handle empty/zero-first-stage input outside the wrapper. Name percentages as retained from first stage unless another calculation is actually implemented.
- These source/API checks are not an interactive browser test. When implementing a real chart, verify desktop/mobile size, touch, keyboard, loading/empty/error states, units, label collisions, and actual data volume. Preserve textual results without relying on color or animation.

## Related dashboard composition

- [Stat Card](https://www.sakaniui.com/docs/components/stat-card): one primary KPI, trend and optional sparkline; use several cards rather than cramming several unrelated values into one.
- [Finance](https://www.sakaniui.com/docs/components/finance): Balance, SpendingBalance, Expenses, Transactions, StockMarket and Ticker. Preserve signed transaction amounts and consistent formatting; demos are not market/payment data.
- [App Shell](https://www.sakaniui.com/docs/blocks/app-shell): account/dashboard framing. [Data Table](https://www.sakaniui.com/docs/blocks/data-table) provides the inspectable record view alongside charts.
- Glass is a surrounding surface choice, not permission to place low-contrast translucent fills behind dense chart labels. Use semantic colors, legible contrast and a solid plot surface.

## Complete remaining documentation groups — 72

Charts above account for 9 of the 81 groups. Every group below is linked once in this index; a group can document multiple APIs.

### Core — 10

- [Button](https://www.sakaniui.com/docs/components/button)
- [Badge](https://www.sakaniui.com/docs/components/badge)
- [Icon Button](https://www.sakaniui.com/docs/components/icon-button)
- [Card](https://www.sakaniui.com/docs/components/card)
- [Avatar](https://www.sakaniui.com/docs/components/avatar)
- [Alert](https://www.sakaniui.com/docs/components/alert)
- [Accordion](https://www.sakaniui.com/docs/components/accordion)
- [Divider](https://www.sakaniui.com/docs/components/divider)
- [Link](https://www.sakaniui.com/docs/components/link)
- [Kbd](https://www.sakaniui.com/docs/components/kbd)

### Forms — 11

- [Input](https://www.sakaniui.com/docs/components/input)
- [Textarea](https://www.sakaniui.com/docs/components/textarea)
- [Select](https://www.sakaniui.com/docs/components/select)
- [Combobox](https://www.sakaniui.com/docs/components/combobox)
- [Checkbox](https://www.sakaniui.com/docs/components/checkbox)
- [Radio](https://www.sakaniui.com/docs/components/radio)
- [Switch](https://www.sakaniui.com/docs/components/switch)
- [Slider](https://www.sakaniui.com/docs/components/slider)
- [Segmented Control](https://www.sakaniui.com/docs/components/segmented-control)
- [File Upload](https://www.sakaniui.com/docs/components/file-upload)
- [Label](https://www.sakaniui.com/docs/components/label)

### Navigation — 8

- [Sidebar](https://www.sakaniui.com/docs/components/sidebar)
- [Top Bar](https://www.sakaniui.com/docs/components/top-bar)
- [Menu](https://www.sakaniui.com/docs/components/menu)
- [Breadcrumb](https://www.sakaniui.com/docs/components/breadcrumb)
- [Pagination](https://www.sakaniui.com/docs/components/pagination)
- [Stepper](https://www.sakaniui.com/docs/components/stepper)
- [Popover](https://www.sakaniui.com/docs/components/popover)
- [Filter Chip](https://www.sakaniui.com/docs/components/filter-chip)

### Application — 8

- [Modal](https://www.sakaniui.com/docs/components/modal)
- [Notifications](https://www.sakaniui.com/docs/components/notifications)
- [Activity Feed](https://www.sakaniui.com/docs/components/activity-feed)
- [Progress Steps](https://www.sakaniui.com/docs/components/progress-steps)
- [Finance](https://www.sakaniui.com/docs/components/finance)
- [Code Snippet](https://www.sakaniui.com/docs/components/code-snippet)
- [Avatar Upload](https://www.sakaniui.com/docs/components/avatar-upload)
- [Tags](https://www.sakaniui.com/docs/components/tags)

### Marketing — 6

- [Section Heading](https://www.sakaniui.com/docs/components/section-heading)
- [Rich Text](https://www.sakaniui.com/docs/components/rich-text)
- [Blog Listing](https://www.sakaniui.com/docs/components/blog-listing)
- [Team Cards](https://www.sakaniui.com/docs/components/team-cards)
- [Marketing Elements](https://www.sakaniui.com/docs/components/marketing-elements)
- [Mobile Navigation](https://www.sakaniui.com/docs/components/mobile-navigation)

### E-commerce — 5

- [Product Card](https://www.sakaniui.com/docs/components/product-card)
- [Product Options](https://www.sakaniui.com/docs/components/product-options)
- [Product Gallery](https://www.sakaniui.com/docs/components/product-gallery)
- [Cart](https://www.sakaniui.com/docs/components/cart)
- [Star Rating](https://www.sakaniui.com/docs/components/star-rating)

### Feedback — 6

- [Toast](https://www.sakaniui.com/docs/components/toast)
- [Tooltip](https://www.sakaniui.com/docs/components/tooltip)
- [Progress](https://www.sakaniui.com/docs/components/progress)
- [Spinner](https://www.sakaniui.com/docs/components/spinner)
- [Skeleton](https://www.sakaniui.com/docs/components/skeleton)
- [Empty State](https://www.sakaniui.com/docs/components/empty-state)

### Data display — 7

- [Table](https://www.sakaniui.com/docs/components/table)
- [Tabs](https://www.sakaniui.com/docs/components/tabs)
- [Stat Card](https://www.sakaniui.com/docs/components/stat-card)
- [List Item](https://www.sakaniui.com/docs/components/list-item)
- [Board Card](https://www.sakaniui.com/docs/components/board-card)
- [Chat](https://www.sakaniui.com/docs/components/chat)
- [Calendar](https://www.sakaniui.com/docs/components/calendar)

### Blocks — 11

- [Data Table](https://www.sakaniui.com/docs/blocks/data-table)
- [Kanban Board](https://www.sakaniui.com/docs/blocks/kanban-board)
- [App Shell](https://www.sakaniui.com/docs/blocks/app-shell)
- [Panels & Flows](https://www.sakaniui.com/docs/blocks/panels)
- [Authentication](https://www.sakaniui.com/docs/blocks/authentication)
- [Marketing Sections](https://www.sakaniui.com/docs/blocks/marketing-sections)
- [Content Sections](https://www.sakaniui.com/docs/blocks/content-sections)
- [E-commerce](https://www.sakaniui.com/docs/blocks/ecommerce)
- [Pricing Table](https://www.sakaniui.com/docs/blocks/pricing-table)
- [Billing](https://www.sakaniui.com/docs/blocks/billing)
- [Billing Address](https://www.sakaniui.com/docs/blocks/billing-address)

## API-name lookup — 165 manifest entries, not extra designs

Use [the versioned source tree](https://github.com/samzydd/Sakaniui/tree/ebc2ca8fd1644d7c6ec82a730fdc47ff8f2f8e13) and the [live manifest](https://www.sakaniui.com/manifest.json) to find each exact contract. Read `source`, `props`, `contract.requiredProps`, and the import subpath. Package versions can differ from the site. The lists below preserve all manifest names, including compound children and social helpers, without adding them to the 81-group count.

### Composite — 21

`Accordion`, `AccordionItem`, `Alert`, `BoardCard`, `BoardColumn`, `Breadcrumb`, `Calendar`, `Card`, `CardMetaItem`, `Combobox`, `FileUpload`, `ListItem`, `Pagination`, `Popover`, `SegmentedControl`, `StatCard`, `Stepper`, `StepperStep`, `Table`, `Tabs`, `Toast`

### Application — 18

`ActivityFeed`, `ActivityFeedHighlight`, `Announcement`, `AvatarUpload`, `Balance`, `CodeSnippet`, `Expenses`, `InlineHint`, `Modal`, `NotificationItem`, `ProgressItem`, `ProgressStat`, `RichSeparator`, `SpendingBalance`, `StockMarket`, `Tags`, `Ticker`, `Transactions`

### Charts — 9

`AreaChart`, `BarChart`, `DonutChart`, `FunnelChart`, `HeatmapChart`, `LineChart`, `PieChart`, `RadarChart`, `RadialChart`

### Core — 13

`Avatar`, `AvatarGroup`, `Badge`, `Button`, `Divider`, `IconButton`, `Kbd`, `Label`, `Link`, `Progress`, `Skeleton`, `Spinner`, `Tooltip`

### Marketing — 25

`BlogBlockquote`, `BlogFeatureText`, `BlogImage`, `BlogListingCard`, `BlogListingFeaturedCard`, `FacebookIcon`, `FeaturedIcon`, `FirstPageHeading`, `GithubIcon`, `InstagramIcon`, `JobListing`, `LinkedinIcon`, `List`, `LocationDot`, `Marquee`, `Metric`, `MobileNavigationMenu`, `PlaceholderLogo`, `ProfileCard`, `RichTextHeading`, `RichTextParagraph`, `SectionHeading`, `SubFeature`, `TeamCard`, `XIcon`

### E-commerce — 11

`CartItem`, `CheckoutSteps`, `ColorSwatch`, `PriceDisplay`, `ProductCard`, `ProductGallery`, `QuantitySelector`, `SizeSelector`, `StarRating`, `StockStatus`, `WishlistButton`

### Chat — 3

`ChatComposer`, `ConversationItem`, `MessageBubble`

### Forms — 7

`Checkbox`, `Input`, `Radio`, `Select`, `Slider`, `Switch`, `Textarea`

### Data — 2

`EmptyState`, `FilterChip`

### Overlays — 3

`Menu`, `MenuDivider`, `MenuItem`

### Composite/Sidebar — 9

`Sidebar`, `SidebarDivider`, `SidebarFooter`, `SidebarGroupLabel`, `SidebarHeader`, `SidebarItem`, `SidebarPromo`, `SidebarSearch`, `SidebarSubItem`

### Navigation — 2

`TopBar`, `TopBarMobile`

### Blocks/Application — 14

`AccountOverviewBlock`, `ActivityLogBlock`, `AppHeaderBlock`, `CRMDashboardBlock`, `DataTableBlock`, `FileUploadPanelBlock`, `FormModalBlock`, `InlineCtaBlock`, `LiquidDashboardBlock`, `MultistepModalBlock`, `NotificationPanelBlock`, `OnboardingProgressBlock`, `ProfileSettingsBlock`, `SectionFooterBlock`

### Blocks/Billing — 5

`AddCardFormBlock`, `BillingAddressBlock`, `BillingHistoryBlock`, `CurrentPlanBlock`, `PaymentMethodBlock`

### Blocks/Marketing — 10

`BlogListingBlock`, `CareersBlock`, `CtaBannerBlock`, `FaqBlock`, `FeatureGridBlock`, `HeroBlock`, `LogoCloudBlock`, `PricingTableBlock`, `TeamSectionBlock`, `TestimonialBlock`

### Blocks/Chat — 1

`ChatInterfaceBlock`

### Blocks/E-commerce — 5

`CheckoutFlowBlock`, `OrderConfirmationBlock`, `ProductDetailBlock`, `ProductGridBlock`, `ShoppingCartBlock`

### Blocks/Authentication — 6

`EmailVerificationBlock`, `ForgotPasswordBlock`, `LoginBlock`, `ResetPasswordBlock`, `SignUpBlock`, `TwoFactorAuthBlock`

### Blocks/Data & Content — 1

`KanbanBoardBlock`
