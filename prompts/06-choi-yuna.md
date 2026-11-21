# 최유나 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(여섯 시안의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 06-choi-yuna.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 최유나, 여, 전주대학교 인공지능학과 4학년, 데이터 사이언티스트/ML 엔지니어 지망. Fill plausible content: 소개, 프로젝트 3~4개(예: 전주 한옥마을 유동인구 예측, 강의평 감성 분석, 캡스톤 RAG 학사 안내 챗봇, 캐글 스타일 대회 참가. 데이터 크기, 정확도, 순위 같은 숫자 포함하되 과장 없이), 기술(Python, PyTorch, SQL 등), 연혁/수상, 연락처(example.com 메일, 가짜 GitHub 아이디).

Design direction (follow it, it was chosen to differ from 5 sibling pages): "임베딩 공간". Light ground: 회백 #EDEFF2, 가지색 잉크 #2A1E3F, 오렌지 #FF7A1A, 하늘 #5BC0EB, used flat. Signature moment: the hero is a full-bleed canvas scatter of a few thousand small points (an embedding space) that drift gently; the pointer acts like a query vector: nearby points are attracted and light up as "nearest neighbors" with thin lines to the cursor and a small readout (k, distance). Hovering or focusing a project re-clusters the points into a shape that fits that project (a map outline blob, a bar chart, speech bubble, podium), then releases. Charts elsewhere are small, real-looking SVG plots with axis labels, not decorative. Typeface: IBM Plex Sans KR or another deliberate Korean sans; numbers set with tabular figures. Layout: left-aligned, generous margins, project entries as rows of a results table with a plot per row, not cards.

Shared rules for all six pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko".
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px. Keep canvas performant (cap devicePixelRatio at 2, reduce point count on small screens).
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: take a headless screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-06 --window-size=1440,900 --virtual-time-budget=4000 --screenshot=<scratch>/shot-06.png file://<repo>/06-choi-yuna.html
(also one at --window-size=390,844 to shot-06-m.png), Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for — and – (must be 0). Report in 3 lines: what the signature interaction is, palette and fonts, anything not verified.
```
