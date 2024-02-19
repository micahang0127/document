
<br/>

### [[gitLab or github]]
  1) 내 프로필 클릭
  2) access token 클릭
  3) access token 발급


<br/><br/>

### [[로컬 프로젝트에 생성한 git 계정(+access token) 적용 - (by Fork tool)]]
  * [새로운 계정 등록] <br/>
      1) 상단 메뉴 Fork -> Accounts -> + 버튼으로 gitlab 계정 등록(=Login) <br/>
      2) Personal Access Token에 위에서 생성한 access token 입력 <br/>
      ----<br/>
      3) project clone : 연결된 계정에서 Repositories 에서 사용할 프로젝트 clone<br/>
<br/><br/>

  * [access token 수정] <br/>
  : 만료된 토큰 등의 사유로 계정 defined 가 있을 경우, acccess token을 새로 발급하여 수정한다. <br/><br/>
    1) 위와 같이 + 버튼으로 새로운 계정 생성<br/>
    
    [ISSUE]
      문제) 새로 update한 계정이 정상적으로 연결 되었음에도(status: Online) 로컬 프로젝트에서 연결이 불가한 경우 
      해결) 연결이 오류 났던 기존계정은 꼭 삭제 해주어야 한다. 삭제는 - 버튼으로 한다. 


