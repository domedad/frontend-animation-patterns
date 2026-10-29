# Bklit UI — Composable Charts and Visual Recipes

Last reviewed: **2026-10-29**.

## Scope and evidence

- [Components](https://bklit.com/docs/components), [machine-readable index](https://bklit.com/llms.txt), [Recipes](https://bklit.com/recipes), [chart galleries](https://bklit.com/charts), [Area gallery](https://bklit.com/charts/area-chart).
- **60 indexed references = 19 chart/component-family docs + 17 utility/axis docs + 24 named recipes**. The gallery's chart pages and the Area gallery's 22 examples support these entries; do not count them again as new families. Profit/Loss Line has its own documentation entry; Pie includes donut treatments.
- Recipes are paginated: page 1 has 15 entries; [page 2](https://bklit.com/recipes?page=2) has 9. An older search snapshot reports 21; the live browser and official recipe definitions were checked against 24. Keep page query parameters in second-page detail links.
- [Official repository](https://github.com/bklit/bklit-ui), reviewed revision `ec5a9705ee973f95fd0ef2d974e9d00ae3fda011`; [recipe definitions](https://github.com/bklit/bklit-ui/tree/ec5a9705ee973f95fd0ef2d974e9d00ae3fda011/apps/web/components/recipes/definitions).
- This is an index and original selection guidance, not bundled implementation code or a claim that every upstream chart was installed and tested.

## Stack, installation, and licensing

- React, Visx, Motion, Tailwind 4; composable copy-in primitives through the shadcn registry, **not Recharts wrappers**. Radial uses D3 scale/shape primitives. Keep an existing chart stack when it can express the same treatment.
- Follow [installation](https://bklit.com/docs/installation) and [theming](https://bklit.com/docs/theming). Registry namespace: `"@bklit": "https://ui.bklit.com/r/{name}.json"`; example: `npx shadcn@latest add @bklit/area-chart`. Inspect the exact JSON before adding files.
- Registry items carry transitive chart-context, animation, sizing, axes, tooltip and helper dependencies. Area and Heatmap also use `@bklit/shimmering-text` for loading labels. Do not copy only the visible chart TSX or blindly pin this snapshot's dependency versions.
- Website samples may import `@bklitui/ui/charts`, a monorepo path. Adapt to the installed files and the project's `components.json` alias, often `@/components/charts` or per-file imports; do not invent an npm package dependency from that sample import. Use a client boundary where hooks/interactivity require it.
- Map chart CSS variables, surface, foreground, grid, tooltip, categorical palettes and sequential levels to project tokens. Do not use decorative gradients as a quantitative color scale.
- The [repository license](https://github.com/bklit/bklit-ui/blob/ec5a9705ee973f95fd0ef2d974e9d00ae3fda011/LICENSE) is MIT, Copyright (c) 2026 uixmat. Preserve its notice when copying code and inspect dependency notices, including [Visx pattern attribution](https://github.com/bklit/bklit-ui/blob/ec5a9705ee973f95fd0ef2d974e9d00ae3fda011/packages/ui/src/charts/patterns/LICENSE-visx-pattern). Public previews do not relicense third-party assets.
- Keep this Skill's default motion policy: animations remain on regardless of OS reduced-motion settings; only explicit user/app choices turn them off. Adapt copied system-driven gates without changing unrelated app settings. Still retain readable values, offscreen limits and keyboard access.

## Chart/component families — 19

| Official reference | Select for / check |
|---|---|
| [Area Chart](https://bklit.com/docs/components/area-chart) | 趋势与累计量；渐变、堆叠、阶梯、纹理和分段选择。 |
| [Bar Chart](https://bklit.com/docs/components/bar-chart) | 类别比较；分组、堆叠、横向柱及弹簧入场。 |
| [Candlestick Chart](https://bklit.com/docs/components/candlestick-chart) | 真实 OHLC 开高低收数据；不要从单一成交值伪造蜡烛。 |
| [Choropleth Chart](https://bklit.com/docs/components/choropleth-chart) | 按地理区域着色；先核对地图数据、区域 ID 和统计口径。 |
| [Composed Chart](https://bklit.com/docs/components/composed-chart) | 同一时间轴组合柱、线、面积；混合单位须明确轴与单位。 |
| [Funnel Chart](https://bklit.com/docs/components/funnel-chart) | 嵌套转化阶段；不适用于跳步、非同批次的普通分类。 |
| [Gauge](https://bklit.com/docs/components/gauge-chart) | 单一有界指标；径向或线性刻度，明确上下限。 |
| [Heatmap Chart](https://bklit.com/docs/components/heatmap-chart) | 日期贡献/分箱强度；可配置色阶、纹理和联动图例。 |
| [Line Chart](https://bklit.com/docs/components/line-chart) | 多序列时间趋势；点标记、悬停和提示。 |
| [Profit/Loss Line](https://bklit.com/docs/components/profit-loss-line) | 围绕零基线表达正负收益；保留负数和中性状态。 |
| [Live Line Chart](https://bklit.com/docs/components/live-line-chart) | 实时流式时序；平滑滚动、十字线、动态轴。 |
| [Pie Chart](https://bklit.com/docs/components/pie-chart) | 整体中的占比；饼/甜甜圈、纹理和联动图例。 |
| [Radar Chart](https://bklit.com/docs/components/radar-chart) | 同单位或合理归一化的多维轮廓比较。 |
| [Radial Chart](https://bklit.com/docs/components/radial-chart) | 周期时间或类别的极坐标；点柱、堆叠柱、环柱、线和面积。 |
| [Ring Chart](https://bklit.com/docs/components/ring-chart) | 多个独立目标完成度；不是一个总量的扇区占比。 |
| [Scatter Chart](https://bklit.com/docs/components/scatter-chart) | 时序散点；悬停淡化、偏移环、抖动与入场。 |
| [Sankey Chart](https://bklit.com/docs/components/sankey-chart) | 节点之间的数量流向；保留边权及收支口径。 |
| [Sparkline](https://bklit.com/docs/components/sparkline) | 表格/KPI 中的微型线、面积或柱图；不堆叠完整图表容器。 |
| [Sunburst Chart](https://bklit.com/docs/components/sunburst-chart) | 层级数量和钻取；提供面包屑及返回路径。 |

## Utilities and axes — 17

| Official reference | Select for / check |
|---|---|
| [Legend](https://bklit.com/docs/utility/legend) | 图例布局、标记和联动，不只绘制颜色说明。 |
| [Grid](https://bklit.com/docs/utility/grid) | 水平/垂直网格、虚线与边缘淡出。 |
| [Background](https://bklit.com/docs/utility/background) | 绘图区背景纹理；不是页面全屏背景。 |
| [Reference Area](https://bklit.com/docs/utility/reference-area) | 固定 Y 区间/目标阈值，可着色关联轴刻度。 |
| [Projection Line](https://bklit.com/docs/utility/projection-line) | 末端延伸预测/目标路径；与历史数据分开标注。 |
| [Band](https://bklit.com/docs/utility/band) | 每行上下界包络；不是固定 Reference Area。 |
| [Weekends](https://bklit.com/docs/utility/weekends) | 日期轴周末着色；按实际时区与工作日规则定义。 |
| [Deadline](https://bklit.com/docs/utility/deadline) | 截止日期线及其后区间。 |
| [Trend Line](https://bklit.com/docs/utility/trend-line) | 最小二乘趋势线；不是未来预测或因果证据。 |
| [Markers](https://bklit.com/docs/utility/markers) | 真实事件/发布/故障日期标注。 |
| [Tooltip](https://bklit.com/docs/utility/tooltip) | 悬停数据提示、格式化与自定义内容。 |
| [Brush](https://bklit.com/docs/utility/brush) | 时间窗口概览和拖拽缩放。 |
| [Axis](https://bklit.com/docs/utility/axis) | 坐标轴组合及通用样式入口。 |
| [X Axis](https://bklit.com/docs/utility/axis/x-axis) | X 轴日期/类别、刻度、格式与密度。 |
| [Y Axis](https://bklit.com/docs/utility/axis/y-axis) | Y 轴数值、单位、域及多轴。 |
| [useChart Hook](https://bklit.com/docs/utility/use-chart) | 在图表上下文读取坐标/交互信息。 |
| [Custom Indicator](https://bklit.com/docs/utility/custom-indicator) | 自定义悬停指示层；不要虚构现成导出。 |

## Visual and interaction recipes — 24

Recipes adapt existing charts as well as Bklit primitives; check each recipe's supported chart-type tabs instead of assuming every treatment works everywhere.

| Group | Exact recipe | Selection cue |
|---|---|---|
| Backgrounds | [Hatched backdrop](https://bklit.com/recipes#hatched-backdrop) | 斜线底纹替代密集网格。 |
| Backgrounds | [Weekend stripes](https://bklit.com/recipes#weekend-stripes) | 用周末阴影解释工作日节奏。 |
| Backgrounds | [Dot matrix](https://bklit.com/recipes#dot-matrix) | 点阵背景与稀疏点标记。 |
| Skies | [Sunset sky](https://bklit.com/recipes#sky-sunset) | 品牌展示中的落日光晕。 |
| Skies | [Aurora sky](https://bklit.com/recipes#sky-aurora) | 曲线上方的极光氛围。 |
| Colour & shape | [Gradient glow](https://bklit.com/recipes#gradient-glow) | 少量重点序列的渐变填充。 |
| Colour & shape | [Monochrome](https://bklit.com/recipes#monochrome) | 单色主次与虚线区分。 |
| Colour & shape | [Squircle bars](https://bklit.com/recipes#squircle-bars) | 圆角方块堆成的分段柱。 |
| Colour & shape | [Quiet sparkline](https://bklit.com/recipes#quiet-sparkline) | 表格和指标卡的安静微图。 |
| Hover & annotations | [Custom indicators](https://bklit.com/recipes#custom-indicators) | 复用上下文制作悬停指示器。 |
| Hover & annotations | [Event markers](https://bklit.com/recipes#event-markers) | 在时间线上解释真实事件。 |
| Hover & annotations | [Diamond annotations](https://bklit.com/recipes#diamond-markers) | 轻量菱形注释层。 |
| Hover & annotations | [Value labels](https://bklit.com/recipes#value-labels) | 响应式数值标签与防碰撞。 |
| Hover & annotations | [KPI sparklines](https://bklit.com/recipes#kpi-sparklines) | 指针日期联动指标卡数值。 |
| Forecasts & ranges | [Forecast projection](https://bklit.com/recipes#projection-line) | 虚线延伸区分目标/预测。 |
| Forecasts & ranges | [Trend line](https://bklit.com/recipes?page=2#trend-line) | 原始序列与拟合线分层。 |
| Forecasts & ranges | [Range band](https://bklit.com/recipes?page=2#range-band) | 上下界包络与中心线。 |
| Heatmaps | [Dot calendar](https://bklit.com/recipes?page=2#heatmap-dot-calendar) | 圆点贡献日历与季度分隔。 |
| Heatmaps | [Workweek focus](https://bklit.com/recipes?page=2#heatmap-workweek) | 周一开始、弱化周末。 |
| Pie & ring | [Patterned slices](https://bklit.com/recipes?page=2#patterned-slices) | 纹理辅助区分饼/环扇区。 |
| Pie & ring | [Linked legend](https://bklit.com/recipes?page=2#linked-legend) | 图例与扇区/多环双向联动。 |
| Radial cards | [24h activity card](https://bklit.com/recipes?page=2#activity-clock-card) | 24 小时点钟与指标联动。 |
| Radial cards | [Storage usage card](https://bklit.com/recipes?page=2#storage-usage-card) | 半环堆叠容量与剩余空间。 |
| Radial cards | [Seasonal temperature card](https://bklit.com/recipes?page=2#seasonal-temperature-card) | 全年周期与区间/记录联动。 |

## Area chart: choosing the treatment

The [Area gallery](https://bklit.com/charts/area-chart) contains 22 examples, grouped here for lookup rather than counted again:

- **Shape and composition:** default, Step, Stacked, Gradient, No Stroke, Fade Edges.
- **Inspection and data:** Interactive, Value Labels, Segment Selection, Series Markers, Dashed Tail, left Y axis, left/right Y axes.
- **Visual layers:** Pattern, Pattern Background, Dot Grid Background, Reference Band, Pattern Reference Band, Trend Line, Gradient Trend Line.
- **Async state:** Loading and Loading (Sweep).

Use a stepped curve only for held/discrete changes, stacked areas only for additive series, and dual axes only with explicit units. A decorative dashed tail is not automatically a forecast. Preserve the displayed value's date, unit, null/missing semantics and series identity.

## Composition contracts and pitfalls

### Time, loading, brush, and forecasting

- Time-series examples use actual `Date` values under `date`; Bar defaults to `name`. Set `xDataKey` explicitly for other fields, sort input, define timezone and aggregation, and never convert unknown observations to zero for a smoother picture.
- Keep one chart instance for real loading → ready transitions using `status`; do not replay a fake loading timer on refresh. Loading shortcuts exist, but an animated skeleton is not an error/empty-data state.
- For brush zoom, `ChartBrushLayout` owns the window and passes `xDomain`, `xDomainSlotCount`, and optionally `tweenYDomainOnXDomainChange` to the main chart. Use the full dataset in the overview; do not wire a moving miniature that never changes the main query/window.
- **ProjectionLine and brush zoom are not supported together** in the reviewed docs. Choose one or separate views; do not combine them by assumption.
- `buildProjectionPath` supports auto, target, and manual modes. Auto slope/regression is a visualization heuristic, not a validated forecast; target `endValue` is a goal, not actual revenue. Keep predicted/target values separately labeled and sourced.
- Distinguish `ReferenceArea` (fixed Y thresholds), `Band` (per-row lower/upper range), `TrendLine` (least-squares fit), `Weekends` (date context), and `Deadline` (due date). A styled interval is not statistical confidence without a calculation and coverage definition.

### Heatmaps and compact dashboard cards

- Heatmap uses column/bin data (`HeatmapColumn[]`, e.g. week columns with day bins containing `bin`, `count`, and optional date), not Sakani's numeric matrix contract. Pair `HeatmapCells`, X/Y axes, tooltip and legend; `HeatmapInteractionProvider` and `HeatmapInteractionBoundary` coordinate shared hover.
- Define week start, timezone, date completeness, level thresholds, zero vs unknown and a shared scale before comparing panels. Dot calendar and Workweek focus are **two styling recipes of this family**, not separate data models.
- Sparkline's line/area/bar forms fit dense tables; KPI sparklines link a date to the card value. Synchronize by real timestamp rather than array index when series have different/missing dates. Show the selected date and restore the stated default value on exit.
- Radial cards add 24-hour, capacity and annual-cycle layouts. Specify hour/day order, wrap boundary, capacity denominator and units; a storage arc must not silently clip over-capacity usage.

### Styling layers and interaction

- Pattern/gradient IDs are document-global SVG resources: use unique IDs per chart instance, including repeated cards.
- PatternArea supplies the textured fill; an Area layer may still supply stroke/reveal/hover. Avoid duplicate opaque fills hiding one another.
- Squircle bars coordinate `squareSnap`, BarSquares/BarColumnTrack spacing and corner shape with the tooltip indicator; ordinary border-radius does not reproduce the segmented geometry.
- For 3D bars, keep depth-back → bar → depth-front order; a BarDepthProvider must wrap outside BarChart where child discovery requires direct children. Site-only `BarLineIndicator` is not a registry export; inspect installed exports before using it.
- Use value-label collision limits and sparse event markers at mobile width. Do not add every recipe to a single plot or use atmospheric skies behind dense analytical text.
- Hover, legend dimming, brush and drilldown need touch/keyboard alternatives and a readable summary/table. A working mouse demo does not establish complete accessibility. Keep actual data, selection and async state available without motion or color alone.
- Verify repeated mount/unmount, resizing from zero-size containers, tooltip clipping, SVG ID collisions, new data during hover, brush changes and streaming cleanup in the real application. Catalog validation does not replace those tests.
