# 백하은 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 13-baek-haeun.html

## 시안 지시

이 시안은 "한 회사의 채용 공고에 맞춰 만든 지원용 포트폴리오"다. 지원자 본인의 페이지라는 것이 분명해야 하고, 그 회사의 사이트나 앱으로 보여서는 안 된다.

**인물(가상)**: 백하은, 전주대학교 컴퓨터공학과 4학년. 네이버 프론트엔드 개발자 신입에 지원한다.

**사실 자료(골라 쓴다)**
- 교내 수강 후기 검색: 검색 응답 1.8초에서 0.4초. 후기 2만 3천 건.
- 접근성 점검 도구: 학교 홈페이지 40쪽 점검, 오류 312개 보고, 그중 180개 반영.
- 캡스톤 시간표 앱: 주간 사용자 900명, Lighthouse 성능 62에서 96.
- 쓰는 것: TypeScript, React, 웹 접근성, 성능 측정.
- 가상의 공고 요건 다섯 개와 증거: 웹 표준과 접근성 / 컴포넌트 기반 개발 / 성능 측정과 개선 / 코드 리뷰와 협업 / 많은 사용자가 쓰는 서비스에 대한 관심.
- 메일 haeun@example.com.

**형식(뼈대)**: 페이지 전체가 검색창 하나다. 흰 화면 가운데에 입력창 하나만 있다. 아무것도 누르지 않으면 입력창이 스스로 검색어를 친다("백하은 성능", "백하은 접근성"). 검색어에 따라 그 아래에 결과가 뜬다. 결과가 곧 그녀의 프로젝트 사실이고, 일치한 낱말이 초록으로 칠해진다. 방문자가 직접 쳐도 된다. "공고"라고 치면 요건과 증거가 결과로 나온다. 맞는 것이 없으면 "결과 없음" 대신 칠 수 있는 낱말을 보여 준다. 큰 이름 제목, 소개 문단, 메뉴는 없다.

**대표 동작**: 결과는 글자를 칠 때마다 걸러지고, 순서가 바뀔 때 자리 이동이 보인다. 포인터는 돋보기다. 포인터 아래의 글자가 둥근 렌즈 안에서 살짝 커진다.

**색**: 흰 바탕, 거의 검정 글자, 회사의 초록(#03C75A) 하나. 평평하게.

**글꼴**: 마루 부리(네이버가 공개한 명조) 하나만 쓴다.
```css
@font-face{font-family:"MaruBuri";font-weight:400;src:url("https://hangeul.pstatic.net/hangeul_static/webfont/MaruBuri/MaruBuri-Regular.woff2") format("woff2");font-display:swap}
@font-face{font-family:"MaruBuri";font-weight:700;src:url("https://hangeul.pstatic.net/hangeul_static/webfont/MaruBuri/MaruBuri-Bold.woff2") format("woff2");font-display:swap}
```

**브랜드 안전선(엄격)**: 회사 이름은 글자로만, 색은 테마색만 쓴다. 로고, 워드마크 흉내, 캐릭터, 실제 앱 화면, 실제 슬로건과 공고 문구는 쓰지 않는다. 회사와 관계가 있다고 말하지 않는다.

**맨 아래 고지 문장**: "데모용으로 만든 가상의 인물입니다. 네이버와 아무 관계가 없고, 공고 요건도 가상으로 만든 것입니다."
~~~
