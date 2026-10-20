# stock-public-data

Blogger의 `품절주 연구` 페이지에서 읽기 위한 공개용 데이터 저장소입니다.

## 공개 원칙

이 저장소에는 Blogger 화면에 필요한 최종 표시 데이터만 둡니다.

공개 대상:
- `blogger_stock_data.json`
  - 종목명
  - 종목코드
  - 시장
  - 최대주주 등 지분율
  - 판정상태(AUTO / REVIEW)
  - 기준 사업보고서명
  - DART 접수번호
  - DART 원문 링크
  - 데이터 갱신 시각

공개하지 않는 것:
- DART API 키
- GitHub 토큰/인증정보
- 원본 DART CSV 전체
- 내부 판정 원장
- 중간 계산 파일
- 내부 검토 메모

## 데이터 흐름

`dart-stock-automation` (Private)
→ ①~⑥ 자동 계산
→ `blogger_stock_data.json` 생성
→ `stock-public-data` (Public)에 최종 JSON만 반영
→ Blogger `품절주 연구` 페이지가 해당 JSON을 읽어 표시

## 주의

`REVIEW` 후보는 자동 확정값이 아니며 추가 확인이 필요합니다.
