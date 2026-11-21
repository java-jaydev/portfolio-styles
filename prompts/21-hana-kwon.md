# Hana Kwon 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 21-hana-kwon.html

## 시안 지시

**언어**: 페이지는 전부 영어다(lang="en"). 공통 브리프의 글 규칙을 영어에도 똑같이 적용한다: 설명하지 않고, 다짐과 형용사 없이, 사실과 숫자만, 첫 화면 15단어 이하, 전체 300단어 안쪽. 미국식 실무 영어로 쓰고, 이력서 상투어(passionate, results-driven, leverage 등)는 쓰지 않는다. 실제 회사 이름은 쓰지 않고 "a logistics startup"처럼 일반화한다.

**인물(가상)**: Hana Kwon, Product Manager, 경력 8년.

**사실 자료(골라 쓴다. 영어로 옮겨 쓴다)**
- 결제 제품: 결제 단계 5개에서 2개, 완료율 61%에서 78%.
- 하지 않기로 한 것 4가지: 포인트 제도, 다크 모드 우선 개발, 세 번째 요금제, 자체 채팅.
- 출시를 6주 미룬 결정: 환불 오류 재현율 3%가 남아 있었기 때문.
- 팀: 엔지니어 9명, 디자이너 2명. 분기마다 고객 통화 30건.
- 메일 hana@example.com.

**형식(뼈대)**: 페이지 전체가 한 장짜리 메모다. 좁은 단 하나, 타자 친 문서. 제목은 "Decisions"이고 그 아래에 그녀가 내린 결정이 날짜순으로 적혀 있다. 절반은 "하지 않기로 한 것"이고 줄이 그어져 있다. 여백에는 손으로 쓴 듯한 짧은 메모와 숫자가 붙는다. 꾸밈이 거의 없는 것이 이 시안의 꾸밈이다. 큰 이름 제목, 소개 문단, 메뉴는 없다. 이름은 메모의 From 칸에.

**대표 동작**: 줄 그은 결정 위로 포인터를 가져가면 줄이 걷히고 왜 안 했는지 한 줄이 나온다. 여백 메모는 포인터가 가까워지면 종이에서 살짝 떠오른다. 처음 한 번, 문서가 타자 치듯 찍힌다.

**색**: 종이색, 검은 글자, 빨간 교정 펜 하나. 평평하게.

**글꼴**: Fontshare 에서 Gambetta(본문)와 Satoshi(여백 메모와 숫자).
`<link href="https://api.fontshare.com/v2/css?f[]=gambetta@400,600&f[]=satoshi@400,700,900&display=swap" rel="stylesheet">`

**맨 아래 고지 문장**: "A fictional person, made as a demo."
~~~
