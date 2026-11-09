# 视觉系统与组件取证

2026-11-09 只读快照。下列尺寸均为 Figma 设计坐标中的 px；示例基准为 1920×1080，不能直接视为实现端 dp/sp。来源节点见 [source-map.md](source-map.md)。

## 视觉语言

**画面观察**：Home 以内容为中心，使用暗色底、大幅 Hero 图、保护文字可读性的渐变、左侧导航、横向内容行和底部 Apps Row。品牌粉色用于品牌与强调，并非所有焦点统一着粉色。Settings 示例使用暗色双栏浮层，背景内容仍可辨认；OOBE 示例使用开阔双区构图，左侧选择、右侧大尺寸情境反馈。

**用法**：先选与任务接近的项目模板，不把 Home 的海报、渐变或 Apps Row 机械套到设置、首次引导和设备调节场景。

## 字体阶梯：Style / Typography

来源 `649:20346`，已读取实际文字属性。字体为 **Inter**，覆盖 Regular / Medium / Semi Bold；下表是样例字号与行高，行高为字号的 1.5 倍。实际任务优先使用当前绑定的文本样式或变量。

| 原稿角色 | 字号 / 行高 |
| --- | --- |
| Largetitle 的大号样例 | 72 / 108 |
| Largetitle | 56 / 84 |
| Subtitle1 | 46 / 69 |
| Subtitle2 | 42 / 63 |
| Subtitle3 | 36 / 54 |
| Subtitle4 | 32 / 48 |
| Bodytext1 | 30 / 45 |
| Bodytext2 | 28 / 42 |
| Bodytext3 | 26 / 39 |
| Bodytext4 | 24 / 36 |
| Callout | 22 / 33 |
| Lable（原稿拼写） | 20 / 30 |

注意：Typography 中标题标签 “Semi Bold” 自身的实际字体是 Bold，而对应样例文字为 Semi Bold。不要依据说明标签的外观测量组件。多语言字形、换行与 RTL 必须在目标画面检查，不从 Inter 拉丁字符样例推定全部语言表现。

## 色彩与 token

**Style 色板明文**（`649:20798`）：Whale 品牌色 `#FF0055`；Blue Grey Background `#0F0F10`。Blue Grey 0/10/20/30/40/50/60/70/80/90 依次为 `#FAFAFE / #F2F2FA / #EBEBF6 / #D9D9E7 / #C1C1D0 / #9696A3 / #65656F / #494951 / #28282B / #19191C`。另有白色 0%～100% 的透明度阶梯，以及橙、粉、红、绿、紫色板。成功与错误使用其语义，不凭色相给所有控件重新配色。

**实际实例及已解析远程变量**：

| 来源 | 绑定或属性 | 观察值 |
| --- | --- | --- |
| Home `11779:75128` | `semantic-tokens/color/background/layer-0` → `core-tokens/color/other/brand/brand-background` | `#141416` |
| OS 10.4 示例 `41144:5126` | `semantic-tokens/color/overlay/dark` → `core-tokens/color/base/black/80` | 黑色，80% alpha |
| Settings 背景实例 `41144:5128` 左区域 | 实际填充 | `#1F1F22` |
| 同实例右区域 | `core-tokens/color/base/neutral-gray/1000` | `#28282B` |

本次本地变量集合查询返回空，但实例明确绑定了可解析的远程变量。**空的本地集合不等于没有设计 token。** 同样，名为 Blurred Overlay 的已检查实例里只有黑色 80% 背景，未读到 blur effect，不能由名称编造模糊半径。

不要用早期色板覆盖当前实例的语义绑定。语义层、基础层与实例可能有版本差异；新页面先复用目标场景的 token，再用截图检查实际结果。

## 布局与间距

Style / Layout 实际网格：

| 模板节点 | 标注/图层证据 |
| --- | --- |
| Home `649:20413` | 左侧 144，顶部与右侧 48，列间距 24 |
| App Store `649:20611` | 左侧 144，顶部与右侧 72，列间距 24 |
| Search `649:20418` | 左右及顶部 72，列间距 24 |

这些是不同模板的局部规则，不是统一四周安全区。网格还含延伸到屏幕外的列，不能把列数误当作一屏完整卡片数。

Home 实例 `11779:75128`：收起导航宽 144；Hero Banner 1920×630；内容与 Apps Row 从 x=144 开始。图像、阴影、焦点外扩和部分露出的下一卡片可越过内容对齐线，但关键文字和可操作内容需要按当前设备检查可见性。

## 组件、变体与状态

本次从 Home 实例追溯到的组件，ID 是检索线索，后续须重新确认：

| 实例 | 主组件 / 组件集 | 已核对内容 |
| --- | --- | --- |
| Hero Banner `11779:75130` | `51053:7727` / `51053:7726` | State=Default；有 Logo、Co-Branding、Ad Badge 等属性 |
| App Card `11779:75152` | `50845:44604` / `50845:44597` | Type=1:1，State=Focused |
| 默认 App Card `11779:75151` | `50845:44607` / 同集 | Type=1:1，State=Default |
| 内容 Card `11779:75627` | `51100:228299` / `51100:228284` | Type=16:9 Small，State=Default，Skeleton=No |
| Navigation Bar `11779:75154` | `51053:13132` / `51053:13131` | Expanded=False；组件集另有 True |

App Card 的实际变体轴：Type 含 16:9、1:1、Update、Source、16:9 Grid、Recent Source card；State 含 Active、Default、Disabled、Editing、Focused、Pressed。不要把 Active、Focused 和 Editing 合并成一个“选中态”。

**焦点测量样例**：1:1 App Card 外框仍为 138×138，但获焦内部矩形外扩至 160×160，位于 (-11,-11)，圆角 40，白色描边 4；另一内部内容框为 152×152。此值仅属于该样例，不能据此规定全系统统一放大比例或圆角。

Settings 的 10.4 示例面板是 1420×760，左右背景区域宽 548 / 872；同 section 的 Dialog 示例为 864×422。System control 又存在 800、1096、1300 宽的不同规格说明。**这些值并存，未证明是同一组件的现行统一规范**，应按目标场景、组件和版本选择，不能统一替换。

组件搜索还发现 Whale TV Design System、Design Screens 本文件、TV+、Backend、Deprecated 和投影仪测试库。复用前检查当前实例的真实来源；不要仅因库名相近或更新时间更新而换库，也不要把 Deprecated / 测试库作为默认生产依赖。
