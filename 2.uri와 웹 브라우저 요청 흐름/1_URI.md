# URI ( Uniform Resource Identifier )

### 리소스를 식별하는 방법 (자원을 식별하는 방법)
- URI는 L(로케이터)와 N(이름)으로 분류될 수 있다
- URI (Identifier)
  - URL (Locator)
  - URN (Name)

- URL
  - foo://example.com:8042/over/there?name=ferret#nose
  - 웹 브라우저에 URL을 치면 그 장소에 리소스가 있을거야! 하는 것과 같음


| foo://  | example.com:8042 | /over/there | ?name=ferret | #nose    |
|--------|-------------------|-------------|--------------|----------|
| schema | authority         | path        | query        | fragment |


- URN
  - urn:example:animal:ferret:nose
  - 리소스에 이름만 부여하는 것

| urn: | example | :animal | :ferret | :nose    |
|--------|-------------------|---------|---------|----------|
| schema | authority         | path    | query   | fragment |


### URL
```
scheme://[userinfo@]host[:port][/path][?query][#fragment]
https://www.google.com:443/search?q=hello&hl=ko
```
- scheme
  - 주로 프로토콜 사용
    - 프로토콜 : 어떤 방식으로 자원에 접근할 것인가
      - http. https, ftp ...
- ~~userinfo~~
  - 안씀
- host
  - 도메인 혹은 ip
- port
- path
  - 리소스 경로
    - 계층적 구조임
- query
  - queryString
- fragment
  - html 내부에서 사용되는 용도