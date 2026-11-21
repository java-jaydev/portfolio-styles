# 김나은 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(시안들의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 10-kim-naeun.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 김나은, 여, 전주대학교 간호학과 4학년, 병동 간호사 지망. Fill plausible content: 소개, 경험 3~4개(예: 내과 병동 임상 실습 1,000시간 중 기억에 남는 일, 낙상 예방 안내문을 쉬운 말로 다시 만든 프로젝트, 시뮬레이션 실습 팀 리더, 지역 어르신 건강 교실 봉사. 시간, 인원, 횟수 포함. 실제 병원 이름과 환자 정보는 쓰지 않고 일반화), 할 줄 아는 것(활력징후 측정, 투약 계산, 기록, BLS 교육 이수 등), 연혁, 연락처(example.com 메일).

Design direction (chosen to differ from 11 sibling pages): "기록지의 맥박". Not a dark hospital monitor. Pale mint chart paper (#EAF5F0) with a fine printed grid, deep green ink (#0F4C3A), one coral for the pulse line (#FF5D5D), white for note cards. Signature moment: a single ECG trace runs across the full width of the hero on the chart grid, drawn continuously left to right like a paper recorder. The trace responds to the person: the closer the pointer is to the name, and the faster it moves, the higher the heart rate shown beside it (roughly 58 to 120 bpm), with the waveform spacing changing to match; when the pointer rests it settles back to a calm rate. The pen head is visible and the paper scrolls. Tap on touch gives a few fast beats that settle. Elsewhere the experiences read like nursing notes on a chart (time column, short factual entries, a handwritten-feeling signature line), not cards. Typeface: a calm, highly legible Korean sans for records plus one handwriting-flavored Korean face used sparingly for signatures and margin notes.

Shared rules for all pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko". Fonts from Google Fonts only, with system fallbacks.
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback (drag or tap) and an idle auto-motion so the page is alive without a pointer; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px with no horizontal scroll.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, one accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-10 --window-size=1440,900 --virtual-time-budget=12000 --screenshot=<scratch>/shot-10.png file://<repo>/10-kim-naeun.html
Headless Chrome will not go narrower than about 500px, so for mobile write a small wrapper HTML in the scratchpad that embeds the page in a 390x844 iframe and screenshot that to shot-10-m.png. Headless can freeze CSS animations, so make sure nothing important stays invisible if an entrance animation never runs. Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for the em dash and en dash characters (must be 0). Report in 3 lines: the signature interaction, palette and fonts, anything not verified.
```
