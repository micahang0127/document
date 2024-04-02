
# PHP Project local에서 실행하기 (in Mac)

<br/>

### [진행 모두 참고]
  아파치에서 실행 <br/>
  
  https://velog.io/@tkddnwkdb/PHP-%EC%8B%A4%ED%96%89%ED%99%98%EA%B2%BD-%EB%A7%8C%EB%93%A4%EA%B8%B0

<br/><br/>

### [결과 실행]

  * apache 서버 실행 목록 확인 <br/>
    
    ```
      $ brew services list

      // 모두 Status none 
    ```

<br/>

  * apache 서버 시작 <br/>
  
    -> 실행해보기 : 주소창에 http://localhost  <br/>
    
    ```
      $ brew services start httpd
    ```

<br/>

  * apache 서버 중지 <br/>
    
    ```
      $ brew services stop httpd
    ```

<br/>
