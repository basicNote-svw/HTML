# CSS 덮어쓰기 잘하는 법 & 좋은 코드
CSS 덮어쓰기
---
- 업무의 절반 이상은 이미 작성된 CSS 수정

    - 직접 원본 CSS파일을 건드리지 못하는 경우 새로운 CSS로 덮어써야함 

<br>
 

### 1. 같은 클래스명이나 스타일을 하단에 작성
> 하나의 CSS 파일일 경우
```css
.box {
  background : red;
}

.box {
  background : blue;
}
```
- 같은 class 명이라도 하단에 정의한 클래스 명과 스타일을 우선적으로 적용

<br
 
> html
```html
<link href="main.css" rel="stylesheet">
<link href="main2.css" rel="stylesheet">
```
- CSS파일이 여러개 첨부되어있을 때도 유효

    - \<link>를 하단에 사용할 수록 하단에 작성한 것과 똑같은 효과

    - main.css와 main2.css에 같은 class 명이 있더라도 main2.css에 있는 클래스 명을 우선적으로 적용 

<br>

### 2. id, style 등 우선순위를 높여 작성
- 우선순위 : tag < class < id < style="" 

    - 1점 10점 100점 1000점

- class 스타일을 덮어쓰려면 id 써보고 안되면 style속성 열어보고 이렇게 수정

- 속성 뒤에 !important 부여하면 모든 우선순위를 무시하고 최우선적으로 이 속성 적용

    - 10000점

> !important
```css
.box {
  background : red !important;
}

.box {
  background : blue;
}
```
- 이렇게 사용하면 !important가 붙은 스타일 최우선으로 적용

    - 큰 힘으로 다른 힘을 억누르게 되면, 추후 수정시 더 큰 힘으로 억눌러야하기 때문에 근본적인 해결방안 X
    
    - 되도록이면 쓰지않는걸 추천

- id 는 스타일링할 때 쓰지 말기

    - 프론트엔드 백엔드 기능개발시 id 자주 사용하는데 그것과 겹치면 번거로워짐

 
<br>

### 3. Specificity (구체성 점수) 높여서 작성하기 

- 셀렉터를 여러개 나열하면 점수도 높아짐

> css
```css
div.container .box {
  color : red;
}
```
- 10점짜리인 .class 2개 + 1점짜리인 div 태그셀렉터 1개 ⇒ 21점

    - 더 구체적으로 셀렉터를 작성할 수록 점수가 높아져서 저렇게 점수를 높여도 덮어쓰기가 가능

 
<br>

> css
```css
div.container div.box {
  color : red;
}

div.container .box {
  color : blue;
}
```
- 둘 다 똑같이 .box 스타일링

    - color : red가 더 위에 있음에도 불구하고 적용됨

        - div.container  div.box : 22점

        - div.container  .box : 21점 

 
<br>

---

<br>

결론
---
- CSS 파일 사용할 때

    - div.container  div.box 이런 식으로 길게 쓰면 나중에 덮어쓰기가 힘들어짐

    - class 이름은 하나만 써서 작성

<br>

---

<br>

 
좋은 코드의 원칙
---

### 1. 내가 짠 코드가 나중에 수정이 쉽고 관리가 쉬워지면 좋은 코드

<br>

### 2. 확장성이 좋으면 좋은 코드
- 확장성

    - 지금 만든 class를 다른 페이지에서도 계속 활용할 수 있을 것 같은지

    - 지금 만든 class를 살짝 수정해서 더 유용한 class를 만들기 쉬울지

- SASS로 코드 작성시 중요

<br>

### 3. 양이 적으면 좋은 코드 (선택사항)

<br> 


 