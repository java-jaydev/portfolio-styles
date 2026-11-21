# 포트폴리오 스타일 모음

포트폴리오 시안과, 각 시안을 만든 프롬프트.

https://java-jaydev.github.io/portfolio-styles/

## 규칙
- 시안마다 **프롬프트 원문, 모델, 만든 사람**을 함께 둔다. [prompts/](prompts/)
- 프롬프트는 한 번만 보낸다. 그 뒤 사람이 고친 것이 있으면 적는다.
- 모두 가상의 인물이다. 전주대학교, 각 회사와 관계없다. 공고 요건도 지어낸 것이다.

## 가져다 쓰기
1. 마음에 드는 HTML 파일 하나를 내려받는다. 파일 하나로 열린다.
2. 이름과 내용을 자기 것으로 바꾼다.
3. 출처를 남긴다.
   - 파일 맨 위의 주석은 지우지 않는다(MIT 조건).
   - 화면 아래에 한 줄: `디자인 출처: github.com/java-jaydev/portfolio-styles`

새로 만들려면 [prompts/brief-v2.md](prompts/brief-v2.md)와 아무 시안의 프롬프트를 복사해 인물과 형식만 바꾼다.

## 내 것 올리기
풀 리퀘스트로 네 가지를 보낸다.

| 무엇 | 어디에 |
|---|---|
| HTML 파일 하나 | 저장소 맨 위 |
| 프롬프트 원문, 모델 이름, GitHub 아이디 | `prompts/` |
| 첫 화면 캡처(가로 900px jpg) | `thumbs/` |
| 목록 항목 하나 | `index.html` 의 `ITEMS` |

Git이 처음이면 [이슈](https://github.com/java-jaydev/portfolio-styles/issues)에 링크, 프롬프트, 모델, 아이디를 남긴다.

받는 조건: 본인이 만든 본인 것. 프롬프트와 모델이 없으면 받지 않는다. 공개하기 싫은 개인정보는 뺀다.

## 쓴 것
- 모델: Claude Fable 5.2, Claude Code에서 실행
- 디자인 스킬: frontend-design, better-writing, better-typography, better-ui, [Impeccable](https://github.com/pbakaus/impeccable) (Apache-2.0)
- 글꼴: 시안마다 다르다. 각 프롬프트 파일에 주소가 있다.
  - Pretendard, SUIT, Wanted Sans, LINE Seed KR, 마루 부리, 배민 한나체와 주아체, 지마켓 산스, 에스코어 드림, 둥근모꼴, Galmuri
  - Fontshare: Clash Display, Satoshi, Cabinet Grotesk, Gambetta, General Sans
  - 01~12번 중 예전 방식으로 만든 것은 Google Fonts
- 글꼴은 각 배포처에서 불러오며 저장소에 넣지 않았다. 예외는 `Galmuri11.woff2`(SIL OFL 1.1, [라이선스](fonts-license/Galmuri-LICENSE.txt)). 글꼴마다 라이선스가 다르니 자기 사이트에 쓸 때는 배포처의 조건을 확인한다.

## 라이선스
[MIT](LICENSE)
