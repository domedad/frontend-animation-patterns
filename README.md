# Frontend Animation Patterns

一个给 AI 编程 Agent 使用的前端设计选型 Skill：根据页面用途，选择合适的元素样式、交互状态与动效，再引导实现和验证。

An instruction-only Agent Skill for selecting frontend element styles, interaction states, and motion from a maintained, scenario-based reference catalog.

## 三步使用

1. 将 `skills/frontend-animation-patterns` **整个目录**安装到你的 Agent 支持的 Skill 目录，不要只复制 `SKILL.md`。
2. 明确调用 Skill，并说明页面用途、技术栈和需要改善的元素。
3. Agent 先查场景矩阵，再读取匹配来源，核对当前实现与授权后实施。

例如，在 Codex 中：

```text
使用 $frontend-animation-patterns，改善这个后台页面的按钮、卡片和加载状态。
沿用现有 React、Tailwind 和组件库，不给密集数据区域添加装饰性动画。
```

```text
使用 $frontend-animation-patterns，为 AI 聊天页面选择流式回答、
工具调用记录、审批卡和失败重试的展示方案。所有状态必须来自真实任务数据。
```

## 收录范围

当前快照索引 **10 个来源、879 个条目**。这是各来源最近一次收录快照的合计，包含免费和 Pro 参考，不是跨站去重后的设计数，也不是 879 份已安装或逐一运行验证的组件。UIArc 新增 262 项（168 个组件，含 44 个特殊组件，以及 94 个区块），其中 134 项 Free、128 项 Pro；图表栏目包含 21 项，其中数字计数器和数据网格不是独立统计图类型。

| 来源 | 主要用途 |
|---|---|
| Transitions.dev | 产品状态过渡和微交互 |
| Magic UI | 营销展示、文字、背景和卡片动效 |
| MicroInteractions UI | 按钮、输入、标签页等控件交互 |
| COSS UI | 克制的产品基础组件与可访问状态 |
| React Bits | 表现型文字、背景、组件和视觉效果 |
| beUI | 动效控件、应用区块和 Agent 界面 |
| Beautiful UI | AI 聊天、工具、审批、证据和任务界面 |
| Rewamp UI | 高表现力品牌交互、空间和背景效果 |
| EasyUI | 日志流、数据详情、批量操作、恢复和 AI 区块 |
| UIArc / Arc UI | 图表、活动热力图、数字滚动、图片对比、产品控件和业务区块；区分 Free / Pro |

浏览 [场景选型矩阵](skills/frontend-animation-patterns/references/selection-matrix.md) 和 [来源登记表](skills/frontend-animation-patterns/references/source-registry.md)，再按需读取具体来源。该仓库不打包上述网站的完整文档、组件源码、付费内容或展示站。

## 默认动效策略

默认开启动效，不自动跟随操作系统的“减少动态效果”设置。只有用户明确要求关闭，或应用自身已有动效开关时才按该选择关闭；仍保留键盘操作、可读状态、性能限制和离屏暂停。复制上游组件时也需检查其系统动效判断，具体规则见 [Skill](skills/frontend-animation-patterns/SKILL.md#default-motion-policy)。

## 安装到 Codex

可以向 Codex 的 Skill Installer 发出：

```text
$skill-installer 请从 https://github.com/domedad/frontend-animation-patterns
安装 skills/frontend-animation-patterns 目录中的 Skill。
```

也可以下载此仓库后，将整个 Skill 目录放入项目的 `.agents/skills/frontend-animation-patterns`，或用户级的 `~/.agents/skills/frontend-animation-patterns`。如果已安装同名 Skill，先检查内容并明确更新范围，不要盲目覆盖。

安装后显式调用 `$frontend-animation-patterns`。描述匹配可用于自动选择，但是否触发取决于宿主及任务上下文；如未出现，检查安装位置并重启宿主。

参见 [官方 OpenAI Skill 文档](https://learn.chatgpt.com/docs/build-skills)。这是独立 Skill 仓库，不是已经上架的官方插件或插件市场条目。

## 其他 Agent

- 支持 Agent Skills 标准的宿主：按照该宿主的文档安装整个 Skill 目录。不要假设所有产品都使用相同路径、安装命令或调用语法。
- 能读取项目文件但没有 Skill 自动发现的 Agent：显式要求它读取 `skills/frontend-animation-patterns/SKILL.md`，随后按需读取其 `references/`。
- 不能访问本地文件的对话环境：上传完整目录的归档，或提供相应文件内容；只有一个 GitHub 链接不保证它能加载完整 Skill。
- `agents/openai.yaml` 是 OpenAI 宿主的可选展示元数据，其他宿主可能忽略它；主体指导在 `SKILL.md` 和参考文件里。

这个 Skill 本身不需要 npm 依赖、API key、私有服务或另一个 Skill。执行实际页面修改时，Agent 仍需要相应的文件、联网检索、代码执行和浏览器能力；选中的组件可能另有依赖。GSAP Skill 和宿主校验器是可选工具，不随本仓库安装。

## 授权和边界

本项目原创指导、选型组织和说明采用 [MIT 许可证](LICENSE)。来源品牌、组件实现、图像和第三方内容仍保留各自权利及授权；参见 [第三方来源声明](THIRD_PARTY_NOTICES.md)。开源本 Skill 不代表上游 Pro 内容免费或所有条目都可按 MIT 复制。

实施时必须重新核对选中组件的当前官方文档、依赖和许可。不要发布付费代码、未明确授权的实现或伪造的业务状态；不要将该项目描述为上述来源的官方合集。

## 增补与更新

增加新来源时，遵循 [来源更新流程](skills/frontend-animation-patterns/references/source-registry.md)：核对公开目录和授权、增添来源参考、补有价值的场景映射、更新快照统计，再验证相对链接和 Skill 格式。保持原名、精确官方链接、最后核对日期、Pro/访问限制；不要把单个页面当成网站全目录。

仓库更新不会自动同步到用户已安装的副本。升级时先比较版本和本地修改，再重新安装或同步；不要覆盖使用者的自定义内容。

## 发布验证范围

初次发布检查包含 Skill frontmatter、相对参考链接、当时 9 个来源文件的完整性、隐私/凭据和机器路径筛查，以及从发布仓库下载后的内容一致性。2026-10-19 增补 UIArc 后，来源文件增至 10 个，并单独核对其目录、图表文档、代表性免费 registry、授权和外链。这不等于重新验证每个上游组件的兼容性或所有 Agent 宿主的实际行为。
