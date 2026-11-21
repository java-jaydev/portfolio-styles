# 서지훈 시안에 쓴 프롬프트

- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 픽셀 글꼴을 CDN 대신 같은 폴더의 `Galmuri11.woff2` 파일에서 불러오도록 한 줄을 바꿨습니다.
- 이 프롬프트는 앞선 대화(여섯 시안의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 02-seo-jihun.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 서지훈, 남, 전주대학교 게임콘텐츠학과 3학년, 게임 프로그래머 지망. Fill plausible content: 소개, 게임 프로젝트 3~4개(예: 전주 한옥마을 배경 2D 퍼즐 플랫포머, 게임잼 48시간 작품, 모바일 리듬 게임 프로토타입, 다운로드 수나 플레이 시간 같은 숫자 포함), 기술(Unity, C#, 셰이더 등), 연혁/수상, 연락처(example.com 메일, 가짜 itch 아이디).

Design direction (follow it, it was chosen to differ from 5 sibling pages): "픽셀 아케이드". Four-color palette: 진한 남보라 #2B1B4D, 코랄 #FF5A5F, 민트 #7DE2D1, 크림옐로 #FFE66D. Korean pixel typeface (Galmuri11 or similar via jsDelivr, with fallback) for display; a readable Korean sans for body. Signature moment: the hero is a small playable scene on canvas, crisp pixels (image-rendering: pixelated): a pixel character on a tile map walks toward the mouse, collects coins that reveal the nav sections, with a tiny HUD. Hard pixel shadows and stepped animations (steps()) instead of smooth easing. Rest of the page quiet: project entries look like cartridge labels or stage select, not identical rounded cards.

Shared rules for all six pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko".
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details. Do not copy any existing game's characters or art.

Verify before reporting: take a headless screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-02 --window-size=1440,900 --virtual-time-budget=4000 --screenshot=<scratch>/shot-02.png file://<repo>/02-seo-jihun.html
(also one at --window-size=390,844 to shot-02-m.png), Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for — and – (must be 0). Report in 3 lines: what the signature interaction is, palette and fonts, anything not verified.
```
