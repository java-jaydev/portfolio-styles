# 오태현 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(시안들의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 11-oh-taehyun.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 오태현, 남, 전주대학교 경영학과 4학년, 마케터 지망. Fill plausible content: 소개, 프로젝트 3~4개(예: 전주 남부시장 반찬가게 인스타 운영 8주, 학교 앞 카페 쿠폰 실험(A안과 B안 비교), 동아리 굿즈 펀딩, 교내 마케팅 공모전. 팔로워 변화, 전환율, 매출, 표본 수 같은 숫자를 과장 없이), 할 줄 아는 것(설문 설계, 스프레드시트, 간단한 SQL, 광고 문구), 연혁, 연락처(example.com 메일).

Design direction (chosen to differ from 11 sibling pages): "시장 전단지와 가격표 스티커". Loud supermarket flyer energy, on purpose. Flat flyer yellow ground (#FFD400), sale red (#E4002B), stamp-ink blue (#0033A0), white, black. Signature moment: the hero is covered with price-tag and sale stickers (starbursts, round dots, rectangular tags drawn in CSS/SVG) carrying his real numbers ("팔로워 +412", "전환율 3.1%", "8주"). They are physical: grab one with the mouse and throw it, they slide, bump the edges and each other, rotate and settle (simple hand-written 2D physics with friction). Moving the pointer fast gives nearby stickers a nudge. Double click or a button deals a fresh sticker. Underneath, the headline stays readable. On load the stickers get slapped on one after another. Projects are laid out like flyer product blocks with a big number as the price and small print as the method, uneven sizes, not identical cards. Typeface: a very heavy Korean display face for prices and headlines (for example Black Han Sans or Do Hyeon) and a plain sans for small print, chosen deliberately.

Shared rules for all pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images (draw with CSS/SVG/canvas). lang="ko". Fonts from Google Fonts only, with system fallbacks.
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback (drag or tap, without blocking page scroll outside the stickers) and an idle auto-motion so the page is alive without a pointer; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px with no horizontal scroll.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, one accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people, no real brand names or logos, no real contact details.

Verify before reporting: screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-11 --window-size=1440,900 --virtual-time-budget=12000 --screenshot=<scratch>/shot-11.png file://<repo>/11-oh-taehyun.html
Headless Chrome will not go narrower than about 500px, so for mobile write a small wrapper HTML in the scratchpad that embeds the page in a 390x844 iframe and screenshot that to shot-11-m.png. Headless can freeze CSS animations, so make sure nothing important stays invisible if an entrance animation never runs. Read the images, fix what looks broken (stickers hiding the headline, overflow, unreadable contrast, empty hero), and grep the file for the em dash and en dash characters (must be 0). Report in 3 lines: the signature interaction, palette and fonts, anything not verified.
```
