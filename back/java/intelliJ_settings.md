

## IntelliJ 초기 설정

#### [tool 전체]()
1. JDK 설정
   1) defualt jdk 설정
   2) 설치
      - lombock
     
   
#### [특정 project 가 있을 경우]()

1. JDK 설정
   프로젝트에서 사용 할 jdk 설정
    

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
   

