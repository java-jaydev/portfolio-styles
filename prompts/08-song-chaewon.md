# 송채원 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 디자인 스킬 `frontend-design` 을 읽힌 상태에서 실행했습니다.
- 방식: 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 하지 않았고, 에이전트가 스스로 화면을 캡처해 보고 고친 뒤 끝냈습니다.
- 사람이 나중에 고친 것: 없음.
- 이 프롬프트는 앞선 대화(시안들의 방향을 정하던 대화)를 이어받은 에이전트에게 보냈습니다. 새 대화에 그대로 붙여 넣으면 결과가 조금 다를 수 있습니다.
- 내 컴퓨터의 폴더 경로만 `<repo>`, `<scratch>` 로 줄였습니다. 나머지는 보낸 그대로입니다.

```text
You are a fork. Build ONE file only: 08-song-chaewon.html. Do not touch git, do not create other project files, do not edit any other file.

Persona (fictional): 송채원, 여, 전주대학교 음악학과 3학년, 작곡과 싱어송라이터 지망. Fill plausible content: 소개, 작업 3~4개(예: 자작곡 EP 4곡, 학과 뮤지컬 편곡, 지역 카페 정기 공연, 단편영화 음악. 곡 수, 길이, 공연 횟수, 관객 수 같은 숫자 포함. 실제 음원 플랫폼 수치나 수상 사칭 금지), 다루는 악기와 도구(피아노, 기타, Logic 등), 연혁, 연락처(example.com 메일).

Design direction (chosen to differ from 11 sibling pages): "튕기는 현". Deep wine ground (#4A0E2B) with apricot (#FFB38A) and ivory (#FFF6E9), flat color, no gradients. Signature moment: the hero is a set of long horizontal strings across the full width. When the pointer crosses a string it is plucked: the string vibrates as a standing wave that decays (canvas), and a soft note plays through the Web Audio API (a plucked tone from oscillators with a quick decay, pentatonic so anything sounds good). Sound must only start after a user gesture and there must be a clearly visible sound on/off control, off by default until the user turns it on; the visual pluck works with sound off. Keyboard users can pluck with number keys or by focusing string buttons. On load the strings are strung one by one. Works are laid out like a track list with durations and a small waveform per track, not cards. Typeface: a Korean serif with warmth for titles and a quiet sans for body, chosen deliberately.

Shared rules for all pages:
- Single self-contained HTML, inline CSS and JS, no JS libraries, no external images or audio files (draw with CSS/SVG/canvas, synthesize sound). lang="ko". Fonts from Google Fonts only, with system fallbacks.
- Motion graphics plus mouse-reactive behavior are required; use requestAnimationFrame; give a touch fallback (drag or tap) and an idle auto-motion so the page is alive without a pointer; respect prefers-reduced-motion; visible keyboard focus; responsive down to 375px with no horizontal scroll.
- Follow the frontend-design skill already in your context: avoid its listed defaults (all-caps eyebrows, middle-dot meta strings, identical rounded cards, fade-up on every section, arrows on links, one accented word in a headline).
- Never use em dash or en dash anywhere. No AI markers. Footer one line: "데모용으로 만든 가상의 인물입니다."
- Korean copy, natural student voice, specific numbers, no real people or real contact details.

Verify before reporting: screenshot with
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir=<scratch>/chrome-08 --window-size=1440,900 --virtual-time-budget=12000 --screenshot=<scratch>/shot-08.png file://<repo>/08-song-chaewon.html
Headless Chrome will not go narrower than about 500px, so for mobile write a small wrapper HTML in the scratchpad that embeds the page in a 390x844 iframe and screenshot that to shot-08-m.png. Headless can freeze CSS animations, so make sure nothing important stays invisible if an entrance animation never runs. Read the images, fix what looks broken (overlap, overflow, unreadable contrast, empty hero), and grep the file for the em dash and en dash characters (must be 0). Report in 3 lines: the signature interaction, palette and fonts, anything not verified.
```
