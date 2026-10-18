# hitbox
힛박스 - 포켓몬카드 재고·박스 기대값·노원 매장 지도

## 공용 박스 시세

`data/prices.json` 은 GitHub Actions(`.github/workflows/prices.yml`)가 30분마다 크림·중고나라·번개장터를 읽어 갱신합니다. 힛박스 앱은 이 파일을 받아 씁니다.

## 설문 AI 판별

설문 사이트(https://hitbox-siwan.web.app)에 로그인 없이 들어온 장소는 GitHub Actions(`.github/workflows/judge.yml`)가 10분마다 판별합니다.
링크·전화번호·장난 글·중복은 규칙으로 먼저 거르고, 나머지는 GitHub Actions 서버 안에서 띄운 무료 공개 AI 모델(gemma3)이 기준대로 봐서 통과한 곳만 힛박스 앱 지도에 올립니다. 결과는 사이트 완료 화면에 바로 뜹니다.
