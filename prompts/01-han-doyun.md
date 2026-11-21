# 한도윤 시안에 쓴 프롬프트

- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(여섯 시안의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 01-han-doyun.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 한도윤, 남, 전주대학교 컴퓨터공학과 4학년, 백엔드 개발자 지망. Fill plausible content: 소개, 프로젝트 3~4개(예: 전주 시내버스 도착 알림 API, 캡스톤 LLM 챗봇 서버, 동아리 출석 시스템 등 숫자 포함), 기술, 경험/수상 연혁, 연락처(example.com 메일, 가짜 GitHub 아이디).

Design direction (follow it, it was chosen to differ from 5 sibling pages): "시스템 회로도". Saturated cobalt blue ground (#1437C8 계열) with white line work and one signal yellow. Signature moment: the hero is a live architecture diagram drawn in SVG/canvas (client, gateway, queue, workers, DB); small request packets travel along the wires, and the mouse acts as the request source: packets spawn from the cursor and route into the nearest node, nodes pulse when hit. Rest of the page stays quiet and disciplined. Typeface: pick deliberately (Korean-capable, via Google Fonts or jsDelivr, with system fallback). Not a dark terminal look, no acid green.

Shared rules for all six pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko".
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: take a headless screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-01 --window-size=1440,900 --virtual-time-budget=4000 --screenshot=<scratch>/shot-01.png file://<repo>/01-han-doyun.html
(also one at --window-size=390,844 to shot-01-m.png), Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for — and – (must be 0). Report in 3 lines: what the signature interaction is, palette and fonts, anything not verified.
```
