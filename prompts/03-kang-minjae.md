# 강민재 시안에 쓴 프롬프트

- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(여섯 시안의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 03-kang-minjae.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 강민재, 남, 전주대학교 영화방송학과 4학년, 촬영감독/연출 지망. Fill plausible content: 소개, 작품 3~4편(단편영화, 다큐, 뮤직비디오 등. 제목, 러닝타임, 역할, 가상의 영화제 상영 이력. 전주가 영화 도시라는 맥락은 살리되 실제 영화제 수상을 사칭하지 말고 "교내 영화제", "지역 단편 상영회"처럼 일반화), 장비/기술, 연혁, 연락처(example.com 메일).

Design direction (follow it, it was chosen to differ from 5 sibling pages): "랙 포커스 시네마". True black is justified here (projection room), with tungsten amber #E8A33D, a muted film teal, and white. Letterboxed 2.39:1 hero. Signature moment: the mouse is the focus puller. Layers of the page (title, frame stills drawn with CSS/SVG gradients and shapes, captions) sit at different depths; whatever is near the cursor snaps sharp and the rest falls softly out of focus (CSS blur driven by pointer distance), with slight parallax and a thin viewfinder reticle following the cursor showing fake lens data (35mm, T2.0, focus distance changing with position). Works are presented as a horizontal film strip / shot list rather than cards. Typeface: a Korean serif for titles plus a condensed or neutral sans for credits, chosen deliberately. Keep text readable: never blur body text the user is trying to read (text within reach of the cursor or in keyboard focus is sharp; on touch and reduced-motion everything is sharp).

Shared rules for all six pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko".
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: take a headless screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-03 --window-size=1440,900 --virtual-time-budget=4000 --screenshot=<scratch>/shot-03.png file://<repo>/03-kang-minjae.html
(also one at --window-size=390,844 to shot-03-m.png), Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero, everything blurred when there is no pointer), and grep the file for — and – (must be 0). Report in 3 lines: what the signature interaction is, palette and fonts, anything not verified.
```
