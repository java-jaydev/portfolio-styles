# Daniel Yoon 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 20-daniel-yoon.html

## 시안 지시

**언어**: 페이지는 전부 영어다(lang="en"). 공통 브리프의 글 규칙을 영어에도 똑같이 적용한다: 설명하지 않고, 다짐과 형용사 없이, 사실과 숫자만, 첫 화면 15단어 이하, 전체 300단어 안쪽. 미국식 실무 영어로 쓰고, 이력서 상투어(passionate, results-driven, leverage 등)는 쓰지 않는다. 실제 회사 이름은 쓰지 않고 "a logistics startup"처럼 일반화한다.

**인물(가상)**: Daniel Yoon, Growth Marketer, 경력 5년.

**사실 자료(골라 쓴다. 영어로 옮겨 쓴다)**
- 구독 앱: 가입 전환율 2.1%에서 3.4%, 실험 41번 중 9번 성공.
- 추천인 프로그램: 신규 가입의 18%가 추천으로. 고객 획득 비용 31% 감소.
- 실패한 것: 6주 걸린 리브랜딩 캠페인, 지표 변화 없음.
- 뉴스레터 0명에서 22,000명, 열람률 44%.
- 쓰는 것: SQL, 실험 설계, 카피.
- 메일 daniel@example.com.

**형식(뼈대)**: 페이지 전체가 그래프 한 장이다. 5년을 가로축으로 한 선 하나가 화면을 가로지른다. 선이 꺾이는 지점마다 그가 한 일이 있다. 오른 곳만이 아니라 평평했던 곳과 떨어진 곳도 그대로 있다(실패한 캠페인 포함). 글자는 꺾이는 지점에 붙은 짧은 주석뿐이다. 축 이름과 눈금은 진짜 그래프처럼 정확하다. 큰 이름 제목, 소개 문단, 메뉴는 없다. 이름은 그래프 제목 자리에 작게.

**대표 동작**: 포인터가 시간을 훑는다. 세로 안내선이 포인터를 따라가고, 그 시점의 숫자와 주석이 나타난다. 선은 처음 한 번 왼쪽에서 오른쪽으로 그려진다. 구간을 끌어서 고르면 그 사이의 변화율이 나온다.

**색**: 흰 바탕, 검은 축, 선은 선명한 주황 하나. 실패 구간은 회색. 평평하게.

**글꼴**: Fontshare 에서 Clash Display(숫자)와 General Sans(주석).
`<link href="https://api.fontshare.com/v2/css?f[]=clash-display@400,600,700&f[]=general-sans@400,600&display=swap" rel="stylesheet">`

**맨 아래 고지 문장**: "A fictional person, made as a demo."
~~~
