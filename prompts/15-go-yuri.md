# 고유리 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 15-go-yuri.html

## 시안 지시

이 시안은 "한 회사의 채용 공고에 맞춰 만든 지원용 포트폴리오"다. 지원자 본인의 페이지라는 것이 분명해야 하고, 그 회사의 사이트나 앱으로 보여서는 안 된다.

**인물(가상)**: 고유리, 전주대학교 일본언어문화학과 4학년(소프트웨어 융합 복수전공). 라인 글로벌 서비스 현지화 담당 겸 QA 신입에 지원한다.

**사실 자료(골라 쓴다)**
- 학교 앱 일본어판 문구 420개 검수, 어색한 표현 63개 고침.
- 오픈소스 앱 번역 기여 3건 반영.
- 도쿄 교환학생 1년, 현지 사용자 12명 인터뷰.
- 테스트 케이스 180개 작성, 버그 27건 보고.
- JLPT N1, 영어 문서 읽기.
- 가상의 공고 요건 다섯 개와 증거: 일본어 업무 수준 / 테스트 케이스 설계 / 다국어 문구 검수 / 여러 나라 팀과 협업 / 버그를 정확히 적기.
- 메일 yuri@example.com.

**형식(뼈대)**: 회사 이름이 "선"이다. 페이지 전체를 끊기지 않는 선 하나로 그린다. 선은 이름에서 시작해 페이지 끝까지 내려가며, 지구본, 도시(전주, 도쿄, 방콕, 타이베이), 말풍선, 체크 표시를 한 붓으로 그리고 지나간다. 글자는 선 옆에 조금씩만 붙는다. 같은 문장이 한국어, 日本語, English 세 줄로 나오는 곳을 몇 군데 둔다(각각 올바른 lang 속성, 일본어와 영어는 자연스럽고 정확하게). 그 자체가 현지화 실력의 증거다. 큰 이름 제목, 소개 문단, 메뉴는 없다.

**대표 동작**: 스크롤하면 선이 그려진다. 선의 끝은 포인터를 실처럼 따라온다. 약간 늘어지고, 포인터가 원을 그리면 고리가 생긴다. 가만히 두면 혼자 천천히 고리를 그린다.

**색**: 회사의 초록(#06C755) 선, 흰 바탕, 진한 남색 글자(#0B1F3A). 평평하게.

**글꼴**: LINE Seed KR(라인이 공개한 글꼴). 일본어는 시스템 일본어 글꼴로 폴백한다.
```css
@font-face{font-family:"LINESeedKR";font-weight:400;src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_11-01@1.0/LINESeedKR-Rg.woff2") format("woff2");font-display:swap}
@font-face{font-family:"LINESeedKR";font-weight:700;src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_11-01@1.0/LINESeedKR-Bd.woff2") format("woff2");font-display:swap}
```

**브랜드 안전선(엄격)**: 회사 이름은 글자로만, 색은 테마색만 쓴다. 로고, 워드마크 흉내, 캐릭터, 실제 앱 화면, 실제 슬로건과 공고 문구는 쓰지 않는다. 회사와 관계가 있다고 말하지 않는다.

**맨 아래 고지 문장**: "데모용으로 만든 가상의 인물입니다. 라인과 아무 관계가 없고, 공고 요건도 가상으로 만든 것입니다."
~~~
