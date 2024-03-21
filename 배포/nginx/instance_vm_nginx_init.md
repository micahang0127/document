
### [ec2(외 서버) front 배포]

<br/>

folder simbol <br/>

** nginx <br/>

1. 설치 <br/>
  ```
  $ sudo apt install nginx
  ```
  -> 설치 완료 시 /etc 폴더에 nginx 폴더 생김 ex> /etc/nginx

<br/><br/>

2. site_available, site-enabled <br/>

   1) 폴더 생성  (있으면 생략) <br/>
   
      ```
      $ sudo mkdir /etc/nginx/site-available
      $ sudo mkdir /etc/nginx/site-enabled
      ```
      
    2) conf 파일 생성 (있으면 생략) <br/>
    
      ```
          site-available/default         
          site-enabled           
      ```
      => site-available/default 와 심볼릭 링크 걸어준다.         <br/>
      그러면 site-available/default 파일이 변경 될 때, site-enabled/default 도 같이 변경 반영 된다.  <br/>
     
        $ sudo ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/default
        $ sudo nginx -t      // test 해보기
   
     => nginx/conf.d 파일에 해당 내용 있는지 확인     <br/>
      ```
       $ include /etc/nginx/modules-enabled/*.conf;   
      ```



 <br/> <br/> <br/> <br/>
 

  * nginx 실행에 문제없는지 테스트   <br/>
  
    ```
	  $ sudo nginx -t
    ```
    
	  결과) 아래와 같이 나오는지 확인   <br/>
   
     ```
    nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
    nginx: configuration file /etc/nginx/nginx.conf test is successful
     ```

 <br/> <br/>
 

  * nginx 설정 에러  <br/>

    error)  <br/>
      ```
       pam_unix(sshd:auth): check pass; user unknown 
      ```



 <br/> <br/>



  * 권한 관련 이슈  <br/>
    ```
      sudo chmod -R 777 /var/www
      되돌려놓기
      sudo chmod -R 755 /var/www
      sudo chmod -R 755 /var/www/ems
    ```


