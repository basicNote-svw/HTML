# Transition 속성으로 CSS 애니메이션 구현
overflow 속성 
---
> html
```html
<div style="width: 50px; height: 50px; overflow: hidden">
    <p>aaaaaaaaaaaaaaaaaaa</p>
</div> 
```
- overflow 속성 : 박스의 폭이나 높이를 초과하는 내부요소를 처리하기 위한 속성

    - hidden : 넘치는 내부요소를 자동으로 잘라 없앰

        - 글자 뿐만 아니라 이미지, 박스가 넘쳐 흘러도 똑같이 잘라 없앰

    - visible : 넘치는 부분을 그대로 보여줌

    - scroll : 넘치는 요소를 보기 위한 스크롤바 생성됨

<br>
 
---

<br>

opacity 속성
---
 
> CSS
```css
.box {
  opacity : 0
}
```
- 현재 HTML 요소의 투명도를 조절

    - 0부터 1까지의 실수 입력

<br> 

---

<br>

transition 속성
---
 
> css
```css
.box {
  opacity : 0;
  transition : all 1s;
}
```
- transition : 적용된 CSS가 변할 때 서서히 변경됨

    - all : 모든 스타일이 변할 때 서서히 변경하라는 뜻
    
        - all 대신 opacity 이렇게 하나만 줄 수도 있음

    - 1s : 1초에 걸쳐서 서서히 변경해달라는 뜻

 
<br>

---

<br>

transition 세부 속성
---
 
> css
```css
.box {
  transition-delay: 1s; /* 시작 전 딜레이 */
  transition-duration: 0.5s; /* transition 작동 속도 */
  transition-property: opacity; /* 어떤 속성에 transition 입힐건지 */
  transition-timing-function: ease-in; /* 동작 속도 그래프조정 */
}
```
- 예시처럼 세부 설정 가능

<br>

---

<br>


one-way 애니메이션 만드는 법칙
---
- one-way 애니메이션 : A에서 B로 정지없이 쭉 이동하는 애니메이션 

 
### 1. 시작스타일 정하기

<br>

### 2. 최종스타일 정하기

<br>

### 3. 언제 최종스타일로 변할지 트리거 주기 
    
- 마우스 올렸을 때 :hover 등

<br>

### 4. transition 으로 서서히 동작하게 만들기 

<br>
이런 스텝으로 CSS 코드 짜면 끝입니다. 

 
<br>


---

<br>

상품 진열 레이아웃
---
 
> html
```html
<div class="shop-bg">
    <div class="shop-container">
      <div class="shop-item">
        <div>
          <img src="img/product1.jpg">
        </div>
      </div>
      <div class="shop-item">
        <img src="img/product2.jpg">
      </div>
      <div class="shop-item">
        <img src="img/product3.jpg">
      </div>
    </div>
</div>
```

> css
```css
.shop-bg {
  background-color: #eee;
  padding: 20px;
}
.shop-container {
  display: flex;
  width: 90%;
  margin: auto;
}
.shop-item {
  width: 33%;
  padding: 10px;
}
.shop-item img {
  width: 100%;
  display: block;
}
```

<br>
 
---

<br>

상품진열 레이아웃
---
> html
```html
<div class="overlay-wrap">
  <div class="overlay-black">
    <span>$60</span>
  </div>
</div>
<img src="img/product1.jpg">
```
> css
```css
.overlay-wrap {     /* 이미지를 덮는 투명한 박스로 디자인 */
  position : absolute;
  width : 100%;
  height : 100%;
  overflow : hidden;    /* 넘치는건 안보이게 처리 */
}

.overlay-black {    /* 투명한 박스 내에 존재하는 검정 박스 */
  width : 100%;
  height : 100%;
  background : rgba(0,0,0,0.3);
  padding : 20px;
  margin-top : 100%; /* margin-top 조정해 최종스타일과 시작스타일 만들기 */
}

/* .overlay-wrap 박스에 마우스를 올리면 .overlay-black이 최종화면이 되도록 코드 작성 */
.overlay-wrap:hover .overlay-black {
  margin-top : 50%;
}
```
- 기존 요소에 :hover 시 뭔가 덮어주는 애니메이션 만들 때

    - 기존 요소를 덮고나면 더 이상 :hover 상태가 아닐 수 있음

- box:hover .box2 라고 사용하면 .box에 마우스를 올렸을 때 내부에 있는 .box2를 움직이게 만들 수 있음


<br>