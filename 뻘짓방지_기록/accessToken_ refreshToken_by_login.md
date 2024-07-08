

## 로그인 처리 시 accessToken, refreshToken <br/>

```
  [!] login 시 (accessToken,refreshToken 발행) session(브라우저에 token을 저장하는 곳)에 accessToken은 물론,
      refreshToken도 함께 저장해주어야 한다.
  
  [이유] accessToken이 만료되었을 때, front에서 다시 refreshToken을 요청하는 api 를 request 한다.     
        이를 위해 login 시 (accessToken,refreshToken 발행) session(브라우저에 token을 저장하는 곳)에 accessToken은 물론,
        refreshToken도 함께 저장해주어야 한다.     
        그래야 api 로 refreshToken 요청을 할 때,
        client쪽 headers에 refreshToken을 넣어주고 refreshToken은 유효한지 체크할 수 있기 때문.
```
