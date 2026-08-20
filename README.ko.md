# awesome-deepseek-harness

> DeepSeek Harness(DSH) 생태계 큐레이션 목록: 플러그인, 도구 및 인프라.
> 출처: [0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness), [omdsh-dev](https://github.com/omdsh-dev)(이전 `dsh-external`, 커뮤니티 플러그인 허브) 및 공개 `dsh-plugin` GitHub 토픽.
> 본 문서는 한국어 큐레이션 판으로, 중복되거나 장난감 성격의 플러그인을 걸러내고 배울 가치가 있는 프로젝트만 수록했습니다. 모든 항목은 링크 유효성을 검증했습니다.

## 목차

- [설치](#설치)
- [코어 및 번들](#코어-및-번들)
- [에이전트 및 오케스트레이션](#에이전트-및-오케스트레이션)
- [컨텍스트 및 검색](#컨텍스트-및-검색)
- [메모리 및 지식](#메모리-및-지식)
- [입력 및 편집](#입력-및-편집)
- [UI, 테마 및 상호작용](#ui-테마-및-상호작용)
- [대시보드 및 세션 UX](#대시보드-및-세션-ux)
- [IDE 및 데스크톱 클라이언트](#ide-및-데스크톱-클라이언트)
- [브라우저 및 원격](#브라우저-및-원격)
- [모델 및 추론](#모델-및-추론)
- [Git 및 엔지니어링](#git-및-엔지니어링)
- [보안 및 거버넌스](#보안-및-거버넌스)
- [출력 및 산출물](#출력-및-산출물)
- [알림 및 채널](#알림-및-채널)
- [빌려올 만한 설계 패턴](#빌려올-만한-설계-패턴)
- [관련 자료](#관련-자료)

## 설치

공식 런타임(Node.js):

```bash
npx @deepseek-ai/dsh web
```

외부 프로필 번들 설치(pnpm):

```bash
dsh plugin --profile web add "github:owner/repo#ref"
```

`dsh plugin`은 pnpm로 전달되며 npm, Git/GitHub, 로컬 경로, `file:` 및 `link:` 사양을 지원합니다. `dsh.bundle.patch`를 선언한 패키지만 활성 레이어가 됩니다. 관리 패널: 설정 → 플러그인.

## 코어 및 번들

- **[dsh-deepresearch](https://github.com/dsh-external/dsh-deepresearch)** — DeepResearch 플러그인(cordis 아키텍처).
- **[dsh-plan-execute](https://github.com/dsh-external/dsh-plan-execute)** — 듀얼 모델 plan/execute 라우팅: 플래너 모델이 사고하고, 실행 모델이 행동합니다.
- **[dsh-toolkit](https://github.com/dsh-external/dsh-toolkit)** — 의존성 없는 도구 모음(계산기/CSV/diff/인코딩/JSON/markdown/정규식/시간).
- **[dsh-101](https://github.com/dsh-external/dsh-101)** — DSH 문서 읽기 모드.
- **[dsh-equip-engine](https://github.com/wuykjl/dsh-equip-engine)** — 작업 주도형 플러그인 장착 엔진: 이중 검색, 조합 채점, 충돌 감지.
- **[dsh-claude-move](https://github.com/PerryLink/dsh-claude-move)** — 마이그레이션 마법사: Claude Code, Codex, OpenCode, Hermes 세션을 DSH로 가져옵니다.
- **[dsh_workflow](https://github.com/omdsh-dev/dsh_workflow)** — UltraCode 스타일 워크플로 계층: 일회성 다중 에이전트 스케줄링을 생성/저장/거버넌스/관찰/재개 가능한 워크플로로 승격.

## 에이전트 및 오케스트레이션

- **[dsh-agent-arena](https://github.com/LeemanCheung/dsh-agent-arena)** — 격리된 Git worktree에서 코딩 에이전트들을 비교합니다.
- **[coding-coach](https://github.com/xiehuan123/coding-coach)** — 코딩 코치: 비개발자를 위한 35개 스킬 번들 + 에이전트 프리셋.
- **[dsh-plans](https://github.com/Optim-Agent/dsh-plans)** — 계획 우선 에이전트 프리셋.
- **[dsh-agent-team-gui](https://github.com/toolclub/dsh-agent-team-gui)** — 설정에서 영속적 멀티 모델 팀을 관리합니다.
- **[Knotline](https://github.com/MrMaii/knotline)** — 영속적 에이전트 워크플로를 구성하기 위한 시각적 DSH 프로젝트 맵.
- **[dsh-self-evolving](https://github.com/timwhitez/dsh-self-evolving)** — 증거 우선, 크래시 복구 가능한 자가 진화 엔진.
- **[dsh-ha-orchestrator](https://github.com/Saktawdi/dsh-ha-orchestrator)** — 모델 고가용성 장애 조치 + 하위 에이전트 오케스트레이션.
- **[dsh-background-agents](https://github.com/PerryLink/dsh-background-agents)** — 공식 하위 에이전트 심을 기반으로 한 영속 백그라운드 자식 에이전트.

## 컨텍스트 및 검색

- **[dsh-github-intelligence](https://github.com/zoahdev/dsh-github-intelligence)** — 16개 생태계에 걸친 읽기 전용 개발자 인텔리전스 도구.
- **[dsh-deepread](https://github.com/xiehuan123/dsh-deepread)** — 5가지 모드를 갖춘 심층 읽기 어시스턴트 DeepRead.
- **[dsh-context](https://github.com/bowenliang123/dsh-context)** — 컨텍스트 인사이트 패널.
- **[dsh-scope](https://github.com/helloxkk/dsh-scope)** — 컨텍스트 렌즈: 세션별 KV 캐시 적중률.
- **[dsh-compressor](https://github.com/lifeodyssey/dsh-compressor)** — Headroom의 경량 포트: 도구 출력을 압축합니다.
- **[context-vista](https://github.com/GooodWei/context-vista)** — 컨텍스트 토큰 사용량을 보여주는 우측 플로팅 패널.
- **[dsh-context-doctor](https://github.com/Zhenyu98/dsh-context-doctor)** — 모든 요청이 실제로 무엇을 담는지 확인합니다.
- **[dsh-mcp-lens](https://github.com/labmimors/dsh-mcp-lens)** — 점진적 노출(progressive-disclosure) MCP 게이트웨이.
- **[dsh-web-search-exa](https://github.com/TonyDua/dsh-web-search-exa)** — 제로 구성 Exa 웹 검색 제공자.
- **[dsh-web-search-pro](https://github.com/anweat/dsh-web-search-pro)** — DSH용 영속 강화 웹 검색.
- **[dsh-session-search](https://github.com/dsh-external/dsh-session-search)** — 인덱스 없는 세션 간 읽기 전용 검색.
- **[dsh-context-pruner](https://github.com/JohnXu22786/context-pruner)** — 세션 컨텍스트 트라이지: 휴리스틱 규칙으로 오래된/중복/실패/과대 블록 정리, 모델 의존성 없음, 감사 보고서 제공.
- **[cross-harness-cite](https://github.com/dsh-external/cross-harness-cite)** — 서로 다른 harness 간 과거 대화를 인용합니다.

## 메모리 및 지식

- **[dsh-hme](https://github.com/weopenfire-git/hme-plugin)** — 세션 간 장기 메모리.
- **[dsh-mnemon](https://github.com/omdsh-dev/dsh-mnemon)** — 3계층 메모리 컨트롤 플레인: 영속 런타임 컨텍스트 + 검색 가능한 프로젝트 문서 + 플러그형 장기 메모리와 스마트 라우팅.
- **[dsh-memory-vault](https://github.com/flymysql/dsh-memory)** — 세션 간 메모리 볼트.
- **[dsh-memory-evolve](https://github.com/dsh-external/dsh-memory-evolve)** — 세션 간 장기 메모리 + 백그라운드 자가 진화.
- **[dsh-memento](https://github.com/PerryLink/dsh-memento)** — 유계(bounded), 계층적, 승인 기반 메모리.
- **[dsh-engramory](https://github.com/tinqiao-oss/engramory/tree/master/adapters/dsh)** — 파일 기반 큐레이션 메모리.
- **[dsh-memory-porter](https://github.com/Shiye-10Pages/dsh-memory-porter)** — 벤더 간 메모리 마이그레이션.
- **[dsh-library](https://github.com/PerryLink/dsh-library)** — 로컬 우선 문서 지식 베이스.
- **[kb-rag](https://github.com/Breeze136/kb-rag)** — 로컬 문헌 지식 베이스 RAG.
- **[dsh-ragflow](https://github.com/staff-os/dsh-ragflow)** — RAGFlow 지식 베이스 검색 플러그인.
- **[docs-retriever](https://github.com/JohnXu22786/docs-retriever)** — doctrove: 버전 관리되는 라이브러리 문서 검색.
- **[snippet-expander](https://github.com/JohnXu22786/snippet-expander)** — Steno: 인라인 `#태그` 약어 전개.
- **[deepddw](https://github.com/ccch713/deepddw)** — 메모리 + 지식 베이스 + 문서 검색을 한 곳에.

## 입력 및 편집

- **[dsh-voice-input-plugin](https://github.com/Zhangbo-cn/dsh-voice-input-plugin)** — Web UI 작성기용 마이크 입력.
- **[dsh-message-edit](https://github.com/dsh-external/dsh-message-edit)** — 분기 기반 메시지 편집.
- **[dsh-prompt-studio](https://github.com/dsh-external/dsh-prompt-studio)** — 시스템 프롬프트 구간을 실시간 미리보기와 함께 편집.
- **[dsh-paste-input](https://github.com/dsh-external/dsh-paste-input)** — Ctrl+V로 파일 붙여넣기 / 드래그 앤 드롭.
- **[dsh-voice](https://github.com/motongv/dsh-voice)** — 작성기용 음성 입력 및 읽어주기.
- **[dsh-drag-and-drop](https://github.com/dsh-external/dsh-drag-and-drop)** — 크로스 플랫폼 드래그 앤 드롭.
- **[dsh-chat-import](https://github.com/Nwflower/dsh-chat-import)** — 13종 코딩 에이전트에서 대화 기록 가져오기.
- **[dsh-file-claim](https://github.com/Nwflower/dsh-file-claim)** — 병렬 세션을 위한 파일 점유/해제 보호.
- **[dsh-plugin-quote-reply](https://github.com/yangYzc/dsh-plugin-quote-reply)** — 텍스트를 선택해 작성기에 인용으로 넣기.
- **[dsh-pathlink](https://github.com/penguin-oo/dsh-pathlink)** — 채팅에서 파일 경로와 링크를 Ctrl+클릭.
- **[dsh-prompt-optimize](https://github.com/peterliucius/dsh-prompt-optimize)** — 보조 LLM으로 작성기 초안 재작성.
- **[dsh-composer-history](https://github.com/PerryLink/dsh-composer-history)** — 웹 작성기를 위한 터미널 스타일 입력 기록.
- **[dsh-at-file](https://github.com/omdsh-dev/dsh-at-file)** — Codex 스타일 `@file` 언급: 작성기에서 워크스페이스 파일을 검색하고 경로를 첨부.
- **[dsh-annotation](https://github.com/omdsh-dev/dsh-annotation)** — 텍스트 선택 주석: 주석 블록이 메시지와 함께 전송되고 답변이 하나씩 대조(코어 변경 없음).

## UI, 테마 및 상호작용

- **[dsh-skin-studio](https://github.com/LeemanCheung/dsh-skin-studio)** — 로컬 의미 토큰 테마 편집기.
- **[deepseek-harness-zh-tw](https://github.com/chiyulogg-commits/deepseek-harness-zh-tw)** — 번체 중국어 로케일 판.
- **[dsh-spotlight](https://github.com/0xsline/dsh-spotlight)** — 키보드 우선 명령 팔레트.
- **[arcana](https://github.com/GooodWei/arcana)** — 슬래시 명령용 플로팅 명령 데크.
- **[dsh-i18n](https://github.com/Semidia/dsh-i18n)** — 도구 결과의 중국어 현지화.
- **[dsh-plugin-workshop](https://github.com/yyyyukari/dsh-plugin-workshop)** — Steam Workshop 스타일 플러그인 브라우저.
- **[dsh-markdown-preview](https://github.com/GitHubJiKe/dsh-markdown-preview)** — 생성된 파일을 채팅에서 미리보기.
- **[dsh-diff-viewer](https://github.com/dsh-external/dsh-diff-viewer)** — PiUI 스타일 Web diff 뷰어.
- **[dsh-split-panes](https://github.com/dsh-external/dsh-split-panes)** — 분할 패널.
- **[dsh-plugin-help](https://github.com/Semidia/dsh-plugin-help)** — 설치된 플러그인 README 요약 패널.
- **[dsh-mcp-panel](https://github.com/PerryLink/dsh-mcp-panel)** — MCP 관리 콘솔.
- **[DSH-better-sidebar](https://github.com/omdsh-dev/DSH-better-sidebar)** — 확장 가능한 사이드바 베이스(커뮤니티 최다 스타): 파일 렌더/편집, 터미널, Git, 하위 에이전트 통합 워크스페이스, 서드파티 페이지 등록 지원.
- **[dsh-genui](https://github.com/omdsh-dev/dsh-genui)** — 답변 내 인라인 대화형 UI 컴포넌트: 레이아웃/차트/폼/퀴즈/Mermaid/3D 씬 + 모델로 돌아가는 액션 루프.

## 대시보드 및 세션 UX

- **[dsh-replay](https://github.com/zoahdev/dsh-replay)** — 타임 트래블 디버거.
- **[dsh-token-usage](https://github.com/jiamuAi/dsh-token-usage)** — Codex 스타일 토큰 사용량 패널.
- **[dsh-usage-panel](https://github.com/AlfredChaos/dsh-usage-panel)** — 설정 페이지 형태의 토큰 사용량 통계.
- **[dsh-web-billing](https://github.com/bpc-oss/dsh-web-billing)** — 위안화/달러 토큰 과금.
- **[dsh-budget](https://github.com/PerryLink/dsh-budget)** — DeepSeek Harness 비용 거버넌스.
- **[dsh-fork-graph](https://github.com/chouyong/dsh-fork-graph)** — Git 스타일 대화 분기 그래프.
- **[dsh-branch-review](https://github.com/chouyong/dsh-branch-review)** — 브랜치에 대한 인간 결정을 추적.
- **[dsh-fork-diff](https://github.com/chouyong/dsh-fork-diff)** — 부모 및 형제 브랜치 비교.
- **[dsh-auto-continue](https://github.com/HsiangNianian/dsh-auto-continue)** — 중단된 요청을 자동으로 재개.
- **[dsh-trajectory-debug](https://github.com/devmom/dsh-trajectory-debug)** — 궤적 워터폴 및 재생.
- **[dsh-session-manager](https://github.com/Semidia/dsh-session-manager)** — 세션에 대한 우클릭 컨텍스트 메뉴.
- **[dsh-session-titler](https://github.com/JohnXu22786/session-titler)** — 2단계 세션 명명: 활성 시 제로 코스트 키워드 즉시 명명, 유휴 시 최저가 모델로 다듬기 + 한 줄 요약.
- **[dsh-session-handoff](https://github.com/WeiYe6/dsh-session-handoff)** — 긴 세션을 깨끗한 새 세션으로 인계.
- **[dsh-event-auditor](https://github.com/qing3a/dsh-event-auditor)** — 이벤트 흐름 감사 패널.

## IDE 및 데스크톱 클라이언트

- **[dsh-cc-tui](https://github.com/dsh-external/dsh-cc-tui)** — Claude Code 스타일 전체 화면 TUI.
- **[deepseek-harness-tui](https://github.com/openma-ai/deepseek-harness-tui)** — Rust/ratatui 터미널 클라이언트.
- **[deepseek-harness-desktop](https://github.com/fendouai/deepseek-harness-desktop)** — Tauri 2 데스크톱 배포판.
- **[dsh-vscode](https://github.com/Lixxx1/dsh-vscode)** — VS Code 우측 사이드바 클라이언트.
- **[dsh4vscode](https://github.com/DoggyHU/dsh4vscode)** — DSH 기반 VS Code 채팅 창.
- **[dsh-plugin-open-editor](https://github.com/Civitasv/dsh-plugin-open-editor)** — 로컬 편집기에서 작업 영역 열기.
- **[dsh-launcher](https://github.com/iceleaf916/dsh-launcher)** — macOS 메뉴 막대 실행기.
- **[browser-automation](https://github.com/JohnXu22786/browser-automation)** — Web Bridge: 브라우저 자동화 MCP.
- **[computer-control](https://github.com/JohnXu22786/computer-control)** — dsh용 데스크톱 제어.

## 브라우저 및 원격

- **[dsh-browser-panel](https://github.com/dsh-external/dsh-browser-panel)** — WebUI에 내장된 헤드리스 브라우저(headed).
- **[dsh-builtin-browser](https://github.com/wqty123/dsh-browser)** — DSH용 공유 실제 브라우저.
- **[dsh-remote](https://github.com/flymysql/dsh-remote)** — 다중 머신 원격 작업 영역.
- **[dsh-ssh](https://github.com/jmcc-guo/dsh-ssh)** — AI 관리형 SSH 연결.
- **[dsh-lan-access](https://github.com/Leon0555/dsh-lan-access)** — Web GUI LAN 접근.
- **[dsh-computer-use](https://github.com/ZRui-C/dsh-computer-use)** — 텍스트 우선 컴퓨터 사용.
- **[dsh-adb](https://github.com/SamXiaBing/dsh-adb)** — ADB 기기 및 벤치 작업.
- **[dsh-vision](https://github.com/zoahdev/dsh-vision)** — vision_analyze 도구.
- **[dsh-browser-use](https://github.com/zoahdev/dsh-browser-use)** — Browser Use 클라우드 브리지.

## 모델 및 추론

- **[dsh-image-gen](https://github.com/shanliuling/dsh-image-gen)** — 네이티브 이미지 생성.
- **[dsh-codex-oauth](https://github.com/WNJXYK/dsh-codex-oauth)** — ChatGPT/Codex 구독 통합.
- **[dsh-vision-router](https://github.com/ysr666/dsh-vision-router)** — 텍스트 전용 에이전트를 위한 무료 비전.
- **[dsh-advisor](https://github.com/dsh-external/dsh-advisor)** — 두 번째 모델이 매 턴을 검토.
- **[dsh-auxiliary](https://github.com/dsh-plugins/dsh-auxiliary)** — 보조 모델 플러그인: 메인 대화 모델을 건드리지 않고 비전/압축/승인/하위 에이전트/제목 등을 별도 모델로 라우팅.
- **[dsh-vision-toolkit](https://github.com/Anionex/dsh-vision-toolkit)** — 텍스트 전용 모델용 10가지 구조화된 비전 도구: 의도 인식 이미지 Q&A, 긴 스크린샷 OCR, UI 재구성.
- **[dsh-llm-fallbacks](https://github.com/omdsh-dev/dsh-llm-fallbacks)** — 역할 기반 LLM 재시도/폴백.
- **[dsh-acp](https://github.com/dsh-external/dsh-acp)** — 클라이언트 중립적 ACP 어댑터.
- **[dsh-subagent-tools](https://github.com/lynx-gt/dsh-subagent-tools)** — 호출별 모델/제공자 재정의.
- **[dsh-delegate-router](https://github.com/penguin-oo/dsh-delegate-router)** — 자동 Flash/Pro 라우팅.
- **[dsh-smart-route](https://github.com/Semidia/dsh-smart-route)** — 스마트 제공자 라우팅.
- **[dsh-local-ai](https://github.com/PerryLink/dsh-local-ai)** — Ollama 로컬 모델 어댑터.
- **[dsh-llm-ollama](https://github.com/NOirBRight/dsh-llm-ollama)** — Ollama Cloud 네이티브 채팅 어댑터.
- **[dsh-github](https://github.com/PerryLink/dsh-github)** — 공식급 GitHub CI 통합.
- **[worktree-mgr](https://github.com/JohnXu22786/worktree-mgr)** — 작업 격리형 Git worktree.
- **[spec-driven](https://github.com/JohnXu22786/spec-driven)** — keel: 스펙 기반 개발.
- **[adversarial-review](https://github.com/JohnXu22786/adversarial-review)** — gavel-review: 적대적 코드 리뷰.

## Git 및 엔지니어링

- **[dsh-git-identity](https://github.com/dsh-external/dsh-git-identity)** — Git 커밋 작성자 고정.
- **[dsh-tool-git](https://github.com/lxj808624/dsh-tool-git)** — 구조화된 Git 도구.
- **[deepseek-harness-action](https://github.com/Lixiaoyiao/deepseek-harness-action)** — PR 리뷰/CI용 GitHub Action.
- **[dsh-inspect](https://github.com/dsh-external/dsh-inspect)** — 적대적 점검 → 수정 → 리뷰.
- **[dsh-review-loop](https://github.com/wuxiangru915/dsh-review-loop)** — 증분 diff 리뷰어.
- **[dsh-test-runner](https://github.com/suimi8/dsh-test-runner)** — 구조화된 테스트 실행 도구.
- **[dsh-doublecheck](https://github.com/PerryLink/dsh-doublecheck)** — 엔지니어링 규율 루프.
- **[dsh-checkpoint-rewind](https://github.com/PerryLink/dsh-checkpoint-rewind)** — DSH용 Claude Code `/rewind`.
- **[dsh-lsp-actions](https://github.com/PerryLink/dsh-lsp-actions)** — LSP 액션 서피스.
- **[dsh-git-status](https://github.com/Wongzexu/dsh-git-status)** — Git 브랜치 및 상태 처리.
- **[safety-net](https://github.com/JohnXu22786/safety-net)** — 파괴적 명령 차단 게이트.
- **[secret-guard](https://github.com/JohnXu22786/secret-guard)** — 민감 파일 읽기/쓰기 차단.
- **[arch-doc](https://github.com/duyanta123/arch-doc)** — 코드베이스를 분석하고 문서 생성.

## 보안 및 거버넌스

- **[dsh-poison-guard](https://github.com/zoahdev/dsh-poison-guard)** — 설치 전 공급망 포이즌 스캐너.
- **[dsh-skill-pack-security](https://github.com/PerryLink/dsh-skill-pack-security)** — 보안 감사 스킬 팩 + plugin_vet.
- **[dsh-encrypt](https://github.com/yauntyour/DSH-Encrypt)** — AES-256-GCM 자격 증명 제공자.
- **[dsh-telemetry-redactor](https://github.com/030611/dsh-telemetry-redactor)** — 텔레메트리 내보내기에서 비밀 제거.
- **[dsh-yolo-mode](https://github.com/SeverusZh/dsh-yolo-mode)** — 샌드박스 승격을 위한 LLM 자동 승인.
- **[dsh-auto-review](https://github.com/PerryLink/dsh-auto-review)** — 두 번째 모델 AI 자동 리뷰.
- **[dsh-permission-rules](https://github.com/PerryLink/dsh-permission-rules)** — 선언적 허용/거부/확인 규칙.
- **[dsh-safeguard](https://github.com/ZhijiangTang/dsh-safeguard)** — 실행 전 가드레일.
- **[dsh-mask](https://github.com/PerryLink/dsh-mask)** — PII 마스킹 미들웨어.
- **[dsh-defend](https://github.com/PerryLink/dsh-defend)** — 프롬프트 주입/탈옥(jailbreak) 탐지.
- **[dsh-change-budget](https://github.com/Raphaelutumn/dsh-change-budget)** — 구성 가능한 턴별 예산.
- **[upstream-radar](https://github.com/MicroMilo/upstream-radar)** — 의존성 보안 모니터링.

## 출력 및 산출물

- **[dsh-artifacts](https://github.com/zoahdev/dsh-artifacts)** — Claude Artifacts 스타일 렌더러.
- **[folio](https://github.com/nyantused-cpun/folio)** — 컨설팅 문서 생성 엔진.
- **[dsh-report-studio](https://github.com/ciceroyang/dsh-report-studio)** — 세션을 업무 보고서로 변환.
- **[dsh-trajectory](https://github.com/ciceroyang/dsh-trajectory)** — 세션 로그를 HTML 문서로 렌더링.
- **[plugin-session-export](https://github.com/whyihaveyou/dsh-suite/tree/main/packages/plugins/plugin-session-export)** — 세션 로그를 Markdown/HTML로 내보내기.
- **[dsh-translate](https://github.com/PerryLink/dsh-translate)** — 벤더 파라미터 번역 및 JSON 복구.

## 알림 및 채널

- **[dsh-feishu](https://github.com/PGZXB/dsh-feishu)** — DSH용 Feishu(Lark) UI.
- **[dsh-feishu-bot](https://github.com/dsh-external/dsh-feishu-bot)** — Feishu 봇.
- **[dsh-telegram-channel](https://github.com/hi-wenw/dsh-telegram-channel)** — Telegram 모바일 원격.
- **[dsh-wecom-bot](https://github.com/dsh-external/dsh-wecom-bot)** — WeCom 봇.
- **[dsh-weixin-bot](https://github.com/dsh-external/dsh-weixin-bot)** — WeChat 봇.
- **[dsh-im-hub](https://github.com/ThreeBody6666/dsh-im-hub)** — 다중 플랫폼 IM 게이트웨이.
- **[dsh-voice-chat](https://github.com/dsh-external/dsh-voice-chat)** — 음성 채팅.
- **[dsh-notify-windows](https://github.com/SeverusZh/dsh-notify-windows)** — Windows 알림.
- **[dsh-notification-sounds](https://github.com/qq33357486/dsh-notification-sounds)** — 크로스 플랫폼 브라우저 오디오 알림.

## 빌려올 만한 설계 패턴

위 프로젝트를 검토한 후, 자신의 harness/agent 프로젝트에서 차용할 만한 패턴은 다음과 같습니다:

1. **듀얼 모델 plan/execute** — `dsh-plan-execute`와 `dsh-plans`는 "사고"와 "행동"을 다른 모델로 분리해 추론 품질과 실행 비용을 균형있게 잡습니다.
2. **컨텍스트 압축 및 렌즈** — `dsh-compressor`, `dsh-scope`, `dsh-context-doctor`는 컨텍스트 사용량을 시각화하고 필요할 때 압축하는 것이 긴 세션의 핵심 과제임을 보여줍니다.
3. **계층적 및 승인 기반 메모리** — `dsh-memento`와 `dsh-memory-gate`는 유계/계층적/승인 기반 설계로 무한 메모리가 컨텍스트를 오염시키는 것을 막습니다.
4. **비용 거버넌스** — `dsh-budget`, `dsh-web-billing`, `dsh-change-budget`는 토큰 계량부터 턴별 예산까지 폐쇄 루프를 제공합니다.
5. **보안 가드레일 3종** — 설치 전 포이즌 스캔(`dsh-poison-guard`), 실행 전 가드레일(`dsh-safeguard`), 프롬프트 주입 탐지(`dsh-defend`)가 재사용 가능한 보호 계층을 이룹니다.
6. **하위 에이전트 및 worktree 격리** — `dsh-background-agents`와 `worktree-mgr`은 Git worktree로 병렬 작업을 격리하는 동시성 안전 패턴입니다.
7. **제공자 폴백 및 라우팅** — `dsh-llm-fallbacks`, `dsh-delegate-router`, `dsh-smart-route`는 멀티 모델 스케줄링을 구성 가능한 라우팅으로 추상화합니다.
8. **관측 가능성(observability)** — `dsh-replay`(타임 트래블), `dsh-trajectory-debug`(궤적 재생), `dsh-event-auditor`(이벤트 감사)는 에이전트 디버깅을 위한 핵심 도구 형태입니다.
9. **보조 LLM 심(Auxiliary-LLM seam)** — `dsh-auxiliary`는 메인 모델을 건드리지 않고 비전/압축/승인/제목 등의 저비용 작업을 별도 모델로 라우팅하며, "메인 모델은 사고에 집중"하게 하는 핵심 확장 지점입니다.
10. **텍스트 전용 모델의 비전 보강** — `dsh-vision-toolkit`과 `dsh-vision-router`는 "의도 인식 비전 + 픽셀 수준 OCR/grounding"이 텍스트 모델에 멀티모달 능력을 보완하는 강한 커뮤니티 수요임을 보여줍니다.

## 관련 자료

- [0xsline/awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness) — 원본 전체 영문 목록(장난감 성격 플러그인이 더 많음).
- [omdsh-dev(Oh My DSH)](https://github.com/omdsh-dev) — 커뮤니티 플러그인 허브(이전 `dsh-external`에서 개명, 106개 저장소), [hub.omdsh.dev](https://hub.omdsh.dev)에서 스타 기준으로 탐색 가능.
- DSH 플러그인 사양: `dsh.bundle.patch`를 선언한 패키지만 활성 레이어가 됩니다.
