
## Rollup 
  : ES6 모듈 형식으로 빌드 결과물을 생성할 수 있는 번들러 입니다. <br/>
    라이브러리나 패키지에 활용하기 유리합니다. <br/>
    트리쉐이킹이 가능하다는 특징을 가지고 있어 라이브러리에 가장 적합한 번들러이다. (웹팩은 ES6 모듈에서만 지원 가능) <br/>



### React + Rollup

  ** 라이브러리 사용하기 <br/>
  ```

    $ npm install --save git+https://gitlab.com/your-username/your-package.git

    ex>
        npm install --save git+https://gitlab.com/ems9560420/epikar-lib-react.git
        => 그럼 package.json 에 아래가 자동 설치 되고 아래와 같이 나타남
           "epikar-lib-react": "gitlab:ems9560420/epikar-lib-react",
  ```
