# Theo Lim 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 22-theo-lim.html

## 시안 지시

**언어**: 페이지는 전부 영어다(lang="en"). 공통 브리프의 글 규칙을 영어에도 똑같이 적용한다: 설명하지 않고, 다짐과 형용사 없이, 사실과 숫자만, 첫 화면 15단어 이하, 전체 300단어 안쪽. 미국식 실무 영어로 쓰고, 이력서 상투어(passionate, results-driven, leverage 등)는 쓰지 않는다. 실제 회사 이름은 쓰지 않고 "a logistics startup"처럼 일반화한다.

**인물(가상)**: Theo Lim, Senior Product Designer, 경력 7년.

**사실 자료(골라 쓴다. 영어로 옮겨 쓴다)**
- 은행 앱 송금 흐름: 화면 7개에서 3개, 오송금 문의 40% 감소.
- 디자인 시스템: 컴포넌트 84개, 4개 팀이 사용, 새 화면 제작 시간 절반.
- 접근성 개편: 명도 대비 실패 212곳 수정.
- 버린 시안 60개 넘음.
- 메일 theo@example.com.

**형식(뼈대)**: 페이지 전체가 끝없는 작업대다. 스크롤 문서가 아니라 끌어서 돌아다니고 확대하는 판이다. 판 위에 화면 시안들이 흩어져 있다. 최종안 옆에 버린 시안들이 엑스 표시와 함께 그대로 있다. 시안은 CSS 로 그린 단순한 와이어프레임이다. 글자는 시안 아래 붙은 짧은 이름표와 숫자뿐이다. 어떤 실제 디자인 도구의 화면도 따라 하지 않는다(도구 모음, 패널 없음). 큰 이름 제목, 소개 문단, 메뉴는 없다. 이름은 판 한가운데 작은 쪽지에.

**대표 동작**: 끌면 판이 움직이고(관성), 휠이나 두 손가락으로 확대된다. 다른 사람의 커서 두세 개가 판 위를 돌아다니며 가끔 시안에 의견 쪽지를 남긴다. 구석의 작은 지도가 지금 위치를 보여 준다. 키보드 화살표로도 움직인다.

**색**: 옅은 회색 판에 점 격자, 흰 시안, 검은 선, 선택 표시용 파랑 하나, 커서마다 다른 색. 평평하게.

**글꼴**: Fontshare 에서 Satoshi 하나만.
`<link href="https://api.fontshare.com/v2/css?f[]=satoshi@400,700,900&display=swap" rel="stylesheet">`

**맨 아래 고지 문장**: "A fictional person, made as a demo."
~~~
