

## [cache issue]

### [현상]  
vue나 react 프로젝트에서 배포 시, css나 javascript 의 cache 관련 에러가 발생한다. 

<br/>

### [error]
Uncaught SyntaxError: Unexpected token '<'

or 

chunk


<br/>

### [해결] <br/>

  배포 시 마다 캐시가 먹지 않도록 파일명을 변하게 하거나, 캐시를 저장 하지 않은 설정을 해 준다. <br/>
  
  1) CSS file
     ```
       [public/index.html]
       <link rel="stylesheet" href="<%= BASE_URL %>css/style.css?ver=2022-01-25" id="style">

       // 파일명 뒤에 날짜등의 문자열로 파일명을 바꿔준다. 
      
     ```

     <br/>
     
  2) JS file
     2-1) vue project의 경우 vue.config.js 파일에 배포 시 마다 파일명을 변경하는 설정을 해 준다. 

