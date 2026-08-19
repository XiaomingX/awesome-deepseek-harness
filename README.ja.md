# awesome-deepseek-harness

> DeepSeek Harness（DSH）エコシステムの厳選リスト：プラグイン、ツール、インフラ。
> 出典：[0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness)、`dsh-external/hub` カタログ、および公開 `dsh-plugin` GitHub トピック。
> 本リストは日本語厳選版であり、重複やお遊び目的のプラグインを除外し、参考になるプロジェクトのみを収録しています。

## 目次

- [インストール](#インストール)
- [コアとバンドル](#コアとバンドル)
- [エージェントとオーケストレーション](#エージェントとオーケストレーション)
- [コンテキストと検索](#コンテキストと検索)
- [メモリと知識](#メモリと知識)
- [入力と編集](#入力と編集)
- [UI、テーマとインタラクション](#uiテーマとインタラクション)
- [ダッシュボードとセッション体験](#ダッシュボードとセッション体験)
- [IDE とデスクトップクライアント](#ide-とデスクトップクライアント)
- [ブラウザとリモート](#ブラウザとリモート)
- [モデルと推論](#モデルと推論)
- [Git とエンジニアリング](#git-とエンジニアリング)
- [セキュリティとガバナンス](#セキュリティとガバナンス)
- [出力とデリバラブル](#出力とデリバラブル)
- [通知とチャネル](#通知とチャネル)
- [参考にできる設計パターン](#参考にできる設計パターン)
- [関連リソース](#関連リソース)

## インストール

公式ランタイム（Node.js）:

```bash
npx @deepseek-ai/dsh web
```

外部プロフィールバンドルのインストール（pnpm）:

```bash
dsh plugin --profile web add "github:owner/repo#ref"
```

`dsh plugin` は pnpm に処理を渡し、npm、Git/GitHub、ローカルパス、`file:` および `link:` 仕様をサポートします。`dsh.bundle.patch` を宣言したパッケージのみが有効なレイヤーとなります。管理パネル: 設定 → プラグイン。

## コアとバンドル

- **[dsh-deepresearch](https://github.com/dsh-external/dsh-deepresearch)** — DeepResearch プラグイン（cordis アーキテクチャ）。
- **[dsh-plan-execute](https://github.com/dsh-external/dsh-plan-execute)** — デュアルモデルの計画/実行ルーティング：プランナーモデルが思考し、実行モデルが行動する。
- **[dsh-toolkit](https://github.com/dsh-external/dsh-toolkit)** — 依存関係のないツール一式（電卓/CSV/diff/エンコード/JSON/markdown/正規表現/時刻）。
- **[dsh-101](https://github.com/dsh-external/dsh-101)** — DSH ドキュメント読み取りモード。
- **[dsh-equip-engine](https://github.com/wuykjl/dsh-equip-engine)** — タスク駆動型プラグイン装備エンジン：二重検索、組み合わせスコアリング、競合検出。
- **[dsh-claude-move](https://github.com/PerryLink/dsh-claude-move)** — 移行ウィザード：Claude Code、Codex、OpenCode、Hermes のセッションを DSH へ取り込む。

## エージェントとオーケストレーション

- **[dsh-agent-arena](https://github.com/LeemanCheung/dsh-agent-arena)** — 隔離された Git worktree 上でコーディングエージェントを比較。
- **[coding-coach](https://github.com/xiehuan123/coding-coach)** — コーディングコーチ：非開発者向け 35 スキルバンドル＋エージェントプリセット。
- **[dsh-plans](https://github.com/Optim-Agent/dsh-plans)** — 計画優先のエージェントプリセット。
- **[dsh-agent-team-gui](https://github.com/toolclub/dsh-agent-team-gui)** — 設定で永続的なマルチモデルチームを管理。
- **[Knotline](https://github.com/MrMaii/knotline)** — 永続的エージェントワークフローを構成するための視覚的 DSH プロジェクトマップ。
- **[dsh-self-evolving](https://github.com/timwhitez/dsh-self-evolving)** — 証拠優先、クラッシュから再開可能な自己進化エンジン。
- **[dsh-ha-orchestrator](https://github.com/Saktawdi/dsh-ha-orchestrator)** — モデルの高可用性フェイルオーバー＋サブエージェントオーケストレーション。
- **[dsh-background-agents](https://github.com/PerryLink/dsh-background-agents)** — 公式サブエージェント層を基盤とした永続バックグラウンド子エージェント。

## コンテキストと検索

- **[dsh-github-intelligence](https://github.com/zoahdev/dsh-github-intelligence)** — 16 のエコシステムにまたがる読み取り専用開発者インテリジェンスツール。
- **[dsh-deepread](https://github.com/xiehuan123/dsh-deepread)** — 5 つのモードを持つ深読みアシスタント DeepRead。
- **[dsh-context](https://github.com/bowenliang123/dsh-context)** — コンテキスト洞察パネル。
- **[dsh-scope](https://github.com/helloxkk/dsh-scope)** — コンテキストレンズ：セッションごとの KV キャッシュヒット率。
- **[dsh-compressor](https://github.com/lifeodyssey/dsh-compressor)** — Headroom の軽量ポート：ツール出力を圧縮。
- **[context-vista](https://github.com/GooodWei/context-vista)** — コンテキストトークン使用量を示す右側フローティングパネル。
- **[dsh-context-doctor](https://github.com/Zhenyu98/dsh-context-doctor)** — 各リクエストが実際に何を運ぶかを確認。
- **[dsh-mcp-lens](https://github.com/labmimors/dsh-mcp-lens)** — 段階的開示（progressive-disclosure）MCP ゲートウェイ。
- **[dsh-web-search-exa](https://github.com/TonyDua/dsh-web-search-exa)** — ゼロ設定の Exa Web 検索プロバイダ。
- **[dsh-web-search-pro](https://github.com/anweat/dsh-web-search-pro)** — DSH 向け永続強化 Web 検索。
- **[dsh-session-search](https://github.com/dsh-external/dsh-session-search)** — インデックス不要のセッション間読み取り専用検索。
- **[cross-harness-cite](https://github.com/dsh-external/cross-harness-cite)** — 異なる harness 間で過去の対話を引用。

## メモリと知識

- **[dsh-hme](https://github.com/weopenfire-git/hme-plugin)** — セッション間の長期メモリ。
- **[dsh-memory-vault](https://github.com/flymysql/dsh-memory)** — セッション間メモリボールト。
- **[dsh-memory-evolve](https://github.com/dsh-external/dsh-memory-evolve)** — セッション間長期メモリ＋バックグラウンド自己進化。
- **[dsh-memento](https://github.com/PerryLink/dsh-memento)** — 境界付き（bounded）、階層的、承認ゲート付きメモリ。
- **[dsh-engramory](https://github.com/tinqiao-oss/engramory/tree/master/adapters/dsh)** — ファイルベースのキュレーション済みメモリ。
- **[dsh-memory-porter](https://github.com/Shiye-10Pages/dsh-memory-porter)** — ベンダー間メモリ移行。
- **[dsh-library](https://github.com/PerryLink/dsh-library)** — ローカル優先のドキュメント知識ベース。
- **[kb-rag](https://github.com/Breeze136/kb-rag)** — ローカル文献知識ベース RAG。
- **[dsh-ragflow](https://github.com/staff-os/dsh-ragflow)** — RAGFlow 知識ベース検索プラグイン。
- **[docs-retriever](https://github.com/JohnXu22786/docs-retriever)** — doctrove：バージョン管理されたライブラリドキュメント検索。
- **[snippet-expander](https://github.com/JohnXu22786/snippet-expander)** — Steno：インライン `#タグ` 短縮展開。
- **[deepddw](https://github.com/ccch713/deepddw)** — メモリ＋知識ベース＋文書検索を一つに。

## 入力と編集

- **[dsh-voice-input-plugin](https://github.com/Zhangbo-cn/dsh-voice-input-plugin)** — Web UI コンポーザ用マイク入力。
- **[dsh-message-edit](https://github.com/dsh-external/dsh-message-edit)** — ブランチベースのメッセージ編集。
- **[dsh-prompt-studio](https://github.com/dsh-external/dsh-prompt-studio)** — システムプロンプトのセクションをライブプレビュー付きで編集。
- **[dsh-paste-input](https://github.com/dsh-external/dsh-paste-input)** — Ctrl+V でファイル貼り付け／ドラッグ＆ドロップ。
- **[dsh-voice](https://github.com/motongv/dsh-voice)** — コンポーザ用音声入力と読み上げ。
- **[dsh-drag-and-drop](https://github.com/dsh-external/dsh-drag-and-drop)** — クロスプラットフォームのドラッグ＆ドロップ。
- **[dsh-chat-import](https://github.com/Nwflower/dsh-chat-import)** — 13 種類のコーディングエージェントから対話履歴をインポート。
- **[dsh-file-claim](https://github.com/Nwflower/dsh-file-claim)** — 並列セッション向けファイル占有／解放保護。
- **[dsh-plugin-quote-reply](https://github.com/yangYzc/dsh-plugin-quote-reply)** — テキストを選択してコンポーザへ引用として挿入。
- **[dsh-pathlink](https://github.com/penguin-oo/dsh-pathlink)** — チャット内のファイルパスとリンクを Ctrl+クリック。
- **[dsh-prompt-optimize](https://github.com/peterliucius/dsh-prompt-optimize)** — 補助 LLM でコンポーザ下書きを書き直し。
- **[dsh-composer-history](https://github.com/PerryLink/dsh-composer-history)** — Web コンポーザ向けターミナル風入力履歴。

## UI、テーマとインタラクション

- **[dsh-skin-studio](https://github.com/LeemanCheung/dsh-skin-studio)** — ローカル意味トークンテーマエディタ。
- **[deepseek-harness-zh-tw](https://github.com/chiyulogg-commits/deepseek-harness-zh-tw)** — 繁体字中国語ロケール版。
- **[dsh-spotlight](https://github.com/0xsline/dsh-spotlight)** — キーボード優先のコマンドパレット。
- **[arcana](https://github.com/GooodWei/arcana)** — スラッシュコマンド用フローティングコマンドデッキ。
- **[dsh-i18n](https://github.com/Semidia/dsh-i18n)** — ツール結果の中国語ローカライズ。
- **[dsh-plugin-workshop](https://github.com/yyyyukari/dsh-plugin-workshop)** — Steam Workshop 風プラグインブラウザ。
- **[dsh-markdown-preview](https://github.com/GitHubJiKe/dsh-markdown-preview)** — 生成ファイルのチャット内プレビュー。
- **[dsh-diff-viewer](https://github.com/dsh-external/dsh-diff-viewer)** — PiUI 風 Web diff ビューア。
- **[dsh-split-panes](https://github.com/dsh-external/dsh-split-panes)** — 分割ペイン。
- **[dsh-plugin-help](https://github.com/Semidia/dsh-plugin-help)** — インストール済みプラグインの README 要約パネル。
- **[dsh-mcp-panel](https://github.com/PerryLink/dsh-mcp-panel)** — MCP 管理コンソール。

## ダッシュボードとセッション体験

- **[dsh-replay](https://github.com/zoahdev/dsh-replay)** — タイムトラベルデバッガ。
- **[dsh-token-usage](https://github.com/jiamuAi/dsh-token-usage)** — Codex 風トークン使用量パネル。
- **[dsh-usage-panel](https://github.com/AlfredChaos/dsh-usage-panel)** — 設定ページ形態のトークン使用量統計。
- **[dsh-web-billing](https://github.com/bpc-oss/dsh-web-billing)** — 人民元／米ドル建てトークン課金。
- **[dsh-budget](https://github.com/PerryLink/dsh-budget)** — DeepSeek Harness のコストガバナンス。
- **[dsh-fork-graph](https://github.com/chouyong/dsh-fork-graph)** — Git 風の対話フォークグラフ。
- **[dsh-branch-review](https://github.com/chouyong/dsh-branch-review)** — ブランチに対する人間の決定を追跡。
- **[dsh-fork-diff](https://github.com/chouyong/dsh-fork-diff)** — 親および兄弟ブランチの比較。
- **[dsh-auto-continue](https://github.com/HsiangNianian/dsh-auto-continue)** — 中断されたリクエストを自動再開。
- **[dsh-trajectory-debug](https://github.com/devmom/dsh-trajectory-debug)** — 軌跡ウォーターフォールと再生。
- **[dsh-session-manager](https://github.com/Semidia/dsh-session-manager)** — セッションの右クリックコンテキストメニュー。
- **[dsh-session-handoff](https://github.com/WeiYe6/dsh-session-handoff)** — 長いセッションを清潔な新セッションへ引き継ぎ。
- **[dsh-event-auditor](https://github.com/qing3a/dsh-event-auditor)** — イベントフロー監査パネル。

## IDE とデスクトップクライアント

- **[dsh-cc-tui](https://github.com/dsh-external/dsh-cc-tui)** — Claude Code 風全画面 TUI。
- **[deepseek-harness-tui](https://github.com/openma-ai/deepseek-harness-tui)** — Rust/ratatui ターミナルクライアント。
- **[deepseek-harness-desktop](https://github.com/fendouai/deepseek-harness-desktop)** — Tauri 2 デスクトップ配布版。
- **[dsh-vscode](https://github.com/Lixxx1/dsh-vscode)** — VS Code 右サイドバークライアント。
- **[dsh4vscode](https://github.com/DoggyHU/dsh4vscode)** — DSH 基盤の VS Code チャットウィンドウ。
- **[dsh-plugin-open-editor](https://github.com/Civitasv/dsh-plugin-open-editor)** — ローカルエディタでワークスペースを開く。
- **[dsh-launcher](https://github.com/iceleaf916/dsh-launcher)** — macOS メニューバーランチャー。
- **[browser-automation](https://github.com/JohnXu22786/browser-automation)** — Web Bridge：ブラウザ自動化 MCP。
- **[computer-control](https://github.com/JohnXu22786/computer-control)** — dsh 向けデスクトップ制御。

## ブラウザとリモート

- **[dsh-browser-panel](https://github.com/dsh-external/dsh-browser-panel)** — WebUI に組み込まれたヘッド付きブラウザ。
- **[dsh-builtin-browser](https://github.com/wqty123/dsh-browser)** — DSH 向け共有実ブラウザ。
- **[dsh-remote](https://github.com/flymysql/dsh-remote)** — マルチマシンリモートワークスペース。
- **[dsh-ssh](https://github.com/jmcc-guo/dsh-ssh)** — AI 管理型 SSH 接続。
- **[dsh-lan-access](https://github.com/Leon0555/dsh-lan-access)** — Web GUI の LAN アクセス。
- **[dsh-computer-use](https://github.com/ZRui-C/dsh-computer-use)** — テキスト優先のコンピュータ使用。
- **[dsh-adb](https://github.com/SamXiaBing/dsh-adb)** — ADB デバイスおよびベンチ操作。
- **[dsh-vision](https://github.com/zoahdev/dsh-vision)** — vision_analyze ツール。
- **[dsh-browser-use](https://github.com/zoahdev/dsh-browser-use)** — Browser Use クラウドブリッジ。

## モデルと推論

- **[dsh-image-gen](https://github.com/shanliuling/dsh-image-gen)** — ネイティブ画像生成。
- **[dsh-codex-oauth](https://github.com/WNJXYK/dsh-codex-oauth)** — ChatGPT/Codex サブスクリプション統合。
- **[dsh-vision-router](https://github.com/ysr666/dsh-vision-router)** — テキスト専用エージェント向け無料ビジョン。
- **[dsh-advisor](https://github.com/dsh-external/dsh-advisor)** — 2 つ目のモデルが各ターンをレビュー。
- **[dsh-llm-fallbacks](https://github.com/dsh-external/dsh-llm-fallbacks)** — 役割ベースの LLM 再試行／フォールバック。
- **[dsh-acp](https://github.com/dsh-external/dsh-acp)** — クライアント非依存の ACP アダプタ。
- **[dsh-subagent-tools](https://github.com/lynx-gt/dsh-subagent-tools)** — 呼び出しごとのモデル／プロバイダ上書き。
- **[dsh-delegate-router](https://github.com/penguin-oo/dsh-delegate-router)** — 自動 Flash/Pro ルーティング。
- **[dsh-smart-route](https://github.com/Semidia/dsh-smart-route)** — スマートプロバイダルーティング。
- **[dsh-local-ai](https://github.com/PerryLink/dsh-local-ai)** — Ollama ローカルモデルアダプタ。
- **[dsh-llm-ollama](https://github.com/NOirBRight/dsh-llm-ollama)** — Ollama Cloud ネイティブチャットアダプタ。
- **[dsh-github](https://github.com/PerryLink/dsh-github)** — 公式級 GitHub CI 統合。
- **[worktree-mgr](https://github.com/JohnXu22786/worktree-mgr)** — タスク隔離型 Git worktree。
- **[spec-driven](https://github.com/JohnXu22786/spec-driven)** — keel：仕様駆動開発。
- **[adversarial-review](https://github.com/JohnXu22786/adversarial-review)** — gavel-review：敵対的コードレビュー。

## Git とエンジニアリング

- **[dsh-git-identity](https://github.com/dsh-external/dsh-git-identity)** — Git コミット作成者を固定。
- **[dsh-tool-git](https://github.com/lxj808624/dsh-tool-git)** — 構造化された Git ツール。
- **[deepseek-harness-action](https://github.com/Lixiaoyiao/deepseek-harness-action)** — PR レビュー／CI 向け GitHub Action。
- **[dsh-inspect](https://github.com/dsh-external/dsh-inspect)** — 敵対的点検 → 修正 → レビュー。
- **[dsh-review-loop](https://github.com/wuxiangru915/dsh-review-loop)** — 増分 diff レビューア。
- **[dsh-test-runner](https://github.com/suimi8/dsh-test-runner)** — 構造化されたテストランナーツール。
- **[dsh-doublecheck](https://github.com/PerryLink/dsh-doublecheck)** — エンジニアリング規律ループ。
- **[dsh-checkpoint-rewind](https://github.com/PerryLink/dsh-checkpoint-rewind)** — DSH 向け Claude Code `/rewind`。
- **[dsh-lsp-actions](https://github.com/PerryLink/dsh-lsp-actions)** — LSP アクションサーフェス。
- **[dsh-git-status](https://github.com/Wongzexu/dsh-git-status)** — Git ブランチとステータス処理。
- **[safety-net](https://github.com/JohnXu22786/safety-net)** — 破壊的コマンド遮断ゲート。
- **[secret-guard](https://github.com/JohnXu22786/secret-guard)** — 機密ファイルの読み書きをブロック。
- **[arch-doc](https://github.com/duyanta123/arch-doc)** — コードベースを分析してドキュメントを生成。

## セキュリティとガバナンス

- **[dsh-poison-guard](https://github.com/zoahdev/dsh-poison-guard)** — インストール前サプライチェーン汚染（poison）スキャナ。
- **[dsh-skill-pack-security](https://github.com/PerryLink/dsh-skill-pack-security)** — セキュリティ監査スキルパック＋plugin_vet。
- **[dsh-encrypt](https://github.com/yauntyour/DSH-Encrypt)** — AES-256-GCM 資格情報プロバイダ。
- **[dsh-telemetry-redactor](https://github.com/030611/dsh-telemetry-redactor)** — テレメトリ出力からシークレットを削除。
- **[dsh-yolo-mode](https://github.com/SeverusZh/dsh-yolo-mode)** — サンドボックス権限昇格の LLM 自動承認。
- **[dsh-auto-review](https://github.com/PerryLink/dsh-auto-review)** — 2 つ目のモデルによる AI 自動レビュー。
- **[dsh-permission-rules](https://github.com/PerryLink/dsh-permission-rules)** — 宣言的な許可／拒否／確認ルール。
- **[dsh-safeguard](https://github.com/ZhijiangTang/dsh-safeguard)** — 実行前ガードレール。
- **[dsh-mask](https://github.com/PerryLink/dsh-mask)** — PII マスキングミドルウェア。
- **[dsh-defend](https://github.com/PerryLink/dsh-defend)** — プロンプトインジェクション／ジェイルブレイク検知。
- **[dsh-change-budget](https://github.com/Raphaelutumn/dsh-change-budget)** — 設定可能なターンごとの予算。
- **[upstream-radar](https://github.com/MicroMilo/upstream-radar)** — 依存関係セキュリティ監視。

## 出力とデリバラブル

- **[dsh-artifacts](https://github.com/zoahdev/dsh-artifacts)** — Claude Artifacts 風レンダラ。
- **[folio](https://github.com/nyantused-cpun/folio)** — コンサルティング文書生成エンジン。
- **[dsh-report-studio](https://github.com/ciceroyang/dsh-report-studio)** — セッションを業務レポートに変換。
- **[dsh-trajectory](https://github.com/ciceroyang/dsh-trajectory)** — セッションログを HTML 文書にレンダリング。
- **[plugin-session-export](https://github.com/whyihaveyou/dsh-suite/tree/main/packages/plugins/plugin-session-export)** — セッションログを Markdown/HTML として書き出し。
- **[dsh-translate](https://github.com/PerryLink/dsh-translate)** — ベンダパラメータ翻訳と JSON 修復。

## 通知とチャネル

- **[dsh-feishu](https://github.com/PGZXB/dsh-feishu)** — DSH 向け Feishu（Lark）UI。
- **[dsh-feishu-bot](https://github.com/dsh-external/dsh-feishu-bot)** — Feishu ボット。
- **[dsh-telegram-channel](https://github.com/hi-wenw/dsh-telegram-channel)** — Telegram モバイルリモート。
- **[dsh-wecom-bot](https://github.com/dsh-external/dsh-wecom-bot)** — WeCom ボット。
- **[dsh-weixin-bot](https://github.com/dsh-external/dsh-weixin-bot)** — WeChat ボット。
- **[dsh-im-hub](https://github.com/ThreeBody6666/dsh-im-hub)** — マルチプラットフォーム IM ゲートウェイ。
- **[dsh-voice-chat](https://github.com/dsh-external/dsh-voice-chat)** — 音声チャット。
- **[dsh-notify-windows](https://github.com/SeverusZh/dsh-notify-windows)** — Windows 通知。
- **[dsh-notification-sounds](https://github.com/qq33357486/dsh-notification-sounds)** — クロスプラットフォームブラウザ音声アラート。

## 参考にできる設計パターン

上記のプロジェクトを検討した結果、自らの harness／agent プロジェクトで採用する価値のあるパターンは以下の通りです:

1. **デュアルモデル plan/execute** — `dsh-plan-execute` と `dsh-plans` は「思考」と「行動」を異なるモデルに分割し、推論品質と実行コストのバランスをとります。
2. **コンテキスト圧縮とレンズ** — `dsh-compressor`、`dsh-scope`、`dsh-context-doctor` は、コンテキスト使用量の可視化とオンデマンド圧縮が長いセッションの核心的課題であることを示しています。
3. **階層的かつ承認ゲート付きメモリ** — `dsh-memento` と `dsh-memory-gate` は、境界付き／階層的／承認制の設計で無制限なメモリがコンテキストを汚染するのを防ぎます。
4. **コストガバナンス** — `dsh-budget`、`dsh-web-billing`、`dsh-change-budget` はトークン計測からターンごとの予算までの閉ループを提供します。
5. **セキュリティガードレール三点セット** — インストール前汚染スキャン（`dsh-poison-guard`）、実行前ガードレール（`dsh-safeguard`）、プロンプトインジェクション検知（`dsh-defend`）が再利用可能な保護層を構成します。
6. **サブエージェントと worktree 隔離** — `dsh-background-agents` と `worktree-mgr` は Git worktree で並列タスクを隔離する、並行性安全の実践パターンです。
7. **プロバイダフォールバックとルーティング** — `dsh-llm-fallbacks`、`dsh-delegate-router`、`dsh-smart-route` はマルチモデルスケジューリングを設定可能なルーティングとして抽象化します。
8. **オブザーバビリティ** — `dsh-replay`（タイムトラベル）、`dsh-trajectory-debug`（軌跡再生）、`dsh-event-auditor`（イベント監査）はエージェントをデバッグするための重要なツール形態です。

## 関連リソース

- [0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness) — 原文の完全な英語リスト（お遊び目的のプラグインがより多く含まれます）。
- [dsh-external/hub](https://github.com/dsh-external) — 公式カタログ。
- DSH プラグイン仕様: `dsh.bundle.patch` を宣言したパッケージのみが有効なレイヤーとなります。
