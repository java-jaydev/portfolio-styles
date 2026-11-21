# 문지우 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(시안들의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 12-moon-jiwoo.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 문지우, 여, 전주대학교 패션산업학과 3학년, 패션 디자이너와 패턴사 지망. Fill plausible content: 소개, 작업 3~4개(예: 한복 깃을 응용한 재킷 3벌, 버려진 현수막으로 만든 가방 20개, 학과 패션쇼 2벌 출품, 니트 스와치 연구 30장. 벌 수, 원단 길이, 제작 시간 포함), 할 줄 아는 것(패턴 제도, 봉제, CLO 3D, 일러스트 도식화), 연혁, 연락처(example.com 메일, 가짜 인스타 아이디).

Design direction (chosen to differ from 11 sibling pages, one of which already uses a flat patchwork cloth, so this must be real hanging fabric): "걸린 원단". Studio grey ground (#D9D9D6), real black, olive (#5B6236) and butter (#F2E3B3), flat color. Signature moment: the hero has three fabric swatches hanging from pins on a rail, simulated as cloth with a hand-written verlet particle grid (points, distance constraints, gravity, a little air). The swatches drape and sway; the pointer pushes the cloth like a hand passing through, and you can grab a corner and pull it, then let it fall back. Each swatch is a different weight (light, medium, heavy) so they move differently, and each is labeled with fabric name and weight in g/m2. Render on canvas with filled quads and subtle fold shading by angle. On load the swatches drop and settle once. Works are laid out like a lookbook spread with garment flats drawn as simple line SVG and a spec sheet (원단, 치수, 제작 시간), not cards. Typeface: an elegant Korean serif or a refined thin sans for titles with generous spacing, plus a plain sans for specs, chosen deliberately.

Shared rules for all pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko". Fonts from Google Fonts only, with system fallbacks.
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback (drag or tap, without blocking page scroll outside the cloth) and an idle auto-motion so the page is alive without a pointer; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px with no horizontal scroll. Keep the simulation light (cap grid size and devicePixelRatio at 2, fewer points on small screens).
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, one accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people, no real brand names, no real contact details.

Verify before reporting: screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-12 --window-size=1440,900 --virtual-time-budget=12000 --screenshot=<scratch>/shot-12.png file://<repo>/12-moon-jiwoo.html
Headless Chrome will not go narrower than about 500px, so for mobile write a small wrapper HTML in the scratchpad that embeds the page in a 390x844 iframe and screenshot that to shot-12-m.png. Headless can freeze CSS animations, so make sure nothing important stays invisible if an entrance animation never runs. Read the images, fix what looks broken (cloth exploding or missing, overlap, overflow, unreadable contrast, empty hero), and grep the file for the em dash and en dash characters (must be 0). Report in 3 lines: the signature interaction, palette and fonts, anything not verified.
```
