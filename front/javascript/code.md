

### 연산자
* 논리 연산자( &&, ||, ?? )
  * && 연산자
    코드 예시: data && data.fetchprofile <br>
    코드 해석: 앞의 값이 참일 경우에만 뒤를 반환. 그 외의 경우는 앞을 반환<br>

    논리연산자는 데이터가 없을 경우 자동으로 undefined를 반환해 줌<br>
    data && data.fetchprofile의 경우 앞의 값(data)이 참일 경우에만 뒤의 값(data.fetchprofile)을 보여줌<br>

  * || 연산자
    코드 예시: data || data.fetchProfile<br>
    코드 해석: 앞의 값이 거짓일 경우에만 뒤를 반환. 그 외의 경우 앞을 반환<br>

  * ?? 연산자
    코드 예시: data ?? data.fetchProfile<br>
    코드 해석: 앞의 값이 빈 값이면 뒤의 값을 보여줌<br>
<br>

* 옵셔널 체이닝(Optional - Chaining) <br>
    기존의 논리 연산자를 쓰면서 길어졌던 코드를 더욱 간결하게 사용하는 연산자<br>
    코드 예시: data?.fetchprofile<br>
    코드 해석: ? 연산자 앞 객체의 참조가 undefined 또는 null 이라면 undefined를 리턴<br>
