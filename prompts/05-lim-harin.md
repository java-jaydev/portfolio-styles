# 임하린 시안에 쓴 프롬프트

- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(여섯 시안의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 05-lim-harin.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 임하린, 여, 전주대학교 한식조리학과 3학년, 푸드 스타일리스트/한식 메뉴 개발 지망. Fill plausible content: 소개, 작업 3~4개(예: 계절 반상 차림 연작, 전주비빔밥 재해석 팝업 식당 하루 운영, 전통주 페어링 코스, 학과 요리 대회 출품작. 인원, 접시 수, 준비 기간 같은 숫자 포함), 할 줄 아는 것(조리, 플레이팅, 촬영), 연혁/자격증(한식조리기능사 등), 연락처(example.com 메일).

Design direction (follow it, it was chosen to differ from 5 sibling pages): "조각보 상차림". Do NOT use warm cream with terracotta. Palette: 백자 흰색 #F7F8F5 (cool), 쪽빛 #1F3A5F as the main ink, 치자 노랑 #E3A72F, 오미자 빨강 #B4233A, 쑥색 for small touches. Signature moment: the hero is a 조각보(보자기 patchwork) composed of flat colored patches with visible stitch lines; patches hold dishes drawn as simple top-down SVG (그릇, 반찬, 수저). The cloth responds to the pointer like fabric: patches near the cursor lift and tilt slightly, stitch lines stretch, and one orchestrated load moment unfolds the cloth to set the table. Works are laid out like a 반상 (dishes around a center) or a menu course list, not cards. Typeface: a Korean serif or brush-flavored display (for example Song Myung, Gowun Batang, Nanum Myeongjo from Google Fonts) with a quiet sans for body. Calm, precise, appetizing without photos.

Shared rules for all six pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko".
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: take a headless screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-05 --window-size=1440,900 --virtual-time-budget=4000 --screenshot=<scratch>/shot-05.png file://<repo>/05-lim-harin.html
(also one at --window-size=390,844 to shot-05-m.png), Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for — and – (must be 0). Report in 3 lines: what the signature interaction is, palette and fonts, anything not verified.
```
