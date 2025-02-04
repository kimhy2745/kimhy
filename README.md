[리눅스 프로세스 관리 명령어]
---------------------------------------------------------------
#1. top
 : 실시간으로 시스템의 프로세스와 메모리 사용 현황을 모니터링할 수 있는 명령어 
   CPU 사용률이 높은 프로세스 순으로 출력

- 옵션
  d : 화면 갱신 주기 설정
  p : 특정 PID만 모니터링
  u : 특정 사용자의 프로세스만 표시

- 출력 정보
  
  PID : 프로세스 ID
  USER : 프로세스 소유자
  PR : 우선순위
  NI : nice 값
  VIRT : 가상 메모리 사용량
  RES : 실제 메모리 사용량
  SHR : 공유 메모리 사용량
  S : 프로세스 상태 (S = 수면 / R = 실행 / Z = 좀비)
  %CPU : CPU 사용률
  %MEM : 메모리 사용률
  TIME+ : 누적 CPU 시간
  COMMAND : 실행된 명령어
---------------------------------------------------------------
#2. ps
 : 현재 실행 중인 프로세스의 스냅샷을 보여주는 명령어
   옵션을 통해 출력 형식 제어 가능

- 옵션

  e / -A : 모든 프로세스 표시
  f : 전체 형식(full format)으로 출력
  u : 특정 사용자의 프로세스 표시
  p : 특정 PID의 프로세스 표시
  aux : BSD 형식으로 모든 프로세스 표시

- 출력 정보

  PID : 프로세스 ID
  TTY : 터미널 타입
  TIME : 누적 CPU 시간
  CMD : 실행된 명령어
---------------------------------------------------------------
#3. jobs
 : 현재 쉘 세션에서 백그라운드로 실행 중인 작업을 보여줌

- 옵션

  l : 프로세스 ID와 함께 작업 표시
  n : 최근에 상태가 변경된 작업만 표시
  p : 각 작업의 프로세스 ID만 표시
  
- 출력 정보

  [N] : 작업 번호
  status : 작업 상태 (Running, Stopped ..)
  command : 실행된 명령어
---------------------------------------------------------------
4. kill
 : 특정 프로세스에 시그널을 보내는 명령어 주로
   주로 프로세스를 종료 시 사용

- 옵션

  l : 사용 가능한 시그널 목록 표시
  s : 시그널 이름을 지정
  9 : 강제 종료 시그널 (SIGKILL)
  15 : 정상 종료 시그널 (SIGTERM, 기본값)
  
- 시그널
  
  SIGTERM (15) : 프로세스를 정상 종료
  SIGKILL (9) : 프로세스를 즉시 강제 종료
  SIGHUP (1) : 프로세스를 재시작
---------------------------------------------------------------
  
