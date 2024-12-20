# 레이아웃 만들기 1 : 호환성 좋은 float

html css로 사이트 레이아웃 만들기
---
- 만들고 싶은 레이아웃 디자인 위에 네모박스를 먼저 그린 후 바깥 네모부터 \<div> 로 구현

<br>

요소를 공중에 띄워 왼쪽/오른쪽 정렬하는 float 속성 
---
> layout1.html
```html
<div>
  <div class="left-box"></div>
  <div class="right-box"></div>
</div>
```
- 박스 두개를 만들어 각각 왼쪽으로 정렬

> layout1.css
```css
.left-box {
  width : 100px; 
  height : 100px;
  float : left;
}
.right-box {
  width : 100px; 
  height : 100px;
  float : left;
}
```
- float를 쓰면 요소를 붕 띄움

    - 그 다음에 오는 HTML 요소들이 제자리를 찾지 못함 

<br>

### float 속성으로 가로정렬할 땐
- float 박스들을 싸매는 하나의 큰 div 박스를 만들고 폭을 지정

    - 모바일에서 안 흘러넘침

- float를 쓰고 나면 항상 clear 속성

> layout1.html
```html
<div>
  <div class="left-box"></div>
  <div class="right-box"></div>
  <div class="footer"></div>
</div>
```

> layout1.css
```css
.footer {
  clear : both
}
```
- clear 속성을 사용하면 float 다음에 오는 박스들이 제자리에 위치

    - float 썼으면 항상 넣기

#### 💡 float : none 추가해주면 나중에 생길 버그예방차원에서 좋음

<br>

상대적인 크기 단위인 퍼센트 단위 
---
> layout1.css
```css
.box {
  width : 80%
}
```
- 부모 태그의 width에 비해 80% 만큼 차지

    - 부모태그 : 나를 감싸고 있는 태그 

<br>