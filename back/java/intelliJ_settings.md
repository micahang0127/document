

## IntelliJ 초기 설정

#### [tool 전체]()
1. JDK 설정
   1) defualt jdk 설정
   2) 설치
      - lombock
     
   
#### [특정 project 가 있을 경우]()

<br/>

1. JDK 설정
   프로젝트에서 사용 할 jdk 설정
    

<br/>


2. Modules 설정 
   file -> Project Structure -> Modules -> sources, tests, resource등 맞게 설정
   
    ```
      ex> 
      * Source Folders
        src/main/java
        target/generated-sources/annotations
        target/generated-sources/java
    
      * Test Source Folders
        src/test/java
        target/generated-test-sources/test-annotations

      * Resource Folders
        src/main/resources

      * Tst Resource Folders
        src/test/resources

      * Excluded Folders
        target
    ```


<br/>


3. VM options 설정
   1) 우측상단 프로젝트 select 선택 (재생버튼 왼쪽) -> Edit Configurations 선택
   2) Build and run -> 사용할 java 선택/확인
   3) modify options -> Add VM options -> 하면  Build and run 오른쪽에 입력 창 새로 생김 -> 직접 설정한 값으로 입력
   -> Apply -> OK


<br/>


3. 프로젝트 첫 실행
   프로젝트 파일 부분에서 root 파일 (ex> ~~Application.java)
   -> public static void main(String[] args) { ... } 함수(옆에 나와있는)에서 재생 버튼 눌러야 함












