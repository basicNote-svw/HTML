# 레이아웃 만들기 3 : 편리한 Flexbox

Flexbox 레이아웃 사용법
---
> html
```html
<div class="flex-container">
  <div class="box"></div>
  <div class="box"></div>
  <div class="box"></div>
</div>
```

> css
```css
.flex-container {
  display : flex;
}
.box {
  width : 100px;
  height : 100px;
  background : grey;
  margin : 5px;
}
```
- 박스들을 감싸는 부모 요소에게 display : flex 사용

    - 그럼 박스들이 기본적으로 가로정렬로 배치

- flex 특징

    - width : 100% or 600px 기재시, 실제 width 가 100% 혹은 600px 아님

        - 최대한 100% 혹은 600px 에 맞추는 것

- 인터넷 익스플로러 11 이상에서 사용가능한 속성

    - 11미만에선 flex 없다고 에러 발생 

<br>

---

<br>

Flexbox 세부속성 사용하기 
---
> css
```css
.flex-container {
  display : flex;
  flex-direction : column   /* 세로배치 */
  justify-content : center;  /* 좌우정렬 */
  align-items : center;  /* 상하정렬 */
  flex-direction : column; /* 세로정렬 */
  flex-wrap : wrap;  /* 폭이 넘치는 요소 wrap 처리 */
}
.box {
  flex-grow : 2;  /* 폭이 상대적으로 몇배인지 결정 */
}
```
- 필요할 때마다 찾아쓰는기

<br>

---

<br>

박스 좌측 & 우측정렬 동시에 하는 법 
---
> html
```html
<div class="flex-container">
  <div class="box"></div>
  <div class="box" style="flex-grow : 1"></div>
  <div class="box"></div>
</div>
```
- 첫 \<div>는 왼쪽, 마지막 \<div>는 우측정렬을 하고싶으면?

    - 가운데 임시 \<div> 생성

    - flex-grow: 1 이런 식으로 사이즈를 크게 키우기

        - 나머지 요소들은 좌측 우측으로 퍼짐 

<br>

---

<br>

align-content
---

|-|
|-|
|![이미지](./img/01.png)|

- display : flex; 준 요소에 align-content 속성 사용 가능

    - 내부에 들어있는 박스들의 상하정렬이 어떻게 될지 조절 가능

- align-content : 박스가 가로로 여러줄일 때 박스들의 상하배치를 조절 가능한 속성

- justify-content 의 세로버전 

 
<br>
 

 