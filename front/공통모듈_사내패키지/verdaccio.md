

## verdaccio 
  : private npm package 저장소 


<br/>

  [[진행]()] <br/>
  ```
    1. 터미널에서 로컬에 verdaccio 설치
      $  sudo nom Install -g verdaccio
  ```
<br/>

  [[실행]()] <br/>
  ```

    * 실행
      $ verdaccio

    * 실행확인
      - 접속 : 기본포트 4873
      http://localhost:4873

  ```

<br/>

  [[라이브러리(공통모듈) 가져와 사용하기]()] <br/>
  ```

    [package.json]
     라이브러리 프로젝트를 가져와 사용 하는 프로젝트의 package.json파일에서,

    "publishConfig": {
      "registry": "http://localhost:4873"
    },

  ```

<br/><br/>

  [[Issue]()] <br/>

  1) [Error]  verdaccio 사용 뒤, 다른 프로젝트에서 npm install 할때 에러 <br/>
  ```

      [이슈]
         verdaccio로 localhost:4873 으로 어떤 프로젝트를 연동(업로드)하고 난 뒤,
        관련없는 다른 프로젝트에서 $ npm install 을 하면, 에러가 나면서 안됨

      [원인]
         npm 의 proxy 관련 에러

      [해결]
         일단 아래 명령어로 npm 관련 설정(config)을 npmjs 로 verdaccio 프로젝트 연동 전 초기 설정으로 바꿔주었다.
          $ npm config set registry “http://registry.npmjs.org/”
          — 임시방편으로 당장의 프로젝트 진행을 위한 reset 해결임.

         진짜 해결은 아래와 같이 proxy 설정으로 해결 해야 하는 듯 하나, 시도는 아직 안해 봄.
          $ npm config set proxy http://your-proxy-address:your-proxy-port
          $ npm config set https-proxy http://your-proxy-address:your-proxy-port

  ```



<br/><br/>
[참고] 
https://mygumi.tistory.com/371
