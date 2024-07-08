

## verdaccio

  [실행] <br/>
  ```

    * 실행
      $ verdaccio

    * 실행확인
      http://localhost:4873 접속

  ```

<br/>

  [라이브러리(공통모듈) 가져와 사용하기] <br/>
  ```

    [package.json]
     라이브러리 프로젝트를 가져와 사용 하는 프로젝트의 package.json파일에서,

    "publishConfig": {
      "registry": "http://localhost:4873"
    },

  ```
