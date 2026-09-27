# bokwatch — 한국은행 기준금리 결정 확률 모델

공개: https://april774936.github.io/bokwatch/
저장소: github.com/april774936/bokwatch (public)
마지막 갱신: 2026-09-27 (Claude)

## 무엇인가
CME FedWatch를 한국(KOFR 3개월 선물)에 이식한 한국은행 기준금리 결정 확률 모델. 취업 포트폴리오(증권사 RA/IB/Deals 지원용 정량 소재). FedWatch와 거의 동일한 디자인의 공개 페이지 + 방법론 해설 아티팩트.

## 자동화
GitHub Actions가 매 영업일 KRX Open API에서 데이터를 받아 `bokwatch_data.json`을 갱신.

## ⚠ 확인 필요 (2026-09-27 기준)
- KRX Open API 키가 2026-09-25 무렵 만료 예정이었음. 마지막으로 확인된 자동 동기화 커밋은 09-24 — **키 갱신 여부와 최신 GitHub Actions 실행 로그(성공/실패)를 확인할 것.**
- 다음 금통위 결정(2026-10-22, 11-26) 발표되면 수동으로 RATE_STEPS 업데이트 필요.

## 방법론 원칙 (건드리지 말 것)
- 인하-클램프/단조 강제 금지 — raw curve 역전 시에도 결과 그대로 표시.
- 예측치는 최대확률 이산 레벨(예: 3.00)로 표시, 기대값 평균 아님.
- 검증/백테스트 없음은 이 프로젝트만의 약점이 아니라 FedWatch류 지표 전체의 공통 한계 — 과대 비판하지 말 것.
