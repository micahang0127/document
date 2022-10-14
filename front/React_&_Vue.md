### Vue2.x & Vue3.x. & React

<br />
* 공통점 <br />
  **SPA (Single Page Application)** <br />
  정적 리소스를 최초에만 로드하고 이후 새로운 페이지 요청을 받을 때 새로고침 없이 갱신에 필요한 데이터만 받아와서 갱신하는 방식이다.
       
**  Virtual DOM 렌더링**<br />
  실제 DOM을 조작하지 않고 가상 DOM으로 html을 렌더링하기 때문에 브러우저의 렌더링 횟수가 줄어들고, pc자원 소모를 감소할 수 있다.
  <br />

<br />
* 차이점 <br />
  Vue 2.x : 러닝커브가 낮아 학습이 용이하고 생산성이 뛰어나다<br />
  Vue 3.x : 기존 data, computed를 사용하는 방식 -> setup 을 통해 
            IE 지원을 하지 않는다.
  R : 상대적으로 자유도가 높고 개발자의 역량에 따라 영향이 높다



* 프로세스에 익숙해지기 까지의 러닝 커브

V: react에 비해 러닝커브가 낮다. 즉 더 쉽다.


* 속도
V: 렌더링 하는 시간이 더 빠르다.

* UI라리브러리 
R : Material UI (MUI)
V :  Vuetify, Quasar

* CSS
R: react의 경우 css in js  방식으로 styled components 라이브러리를 사용할 수 있다. 
V: 퍼블리셔와 협업에는 jsx을 사용하는 리액트 보다는 뷰를 사용하는데 작업에 더욱 용이하다

* Typescript 에 대한 자유도
V 2.x : 타입 스크립트 지원이 완벽하지 않다. 
           props의 경우 타입스트립트로 정의한 타입을 사용 할수 없다. 
V 3.x : 2.x 대 버전보다 원활애 졌다. 하지만 좀 더 안정화가 필요하다


