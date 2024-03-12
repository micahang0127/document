
## [JDK1.8 설치 - Mac]

1.  Open JDK인 Azul Zulu에서 설치  <br/>
 설치 참고 : https://techblog-hyunjun.tistory.com/4  <br/><br/>
   
   ```
     다운로드 : https://www.azul.com/downloads/?package=jdk#download-openjdk%EF%BB%BF  
     java version : Java 8 (LTS) 
     operating system : macOS   
     architecture : ARM 64-bit 
     java package : JDK       
     download : .dmg

   ```

<br/>

2. 설치 확인    <br/>
참고 : https://techblog-hyunjun.tistory.com/4      <br/><br/>
  
    1) 터미널.app 열기    <br/>
    2) java 확인        <br/>
  
        ```
          $ java -version # 자바 버전 확인
  
          $ javac -version # 자바 컴파일러 버전 확인
  
          $ /usr/libexec/java_home -V  # 설치된 모든 JDK 버전, 배급사, 설치폴더 확인
          
        ```

    <br/>
    
    3) 환경변수등록      <br/>
  
        1) shell확인    <br/>
        
          ```
            $ echo $SHELL    # 현재 shell 확인  
          ```

         2) 위 명령어로 나오는 위치에 따라 환경변수 처리 (zsh or bash)     <br/>

          ```
            export JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-8.jdk/Contents/Home
            export PATH=${PATH}:$JAVA_HOME/bin
          ```

        3) 환경 변수 적용        <br/>
        
          ```
            source ~/.bash_profile
    
            or
            
            source ~/.zshrc
          ```

          
<br/><br/>

  => 현재까지 과정 정리    <br/>
  ```
    자신의 운영체제에 맞는 해당 버전의 JDK 설치
    /usr/libexec/java_home -V (설치된 JDK 리스트 확인)
    .bash_profile, .zshrc 2개의 파일을 새로운 버전 파일의 경로로 변경
    source로 .bash_profile, .zshrc 적용
    최종적으로 java -version, javac -version으로 확인
  ```


<br/><br/>

  
  3. intelliJ에서 jdk 추가       <br/>
    참고 : https://covenant.tistory.com/276
  
      3-1) Project Structure 설정      <br/>
      
          file -> project structure -> project  
          -> SDK : Add SDK -> 1.8 (or 원하는 버전 선택) -> Apply
        
      
      

