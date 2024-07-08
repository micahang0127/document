

## [배포]-[Error]


 [권한 에러]()
  ```

      [Error]
        * Failed to connect session for config []. Message [Auth fail for methods 'publickey
        * EC2 인스턴스에 액세스할 때 "Permission denied (publickey)" 또는 "Authentication failed, permission denied"
        * Uncaught SyntaxError: Unexpected token '<’ 오류 해결하기

      [해결]
        배포되는 상위 (거의 root)폴더에 권한 허용 해줘야 함 : chmod 755

  ```

