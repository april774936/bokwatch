# Agent rules for this repo (Claude & Antigravity)

Read `HANDOFF.md` first.

1. 독립 git 저장소 — GitHub Pages 배포, GitHub Actions가 매 영업일 KRX Open API로 자동 동기화.
2. ★확률 로직에 인하-클램프/단조(isotonic) 강제를 절대 넣지 말 것(2026-09-17 사용자 결정). raw forward curve가 역전돼 기이한 확률이 나와도 그대로 둔다 — 데이터에 실재하는 신호로 취급, 모델은 시장 implied curve의 transcriber지 editor가 아님.
3. 금통위 결정 발표 시 `RATE_STEPS`에 한 줄 수동 추가(자동화 안 돼있음). 다음 결정일: 2026-10-22, 2026-11-26.
4. 예측치는 기대값 평균이 아니라 최대확률 이산 레벨로 표시(예: 3.03이 아니라 3.00).
5. FedWatch류 방법론과 동일선상의 한계(백테스트 없음, 유동성 낮음)를 이 프로젝트만의 개별 약점처럼 과장하지 말 것 — FedWatch 원본도 동일한 한계를 가짐.
6. 커밋 메시지 접두어: `[claude]` / `[antigravity]`.
