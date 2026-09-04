# 판매 사이트

정적 HTML 여섯 장. 빌드 없음, 외부 폰트·스크립트 없음. 어디에 올려도 그대로 뜬다.

    index.html        홈 — 고객군 셋 입구
    firm.html         회계법인·세무사무소용 (평가 8종 · 사업비 정산 · 부가세 대사 · TP 포함)
    finance.html      기업 재무팀용 (부가세 대사 · IFRS 18 · KSSB 준비 중)
    actuary.html      계리사용 (계리평가)
    free/index.html   무료 도구·글 목록
    free/penalty.html 세금계산서 가산세 계산기 — expert-service `vat_recon/penalty.py` 의 JS 이식.
                      정답지 6건을 페이지가 열릴 때 스스로 검산한다. 규칙이 바뀌면 **양쪽을 같이** 고친다
    free/mismatch.html 글 — 홈택스와 장부가 안 맞을 때
    buy.html          가격 · 체험판 · 계좌 · 세금계산서 · FAQ
    style.css         공용

## 사장님이 채울 자리 — 노란 밑줄(`.todo`)

브라우저에서 노랗게 보이는 곳이 전부다. 채우면 `class="todo"` 를 지운다.

- 회사명(모든 페이지 상단·하단)
- 사업자등록번호 · 대표
- 문의 메일 (`buy.html` 의 `mailto:CHANGE-ME@example.com` 포함)
- 가격 셋 (`buy.html`)
- 은행 · 계좌번호 · 예금주 (`buy.html`)

## 올리기 — Cloudflare Pages

1. 이 폴더를 GitHub 저장소에 올린다.
2. Cloudflare Pages → Create project → 저장소 연결 → 빌드 명령 없음, 출력 디렉토리 `/`.
3. 도메인을 연결한다. 도메인 연 1~2만원 외 비용 없음.

## 왜 카탈로그가 아닌가

사는 사람이 셋(회계법인 · 기업 재무팀 · 계리사)이고 파는 물건과 배포 형태가 다르다.
14개를 한 목록에 놓으면 아무에게도 말하지 않는 페이지가 된다. 사이트의 역할은
카탈로그가 아니라 **신뢰 장치**다 — 법인은 이름 없는 zip 에 송금하지 않는다.
첫 판매는 손으로 하고, 무료 페이지가 사람을 데려온다.

## 로컬 확인

    python -m http.server 8888

`http://127.0.0.1:8888` — `localhost` 는 이 PC 에서 IPv6 문제로 안 뜬다.
