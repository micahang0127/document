## [Jenkins Item 구성 - ver.Front]()

1. jenkins 접속 및 로그인 <br/> 
2. Item 생성 <br/>
     1) (좌메뉴) 새로운 Item 클릭  <br/>
     2) <b>name</b> 입력 →  <b>Freestyle project</b> 클릭 → OK 클릭 <br/>



3. 구성 
    
      1) <b>General</b>
           - 설명 입력  <br/>
           <b> [메모리 용량 확보를 위한 오래된 빌드 삭제] </b>  <br/>
           
           - 오래된 빌드 삭제 check  <br/>
               : 보관할 최대갯수
               > ex> 3  <br/>


      
      2) 소스 코드 관리  <br/>
           <b> [Gitlab-Jenkins 연동 - gitlab repository의 프로젝트 코드 jenkins로 가져옴] </b> <br/>
           - Git <br/>
               : Repository URL ⇒ <연동할 gitlab repository URL> 입력  <br/>
           - Credentials <br/>
               : 해당 git repository 접속인증 되어있는 git 계정 선택 <br/>
            - Branches to build <br/>
               : 가져올 프로젝트(코드)의 branch 입력
               > ex>  * /pre-production
               > 
   <br/>
      
     3) 빌드 유발 <br/>
      
      
     4) 빌드 환경 <br/>
      
        : 해당하는(프로젝트(코드)에 지원되는) NodeJS version 선택 <br/>
    
       

     5) Build Steps - 빌드(코드가져오기) 후 처리 할 거 <br/>
     
        - Add build step → Execute shell 클릭 <br/>
        - Command 에 빌드 후 처리해 줄 명령어 입력       <br/>
  
        ```
        입력예시> 
        
        1) 기본
        npm install
        CI=false npm run build
        
        2) sass 사용 시 or 프로젝트 내용에 맞게 명령문 실행
        npm install
        npm install sass
        CI=false npm run build
        
        => 추가설명)
        CI=false
        리액트는 CI라는 환경 변수가 기본적으로 true로 되어있는데,리액트의 경고를 빌드 오류로 처리한다는 것임.
        즉, CI=false 로 해주지 않으면 경고(warn)에도 빌드가 실패함.
        ```

      6) 빌드 후 조치 <br/>

      - 빌드 후조치 추가 → Send build artifacts over SSH 클릭 <br/>
      - SSH Server : 해당하는 SSH server 선택 <br/>
      - <b>Transfers </b> <br/>
      
            ex> 입력예시
            Source files : build/**
            Remove prefix : build
            Remote directory (빌드된 프로젝트 코드를 올릴 instance 내 폴더 경로)  
              : deploy/front/target/<project folder name>
    
            Exec command (실행할 shell 파일 - instance 내 경로 포함)
              : deploy/front/deploy_front_<project folder name>.sh
        

     7) 저장

    8) 완료


<br/><br/><br/>
  
[작성일] : 24.01.16
