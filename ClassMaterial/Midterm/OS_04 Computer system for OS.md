# OS_04 Computer system for OS

## 목차

- Computer system
  - Computer system components
    - Processor, Memory, IO devices
  - Computer system with bus
    - 초기엔 단일 버스, 속도 차이 커지며 병목 발생
  - What is bottleneck
    - 느린 장치가 전체 속도를 제한 (CPU > Memory >> I/O)
  - How can the bottleneck be solved?
    - 비슷한 속도 장치끼리 묶는 계층적 버스
  - Example: system bus and IO bus
    - System bus(CPU, 메모리) + IO bus(IO 장치) + bridge
  - What is an instruction?
    - CPU 작업의 최소 단위, ISA, 프로그램 = 명령어 나열
  - How a program runs
    - 저장소 → 메모리 적재 후 Fetch → Decode → Execute 반복, PC = 다음 명령 주소
  - CPU execution modes
    - 시스템 보호를 위한 커널 모드 / 유저 모드 구분
- Event handling mechanisms
  - CPU event processing techniques
    - 동기 이벤트 = trap(시스템 콜, 예외) / 비동기 이벤트 = interrupt(IO 완료)
  - Trap processing
    - PC·레지스터 저장 → 커널 모드로 trap handler → 같은 프로세스로 복귀 (SW interrupt)
  - Interrupt handling
    - 실행 중 프로세스와 무관한 HW(타이머, NIC)가 발생 → ISR 실행 → 다른 프로세스로 복귀 가능 (HW interrupt)
  - Interrupt handling (Note)
    - 장치별 우선순위, ISR은 짧아야 함, 타임셰어링도 인터럽트로 가능
