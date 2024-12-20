# 레이아웃 만들기 2 : inline-block
display : inline-block 사용 법 
---
- 가로 정렬 방법

  - 1. float : left

  - 2. display : inline-block

- display : inline-block 사용

> html 
```html
<div>
  <div class="left-box"></div><div class="right-box"></div>
</div>
```

> css
```css
.left-box {
  width : 100px; 
  height : 100px;
  display : inline-block;
}
.right-box {
  width : 100px; 
  height : 100px;
  display : inline-block;
}
```
- 박스를 만들어 왼쪽으로 정렬시키는 코드

  - display 속성만 inline-block으로 조정하면 가로 배치 가능

  - inline- block : 내 폭과 높이만큼 자리차지하게 해달라는 뜻

- 간편하지만 <태그> 사이에 스페이스바 공백이 있다면 그대로 보여줌

  - 가로로 정렬하려면 태그 사이의 공백도 제거 필수

<br>

---

<br>

공백제거
---
### 1. 주석처리 기호 사용하기
> html
```html
<div>
   <div class="left-box"></div><!--
--><div class="right-box"></div>
</div>
```
- 주석은 실행되지 않는 코드

  - 에디터에선 ctrl + / 로 주석처리가 가능 (맥은 command + ?)

- HTML 의 주석처리 코드 : <!-- -->

  - 사이에 코드를 집어넣으면 실행되지 않음

<br> 

### 2. 부모의 폰트사이즈를 0으로 만들기
> html
```html
<div style="font-size : 0px;">
    <div class="left-box"></div>
    <div class="right-box"></div>
</div>
```
- font-size 속성은 inherit 되기 때문에 안에 있는 <div>와 그 사이에 있는 공백도 font-size가 0px 

  - HTML 깔끔해지지만 CSS 복잡해짐

<br>
 
