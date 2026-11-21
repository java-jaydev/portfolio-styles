# 윤서아 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(여섯 시안의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 04-yoon-seoa.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 윤서아, 여, 전주대학교 시각디자인학과 4학년, 브랜드/타이포그래피 디자이너 지망. Fill plausible content: 소개, 프로젝트 3~4개(예: 전주 남부시장 청년몰 가게 리브랜딩, 한글 레터링 포스터 연작, 졸업전시 아이덴티티, 독립출판 진. 기간, 역할, 결과 숫자 포함), 도구/기술, 전시/수상 연혁(가상, 일반화된 이름), 연락처(example.com 메일, 가짜 인스타 아이디).

Design direction (follow it, it was chosen to differ from 5 sibling pages): "키네틱 타이포". Pure white paper, real black, hot magenta #FF2E88 and lemon #FFE94A used as flat blocks, no gradients. Signature moment: the hero is her name set huge, and every glyph reacts to the pointer: use a variable font with real axes for the Latin setting (for example "Anybody" or "Roboto Flex" from Google Fonts, wdth and wght driven per letter by distance to the cursor) and per-glyph transforms (scaleX, skew, weight via font-variation where available) for the Hangul setting 윤서아; letters squeeze and swell like a wave following the mouse, and on load the name assembles once. Layout is an asymmetric poster grid with oversized type crossing column edges, project entries as typographic specimens (big title type, small facts), not cards. Use type treatment itself as the image; no illustrations needed.

Shared rules for all six pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko".
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, single accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: take a headless screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-04 --window-size=1440,900 --virtual-time-budget=4000 --screenshot=<scratch>/shot-04.png file://<repo>/04-yoon-seoa.html
(also one at --window-size=390,844 to shot-04-m.png), Read the images, fix what looks broken (overlap that hides text, horizontal overflow, unreadable contrast, empty hero), and grep the file for — and – (must be 0). Report in 3 lines: what the signature interaction is, palette and fonts, anything not verified.
```
