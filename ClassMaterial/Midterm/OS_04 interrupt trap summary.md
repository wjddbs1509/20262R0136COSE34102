# OS_04 interrupt trap summary

## 목차

- Trap and interrupt summary
  - Trap: 실행 중인 A의 명령이 원인(시스템 콜), 처리 후 A로 복귀
  - Interrupt: A와 무관한 장치·타이머가 원인, B로 context switch 가능
  - 원인에 따라 trap/interrupt 구분, 공통적으로 상태 저장·복원
- For question; cost comparison
  - Mode switch: 유저 ↔ 커널 모드 전환 (커널 진입·복귀 시)
  - Context switch: CPU에서 실행할 프로세스 교체, 주소 공간·캐시 영향으로 더 비쌈
  - 총 비용 = 전환당 비용 × 빈도
