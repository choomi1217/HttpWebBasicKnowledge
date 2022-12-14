# HTTP 메소드의 속성

- 안전(Safe Method)
- 멱등(Idempotent Method)
- 캐시(Cacheable Method)

### 안전
- 호출해도 리소스를 변경하지 않는다.
- GET 처럼 보여주기만 하는 메소드는 안전

### 멱등
- 한 번 호출을 하던 여러번 호출을 하던 결과가 똑같다.
- 멱등 메소드
  - GET    : 여러번 조회 해도 같은 값
  - PUT    : 결과를 대체하므로 여러번 해도 최종 결과가 같음
  - DELETE : 결과를 삭제하므로 여러번 해도 삭제라는 결과가 나옴
- 멱등 하지 않은 메소드
  - POST
    - 두번 호출하면 결제가 중복 발생함! 
- 멱등이 필요한 이유
  - 자동 복구 매커니즘
    - DELETE를 시도 했는데 서버 에러로 인해 중단 되어도 다시 요청할 수 있음.
      - 몇번을 시도 해도 같은 결과가 나올거란 보장을 해주기 때문.

### 캐시
- 응답 결과를 웹브라우저 내부에 캐싱 해두고 사용함.
- GET, HEAD 정도만 캐시가 가능함

