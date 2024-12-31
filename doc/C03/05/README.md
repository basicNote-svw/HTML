# Sass 핵심 문법
- 문법 내용보다 문법을 어디에 쓸지 그 용도를 기억

    - 용도를 알아야 문법을 자유자재로 사용가능

 
<br>

 

sass 파일과 scss 파일
---
- .sass 파일도 만들 수 있음

    - 이 파일은 SASS 문법으로 코드짤 때 중괄호 생략 가능

> sass
```sass
.box 
    font-size : 16px;

.main-bg 
    color : red
```
- 인터넷에서 예제코드 복붙 많이 하면 .scss 파일 쓰는게 좋음


<br>

---

<br>
 

Sass 문법 2. 셀렉터 대신 쓰는 Nesting
---
- 셀렉터를 많이 사용하다보면 코드 자체가 복잡해짐

    - 예) div.container > div p.first > span::after

    - 셀렉터 복잡해지면 처음 보는사람은 무슨 요소인지 제대로 파악 어려워짐

- 셀렉터의 외모를 개선할 수 있는 Nesting 문법 존재

- 필수는 아님
 
> scss
```scss
.navbar {
  ul {
    width : 100%;
  }
  li {
    color : black;
  }
}
/*위에건 SASS 문법*/

.navbar ul { 
  width : 100%; 
}
.navbar li { 
  color : black; 
}
/*밑에건 CSS 문법*/
```
- 위 두개의 코드는 같은 기능을 하는 코드

    - 중괄호 안에 셀렉터 추가
    
        - 셀렉터상의 스페이스바 문법과 동일하게 작성가능

- 사용하는 이유

    - UI들을 묶음으로 관리할 수 있어서

    - navbar 내부에 속한 요소들을 정리해놓으면 나중에 관리가 편해짐

        - navbar 내부에 있는 글자 하나 바꾸려고 하면 .navbar {} 중괄호만 확인하면 OK

<br>

### 💡 div.container > div p.first > span 의 Nesting

> scss
```scss
div.container {
  >div {
    p.first {
      >span {
      }
    }
  }
}
```
- Nesting 시 괄호를 3~4개 타고 들어가는건 권장 X

- SASS 문법 t사용여부와 관계없이, 셀렉터를 길게 나열하는건 좋은 관습 X

    - 깔끔하게 클래스 하나 선언

<br>

 

### 💡 :hover 등 pseudo-class 붙이려면

> scss
```scss 
.navbar {
  :hover {
    color : blue;
  }
}

.navbar {
  &:hover {
    color : blue;
  }
}
```
- 위 코드 ⇒ .navbar :hover

- 아래 코드 ⇒ .navbar:hover

    - &기호 붙이면 셀렉터를 스페이스바 없이 붙알 수 있음


<br>

---

<br>
 

Sass 문법 3. 이미 있는 클래스를 확장하는 @extend 
---
- 이미 존재하는 속성들을 복붙하지 않고 사용 가능

- @extend + 복붙해야할 클래스 명

- 비슷한 디자인의 요소들을 양산할 때 많이 사용

- % 기호 : .대신 쓸 수 있는 임시클래스

    - CSS파일에서 클래스로 컴파일하지 않고싶을 때 쓰는 기호

    - 컴파일하고나면 %기호 안에 있는 것들은 사라짐

> scss
```scss
%btn {
    width: 100px;
    height: 100px;
    padding : 20px;
}

.btn-green {
    @extend %btn;
    background : green;
}

.btn-red {
    @extend %btn;
    background : red;
}
```
- @extend 사용 후 복붙할 클래스명을 뒤에 적으면 클래스명에 있던 모든 내용이 복붙됨

 

<br>
 

 

 

 