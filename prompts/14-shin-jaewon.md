# 신재원 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 14-shin-jaewon.html

## 시안 지시

이 시안은 "한 회사의 채용 공고에 맞춰 만든 지원용 포트폴리오"다. 지원자 본인의 페이지라는 것이 분명해야 하고, 그 회사의 사이트나 앱으로 보여서는 안 된다.

**인물(가상)**: 신재원, 전주대학교 컴퓨터공학과 4학년. 카카오 서버 개발자 신입에 지원한다.

**사실 자료(골라 쓴다)**
- 교내 축제 선착순 예매 서버: 동시 접속 500명, 중복 예매 0건, 좌석 1,200석이 4분 만에 매진.
- 채팅 서버 과제: 메시지 유실 0건(재전송과 순번 확인), 지연 중앙값 42ms.
- 장애 한 번: 새벽 2시 커넥션 풀 고갈, 17분 만에 복구, 회고 문서 작성.
- 쓰는 것: Kotlin, Spring, MySQL, Redis, Kafka 기초.
- 가상의 공고 요건 다섯 개와 증거: 서버 개발 경험 / 자료구조와 네트워크 기초 / 많은 요청을 다뤄 본 경험 / 장애 대응 / 코드 리뷰와 협업.
- 메일 jaewon@example.com.

**형식(뼈대)**: 페이지 전체가 대화 한 줄기다. 면접관이 짧게 묻고 그가 말풍선으로 답한다. 방문자가 다음 질문을 고른다("뭘 만들었어요?", "터진 적 있어요?", "공고랑 맞춰 보면요?"). 답은 길지 않다. 한 풍선에 한 사실, 숫자는 크게. 말투는 실제 메신저처럼 짧고 편하다. 말풍선 모양은 직접 그리고, 어떤 실제 메신저의 화면 배치나 아이콘도 따라 하지 않는다. 한 번에 다 보고 싶은 사람을 위해 대화 전체를 펼치는 길을 하나 둔다. 큰 이름 제목, 소개 문단, 메뉴는 없다.

**대표 동작**: 풍선은 말랑하다. 나올 때 튀어 오르고, 포인터가 지나가면 그쪽으로 살짝 늘어났다가 돌아온다. 답이 오기 전에 입력 중 점 세 개가 뜬다.

**색**: 회사의 노랑(#FEE500), 따뜻한 검정(#191919), 흰색. 평평하게.

**글꼴**: 지마켓 산스.
```css
@font-face{font-family:"GmarketSans";font-weight:300;src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2001@1.1/GmarketSansLight.woff") format("woff");font-display:swap}
@font-face{font-family:"GmarketSans";font-weight:500;src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2001@1.1/GmarketSansMedium.woff") format("woff");font-display:swap}
@font-face{font-family:"GmarketSans";font-weight:700;src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2001@1.1/GmarketSansBold.woff") format("woff");font-display:swap}
```

**브랜드 안전선(엄격)**: 회사 이름은 글자로만, 색은 테마색만 쓴다. 로고, 워드마크 흉내, 캐릭터, 실제 앱 화면, 실제 슬로건과 공고 문구는 쓰지 않는다. 회사와 관계가 있다고 말하지 않는다.

**맨 아래 고지 문장**: "데모용으로 만든 가상의 인물입니다. 카카오와 아무 관계가 없고, 공고 요건도 가상으로 만든 것입니다."
~~~
