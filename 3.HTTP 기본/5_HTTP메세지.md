# HTTP 메세지

###### ~~SP : SPACE , CRLF : ENTER~~

- HTTP 메세지 구조
    - start-line (request-line / status-line)
      - request-line 
        - method(SP)request-target(SP)Http-version(CRLF)
    - header
    - empty line
    - message body

|    start line    |
|:----------------:|
|      **header**      |
| **empty line(CRLF)** |
|   **message body**   |



- 요청 메세지

| GET /search?q=hello&hl=ko HTTP/1.1 | **start-line** |
|:----------------------------------:|:----------:|
|        **Host: www.google.com**        |   **header**   |
|             **empty line**             | **empty line** |


- 응답 메세지

|                         HTTP/1.1 200 OK                          |  start-line  |
|:----------------------------------------------------------------:|:------------:|
| **Content-Type: text/html; charset=UTF-8 <br> Content-Length: 3423** |    **header**    |
|                            **empty line**                            |  **empty line**  |
|      **\<html> <br> \<body>...\</body> <br> \</html> <br> ...**      | **message body** |


### start-line (request-line / status-line)
- request-line
  - method(SP)request-target(SP)Http-version(CRLF)
    - method
      - GET, POST, PUT, DELETE ... 
      - 서버가 수행 해야하는 동작 지정
    - request-target
      - 절대경로 '/' 로 시작하는 경로
    - Http-version
- status-line
  - http-version(SP)status-code(SP)reason-phrase(CRLF)
    - http-version
    - status-code
      - 2xx, 3xx, 4xx, 5xx
    - reason-phrase
      - 사람이 이해 가능한 짧은 코드

### 
