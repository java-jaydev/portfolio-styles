# 박건우 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(시안들의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 09-park-geonwoo.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 박건우, 남, 전주대학교 태권도학과 4학년, 선수 트레이너와 지도자 지망. Fill plausible content: 소개, 한 일 3~4개(예: 초등부 겨루기 팀 12주 훈련 프로그램, 발차기 속도 측정 기록 프로젝트, 시범단 공연 구성, 생활체육 지도 실습. 인원, 주차, 기록 변화 같은 숫자 포함. 실제 대회 입상 사칭 금지, "교내 대회", "도 대회 출전"처럼 일반화), 자격과 기술(단증, 생활스포츠지도사 준비, 테이핑, 영상 분석), 연혁, 연락처(example.com 메일).

Design direction (chosen to differ from 11 sibling pages): "발차기 궤적". White dobok ground (#FFFFFF), black belt black (#000000), with flat red (#E0282E) and blue (#1B4BA0) as in sparring gear. Heavy poster energy. Signature moment: the hero has a jointed stick figure in fighting stance drawn on canvas with thick strokes. The kicking foot reaches toward the pointer using simple two-bone inverse kinematics (hip, knee, foot), the body leans and the guard arm counterbalances, and the foot leaves a fading motion trail whose color flips between red and blue by side. A small readout shows kick height in cm and angle. Click or tap snaps a fast kick with a hit flash at the target. When idle the figure bounces lightly in stance and throws an occasional kick. Works are presented like a match scoreboard or training log rows with big numerals, not cards. Typeface: a heavy Korean display face (for example Black Han Sans) for big type and a plain sans for body, chosen deliberately.

Shared rules for all pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko". Fonts from Google Fonts only, with system fallbacks.
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback (drag or tap) and an idle auto-motion so the page is alive without a pointer; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px with no horizontal scroll.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, one accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-09 --window-size=1440,900 --virtual-time-budget=12000 --screenshot=<scratch>/shot-09.png file://<repo>/09-park-geonwoo.html
Headless Chrome will not go narrower than about 500px, so for mobile write a small wrapper HTML in the scratchpad that embeds the page in a 390x844 iframe and screenshot that to shot-09-m.png. Headless can freeze CSS animations, so make sure nothing important stays invisible if an entrance animation never runs. Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero, a figure whose limbs look broken), and grep the file for the em dash and en dash characters (must be 0). Report in 3 lines: the signature interaction, palette and fonts, anything not verified.
```
