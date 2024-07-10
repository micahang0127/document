
## [Jenkins 설치(in Docker)]()


1. docker 설치  <br/>
    : 필요에 따라 AWS EC2 or GCP VM instance에 docker를 설치한다. 

<br/>

2. jenkins 이미지 다운로드 - in docker
    
    1) 다운로드(설치)
    
        ```
        $ docker pull jenkins/jenkins:lts
        
        or
        
        $ docker pull jenkins/jenkins:jdk11
        
        //   참고) jenkins:lts 는 jdk8로 실행이 된다. 
        //   자바11을 상용한다면 jdk11 로 실행하는 이미지를 받아야 한다. 
        ```
    
    
    2) 다운로드 된 이미지 확인
    
        ```
        $ docker images
        ```


<br/>

3. jenkins 이미지를 컨테이너로 실행
   
    1) jenkins 이미지 실행
        
            $ docker run -d -p 9090:8080 -v /var/jenkins_home --name jenkins -u root jenkins/jenkins:jdk11
            
            /*
            
            [위 명령어 옵션설명]
            
            -d	detached mode 흔히 말하는 백그라운드 모드
            -p	호스트와 컨테이너의 포트를 연결 (포워딩)
                컨테이너 외부와 통신할 port(9090)와 내부적으로 사용할 port(8080)를 지정해 포워딩할 수 있다. 
                9090 port로 접속하기 위해 설정
            -v	호스트와 컨테이너의 디렉토리를 연결 (마운트)
            –name	컨테이너 이름 설정
            -u 실행할 사용자 지정
            
            맨 마지막 jenkins/jenkins:jdk11 는 실행할 이미지의 레포지토리 이름이며 만약 이미지가 없을 경우 이미지를 docker hub 에서 땡겨오므로 주의한다
            
            */
    
    
    2) 컨테이너 실행 후 확인
      
        ```
        $ docker container ps
        ```

    3) 이후부터는 생성된 컨테이너를 바로 실행시키면 된다.
    
        ```
        $ docker start jenkins
        ```

<br/>

4. Jenkins 접속 <br/>
   
    : web에서 jenkins에 접속한다. <br/>
    > instance ip :
    



<br/><br/><br/>

[작성일] : 24.01.16
