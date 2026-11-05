# OS_07 IPC

## 목차

- IPC models
  - Interprocess communication
    - 메모리 보호 때문에 프로세스 간 협력은 커널이 제공하는 IPC로
  - Two IPC models
    - Shared memory / Message passing
  - Shared memory
    - 커널이 공유 영역만 만들고, 통신은 프로세스가 직접 읽고 씀 → 동시 수정 시 불일치
  - Message passing
    - send/receive로 커널을 거쳐 메시지 복사, 불일치는 커널이 처리
  - Comparison
    - Shared memory: 동기화는 사용자 책임 / Message passing: 커널이 처리
- Examples of message passing IPCs
  - Signal
    - 미리 정의된 이벤트를 비동기로 전달, 수신자가 스케줄될 때 처리
    - 수신 처리: Ignore, Block, Handle
  - Pipe
    - 단방향·1:1, 순서 보장, 커널 버퍼에 저장
  - Message queue (MQ)
    - 고정 크기 큐(우편함), 메시지 단위 통신, 커널에 존재
  - Socket
    - 통신 끝점, 다른 머신과도 통신 가능
  - Socket address: port & IP
    - IP = 머신, Port = 머신 내 ID, 신뢰(TCP) / 비신뢰(UDP) 연결
- IPC APIs
  - Shared memory setup
    - 이름으로 공유 메모리 객체 생성·열기 → 크기 설정 → 주소 공간에 매핑 → 읽기·쓰기 → 제거
