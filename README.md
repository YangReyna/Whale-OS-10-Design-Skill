# Whale OS Design Skills

用于集中存储、维护和复用 Whale OS 相关设计 Skills，把设计规范、工作流程与交付经验整理成 AI 助手可以执行的任务指南。

本仓库从 Whale OS 10 的设计工作出发，逐步沉淀电视端界面、遥控器交互、设计文档和设计检查等场景的可复用方法。

## 仓库目标

- **统一设计依据**：明确适用版本、参考资料、组件规范和交互约束。
- **复用工作流程**：将重复的设计任务整理为输入清晰、步骤可执行的 Skills。
- **稳定交付质量**：约定输出格式、示例与检查标准，减少反复沟通。
- **持续迭代**：通过版本记录积累设计经验，随 Whale OS 的演进更新。

## Skills 目录

当前已收录以下 Skill：

| Skill | 适用场景 | 学习快照 |
| --- | --- | --- |
| [whale-os10-design](https://github.com/YangReyna/Whale-OS-10-Design-Skill/tree/main/skills/whale-os10-design) | Whale OS 10 的 TV、Projector、STB 大屏 UI、遥控器交互原型与用户流程设计及评审 | 2026-11-09 |

`whale-os10-design` 包含技能入口、AI 助手展示配置，以及视觉系统、交互模式、设计流程和 Figma 来源映射四份参考资料。使用时请保留完整目录；学习快照用于定位依据，实际设计仍需核对当前项目文件。

计划逐步覆盖以下方向，具体以实际收录内容为准：

| 方向 | 典型任务 |
| --- | --- |
| 界面与组件设计 | 页面布局、组件状态、设计规范应用 |
| 电视端交互 | 遥控器焦点、方向键导航、确认与返回行为 |
| 设计文档 | 页面说明、操作流程、交互规格与交付整理 |
| 设计检查 | 需求符合性、流程完整性、状态覆盖与一致性检查 |

## 如何使用

1. 在 Skills 目录中选择适合当前任务的 Skill。
2. 阅读该 Skill 的 `SKILL.md`，确认使用范围、所需资料和输出要求。
3. 在支持 Skills 的 AI 助手中按其机制加载 Skill，并提供对应的需求、设计稿或参考资料。
4. 按 Skill 的检查标准复核产出；如果发现通用问题，将改进补充回仓库。

不同 AI 助手的安装和加载方式可能不同，以所用工具的说明为准。

## 目录结构

```text
.
├── README.md             # 仓库介绍，同时作为网站首页内容
├── skills/
│   ├── README.md         # Skill 编写与维护约定
│   └── whale-os10-design/
│       ├── SKILL.md      # Whale OS 10 大屏设计
│       ├── agents/openai.yaml
│       └── references/   # 视觉、交互、设计流程及来源映射
├── _config.yml           # Jekyll 与 GitHub Pages 配置
├── index.md              # 网站入口，直接引用 README
├── assets/css/style.scss # Cayman 主题的海蓝色样式
├── Gemfile               # 本地预览依赖
└── .gitignore            # 本地依赖、缓存和构建产物忽略规则
```

每个正式 Skill 使用独立目录，入口统一命名为 `SKILL.md`。按需添加 `references/`、`assets/` 和 `scripts/`，详细规则见 [Skill 编写与维护约定](skills/README.md)。

## 新增或更新 Skill

1. 在 `skills/` 下创建使用小写英文和连字符命名的目录，例如 `whale-tv-focus-review/`。
2. 编写 `SKILL.md`，说明何时使用、需要什么、如何执行、输出什么，以及如何检查结果。
3. 标注适用的 Whale OS 版本和参考资料；将较长的规范、示例与模板放入对应的支持目录。
4. 用真实任务验证流程，再更新本 README 的 Skills 目录并提交变更。

更新现有 Skill 时，同步检查其引用资料、示例和适用版本，避免规则互相冲突。

## 文档网站

仓库使用 [Jekyll](https://jekyllrb.com/) 和 [Cayman](https://github.com/pages-themes/cayman) 主题，通过 GitHub Pages 展示文档。网站首页直接读取本 README，更新介绍时只需维护一份内容。

GitHub Pages 的发布源应设置为 `main` 分支的 `/ (root)`：在仓库的 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**。发布完成后的地址以 Pages 设置页显示为准。

本地预览需要兼容的 Ruby 和 Bundler 环境：

```sh
bundle install
bundle exec jekyll serve
```

然后打开终端显示的本地地址。主题与站点信息在 `_config.yml` 中维护，颜色和排版在 `assets/css/style.scss` 中维护。

## 维护原则

- 一个 Skill 聚焦一类明确任务，避免将所有规则堆进同一文件。
- 规则写清适用条件、执行步骤和检查依据，示例区分既定规范与说明性内容。
- 共用资料尽量引用，减少多份副本造成的版本差异。
- 以实际收录和验证过的能力为准，及时更新目录与说明。
