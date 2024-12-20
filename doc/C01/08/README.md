# 셀렉터
HTML태그에 클래스 두개 이상 붙이기
---
> html
```html
<div class="container text-center"> </div>
```
- 띄어쓰기 후 원하는 class 추가 작성 

<br> 

---

<br>

셀렉터 사용법
---

### 1. 공백
> html
```html
<ul class="navbar">
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

> css
```css
.navbar li {
  display : inline-block;
}
```
- 공백을 이용해 안에 있는 li 태그인 모든 자손 선택 가능

- 스페이스바 다음에 tag 셀렉터, class 셀렉터, id 셀렉터 사용 가능

- .class .class .class 등 무한히 연달아 사용 가능

<br>
 
### 2. 꺾쇠괄호 > 
> html
```html
<ul class="navbar">
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

> css
```css
.navbar>li {
  display : inline-block;
}
```
- 기호를 이용해 .li-inline 바로 밑에있는 자식만 선택 가능

<br>

### 3. 더욱 상세히 선택하고 싶다면 
> html
```html
<ul class="navbar">
  <li> <span>안녕</span> </li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

> css
```css
.navbar li>span {
  color : red;
}
```
- 셀렉터를 연달아 사용

- .navbar 안에 있는 모든 li, 그 안에 있는 모든 직계 자손 span 태그 선택

<br>

#### 💡 참고
> css
```css
.container div div>p>span
```
- 이렇게 4~5개 이상 연달아 붙여쓰지 않길 권장

    - 어떤 부분을 스타일링하는지 파악 어려움

        - 읽기만 해도 어떤 스타일을 주는지 알 수 있는 셀렉터가 좋은 셀렉터

    - 파일이 커지면 버그의 원인

    - 재사용가능성, 확장성을 염두에 둔다면 이렇게 사용 X

- 셀렉터 잘 쓰면 클래스 추가선언 없이도 개발자가 원하는 요소 쉽게 스타일링 가능

    - 단, 셀렉터를 남발하는 것 보다는 하나의 새로운 클래스를 만드는게 훨씬 더 나을 수 있음

<br>

---

<br>

링크 디자인 
---
> html
```html
<a href="#" class="link">링크</a>
```

> css
```css
.link {
  text-decoration : none;
}
.link:visited {
  color : black;
}
```
- 링크의 기본 밑줄 제거 => text-decoration : none

- 링크를 방문했을 시 보라색으로 변하는 것 조작

    - 셀렉터에 :visited 라는 pseudo-class 붙이기

        - 방문 후(visited) 링크들의 스타일 지정 가능

<br> 