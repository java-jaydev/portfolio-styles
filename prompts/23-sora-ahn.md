# Sora Ahn 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 23-sora-ahn.html

## 시안 지시

**언어**: 페이지는 전부 영어다(lang="en"). 공통 브리프의 글 규칙을 영어에도 똑같이 적용한다: 설명하지 않고, 다짐과 형용사 없이, 사실과 숫자만, 첫 화면 15단어 이하, 전체 300단어 안쪽. 미국식 실무 영어로 쓰고, 이력서 상투어(passionate, results-driven, leverage 등)는 쓰지 않는다. 실제 회사 이름은 쓰지 않고 "a logistics startup"처럼 일반화한다.

**인물(가상)**: Sora Ahn, Developer Advocate, 경력 5년.

**사실 자료(골라 쓴다. 영어로 옮겨 쓴다)**
- 발표 34번, 9개 도시. 가장 큰 청중 1,800명, 가장 작은 청중 6명.
- 예제 저장소: 별 4,200개, 이슈 응답 중앙값 5시간.
- 문서 개편: 첫 API 호출까지 걸리는 시간 22분에서 6분.
- 커뮤니티 질문 2,900개에 답함.
- 메일 sora@example.com.

**형식(뼈대)**: 페이지 전체가 행사 출입증 하나다. 화면 위에서 내려온 목줄 끝에 출입증이 매달려 있다. 앞면에는 이름과 직함만 있다. 뒤집으면 뒷면에 숫자 넷. 그 아래로 지난 행사들의 출입증이 줄줄이 매달려 있고, 하나하나가 발표 하나다(도시 이름은 지어낸다). 큰 이름 제목, 소개 문단, 메뉴는 없다.

**대표 동작**: 출입증은 진짜처럼 매달려 흔들린다(목줄은 물리 계산, matter.js 를 써도 된다). 포인터로 잡아 던지면 흔들리다 멈춘다. 누르면 뒤집힌다. 가만히 두면 공기에 조금씩 흔들린다.

**색**: 진한 가지색 무대, 출입증은 형광 노랑과 흰색, 목줄은 선명한 분홍. 평평하게.

**글꼴**: Fontshare 에서 Clash Display(이름과 숫자)와 General Sans(작은 글자).
`<link href="https://api.fontshare.com/v2/css?f[]=clash-display@400,600,700&f[]=general-sans@400,600&display=swap" rel="stylesheet">`

**맨 아래 고지 문장**: "A fictional person, made as a demo."
~~~
