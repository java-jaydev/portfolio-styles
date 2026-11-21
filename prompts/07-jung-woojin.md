# 정우진 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(시안들의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 07-jung-woojin.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 정우진, 남, 전주대학교 건축학과 5학년, 건축 설계 지망. Fill plausible content: 소개, 설계 프로젝트 3~4개(예: 전주천 옆 작은 도서관, 구도심 빈집을 고친 공유 주방, 한옥마을 골목 쉼터, 졸업 설계. 대지 면적, 층수, 모형 축척, 작업 기간 같은 숫자 포함), 다루는 도구(Rhino, Revit, 모형 제작 등), 연혁과 수상(교내, 지역 공모전처럼 일반화), 연락처(example.com 메일).

Design direction (chosen to differ from 11 sibling pages): "해 그림자 모형". Tracing-paper white ground (#F4F5F1, slightly cool), graphite line work (#2B2D2F), one highlighter orange (#FF6A13) used only for the sun and the section cut, pale blue-grey for shadows. Signature moment: the hero is an axonometric line drawing of a small building model on a site plate (SVG or canvas). The mouse is the sun: its position sets sun azimuth and altitude, and the cast shadows of every volume and tree stretch and swing in real time across the site, with a small readout of time of day and sun altitude. On load the model draws itself once, line by line. Elsewhere, project entries read like drawing sheets with a title block (scale, date, sheet number where the sequence is real), not rounded cards. Typeface: a deliberate Korean sans with a drafting feel plus tabular figures; no monospace labels.

Shared rules for all pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko". Fonts from Google Fonts only, with system fallbacks.
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback (drag or tap) and an idle auto-motion so the page is alive without a pointer; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px with no horizontal scroll.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, one accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-07 --window-size=1440,900 --virtual-time-budget=12000 --screenshot=<scratch>/shot-07.png file://<repo>/07-jung-woojin.html
Headless Chrome will not go narrower than about 500px, so for mobile write a small wrapper HTML in the scratchpad that embeds the page in a 390x844 iframe and screenshot that to shot-07-m.png. Headless can freeze CSS animations, so make sure nothing important stays invisible if an entrance animation never runs. Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for the em dash and en dash characters (must be 0). Report in 3 lines: the signature interaction, palette and fonts, anything not verified.
```
