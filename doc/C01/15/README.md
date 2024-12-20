# 코드양이 줄어드는 class 작명법 (OOCSS, BEM)
코드 양을 줄이는 CSS 작성법 (OOCSS)
---
- 똑같이 생겼는데 색만 빨강/파랑으로 다른 버튼 2개를 만들어야 한다면?

> 방법1. css
```css
.main-btn-red {
  font-size : 20px;
  padding : 15px;
  border : none;
  cursor : pointer;
  background : red;
}

.main-btn-blue {
  font-size : 20px;
  padding : 15px;
  border : none;
  cursor : pointer;
  background : blue;
}
```
- class를 두 개 만들어서 각각 <button> 태그 작성

    - 빨간 버튼 파란 버튼 완성이지만 중복 코드 매우 많이 발생

        - css 파일이 너무 길어서 가독성 좋지 않음

        - 용량이 큰 CSS 파일은 웹사이트 로딩 속도 저하시킴

<br>

> 방법2. css
```css
.main-btn {
  font-size : 20px;
  padding : 15px;
  border : none;
  cursor : pointer;
}

.bg-red {
  background : red;
}
.bg-blue {
  background : blue;
}
```

> html
```html
<button class="main-btn bg-red">빨간버튼</button>
<button class="main-btn bg-blue">파란버튼</button>
```
- Object Oriented CSS 방식 : 버튼의 뼈대와 살을 분리

    - 1. 버튼의 기본 스타일인 padding, font-size 이런걸 정의하는 class 먼저 생성

    - 2. 버튼에 스킨 색깔 변경 용도의 class 여러개 생성

<br>

- 방법2 장점
    - 1. 중복된 스타일 재사용 가능

        - CSS 파일용량도 줄어들고 코딩 시간 절약

    - 2. 유지보수 편리

        - 사이트의 모든 버튼의 font-size를 약간 줄여야하는 경우 한 곳만 건드리면 모든 버튼이 다 수정됨

    - 3. 코드 작성 속도 빨라짐

        - utility class : .bg-red 등 디자인 변경용 class

<br>

> css
```css
.bg-red {
  background : red;
}
.bg-green {
  background : green;
}
.bg-blue {
  background : blue;
}
```
- 앞으로 버튼만들 때 class 명을 두세개 고르기만 하면 됨

    - css 파일 열지않고도 다양한 스타일을 빠르게 만들 수 있음

    - 버튼말고도 다른 UI에 색상 줄 때도 적용가능

 
<br>
 
> css
```css
.font-small {
  font-size : 12px;
}
.font-medium {
  font-size : 16px;
}
.font-lg {
  font-size : 20px;
}
```
- font-size 변경이 잦다면 utility class 많이 만들어두고 글자 스타일링할 때 가져다 쓰면 코딩 시간 단축 가능

    - width, margin, padding, text-align 조정하는 utility class 많이 만들어두면 편리함

<br>

---

<br>

BEM 작명법
---
> html
<div>
  <img>
  <h4>이름</h4>
  <p>소개글</p>
  <button>빨간버튼</button>
  <button>파란버튼</button>
</div>
```
- 모든 HTML 요소에 class 작명하는 경우

    - class 6개나 작명해야하지만, BEM 룰을 적용해보면 작명이 쉬워짐

<br>

### 1. class를 작명할 땐 우선 컴포넌트 이름으로 시작
> html
```html
<div class="profile">
  <img class="profile">
  <h4 class="profile">이름</h4>
  <p class="profile">소개글</p>
  <button class="profile">빨간버튼</button>
  <button class="profile">파란버튼</button>
</div>
```
- 프로필 소개하는 html 컴포넌트를 만드는 경우

    - 안에 있는 모든 class 명은 일단 profile 로 우선 작명

<br>

### 2. 태그마다 다른 class명을 부여하려면 __태그명을 뒤에 붙이기
> html
```html
<div class="profile">
  <img class="profile__img">
  <h4 class="profile__h4">이름</h4>
  <p class="profile__content">소개글</p>
  <button class="profile__button">빨간버튼</button>
  <button class="profile__button">파란버튼</button>
</div>
```
- __태그이름 으로 작명

    - profile 안에 있는 img 태그는 profile__img

    - profile 안에 있는 button 태그는 profile__button

- 태그 이름 쓰기 싫으면 content 이런 식으로 작명해도 OK

<br>

### 3. 같은 태그들의 디자인을 구분하려면 --
> html
```html
<div class="profile">
  <img class="profile__img">
  <h4 class="profile__h4">이름</h4>
  <p class="profile__content">소개글</p>
  <button class="profile__button--red">빨간버튼</button>
  <button class="profile__button--blue">파란버튼</button>
</div>
```
- 버튼이 색깔별로 여러개가 필요하다면 

    - 빨간 버튼은 --red

    - 파란 버튼은 --blue

- 버튼이 사이즈별로 여러개가 필요하다면

    - 큰 버튼은 --big

    - 작은 버튼은 --small 

<br>

#### 💡 BEM 룰을 쉽게 외우려면
- Block__Element--Modifer

    - Element : HTML 요소
    
    - Modifier : 수식어

<br>

---

<br>

참고
---
- OOCSS 클래스 작성방식, BEM 작명방식은 html css 파일이 크고 방대할 때 장점을 보이는 것

- React, Vue 이용해서 웹페이지를 만들 때는 크게 유용하진 않음

    - React : html 페이지 단위가 아니라 작은 UI 단위로 개발

        - styled-components, module CSS 등의 라이브러리 : class명 중복을 알아서 제거해줌

        - UI 덩어리들끼리 class명이 서로 중복되어도 상관없어서 코드를 마구 작성 가능

<br>