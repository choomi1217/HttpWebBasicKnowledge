# HTTP 메소드 - PUT, PATCH, DELETE

### PUT
- 리소스를 대체
- 리소스가 없으면 생성 ( 완전히 대체함 )
- 클라이언트가 구체적인 리소스 경로를 알고 있음 ( 리소스를 식별할 줄 앎 )
  - POST : /members
  - PUT  : /members/100
- 리소스의 부분만 변경할 수 없음 ( 수정의 용도가 아님 )


### PATCH
- 리소스의 부분만 변경함
  - PATCH : /members/100
- PATCH를 지원하지 않는 서버도 있음
  - POST 쓰면 됨

### DELETE
- 리소스 제거
  - DELETE : /members/100
