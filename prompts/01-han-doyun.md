# 한도윤 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.
- 내 컴퓨터의 폴더 경로만 짧게 줄였습니다. 나머지는 보낸 그대로입니다.

```text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
- 브리프의 `<impeccable>` 은 <impeccable 스킬 폴더> 입니다.
- 브리프의 `<scratch>` 는 <임시 폴더> 입니다.
- 만들 파일: 01-han-doyun.html (번호 01). 이미 같은 이름의 옛 시안이 있습니다. 읽어 보고 캔버스 코드는 가져다 써도 되지만, 뼈대와 글은 버리고 새로 만듭니다.

## 시안 지시

**인물(가상)**: 한도윤, 전주대학교 컴퓨터공학과 4학년, 백엔드 개발자 지망.

**사실 자료(이 중에서 골라 쓴다. 다 쓸 필요 없다)**
- 전주 시내버스 도착 알림 API: 하루 요청 4만 건, 응답 중앙값 38ms, 캐시 적중 91%. 2026년 3월부터 운영.
- 캡스톤 LLM 챗봇 서버: 동시 접속 200명 테스트 통과, 큐로 요청을 줄 세워 타임아웃 0건.
- 동아리 출석 시스템: 회원 86명, 3학기째 사용, 장애 1번(DB 디스크 가득 참, 23분 만에 복구).
- 쓰는 것: Kotlin, Spring, PostgreSQL, Redis, Docker.
- 메일 doyun.han@example.com, GitHub doyun-han-example.

**형식(뼈대)**: 페이지 전체가 서버 구조도 한 장이다. 스크롤해서 읽는 문서가 아니라, 화면을 가득 채운 구조도 위를 돌아다니는 지도다. 노드(클라이언트, 게이트웨이, 캐시, 큐, 워커, DB)가 곧 내용이다. 노드를 누르면 그 자리에서 그 노드가 맡은 프로젝트 사실이 펼쳐진다(예: 캐시 노드를 누르면 "적중 91%"). 이름은 도면 귀퉁이의 표제란처럼 작게 둔다. 큰 이름 제목, 한 줄 소개, 상단 메뉴는 없다. 휴대폰에서는 구조도를 세로로 다시 배치한다.

**대표 동작**: 요청 패킷이 선을 따라 계속 흐른다. 포인터가 요청을 보내는 쪽이다. 포인터가 있는 자리에서 패킷이 출발해 가장 가까운 노드로 들어가고, 큐가 차면 줄이 길어지고, 워커가 하나씩 가져간다. 실제 숫자(처리한 요청 수, 대기 길이)가 구조도 안에서 바뀐다.

**색**: 진한 코발트(#1437C8) 바탕, 흰 선, 신호 노랑(#FFD60A)은 사용자 패킷에만. 평평하게.

**글꼴**: Wanted Sans Variable 하나만 쓴다.
`<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/wanteddev/wanted-sans@v1.0.3/packages/wanted-sans/fonts/webfonts/variable/split/WantedSansVariable.min.css">` (font-family: "Wanted Sans Variable")

**맨 아래 고지 문장**: "데모용으로 만든 가상의 인물입니다."
```
