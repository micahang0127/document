### Reactjs


[library]
* common
  - React : <br>
    Javascript Web Front-End Rendering 라이브러리 중 하나<br>
    프레임워크가 아닌 라이브러리. 즉, View를 Rendering 하는 것이 주 기능. <br>
    나머지 기타 기능들(router, ajax등등)은 서드파티 라이브러리를 추가적으로 사용해야 한다.
 
 
* 상태관리 - (여러 컴포넌트 간 데이터를 공유하는 방법)
  - Redux : <br>
    Flux개념을 바탕으로한 React에서 현재 가장 많이 사용되는 State 관리 라이브러리 <br>
    action타입정의, action생성, reducer생성 으로 번잡스럽고 보일러플레이트 코드가 커질 수 있음
    
   - Mobx : <br>
    redux와 같은 State관리 라이브러리. <br>
    @observable 데코레이터로 지정한 State는 관찰대상으로 지정되고 그 State는 값이 변경될 때 마다 Rerendering된다.<br>
    
   - Recoil : <br>
    React에서 제공하는 상태 관리 라이브러리. 상대적으로 가벼운 편이고 리렌더링 이슈를 피할 수 있다는 장점이 있다. 허나 아직 안정적인 devtool이 없어 디버깅에서 약하다.
    
    
* Error <br>
  - Sentry : 오류를 탐지하기 위한 프론트엔드 모니터링 툴. ex>카카오페이에서 사용<br>
