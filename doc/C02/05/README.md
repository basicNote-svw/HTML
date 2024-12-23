# 반응형 레이아웃
모던 웹에서 사용하는 단위정리
---
> css
```css
.box {
  width : 16px; /* 기본 px 단위 */
  width : 1.5rem; /* html태그 혹은 기본 폰트사이즈의 1.5배 */
  width : 2em; /* 내 폰트사이즈 혹은 상위요소 폰트사이즈의 2배 */
  width : 50vw; /* 브라우저(viewport) 화면 폭의 50% */
  width : 50vh; /* 브라우저(viewport) 화면 높이의 50% */
}
```
- em : 내 폰트사이즈의 X배

- vw : 브라우저 폭에 비례

- vh : 브라우저 높이에 비례

- rem : 기본 폰트사이즈에 비례 (html 태그 폰트사이즈의 10배, 16px 의 10배)

    - 모든 div의 사이즈, margin, padding, 버튼 사이즈가 기본 폰트사이즈에 비례해서 움직이게 만들고 싶을 때 사용

        - 브라우저 폰트사이즈를 키운 채로 웹브라우징 하는 사람이 있었기 때문에

    - 페이지를 폰트사이즈에 가변적으로 반응하는 사이트 만들 때 빼고는 그닥 유용한 속성은 아님

        - 요즘은 ctrl + 마우스휠업 이렇게 줌인을 해서 쓰는 사람이 대부분

    - typography 디자인할 때 글자사이즈를 px 단위로 기억하기 힘들 때 폰트사이즈로 rem 사용 

<br>

반응형 웹을 만들 때 head 태그에 들어가야할 내용
---
> html
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- 위 내용이 들어가있어야 모바일에서도 예쁜 레이아웃을 만들 수 있음

<br>

media query 사용하는 법 
---
> css
```css
@media screen and (max-width : 1200px) { 
  .box { 
    font-size : 40px; 
  } 
} 

@media screen and (max-width : 768px) { 
  .box { 
    font-size : 30px; 
  } 
}
```
- CSS 파일 최하단에 사용

    - 현재 브라우저의 폭이 1200px 이하일 경우에 안에 있는 class를 적용해달라는 뜻

        - 브라우저 폭이 1200px 이하면 .box { font-size : 40px } 적용

        - 브라우저 폭이 768px 이하면 .box { font-size : 30px } 적용

- 여러개 원하는 만큼 사용가능

    - 큰 사이즈 → 작은 사이즈 순으로 작성

- 적용은 아니고 class를 밑에 하나 더 추가해준다라고 이해하는게 정확

    - class 안의 font-size 스타일 중복 발생

        - 중복이 발생하면 원래 더 밑에 있는 스타일을 적용

 
<br>

권장 Breakpoint 
---
- Breakpoint : media query 문법 max-width 안에 넣는 브라우저 폭

- 원하는 만큼 저렇게 여러개 넣을 수 있음

- 필요할 때 마다 사이즈를 임의로 넣고 작성하는 것 보다는 breakpoint 쓰는 것 권장

    - 1200px / 992px / 768px / 576px

    - Bootstrap 라이브러리가 기본으로 권장하는 breakpoint

    - (1200px 이하는 태블릿, 768px 이하는 모바일) 이렇게 디자인하는게 가장 간편

 
<br>
 