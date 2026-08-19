# awesome-deepseek-harness

> 语言 / Language: [简体中文](README.md) · [English](README.en.md) · [한국어](README.ko.md) · [日本語](README.ja.md)

> DeepSeek Harness (DSH) 生态精选清单：精选插件、工具与基础设施。
> 来源：[0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness)、`dsh-external/hub` 目录及公开的 `dsh-plugin` GitHub topic。
> 本清单为中文精选版，过滤了大量重复/玩具类插件，保留值得借鉴的项目。

## 目录

- [安装](#安装)
- [核心与聚合包](#核心与聚合包)
- [智能体与编排](#智能体与编排)
- [上下文与搜索](#上下文与搜索)
- [记忆与知识](#记忆与知识)
- [输入与编辑](#输入与编辑)
- [界面、主题与交互](#界面主题与交互)
- [仪表盘与会话体验](#仪表盘与会话体验)
- [IDE 与桌面客户端](#ide-与桌面客户端)
- [浏览器与远程](#浏览器与远程)
- [模型与推理](#模型与推理)
- [Git 与工程](#git-与工程)
- [安全与治理](#安全与治理)
- [输出与交付物](#输出与交付物)
- [通知与渠道](#通知与渠道)
- [可借鉴的设计思路](#可借鉴的设计思路)
- [相关资源](#相关资源)

## 安装

官方运行时（Node.js）：

```bash
npx @deepseek-ai/dsh web
```

外部 profile bundle 安装（pnpm）：

```bash
dsh plugin --profile web add "github:owner/repo#ref"
```

`dsh plugin` 实际转发给 pnpm，支持 npm、Git/GitHub、本地路径、`file:` 与 `link:` 规格。仅声明 `dsh.bundle.patch` 的包会成为激活层。管理面板：设置 → 插件。

## 核心与聚合包

- **[dsh-deepresearch](https://github.com/dsh-external/dsh-deepresearch)** — DeepResearch 插件（cordis 架构）。
- **[dsh-plan-execute](https://github.com/dsh-external/dsh-plan-execute)** — 双模型规划/执行路由：规划模型思考，执行模型行动。
- **[dsh-toolkit](https://github.com/dsh-external/dsh-toolkit)** — 零依赖工具集（计算器/CSV/Diff/编码/JSON/Markdown/正则/时间）。
- **[dsh-101](https://github.com/dsh-external/dsh-101)** — DSH 文档阅读模式。
- **[dsh-equip-engine](https://github.com/wuykjl/dsh-equip-engine)** — 任务驱动的插件装备引擎：双路检索、组合打分、冲突检测。
- **[dsh-claude-move](https://github.com/PerryLink/dsh-claude-move)** — 迁移向导：把 Claude Code、Codex、OpenCode、Hermes 会话迁入 DSH。

## 智能体与编排

- **[dsh-agent-arena](https://github.com/LeemanCheung/dsh-agent-arena)** — 在隔离的 Git worktree 中对比多个编码智能体。
- **[coding-coach](https://github.com/xiehuan123/coding-coach)** — 编程教练：35 个技能包 + 面向非开发者的智能体预设。
- **[dsh-plans](https://github.com/Optim-Agent/dsh-plans)** — 规划优先的智能体预设。
- **[dsh-agent-team-gui](https://github.com/toolclub/dsh-agent-team-gui)** — 在设置中管理持久化的多模型小队。
- **[Knotline](https://github.com/MrMaii/knotline)** — 可视化 DSH 项目地图，用于编排持久智能体工作流。
- **[dsh-self-evolving](https://github.com/timwhitez/dsh-self-evolving)** — 证据优先、崩溃可恢复的自我演进引擎。
- **[dsh-ha-orchestrator](https://github.com/Saktawdi/dsh-ha-orchestrator)** — 模型高可用故障转移 + 子代理编排。
- **[dsh-background-agents](https://github.com/PerryLink/dsh-background-agents)** — 基于官方子代理通道的持久后台子代理。

## 上下文与搜索

- **[dsh-github-intelligence](https://github.com/zoahdev/dsh-github-intelligence)** — 跨 16 个生态的只读开发者情报工具。
- **[dsh-deepread](https://github.com/xiehuan123/dsh-deepread)** — 深度阅读助手，含五种模式。
- **[dsh-context](https://github.com/bowenliang123/dsh-context)** — 上下文洞察面板。
- **[dsh-scope](https://github.com/helloxkk/dsh-scope)** — 上下文透镜：按会话统计 KV 缓存命中率。
- **[dsh-compressor](https://github.com/lifeodyssey/dsh-compressor)** — Headroom 的精简移植：压缩工具输出。
- **[context-vista](https://github.com/GooodWei/context-vista)** — 右侧浮动面板显示上下文 token 用量。
- **[dsh-context-doctor](https://github.com/Zhenyu98/dsh-context-doctor)** — 查看每次请求实际携带的内容。
- **[dsh-mcp-lens](https://github.com/labmimors/dsh-mcp-lens)** — 渐进式披露的 MCP 网关。
- **[dsh-web-search-exa](https://github.com/TonyDua/dsh-web-search-exa)** — 零配置 Exa 网页搜索提供方。
- **[dsh-web-search-pro](https://github.com/anweat/dsh-web-search-pro)** — DSH 持久增强型网页搜索。
- **[dsh-session-search](https://github.com/dsh-external/dsh-session-search)** — 跨会话的无索引只读搜索。
- **[cross-harness-cite](https://github.com/dsh-external/cross-harness-cite)** — 跨不同 harness 引用历史对话。

## 记忆与知识

- **[dsh-hme](https://github.com/weopenfire-git/hme-plugin)** — 跨会话长期记忆。
- **[dsh-memory-vault](https://github.com/flymysql/dsh-memory)** — 跨会话记忆保险库。
- **[dsh-memory-evolve](https://github.com/dsh-external/dsh-memory-evolve)** — 跨会话长期记忆 + 后台自我演进。
- **[dsh-memento](https://github.com/PerryLink/dsh-memento)** — 有界、分层、需审批通过的记忆。
- **[dsh-engramory](https://github.com/tinqiao-oss/engramory/tree/master/adapters/dsh)** — 基于文件的精选记忆。
- **[dsh-memory-porter](https://github.com/Shiye-10Pages/dsh-memory-porter)** — 跨厂商记忆迁移。
- **[dsh-library](https://github.com/PerryLink/dsh-library)** — 本地优先的文档知识库。
- **[kb-rag](https://github.com/Breeze136/kb-rag)** — 本地文献知识库 RAG。
- **[dsh-ragflow](https://github.com/staff-os/dsh-ragflow)** — RAGFlow 知识库检索插件。
- **[docs-retriever](https://github.com/JohnXu22786/docs-retriever)** — doctrove：带版本的库文档检索。
- **[snippet-expander](https://github.com/JohnXu22786/snippet-expander)** — Steno：内联 `#标签` 简写展开。
- **[deepddw](https://github.com/ccch713/deepddw)** — 记忆 + 知识库 + 文档搜索一体化。

## 输入与编辑

- **[dsh-voice-input-plugin](https://github.com/Zhangbo-cn/dsh-voice-input-plugin)** — Web UI 输入框麦克风输入。
- **[dsh-message-edit](https://github.com/dsh-external/dsh-message-edit)** — 基于分支的消息编辑。
- **[dsh-prompt-studio](https://github.com/dsh-external/dsh-prompt-studio)** — 编辑系统提示段落并实时预览。
- **[dsh-paste-input](https://github.com/dsh-external/dsh-paste-input)** — Ctrl+V 粘贴文件 / 拖拽上传。
- **[dsh-voice](https://github.com/motongv/dsh-voice)** — 输入框语音输入与朗读。
- **[dsh-drag-and-drop](https://github.com/dsh-external/dsh-drag-and-drop)** — 跨平台拖拽。
- **[dsh-chat-import](https://github.com/Nwflower/dsh-chat-import)** — 从 13 种编码智能体导入对话历史。
- **[dsh-file-claim](https://github.com/Nwflower/dsh-file-claim)** — 并行会话的文件占用/释放保护。
- **[dsh-plugin-quote-reply](https://github.com/yangYzc/dsh-plugin-quote-reply)** — 选中文并引用到输入框。
- **[dsh-pathlink](https://github.com/penguin-oo/dsh-pathlink)** — Ctrl+点击聊天中的文件路径与链接。
- **[dsh-prompt-optimize](https://github.com/peterliucius/dsh-prompt-optimize)** — 用辅助 LLM 改写输入框草稿。
- **[dsh-composer-history](https://github.com/PerryLink/dsh-composer-history)** — Web 输入框的终端式历史。

## 界面、主题与交互

- **[dsh-skin-studio](https://github.com/LeemanCheung/dsh-skin-studio)** — 本地语义 token 主题编辑器。
- **[deepseek-harness-zh-tw](https://github.com/chiyulogg-commits/deepseek-harness-zh-tw)** — 繁体中文语言包。
- **[dsh-spotlight](https://github.com/0xsline/dsh-spotlight)** — 键盘优先的命令面板。
- **[arcana](https://github.com/GooodWei/arcana)** — 浮动命令台，用于斜杠命令。
- **[dsh-i18n](https://github.com/Semidia/dsh-i18n)** — 工具结果的中文本地化。
- **[dsh-plugin-workshop](https://github.com/yyyyukari/dsh-plugin-workshop)** — Steam 创意工坊式插件浏览器。
- **[dsh-markdown-preview](https://github.com/GitHubJiKe/dsh-markdown-preview)** — 聊天中预览生成文件。
- **[dsh-diff-viewer](https://github.com/dsh-external/dsh-diff-viewer)** — Web Diff 查看器。
- **[dsh-split-panes](https://github.com/dsh-external/dsh-split-panes)** — 分屏面板。
- **[dsh-plugin-help](https://github.com/Semidia/dsh-plugin-help)** — 已安装插件的 README 摘要面板。
- **[dsh-mcp-panel](https://github.com/PerryLink/dsh-mcp-panel)** — MCP 管理控制台。

## 仪表盘与会话体验

- **[dsh-replay](https://github.com/zoahdev/dsh-replay)** — 时间旅行调试器。
- **[dsh-token-usage](https://github.com/jiamuAi/dsh-token-usage)** — Codex 风格 token 用量面板。
- **[dsh-usage-panel](https://github.com/AlfredChaos/dsh-usage-panel)** — 以设置页形式展示 token 用量统计。
- **[dsh-web-billing](https://github.com/bpc-oss/dsh-web-billing)** — 人民币/美元 token 计费。
- **[dsh-budget](https://github.com/PerryLink/dsh-budget)** — DeepSeek Harness 的成本治理。
- **[dsh-fork-graph](https://github.com/chouyong/dsh-fork-graph)** — Git 风格的对话分叉图。
- **[dsh-branch-review](https://github.com/chouyong/dsh-branch-review)** — 跟踪分支的人类决策。
- **[dsh-fork-diff](https://github.com/chouyong/dsh-fork-diff)** — 父分支与兄弟分支对比。
- **[dsh-auto-continue](https://github.com/HsiangNianian/dsh-auto-continue)** — 自动恢复被中断的请求。
- **[dsh-trajectory-debug](https://github.com/devmom/dsh-trajectory-debug)** — 轨迹瀑布流与回放。
- **[dsh-session-manager](https://github.com/Semidia/dsh-session-manager)** — 会话右键上下文菜单。
- **[dsh-session-handoff](https://github.com/WeiYe6/dsh-session-handoff)** — 把长会话交接给干净的新会话。
- **[dsh-event-auditor](https://github.com/qing3a/dsh-event-auditor)** — 事件流审计面板。

## IDE 与桌面客户端

- **[dsh-cc-tui](https://github.com/dsh-external/dsh-cc-tui)** — Claude Code 风格全屏 TUI。
- **[deepseek-harness-tui](https://github.com/openma-ai/deepseek-harness-tui)** — Rust/ratatui 终端客户端。
- **[deepseek-harness-desktop](https://github.com/fendouai/deepseek-harness-desktop)** — Tauri 2 桌面发行版。
- **[dsh-vscode](https://github.com/Lixxx1/dsh-vscode)** — VS Code 右侧栏客户端。
- **[dsh4vscode](https://github.com/DoggyHU/dsh4vscode)** — 由 DSH 支撑的 VS Code 聊天窗口。
- **[dsh-plugin-open-editor](https://github.com/Civitasv/dsh-plugin-open-editor)** — 在本地编辑器打开工作区。
- **[dsh-launcher](https://github.com/iceleaf916/dsh-launcher)** — macOS 菜单栏启动器。
- **[browser-automation](https://github.com/JohnXu22786/browser-automation)** — Web Bridge：浏览器自动化 MCP。
- **[computer-control](https://github.com/JohnXu22786/computer-control)** — 桌面控制。

## 浏览器与远程

- **[dsh-browser-panel](https://github.com/dsh-external/dsh-browser-panel)** — 嵌入 WebUI 的有头浏览器。
- **[dsh-builtin-browser](https://github.com/wqty123/dsh-browser)** — DSH 共享真实浏览器。
- **[dsh-remote](https://github.com/flymysql/dsh-remote)** — 多机远程工作区。
- **[dsh-ssh](https://github.com/jmcc-guo/dsh-ssh)** — AI 托管的 SSH 连接。
- **[dsh-lan-access](https://github.com/Leon0555/dsh-lan-access)** — Web GUI 局域网访问。
- **[dsh-computer-use](https://github.com/ZRui-C/dsh-computer-use)** — 文本优先的计算机使用。
- **[dsh-adb](https://github.com/SamXiaBing/dsh-adb)** — ADB 设备与基准操作。
- **[dsh-vision](https://github.com/zoahdev/dsh-vision)** — vision_analyze 工具。
- **[dsh-browser-use](https://github.com/zoahdev/dsh-browser-use)** — Browser Use 云桥。

## 模型与推理

- **[dsh-image-gen](https://github.com/shanliuling/dsh-image-gen)** — 原生图像生成。
- **[dsh-codex-oauth](https://github.com/WNJXYK/dsh-codex-oauth)** — ChatGPT/Codex 订阅集成。
- **[dsh-vision-router](https://github.com/ysr666/dsh-vision-router)** — 为纯文本智能体提供免费视觉能力。
- **[dsh-advisor](https://github.com/dsh-external/dsh-advisor)** — 用第二个模型逐轮审查。
- **[dsh-llm-fallbacks](https://github.com/dsh-external/dsh-llm-fallbacks)** — 基于角色的 LLM 重试/回退。
- **[dsh-acp](https://github.com/dsh-external/dsh-acp)** — 客户端无关的 ACP 适配器。
- **[dsh-subagent-tools](https://github.com/lynx-gt/dsh-subagent-tools)** — 每次调用可覆盖模型/提供方。
- **[dsh-delegate-router](https://github.com/penguin-oo/dsh-delegate-router)** — 自动 Flash/Pro 路由。
- **[dsh-smart-route](https://github.com/Semidia/dsh-smart-route)** — 智能提供方路由。
- **[dsh-local-ai](https://github.com/PerryLink/dsh-local-ai)** — Ollama 本地模型适配器。
- **[dsh-llm-ollama](https://github.com/NOirBRight/dsh-llm-ollama)** — Ollama Cloud 原生聊天适配器。
- **[dsh-github](https://github.com/PerryLink/dsh-github)** — 官方级 GitHub CI 集成。
- **[worktree-mgr](https://github.com/JohnXu22786/worktree-mgr)** — 任务隔离的 Git worktree。
- **[spec-driven](https://github.com/JohnXu22786/spec-driven)** — keel：规格驱动开发。
- **[adversarial-review](https://github.com/JohnXu22786/adversarial-review)** — gavel-review：对抗式代码审查。

## Git 与工程

- **[dsh-git-identity](https://github.com/dsh-external/dsh-git-identity)** — 固定 Git 提交作者身份。
- **[dsh-tool-git](https://github.com/lxj808624/dsh-tool-git)** — 结构化 Git 工具。
- **[deepseek-harness-action](https://github.com/Lixiaoyiao/deepseek-harness-action)** — 用于 PR 审查/CI 的 GitHub Action。
- **[dsh-inspect](https://github.com/dsh-external/dsh-inspect)** — 对抗式检查 → 修复 → 审查。
- **[dsh-review-loop](https://github.com/wuxiangru915/dsh-review-loop)** — 增量 diff 审查器。
- **[dsh-test-runner](https://github.com/suimi8/dsh-test-runner)** — 结构化测试运行工具。
- **[dsh-doublecheck](https://github.com/PerryLink/dsh-doublecheck)** — 工程纪律循环。
- **[dsh-checkpoint-rewind](https://github.com/PerryLink/dsh-checkpoint-rewind)** — DSH 版 Claude Code `/rewind`。
- **[dsh-lsp-actions](https://github.com/PerryLink/dsh-lsp-actions)** — LSP 动作面。
- **[dsh-git-status](https://github.com/Wongzexu/dsh-git-status)** — Git 分支与状态处理。
- **[safety-net](https://github.com/JohnXu22786/safety-net)** — 破坏性命令拦截闸门。
- **[secret-guard](https://github.com/JohnXu22786/secret-guard)** — 阻止读写敏感文件。
- **[arch-doc](https://github.com/duyanta123/arch-doc)** — 分析代码库并生成文档。

## 安全与治理

- **[dsh-poison-guard](https://github.com/zoahdev/dsh-poison-guard)** — 安装前供应链投毒扫描。
- **[dsh-skill-pack-security](https://github.com/PerryLink/dsh-skill-pack-security)** — 安全审计技能包 + plugin_vet。
- **[dsh-encrypt](https://github.com/yauntyour/DSH-Encrypt)** — AES-256-GCM 凭据提供方。
- **[dsh-telemetry-redactor](https://github.com/030611/dsh-telemetry-redactor)** — 从遥测导出中脱敏密钥。
- **[dsh-yolo-mode](https://github.com/SeverusZh/dsh-yolo-mode)** — LLM 沙箱升级自动批准。
- **[dsh-auto-review](https://github.com/PerryLink/dsh-auto-review)** — 第二模型 AI 自动审查。
- **[dsh-permission-rules](https://github.com/PerryLink/dsh-permission-rules)** — 声明式允许/拒绝/询问规则。
- **[dsh-safeguard](https://github.com/ZhijiangTang/dsh-safeguard)** — 执行前护栏。
- **[dsh-mask](https://github.com/PerryLink/dsh-mask)** — PII 脱敏中间件。
- **[dsh-defend](https://github.com/PerryLink/dsh-defend)** — 提示注入/越狱检测。
- **[dsh-change-budget](https://github.com/Raphaelutumn/dsh-change-budget)** — 可配置的每轮预算。
- **[upstream-radar](https://github.com/MicroMilo/upstream-radar)** — 依赖安全监控。

## 输出与交付物

- **[dsh-artifacts](https://github.com/zoahdev/dsh-artifacts)** — Claude Artifacts 风格渲染器。
- **[folio](https://github.com/nyantused-cpun/folio)** — 咨询文档生成引擎。
- **[dsh-report-studio](https://github.com/ciceroyang/dsh-report-studio)** — 把会话转为工作汇报。
- **[dsh-trajectory](https://github.com/ciceroyang/dsh-trajectory)** — 把会话日志渲染为 HTML 文档。
- **[plugin-session-export](https://github.com/whyihaveyou/dsh-suite/tree/main/packages/plugins/plugin-session-export)** — 导出会话日志为 Markdown/HTML。
- **[dsh-translate](https://github.com/PerryLink/dsh-translate)** — 厂商参数翻译与 JSON 修复。

## 通知与渠道

- **[dsh-feishu](https://github.com/PGZXB/dsh-feishu)** — 飞书（Lark）UI。
- **[dsh-feishu-bot](https://github.com/dsh-external/dsh-feishu-bot)** — 飞书机器人。
- **[dsh-telegram-channel](https://github.com/hi-wenw/dsh-telegram-channel)** — Telegram 移动远程。
- **[dsh-wecom-bot](https://github.com/dsh-external/dsh-wecom-bot)** — 企业微信机器人。
- **[dsh-weixin-bot](https://github.com/dsh-external/dsh-weixin-bot)** — 微信机器人。
- **[dsh-im-hub](https://github.com/ThreeBody6666/dsh-im-hub)** — 多平台 IM 网关。
- **[dsh-voice-chat](https://github.com/dsh-external/dsh-voice-chat)** — 语音聊天。
- **[dsh-notify-windows](https://github.com/SeverusZh/dsh-notify-windows)** — Windows 通知。
- **[dsh-notification-sounds](https://github.com/qq33357486/dsh-notification-sounds)** — 跨平台浏览器音频提醒。

## 可借鉴的设计思路

在分析上述项目后，以下模式值得在自己的 harness/agent 项目中借鉴：

1. **双模型规划/执行（Plan-Execute）** — `dsh-plan-execute` 与 `dsh-plans` 把"思考"与"行动"拆分到不同模型，兼顾推理质量与执行成本。
2. **上下文压缩与透镜** — `dsh-compressor`、`dsh-scope`、`dsh-context-doctor` 揭示了"把上下文占用可视化 + 按需压缩"是长会话的核心难题。
3. **记忆的分层与审批** — `dsh-memento`、`dsh-memory-gate` 用有界/分层/需审批的设计，避免无限制记忆污染上下文。
4. **成本治理** — `dsh-budget`、`dsh-web-billing`、`dsh-change-budget` 提供了从 token 计量到每轮预算的控费闭环。
5. **安全护栏三件套** — 安装前投毒扫描（`dsh-poison-guard`）、执行前护栏（`dsh-safeguard`）、提示注入检测（`dsh-defend`）构成可复用的防护层。
6. **子代理与 worktree 隔离** — `dsh-background-agents`、`worktree-mgr` 用 Git worktree 隔离并行任务，是并发安全的实践范式。
7. **Provider 回退与路由** — `dsh-llm-fallbacks`、`dsh-delegate-router`、`dsh-smart-route` 把多模型调度抽象为可配置路由。
8. **可观测性** — `dsh-replay`（时间旅行）、`dsh-trajectory-debug`（轨迹回放）、`dsh-event-auditor`（事件审计）是调试 agent 的关键工具形态。

## 相关资源

- [0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness) — 英文原版完整清单（含更多玩具类插件）。
- [dsh-external/hub](https://github.com/dsh-external) — 官方聚合目录。
- DSH 插件开发规范：声明 `dsh.bundle.patch` 的包才成为激活层。
