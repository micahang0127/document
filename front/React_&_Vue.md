### Vue2.x & Vue3.x. & React

<br />
* 공통점 <br />
  SPA (Single Page Application) <br>
  정적 리소스를 최초에만 로드하고 이후 새로운 페이지 요청을 받을 때 새로고침 없이 갱신에 필요한 데이터만 받아와서 갱신하는 방식이다.
  <br><br>  
  Virtual DOM 렌더링 <br>
  실제 DOM을 조작하지 않고 가상 DOM으로 html을 렌더링하기 때문에 브러우저의 렌더링 횟수가 줄어들고, pc자원 소모를 감소할 수 있다.
  <br />
  
<hr/>
* 차이점 <br />
  Vue 2.x : <br> 
  - 러닝커브가 낮아 학습이 용이하고 생산성이 뛰어나다<br />
  <br>
  Vue 3.x : <br>
  - wrapper div 제거 => style적용에 용이히짐 
  <br>
  
   ```javascript
   <template>
     <div>
       // Vue2.x에서는 template 하위 전체를 감싸는 div 필요
     </div>
    </template>
   ```
  <br>
  - 기존 data, method 선언 => setup 메소드 사용 <br>
 
 ```javascript
     // Vue2.x
    export default {
      props: {
        title: String
      },
      data () {
        return {
          test: '',
          sample: ''
        }
      },
      methods: {
        sendTest () {
          // sendTest method
        }
      }
    }
 ```
  
  ```javascript
     // Vue 3.x
    export default {
      props: {
        title: String
      },
      setup () {
        const state = reactive({
          test: '',
          sample: ''
        })
    
        const sendTest = () => {
          // sendTest method
        }
        return { 
          sendTest,
          state
        }
      }
    }
  ```
  <br>
  - Composition API <br>
  Vue2.x 버전에서는 코드 재사용으로 믹스인(Mixin)이나 슬롯(slots) 등오로 코드를 재사용 했다. 하지만 믹스인 한계점이 있었다. 프로젝트가 커지고 믹스인을 다중으로 사용하게 되면 속성들이 병합 될때 충돌이 발생할 수 있고 네이밍에 대한 명확한 컨벤션이 필요했다.  또한 매개변수를 믹스인을 통해 전달할 수 없어 코드 재사용 시 유연성이 떨어졌다. <br>
컴포지션 API 는 로직을 유연하게 구성할 수 있도록 하는 함수기반의 API이다. 코드의 재사용성과 타입 추론(타입스크립트)가 크게 개선되었다고 한다. 리액스의 Hooks와 유사한 느낌을 받을수 있다. 
<br>
  
  ```javascript
  // Vue 2.x
  // books에 관련된 코드들이 분산되어 추적이 어렵다.
  export default {
  data() {
    return {
      books: []
    };
  },
  methods: {
    addBook(title, author) {
      this.books.push({ title, author });
    }
  },
  computed: {
    formattedBooks() {
      return this.books.map(book => `${book.title}은 ${book.author}가 썻다`);
    }
  }
};
  ```
  
  ```javascript
  // Vue 3.x
  // setup 내부에 data와 function을 구성한다.
  // ref, reactive, watchEffect 등 사용.
  <script>
  import { ref, reactive } from "vue";

  export default {
    name: "HOME",
    setup() {
      // 데이터를 ref, reactive로 감싸면 반응형으로 바뀐다
      const person1 = ref({ name: "nkh", age: 29 });
      const person2 = reactive({ name: "nki", age: 26 });

      const handleClick = () => {
        // ref로 감싼 값을 변경할 때는 value로 한번 들어가주고 값을 바꾼다
        person1.value.age = 30;

        // reactive는 바로 값을 바꾼다
        person2.age = 30;
      };

      // ref값은 return을 거치게되면 person1.value.age는 person1.age로 바꾼다 (template에서는 person1.age로 사용)
      return { person1, handleClick };
    }
  };
  </script>
  ```
  
  <br>
  - IE 지원을 하지 않는다. 
  <br>
  React : 
  - 상대적으로 자유도가 높고 개발자의 역량에 따라 영향을 미친다.
  - vue는 프레임워크, react는 라이브러리 이다. <br>
    프레임워크는 어느정도의 필요한 것들을 갖추고 있는 느낌이라면, 라이브러리는 최소한의 기능에서 다른 라이브러리들을 추가해 사용하는데 초점을 맞출수 있다.
   - JSX를 사용한다

    프레임워크는 어느정도의 필요한 것들을 갖추고 있는 느낌이라면, 라이브러리는 최소한의 기능에서 다른 라이브러리들을 추가해 사용하는데 초점을 맞출수 있다.



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


