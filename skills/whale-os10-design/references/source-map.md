# Figma 来源、覆盖范围与刷新入口

学习日期：2026-11-09。文件 key：`CO5mm83RUOgYtGwfEeXRGj`。用户提供的 `976:12810` 是 **Whale OS 10 封面 Page**，不是全部页面规范；本次读取了全文件页面目录，再定位相关规范与样例。

## 已深入读取的依据

“深入”指本次读取到文字、具体图层属性、组件来源或原型事件之一；截图取证另列。不表示每一张状态图都已审查或真机测试。

| 来源 | 阅读范围与后续用途 |
| --- | --- |
| [Style / Typography](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=649-20346) | 字号、行高与字重样例 |
| [Style / Color](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=649-20798) | 品牌、Blue Grey、语义色板与白色透明度 |
| [Style / Layout](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=649-20402) | Home / App Store / Search 模板和实际网格；查看过整板截图 |
| [Design System 架构](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=2630-6384) | 风格基础与组件、产品端关系示意，不是可直接复用的完整组件清单 |
| [交付结构 Guideline](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=20470-73353) | 总则、模块、状态文档与目录组织 |
| [Focus Navigation](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=20470-73363) | Slot / Source 非锁定焦点示意；查看过截图 |
| [Focus Mapping](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=20470-74018) | 就近映射与指定一对多记忆例外 |
| [Settings 已有交互总则](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=20470-74560) | 双层级、列表滚动及各控件按键 |
| [Settings 补充板](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=53954-79974) | 仅局部文字读取；另有 `53954:80352` 长篇 Description，含泛化建议，不作为统一定稿 |
| [Home 登录示例](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=11779-75128) | 截图、1920×1080 布局、实际背景 token、主组件及变体、获焦 App Card 外扩 |
| [Home Apps Row 说明](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=23640-113307) | 前六项及推荐联动；相邻 `23640:113355` 读取默认 Netflix 与 400ms 分支 |
| [OOBE Language](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=3437-5741) | 截图及桌面原型事件；说明节点 `4109:42251` |
| [OOBE Network](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=4709-17796) | Wireless/Wired/Skip 状态；说明 `4238:66890` 与 `4328:6613` |
| [Search Page](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=23269-50132) | 文字读取：输入/键盘/提示/返回；未运行完整搜索原型 |
| [Apps Error State](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=23269-71340) | 文字读取：断网暂停恢复、失败、重试、存储不足 |
| [10.4 颜色调整](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=41144-5041) | 设置/遮罩调整说明；`41144:5123` 截图、`41144:5128` 左右背景、`41144:5171` Dialog 测量 |
| [10.4 Discovery Tab](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=34750-33627) | 明确的新旧 OK 行为对比 |
| [10.4 详情页](https://www.figma.com/design/CO5mm83RUOgYtGwfEeXRGj?node-id=41327-73239) | 文字读取首屏、播放源、预告及 Tab 分支；说明 `41327:83619` |

## 已定位，尚未完整验证的模块

以下已读取页面或 section 目录；有些只有目录，不能宣称已经掌握该模块全部业务逻辑。

| Page | ID | 已知入口 |
| --- | --- | --- |
| System control | `6242:36287` | Toast、Dialog、Snack Bar、Action Bar、Watermark 等与多种尺寸说明 |
| Design Helper & Guildline | `50468:71382` | Branding、Co-Branding、Banner Safety、E-Sticker、Lock Background |
| OS 10.4 Iterations | `34750:26180` | 版本差异汇总；骨架、遮罩、Apps、Discovery、详情、LiveTV |
| OOBE | `1:7` | 语言、地区、配对、网络、TOU、注册登录、Setting Up、语音、后续扩展 |
| User Center | `12540:220099` | 账号切换、编辑、Whale Card、FootPrint、Watch&Earn、交易记录 |
| Home | `6888:25092` | FirstScreen、Apps Row、Recent Source、Navigation、Apps Edit、后续屏、User Flow |
| Discovery | `7329:23266` | Landing、各类详情、Filter、Favourites、State |
| Search | `7317:36588` | Search Page、Search Result、State |
| Item Detail Pages | `7649:60401` | Channel、Movie、TV Show、People、Live、Video、长文浮层、骨架 |
| App Store | `7329:59427` | Banner、My Apps、Detail、Recommended、Search、Error、Overview |
| live TV | `14240:6545` | 当前频道、快速跳转、收藏、列表类别、多选、删除、TV Guide、频道列表和地区差异 |
| Network & Connection | `11198:11175` | 有线/无线、Bluetooth、HDMI、AirPlay2 样例 |

全文件目录还包含 Theme Transfer、TV+ Integration、Ads、AI Voice、Screensaver、Global Menu，以及 Picture & Sound、Device Preferences、Child Code、Channel Installation、Accessibility、Software Update、Hotel Mode、App Settings、Voice Service、Lock Device、OTA 等页面。未深入读取其全部状态；部分 Page 在目录中为空，空 Page 不证明功能不存在。Free TV 明示 Before 10.4，后续使用需注意版本。

## 后续刷新与取证

1. 沿对应 Page/section 重新定位当前对象，不假设历史 ID 永远有效。先确认版本、隐藏/废弃状态及用户当前定稿。
2. 对将要复用的具体实例追溯主组件、变体和语义绑定；需要时解析远程变量别名。不要因本地变量集合为空而重建 token。
3. 复杂流程读取实际六键说明、有效目标与分支；只有 User Flow 分组名或附近摆放关系不足以证明流程。本次 Home User Flow 仅核对了结构，未重建全部连线几何。
4. 刷新相关规则与证据即可，不为一个新页面重新导出整个大文件。更新技能时保留适用范围和版本例外，不把新局部规则覆盖全系统。

临时截图资源 URL 不作为永久来源；需要复核时使用本表的稳定 Figma 节点链接重新截图。
