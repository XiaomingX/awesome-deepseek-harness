# awesome-deepseek-harness

> A curated list of the DeepSeek Harness (DSH) ecosystem: plugins, tools, and infrastructure.
> Sources: [0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness), the `dsh-external/hub` catalog, and the public `dsh-plugin` GitHub topic.
> This is an English curated edition: duplicated and toy-style plugins have been filtered out, keeping only projects worth learning from.

## Contents

- [Install](#install)
- [Core & Bundles](#core--bundles)
- [Agents & Orchestration](#agents--orchestration)
- [Context & Search](#context--search)
- [Memory & Knowledge](#memory--knowledge)
- [Input & Editing](#input--editing)
- [UI, Themes & Interaction](#ui-themes--interaction)
- [Dashboards & Session UX](#dashboards--session-ux)
- [IDE & Desktop Clients](#ide--desktop-clients)
- [Browser & Remote](#browser--remote)
- [Models & Inference](#models--inference)
- [Git & Engineering](#git--engineering)
- [Security & Governance](#security--governance)
- [Output & Deliverables](#output--deliverables)
- [Notifications & Channels](#notifications--channels)
- [Design Patterns Worth Borrowing](#design-patterns-worth-borrowing)
- [Related Resources](#related-resources)

## Install

Official runtime (Node.js):

```bash
npx @deepseek-ai/dsh web
```

External profile bundle install (pnpm):

```bash
dsh plugin --profile web add "github:owner/repo#ref"
```

`dsh plugin` forwards to pnpm, supporting npm, Git/GitHub, local paths, and `file:` / `link:` specs. Only packages declaring `dsh.bundle.patch` become active layers. Management panel: Settings → Plugins.

## Core & Bundles

- **[dsh-deepresearch](https://github.com/dsh-external/dsh-deepresearch)** — DeepResearch plugin (cordis architecture).
- **[dsh-plan-execute](https://github.com/dsh-external/dsh-plan-execute)** — Dual-model plan/execute routing: a planner model thinks, an executor model acts.
- **[dsh-toolkit](https://github.com/dsh-external/dsh-toolkit)** — Zero-dependency tool suite (calculator/CSV/diff/encoding/JSON/markdown/regex/time).
- **[dsh-101](https://github.com/dsh-external/dsh-101)** — DSH documentation reading mode.
- **[dsh-equip-engine](https://github.com/wuykjl/dsh-equip-engine)** — Task-driven plugin equip engine: dual retrieval, combo scoring, conflict detection.
- **[dsh-claude-move](https://github.com/PerryLink/dsh-claude-move)** — Migration wizard: bring Claude Code, Codex, OpenCode, and Hermes sessions into DSH.

## Agents & Orchestration

- **[dsh-agent-arena](https://github.com/LeemanCheung/dsh-agent-arena)** — Compare coding agents in isolated Git worktrees.
- **[coding-coach](https://github.com/xiehuan123/coding-coach)** — Coding Coach: a 35-skill bundle plus an agent preset for non-developers.
- **[dsh-plans](https://github.com/Optim-Agent/dsh-plans)** — Planning-first agent preset.
- **[dsh-agent-team-gui](https://github.com/toolclub/dsh-agent-team-gui)** — Manage persistent multi-model squads in Settings.
- **[Knotline](https://github.com/MrMaii/knotline)** — Visual DSH project map for composing persistent agent workflows.
- **[dsh-self-evolving](https://github.com/timwhitez/dsh-self-evolving)** — Evidence-first, crash-resumable self-evolution engine.
- **[dsh-ha-orchestrator](https://github.com/Saktawdi/dsh-ha-orchestrator)** — Model high-availability failover plus subagent orchestration.
- **[dsh-background-agents](https://github.com/PerryLink/dsh-background-agents)** — Durable background child agents on the official subagent seam.

## Context & Search

- **[dsh-github-intelligence](https://github.com/zoahdev/dsh-github-intelligence)** — Read-only developer-intelligence tools across 16 ecosystems.
- **[dsh-deepread](https://github.com/xiehuan123/dsh-deepread)** — DeepRead: a deep-reading assistant with five modes.
- **[dsh-context](https://github.com/bowenliang123/dsh-context)** — Context insight panel.
- **[dsh-scope](https://github.com/helloxkk/dsh-scope)** — Context lens: per-session KV cache hit rate.
- **[dsh-compressor](https://github.com/lifeodyssey/dsh-compressor)** — Slim port of Headroom: compresses tool output.
- **[context-vista](https://github.com/GooodWei/context-vista)** — Right-side floating panel for context token usage.
- **[dsh-context-doctor](https://github.com/Zhenyu98/dsh-context-doctor)** — See what every request carries.
- **[dsh-mcp-lens](https://github.com/labmimors/dsh-mcp-lens)** — Progressive-disclosure MCP gateway.
- **[dsh-web-search-exa](https://github.com/TonyDua/dsh-web-search-exa)** — Zero-config Exa web search provider.
- **[dsh-web-search-pro](https://github.com/anweat/dsh-web-search-pro)** — Persistent enhanced web search for DSH.
- **[dsh-session-search](https://github.com/dsh-external/dsh-session-search)** — Index-free read-only search across sessions.
- **[cross-harness-cite](https://github.com/dsh-external/cross-harness-cite)** — Cite past conversations across harnesses.

## Memory & Knowledge

- **[dsh-hme](https://github.com/weopenfire-git/hme-plugin)** — Cross-session long-term memory.
- **[dsh-memory-vault](https://github.com/flymysql/dsh-memory)** — Cross-session memory vault.
- **[dsh-memory-evolve](https://github.com/dsh-external/dsh-memory-evolve)** — Cross-session long-term memory + background self-evolution.
- **[dsh-memento](https://github.com/PerryLink/dsh-memento)** — Bounded, layered, approval-gated memory.
- **[dsh-engramory](https://github.com/tinqiao-oss/engramory/tree/master/adapters/dsh)** — File-based curated memory.
- **[dsh-memory-porter](https://github.com/Shiye-10Pages/dsh-memory-porter)** — Cross-vendor memory migration.
- **[dsh-library](https://github.com/PerryLink/dsh-library)** — Local-first document knowledge base.
- **[kb-rag](https://github.com/Breeze136/kb-rag)** — Local literature knowledge-base RAG.
- **[dsh-ragflow](https://github.com/staff-os/dsh-ragflow)** — RAGFlow knowledge-base retrieval plugin.
- **[docs-retriever](https://github.com/JohnXu22786/docs-retriever)** — doctrove: versioned library documentation retrieval.
- **[snippet-expander](https://github.com/JohnXu22786/snippet-expander)** — Steno: inline `#tag` shorthand expansion.
- **[deepddw](https://github.com/ccch713/deepddw)** — Memory + knowledge base + document search in one.

## Input & Editing

- **[dsh-voice-input-plugin](https://github.com/Zhangbo-cn/dsh-voice-input-plugin)** — Composer microphone for Web UI.
- **[dsh-message-edit](https://github.com/dsh-external/dsh-message-edit)** — Branch-based message editing.
- **[dsh-prompt-studio](https://github.com/dsh-external/dsh-prompt-studio)** — Edit system-prompt sections with live preview.
- **[dsh-paste-input](https://github.com/dsh-external/dsh-paste-input)** — Ctrl+V paste files / drag & drop.
- **[dsh-voice](https://github.com/motongv/dsh-voice)** — Voice input and read-aloud for the composer.
- **[dsh-drag-and-drop](https://github.com/dsh-external/dsh-drag-and-drop)** — Cross-platform drag & drop.
- **[dsh-chat-import](https://github.com/Nwflower/dsh-chat-import)** — Import conversation histories from 13 coding agents.
- **[dsh-file-claim](https://github.com/Nwflower/dsh-file-claim)** — File claim/release protection for parallel sessions.
- **[dsh-plugin-quote-reply](https://github.com/yangYzc/dsh-plugin-quote-reply)** — Select text and quote it into the composer.
- **[dsh-pathlink](https://github.com/penguin-oo/dsh-pathlink)** — Ctrl+click file paths and links in chat.
- **[dsh-prompt-optimize](https://github.com/peterliucius/dsh-prompt-optimize)** — Rewrite composer drafts via an auxiliary LLM.
- **[dsh-composer-history](https://github.com/PerryLink/dsh-composer-history)** — Terminal-style input history for the web composer.

## UI, Themes & Interaction

- **[dsh-skin-studio](https://github.com/LeemanCheung/dsh-skin-studio)** — Local semantic-token theme editor.
- **[deepseek-harness-zh-tw](https://github.com/chiyulogg-commits/deepseek-harness-zh-tw)** — Traditional Chinese locale edition.
- **[dsh-spotlight](https://github.com/0xsline/dsh-spotlight)** — Keyboard-first command palette.
- **[arcana](https://github.com/GooodWei/arcana)** — Floating command deck for slash commands.
- **[dsh-i18n](https://github.com/Semidia/dsh-i18n)** — Chinese localization for tool results.
- **[dsh-plugin-workshop](https://github.com/yyyyukari/dsh-plugin-workshop)** — Steam Workshop-style plugin browser.
- **[dsh-markdown-preview](https://github.com/GitHubJiKe/dsh-markdown-preview)** — In-chat preview for produced files.
- **[dsh-diff-viewer](https://github.com/dsh-external/dsh-diff-viewer)** — PiUI-style Web diff viewer.
- **[dsh-split-panes](https://github.com/dsh-external/dsh-split-panes)** — Split panes.
- **[dsh-plugin-help](https://github.com/Semidia/dsh-plugin-help)** — Installed-plugins README summary panel.
- **[dsh-mcp-panel](https://github.com/PerryLink/dsh-mcp-panel)** — MCP management console.

## Dashboards & Session UX

- **[dsh-replay](https://github.com/zoahdev/dsh-replay)** — Time-travel debugger.
- **[dsh-token-usage](https://github.com/jiamuAi/dsh-token-usage)** — Codex-style token usage panel.
- **[dsh-usage-panel](https://github.com/AlfredChaos/dsh-usage-panel)** — Token usage statistics as a Settings page.
- **[dsh-web-billing](https://github.com/bpc-oss/dsh-web-billing)** — RMB/USD token billing.
- **[dsh-budget](https://github.com/PerryLink/dsh-budget)** — Cost governance for DeepSeek Harness.
- **[dsh-fork-graph](https://github.com/chouyong/dsh-fork-graph)** — Git-style conversation fork graph.
- **[dsh-branch-review](https://github.com/chouyong/dsh-branch-review)** — Track human decisions for branches.
- **[dsh-fork-diff](https://github.com/chouyong/dsh-fork-diff)** — Parent and sibling branch comparison.
- **[dsh-auto-continue](https://github.com/HsiangNianian/dsh-auto-continue)** — Auto-resumes interrupted requests.
- **[dsh-trajectory-debug](https://github.com/devmom/dsh-trajectory-debug)** — Trajectory waterfall & replay.
- **[dsh-session-manager](https://github.com/Semidia/dsh-session-manager)** — Right-click context menu on sessions.
- **[dsh-session-handoff](https://github.com/WeiYe6/dsh-session-handoff)** — Hand long sessions to a clean one.
- **[dsh-event-auditor](https://github.com/qing3a/dsh-event-auditor)** — Event-flow audit panel.

## IDE & Desktop Clients

- **[dsh-cc-tui](https://github.com/dsh-external/dsh-cc-tui)** — Claude Code-style fullscreen TUI.
- **[deepseek-harness-tui](https://github.com/openma-ai/deepseek-harness-tui)** — Rust/ratatui terminal client.
- **[deepseek-harness-desktop](https://github.com/fendouai/deepseek-harness-desktop)** — Tauri 2 desktop distribution.
- **[dsh-vscode](https://github.com/Lixxx1/dsh-vscode)** — VS Code right-sidebar client.
- **[dsh4vscode](https://github.com/DoggyHU/dsh4vscode)** — VS Code chat windows backed by DSH.
- **[dsh-plugin-open-editor](https://github.com/Civitasv/dsh-plugin-open-editor)** — Open workspace in local editor.
- **[dsh-launcher](https://github.com/iceleaf916/dsh-launcher)** — macOS menu-bar launcher.
- **[browser-automation](https://github.com/JohnXu22786/browser-automation)** — Web Bridge: browser automation MCP.
- **[computer-control](https://github.com/JohnXu22786/computer-control)** — Desktop control for dsh.

## Browser & Remote

- **[dsh-browser-panel](https://github.com/dsh-external/dsh-browser-panel)** — Headed browser embedded in WebUI.
- **[dsh-builtin-browser](https://github.com/wqty123/dsh-browser)** — Shared real browser for DSH.
- **[dsh-remote](https://github.com/flymysql/dsh-remote)** — Multi-machine remote workspace.
- **[dsh-ssh](https://github.com/jmcc-guo/dsh-ssh)** — AI-managed SSH connections.
- **[dsh-lan-access](https://github.com/Leon0555/dsh-lan-access)** — LAN access for Web GUI.
- **[dsh-computer-use](https://github.com/ZRui-C/dsh-computer-use)** — Text-first computer use.
- **[dsh-adb](https://github.com/SamXiaBing/dsh-adb)** — ADB device & bench operations.
- **[dsh-vision](https://github.com/zoahdev/dsh-vision)** — vision_analyze tool.
- **[dsh-browser-use](https://github.com/zoahdev/dsh-browser-use)** — Browser Use cloud bridge.

## Models & Inference

- **[dsh-image-gen](https://github.com/shanliuling/dsh-image-gen)** — Native image generation.
- **[dsh-codex-oauth](https://github.com/WNJXYK/dsh-codex-oauth)** — ChatGPT/Codex subscription integration.
- **[dsh-vision-router](https://github.com/ysr666/dsh-vision-router)** — Free vision for text-only agents.
- **[dsh-advisor](https://github.com/dsh-external/dsh-advisor)** — A second model reviews each turn.
- **[dsh-llm-fallbacks](https://github.com/dsh-external/dsh-llm-fallbacks)** — Role-based LLM retry/fallback.
- **[dsh-acp](https://github.com/dsh-external/dsh-acp)** — Client-neutral ACP adapter.
- **[dsh-subagent-tools](https://github.com/lynx-gt/dsh-subagent-tools)** — Per-call model/provider overrides.
- **[dsh-delegate-router](https://github.com/penguin-oo/dsh-delegate-router)** — Automatic Flash/Pro routing.
- **[dsh-smart-route](https://github.com/Semidia/dsh-smart-route)** — Smart provider routing.
- **[dsh-local-ai](https://github.com/PerryLink/dsh-local-ai)** — Ollama local-model adapter.
- **[dsh-llm-ollama](https://github.com/NOirBRight/dsh-llm-ollama)** — Ollama Cloud native chat adapter.
- **[dsh-github](https://github.com/PerryLink/dsh-github)** — Official-grade GitHub CI integration.
- **[worktree-mgr](https://github.com/JohnXu22786/worktree-mgr)** — Task-isolated git worktrees.
- **[spec-driven](https://github.com/JohnXu22786/spec-driven)** — keel: spec-driven development.
- **[adversarial-review](https://github.com/JohnXu22786/adversarial-review)** — gavel-review: adversarial code review.

## Git & Engineering

- **[dsh-git-identity](https://github.com/dsh-external/dsh-git-identity)** — Pin Git commit authorship.
- **[dsh-tool-git](https://github.com/lxj808624/dsh-tool-git)** — Structured Git tools.
- **[deepseek-harness-action](https://github.com/Lixiaoyiao/deepseek-harness-action)** — GitHub Action for PR review/CI.
- **[dsh-inspect](https://github.com/dsh-external/dsh-inspect)** — Adversarial checkup → fix → review.
- **[dsh-review-loop](https://github.com/wuxiangru915/dsh-review-loop)** — Incremental diff reviewer.
- **[dsh-test-runner](https://github.com/suimi8/dsh-test-runner)** — Structured test runner tool.
- **[dsh-doublecheck](https://github.com/PerryLink/dsh-doublecheck)** — Engineering-discipline loop.
- **[dsh-checkpoint-rewind](https://github.com/PerryLink/dsh-checkpoint-rewind)** — Claude Code /rewind for DSH.
- **[dsh-lsp-actions](https://github.com/PerryLink/dsh-lsp-actions)** — LSP action surface.
- **[dsh-git-status](https://github.com/Wongzexu/dsh-git-status)** — Git branch and status handling.
- **[safety-net](https://github.com/JohnXu22786/safety-net)** — Destructive-command interception gate.
- **[secret-guard](https://github.com/JohnXu22786/secret-guard)** — Blocks reading/writing sensitive files.
- **[arch-doc](https://github.com/duyanta123/arch-doc)** — Analyze codebase and generate docs.

## Security & Governance

- **[dsh-poison-guard](https://github.com/zoahdev/dsh-poison-guard)** — Pre-install supply-chain poison scanner.
- **[dsh-skill-pack-security](https://github.com/PerryLink/dsh-skill-pack-security)** — Security-audit skill pack + plugin_vet.
- **[dsh-encrypt](https://github.com/yauntyour/DSH-Encrypt)** — Credential provider with AES-256-GCM.
- **[dsh-telemetry-redactor](https://github.com/030611/dsh-telemetry-redactor)** — Redacts secrets from telemetry export.
- **[dsh-yolo-mode](https://github.com/SeverusZh/dsh-yolo-mode)** — LLM auto-approval for sandbox escalation.
- **[dsh-auto-review](https://github.com/PerryLink/dsh-auto-review)** — Second-model AI auto-review.
- **[dsh-permission-rules](https://github.com/PerryLink/dsh-permission-rules)** — Declarative allow/deny/ask rules.
- **[dsh-safeguard](https://github.com/ZhijiangTang/dsh-safeguard)** — Pre-execution guardrail.
- **[dsh-mask](https://github.com/PerryLink/dsh-mask)** — PII masking middleware.
- **[dsh-defend](https://github.com/PerryLink/dsh-defend)** — Prompt-injection/jailbreak detection.
- **[dsh-change-budget](https://github.com/Raphaelutumn/dsh-change-budget)** — Configurable per-turn budgets.
- **[upstream-radar](https://github.com/MicroMilo/upstream-radar)** — Dependency security monitoring.

## Output & Deliverables

- **[dsh-artifacts](https://github.com/zoahdev/dsh-artifacts)** — Claude-Artifacts-style renderer.
- **[folio](https://github.com/nyantused-cpun/folio)** — Consulting document-generation engine.
- **[dsh-report-studio](https://github.com/ciceroyang/dsh-report-studio)** — Turn a session into work reports.
- **[dsh-trajectory](https://github.com/ciceroyang/dsh-trajectory)** — Render session log into an HTML document.
- **[plugin-session-export](https://github.com/whyihaveyou/dsh-suite/tree/main/packages/plugins/plugin-session-export)** — Export session log as Markdown/HTML.
- **[dsh-translate](https://github.com/PerryLink/dsh-translate)** — Vendor parameter translation and JSON repair.

## Notifications & Channels

- **[dsh-feishu](https://github.com/PGZXB/dsh-feishu)** — Feishu (Lark) UI for DSH.
- **[dsh-feishu-bot](https://github.com/dsh-external/dsh-feishu-bot)** — Feishu bot.
- **[dsh-telegram-channel](https://github.com/hi-wenw/dsh-telegram-channel)** — Telegram mobile remote.
- **[dsh-wecom-bot](https://github.com/dsh-external/dsh-wecom-bot)** — WeCom bot.
- **[dsh-weixin-bot](https://github.com/dsh-external/dsh-weixin-bot)** — WeChat bot.
- **[dsh-im-hub](https://github.com/ThreeBody6666/dsh-im-hub)** — Multi-platform IM gateway.
- **[dsh-voice-chat](https://github.com/dsh-external/dsh-voice-chat)** — Voice chat.
- **[dsh-notify-windows](https://github.com/SeverusZh/dsh-notify-windows)** — Windows notifications.
- **[dsh-notification-sounds](https://github.com/qq33357486/dsh-notification-sounds)** — Cross-platform browser audio alerts.

## Design Patterns Worth Borrowing

After reviewing the projects above, the following patterns are worth adopting in your own harness/agent projects:

1. **Dual-model plan/execute** — `dsh-plan-execute` and `dsh-plans` split "thinking" and "acting" across different models, balancing reasoning quality with execution cost.
2. **Context compression & lens** — `dsh-compressor`, `dsh-scope`, and `dsh-context-doctor` show that visualizing context usage and compressing on demand is the core challenge for long sessions.
3. **Layered & approval-gated memory** — `dsh-memento` and `dsh-memory-gate` use bounded/layered/approval-gated design to avoid unbounded memory polluting the context.
4. **Cost governance** — `dsh-budget`, `dsh-web-billing`, and `dsh-change-budget` provide a closed loop from token metering to per-turn budgets.
5. **Security guardrail trio** — pre-install poison scanning (`dsh-poison-guard`), pre-execution guardrail (`dsh-safeguard`), and prompt-injection detection (`dsh-defend`) form a reusable protection layer.
6. **Subagents & worktree isolation** — `dsh-background-agents` and `worktree-mgr` use Git worktrees to isolate parallel tasks, a concurrency-safe pattern.
7. **Provider fallback & routing** — `dsh-llm-fallbacks`, `dsh-delegate-router`, and `dsh-smart-route` abstract multi-model scheduling into configurable routing.
8. **Observability** — `dsh-replay` (time travel), `dsh-trajectory-debug` (trajectory replay), and `dsh-event-auditor` (event audit) are key tool shapes for debugging agents.

## Related Resources

- [0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness) — The original full English list (includes more toy-style plugins).
- [dsh-external/hub](https://github.com/dsh-external) — Official catalog.
- DSH plugin spec: only packages declaring `dsh.bundle.patch` become active layers.
