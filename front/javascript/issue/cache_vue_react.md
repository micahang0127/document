

## [cache issue]

#### [현상]()  
vue나 react 프로젝트에서 배포 시, css나 javascript 의 cache 관련 에러가 발생한다. 

<br/>

#### [error]()
Uncaught SyntaxError: Unexpected token '<'

or 

chunk


<br/>

#### [해결]()  <br/>

  배포 시 마다 캐시가 먹지 않도록 파일명을 변하게 하거나, 캐시를 저장 하지 않은 설정을 해 준다. <br/>
  
  1) CSS file
     ```
       [public/index.html]
       <link rel="stylesheet" href="<%= BASE_URL %>css/style.css?ver=2022-01-25" id="style">

       // 파일명 뒤에 날짜등의 문자열로 파일명을 바꿔준다. 
      
     ```

     <br/>
     
  2) JS file <br/>
  
     2-1) 배포 시 마다 파일명을 변경하는 설정을 해 준다. (vue project의 경우 vue.config.js 파일에 설정) <br/>
     
         ```
           // [vue project의 경우 vue.config.js 파일에 설정]
           module.exports = {
            filenameHashing: true,
            configureWebpack: {
              output: {
                filename: 'js/[name].[hash].js',
                chunkFilename: 'js/[name].[hash].js'
              },
            },
             ...
          }

         ```


     2-2) 2-1을 처리해도 가끔 프로젝트 내의 .js 파일이 아닌, 실행하는 브라우저에서 생성한 .js 파일이 캐시가 먹어 실행이 제대로 안 되는 경우가 발생  <br/>
          그럴 경우, 앞으로 아예 캐시를 저장하지 않겠다는 설정으로 넣어 해결.  <br/>
          하지만 그리 추천하지 않는 해결방법.  <br/>
  
         ```
           [public/index.html]
           <meta http-equiv="Cache-Control" content="no-cache">
         
         ```

