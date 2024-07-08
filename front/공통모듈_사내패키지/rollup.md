
## Rollup 
  : ES6 모듈 형식으로 빌드 결과물을 생성할 수 있는 번들러 입니다. <br/>
    라이브러리나 패키지에 활용하기 유리합니다. <br/>
    트리쉐이킹이 가능하다는 특징을 가지고 있어 라이브러리에 가장 적합한 번들러이다. (웹팩은 ES6 모듈에서만 지원 가능) <br/>

<br/>

### React + Rollup

  ** [라이브러리 사용하기]() <br/>
  ```

    $ npm install --save git+https://gitlab.com/your-username/your-package.git

    ex>
        npm install --save git+https://gitlab.com/ems9560420/epikar-lib-react.git
        => 그럼 package.json 에 아래가 자동 설치 되고 아래와 같이 나타남
           "epikar-lib-react": "gitlab:ems9560420/epikar-lib-react",
  ```


<br/>


  ** [React + Rollup 구성하기]() <br/>

  
  [link 걸기] <br/>
  
  ```
     [사내패키지(library)로 쓸 프로젝트에서]
     $ yarn link

     [사내패키지(library)를 가져와 사용할 프로젝트에서]
     $ yarn link epikar-lib-react
  ```

  [배포] <br/>
  
  ```
    build 해야 반영됨.

    [package.json]
    “build": "rollup -c --bundleConfigAsCjs"
  ```


<br/>


  ** [Issue & 유의]() <br/>

  1) <br/>
  ```
      library project에서 내부파일 import 시, import 하는 파일의 확장자(.jsx .js)까지 적어주어야 함. 
      아니면 build 시 에러.

      [Error] Error: Could not load
  ```





