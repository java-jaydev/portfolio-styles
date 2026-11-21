# 한보람 시안에 쓴 프롬프트

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
- 만들 파일: 17-han-boram.html (번호 17)

## 시안 지시

이 시안은 "한 회사의 채용 공고에 맞춰 만든 지원용 포트폴리오"다. 지원자 본인의 페이지라는 것이 분명해야 하고, 그 회사의 사이트나 앱으로 보여서는 안 된다.

**인물(가상)**: 한보람, 전주대학교 시각디자인학과 4학년. 배달의민족 콘텐츠 마케터 겸 UX 라이터 신입에 지원한다.

**사실 자료(이 중에서 골라 쓴다)**
- 학교 앞 분식집 메뉴판 문구를 바꿈: 세트 주문 비율 22%에서 35%. 4주, 주문 612건.
- 학식 알림 문구 A/B 실험: 열람률 1.6배. 표본 1,840명.
- 동아리 모집 포스터 문구 연작 12장: 지원자 31명에서 74명.
- 가게 사장님 10명 인터뷰, 한 명당 40분.
- 가상의 공고 요건 다섯 개와 그에 맞는 증거: 짧은 문장으로 사람을 움직인 경험 / 브랜드 말투를 지키며 쓰기 / 실험하고 숫자로 확인 / 디자이너, 개발자와 협업 / 사장님과 고객을 직접 만남.
- 메일 boram@example.com.

**형식(뼈대)**: 페이지 전체가 주방 주문 프린터에서 나온 긴 영수증 한 장이다. 가운데에 좁고 긴 감열지가 있고, 그것이 포트폴리오의 전부다. 영수증의 문법을 그대로 쓴다: 가게 이름 자리에 그녀의 이름, 주문 항목 자리에 프로젝트(수량과 금액 자리에 실제 숫자), 합계, 절취선, 맨 아래 바코드. "공고 요건과 내 경험"은 영수증의 "요청 사항" 칸처럼, 체크 표시와 한 줄 증거로 넣는다. 영수증은 원래 글이 짧다. 그 짧음을 지킨다. 그녀의 문구 감각은 설명이 아니라 항목 이름 하나하나의 재치로 보여 준다(회사의 실제 슬로건이나 광고 문구를 빌리지 않는다). 큰 이름 제목, 소개 문단, 상단 메뉴는 없다.

**대표 동작**: 처음 열면 영수증이 프린터에서 한 줄씩 밀려 나온다. 종이는 살아 있다. 얇은 감열지처럼 포인터 쪽으로 말리고 흔들리며 그림자가 따라 움직인다. 절취선을 잡아당기면 찢어져 다음 장이 나온다.

**색**: 회사의 민트(#2AC1BC) 바탕, 흰 감열지, 검은 인쇄, 형광펜 노랑 하나. 평평하게.

**글꼴**: 제목급 글자는 배민 한나체 Pro, 보조는 배민 주아체. 영수증 인쇄 줄은 둥근모꼴. 모두 눈누에서 CDN 으로 제공하는 무료 글꼴이다.
```css
@font-face{font-family:"BMHANNAPro";src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_seven@1.0/BMHANNAPro.woff") format("woff");font-display:swap}
@font-face{font-family:"BMJUA";src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_one@1.0/BMJUA.woff") format("woff");font-display:swap}
@font-face{font-family:"DungGeunMo";src:url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_six@1.2/DungGeunMo.woff") format("woff");font-display:swap}
```

**브랜드 안전선(엄격)**: 회사 이름은 글자로만, 색은 테마색만 쓴다. 로고, 워드마크 흉내, 캐릭터, 실제 앱 화면, 실제 슬로건과 공고 문구는 쓰지 않는다. 회사와 관계가 있다고 말하지 않는다.

**맨 아래 고지 문장**: "데모용으로 만든 가상의 인물입니다. 배달의민족과 아무 관계가 없고, 공고 요건도 가상으로 만든 것입니다."
```
