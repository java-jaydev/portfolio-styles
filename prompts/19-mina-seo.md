# Mina Seo 시안에 쓴 프롬프트

- 만든 사람: [java-jaydev](https://github.com/java-jaydev)
- 모델: Claude Fable 5.2 (`claude-fable-5-2`)
- 도구: Claude Code. 새 에이전트에게 아래 프롬프트를 한 번 보냈습니다. 추가 지시는 없었고, 에이전트가 스스로 캡처해 보고 고친 뒤 끝냈습니다.
- 함께 읽힌 것: [공통 브리프 v2](brief-v2.md), 디자인 스킬 frontend-design, better-writing, better-typography, better-ui, 오픈소스 스킬 [Impeccable](https://github.com/pbakaus/impeccable)(Apache-2.0)의 참고 문서.
- 사람이 나중에 고친 것: 없음.

~~~text
포트폴리오 웹페이지 하나를 만들어 주세요.

먼저 공통 브리프를 읽고 그대로 따르세요: prompts/brief-v2.md
만들 파일: 19-mina-seo.html

## 시안 지시

**언어**: 페이지는 전부 영어다(lang="en"). 공통 브리프의 글 규칙을 영어에도 똑같이 적용한다: 설명하지 않고, 다짐과 형용사 없이, 사실과 숫자만, 첫 화면 15단어 이하, 전체 300단어 안쪽. 미국식 실무 영어로 쓰고, 이력서 상투어(passionate, results-driven, leverage 등)는 쓰지 않는다. 실제 회사 이름은 쓰지 않고 "a logistics startup"처럼 일반화한다.

**인물(가상)**: Mina Seo, Forward Deployed Engineer, 경력 6년. 고객사 현장에 들어가 제품을 붙이고 돌아가게 만드는 사람.

**사실 자료(골라 쓴다. 영어로 옮겨 쓴다)**
- 고객사 배치 11곳, 4개국. 가장 긴 현장 14주, 가장 짧은 현장 4일.
- 물류 스타트업: 수작업 대사 작업 주 30시간을 3시간으로.
- 병원 그룹: 예약 연동, 3주 만에 가동, 첫 달 오류율 0.2%.
- 제조사: 20년 된 ERP 에서 야간 배치로 데이터 뽑기, 고객 담당자 2명 교육.
- 현장에서 본사로 올린 제품 개선 요청 23건 중 9건 출시.
- 쓰는 것: Python, SQL, TypeScript, 그리고 고객 회의실 화이트보드.
- 메일 mina@example.com.

**형식(뼈대)**: 페이지 전체가 현장 수첩이다. 가로로 넘기는 낱장들이고, 한 장이 한 현장이다. 장마다 도착 날짜, 머문 기간, 한 줄 문제, 한 줄 결과, 그리고 그 현장의 도장(입국 도장 같은 것, 도시 이름은 지어낸다). 맨 앞 장에는 이름과 직함만 있다. 맨 뒤 장은 연락처다. 큰 제목, 소개 문단, 메뉴는 없다.

**대표 동작**: 낱장을 잡아 넘긴다(관성 있음). 포인터로 누른 자리에 잉크 도장이 실제로 찍힌다. 각도와 번짐이 매번 조금 다르다. 가만히 두면 다음 장 모서리가 살짝 들린다.

**색**: 방안지 느낌의 옅은 회청색 종이, 남색 잉크, 도장용 빨강과 초록. 평평하게.

**글꼴**: Fontshare 에서 Gambetta(본문, 명조)와 Cabinet Grotesk(숫자와 도장).
`<link href="https://api.fontshare.com/v2/css?f[]=gambetta@400,600&f[]=cabinet-grotesk@400,800&display=swap" rel="stylesheet">`

**맨 아래 고지 문장**: "A fictional person, made as a demo."
~~~
