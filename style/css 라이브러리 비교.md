

## CSS 라이브러리 비교


### [SCSS]()
  : SCSS는 CSS의 문법을 확장하여 변수, 중첩, 믹스인 등 강력한 기능을 제공 <br/>
    &nbsp;&nbsp; 단점: SCSS 코드는 브라우저에서 바로 해석되지 않으므로 CSS로 컴파일하는 과정이 필요(빌드 시점에 처리) 
  
  <br/>
  
  EX1> 변수사용 가능
  
        [css]
        .container {
          width: 800px;
          margin: 0 auto;
        }


        [scss] 
        1) 변수 사용 가능
        $base-width: 800px;
 
        .container {
          width: $base-width;
          margin: 0 auto;
        }
    
  <br/>
  
  EX2> 중접구조 허용
  
        [css]
         .header h1 {
            font-size: 24px;
            color: #333;
          }
           
          .nav ul li a {
            color: white;
            text-decoration: none;
          }


        [scss] 
        .header {
          h1 {
            font-size: 24px;
            color: #333;
          }
        }
         
        .nav {
          ul {
            li {
              a {
                color: white;
                text-decoration: none;
              }
            }
          }
        }


<br/><br/>  

### [Tailwind CSS]()
  : Tailwind CSS는 다양한 스타일의 컴포넌트(예: 버튼, 카드, 컨테이너)를 미리 만들어 놓아져 있어, 정해진 클래스명을 기입하면 바로 적용시켜 사용할 수 있다. <br/>
    &nbsp;&nbsp; 장점: 개발 속도가 빠르고, 반응형 디자인에 대응하기 쉽다. 



<br/><br/>  

### [Styled Components  &  Emotion]() 
  : 둘 다 CSS-in-JS 라이브러리 <br/>
  &nbsp;&nbsp; 컴포넌트 상태에 따라 스타일을 유연하게 변경 할 수 있다. <br/>
  &nbsp;&nbsp; [단점] 런타임 오버헤드 - 스타일 계산이 런타임에 이루어지므로 성능에 영향을 줄 수 있습니다. <br/> <br/>
  &nbsp;&nbsp; emotion css는 styled Components와 다르게 인라인 스타일링도 가능. <br/>
  


  <br/>

  EX1> Styled Components

      import styled from 'styled-components';
 
      const Button = styled.button`
        background-color: #4CAF50; /* Green */
        border: none;
        color: white;
        padding: 15px 32px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
       
        &:hover {
          background-color: #3e8e41;
        }
      `;
       
      function App() {
        return (
          <div>
            <Button>Styled Components 버튼</Button>
          </div>
        );
      }


  <br/>

  EX2> Emotion

      /** @jsxImportSource @emotion/react */          // 필수적으로 기입해야하나, 추가 라이브러리 설치로 미기입 할 수 있다. 
      import { css } from '@emotion/react';
       
      const buttonStyle = css`
        background-color: #4CAF50;
        border: none;
        color: white;
        padding: 15px 32px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
       
        &:hover {
          background-color: #3e8e41;
        }
      `;
       
      function App() {
        return (
          <div>
            <button css={buttonStyle}>Emotion 버튼</button>
          </div>
        );
      }




<br/><br/>  <br/><br/>  


[출처] <br/>
https://www.devdive.co.kr/react/css-library-comparison

  
