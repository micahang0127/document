
  * grapql
    GraphQL은 Facebook에서 개발한 쿼리 언어
    
    <br>
    * Apollo Client with React
      Apollo Client는 이해하기 쉽고 유연하며 강력한 GraphQL 클라이언트를 구축하기 위한 커뮤니티 중심 라이브러리<br>
      GraphQL 쿼리를 작성하기만하면 Apollo Client가 데이터를 요청하고 캐싱하고 UI까지 업데이트 <br>
      Apollo Client는 React, Angular, VUE, Ember 등 다양한 플랫폼을 지원한다 <br>
      

      ```
      $ npm install @apollo/client graphql
      ```


      - InMemoryCache <br>
          apollo client 는 gql 의 결과를 InMemoryCache 에 저장하며, 이를 통해 클라이언트는 불필요한 네트워크 요청 없이 동일한 데이터에 대해 요청할 수 있다. <br>
      <br>

      - [useQuery] <br>
          useQuery는 컴포넌트가 Mount, Render 될 때, apollo client가 자동으로 실행됨 <br>
          useQuery는 콜백함수 안에서 사용할 수 없다 <br>
          
      - [useLazyQuery] <br>
          클릭같은 이벤트 발생시 사용 <br>
          
      - [useMutation] <br>
         

