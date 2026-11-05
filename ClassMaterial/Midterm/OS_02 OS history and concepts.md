# OS_02 OS history and concepts

## 목차

- Batch System
  - Mainframe
    - 외부에 저장된 프로그램 실행, OS의 시작
  - OS technique for mainframe: Batch
    - 제출 순서대로 실행, 시작 후 개입 불가
  - Batch challenge: I/O in the middle of job
    - I/O 대기 중 CPU idle 발생
  - Spooling
    - 버퍼를 두어 I/O와 계산을 동시에 수행
  - Spooling problem
    - 비동기 I/O만 가능, 동기 I/O는 여전히 CPU idle
- Multiprogramming
  - Multiprogramming
    - 여러 프로그램을 메모리에 적재, I/O 시 다음 프로그램 실행 → CPU 이용률 증가
  - Multiprogramming problem
    - I/O 안 하는 작업이 CPU 독점 → 공정성 문제
- Timesharing
  - Time sharing
    - CPU 시간을 timeslice로 나눠 시간이 끝나면 선점(preempt)
    - Context switch 시 프로그램 상태(레지스터, PC) 저장·복원
  - Concurrent execution
    - 여러 프로그램이 동시에 실행 중인 것처럼 보임 (단일 코어는 실제 동시 실행 X)
  - Simple summary
    - Multiprogramming: 이용률↑ 공정성↓ / Timesharing: 공정성·응답성↑ 전환 오버헤드
- Multitasking
  - Other terminologies
    - Multitasking: 여러 프로그램이 자원 공유 / Multiplexing: 제한된 자원을 여럿이 사용
  - Other systems
    - 멀티프로세서, 분산, 클러스터, 임베디드, 실시간 시스템
  - Topics to cover in this course
    - 프로세스/CPU 스케줄링, 동기화, 메모리 관리, I/O 시스템
- Lineage of well-known operating systems
  - Is the OS improvement done?
    - 새 HW·앱·시스템 구조(가상화 등)로 OS는 계속 발전 중
  - Linux vs Linux Kernel
    - 배포판 = 커널 + 라이브러리, 툴체인, GUI 등
