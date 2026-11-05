# OS_03 OS structure part 1

## 목차

- OS Design
  - Why does design matter for OS?
    - OS는 크고 복잡해서 좋은 설계가 개발·수정·유지보수를 쉽게 함
  - Design goals
    - 공정성, 실시간, 성능, 확장성, 안정성, 보안, 사용성, 호환성, 에너지 등
  - How to achieve various goals?
    - 목표 간 trade-off (예: 공정성 vs 성능)
  - General- and Special purpose- OS
    - GPOS: 여러 목표를 고르게 / SPOS: 특정 용도 목표
  - OS design principle
    - Policy = 무엇을(설계), Mechanism = 어떻게(구현), 분리해서 복잡도↓
  - OS structure: Layering
    - 인접 계층과만 통신, 복잡도↓ 오버헤드↑
  - OS structure: Modularity
    - 여러 모듈과 연결 가능, 성능↑ 복잡도↑
- How user applications call OS services?
  - CPU execution mode
    - 자원 보호를 위해 모드별 권한 설정, 높은 권한 필요 명령 = privileged instruction
  - OS: User mode and Kernel mode
    - Kernel mode: 전체 권한 / User mode: 특권 명령 불가, 전환 = mode switch
  - System call
    - User mode → kernel mode 진입 통로, 보통 API(라이브러리)로 호출
  - System call - sequence
    - API 호출 → system call interface → system call table → 구현 → return
  - System call: parameter passing
    - 레지스터에 저장(빠름, 개수 제한) 또는 메모리 주소·길이 전달
  - System call handler
    - 번호 확인 → 핸들러 실행 → 파라미터 확인 → 수행(copy vs zero-copy) → 결과 반환
  - POSIX APIs
    - OS 인터페이스 표준, 응용 이식성 목적
