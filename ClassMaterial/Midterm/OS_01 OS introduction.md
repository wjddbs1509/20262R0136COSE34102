# OS_01 OS introduction

## 목차

- What is it?
  - What is OS?
    - HW와 함께 탄생, 정의 범위는 계속 확장
  - Why OS?
    - 다양한 HW를 쉽게 쓰게 하고 자원을 효율적으로 할당·관리
  - Definition
    - HW 숨김 + 추상화 제공 + 정책 결정 + 메커니즘 구현
  - Studying OS means
    - OS = 추상화 + 정책 + 메커니즘, 암기보다 연관 이해
  - Abstraction: process
    - 실행 중인 프로그램
  - Abstraction: address space
    - 프로세스별 독립 메모리 공간 (보호), file = 영구 저장소
  - Abstraction: socket
    - 컴퓨터 간 통신 끝점
  - SW types (at high level)
    - 시스템 SW vs 응용 SW
  - OS features (compared to applications)
    - 커널 모드로 HW 직접 제어, 앱은 불가
  - Notations: OS and Kernel
    - 수업에서는 OS == 커널
  - Relations of Hardware, OS, and Application
    - App(+Library) → OS → HW
