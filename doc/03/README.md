# 기본적인 웹페이지 스타일링

간단한 스타일 넣기
---
```html
<p style="font-size : 20px; color : red"> 글자 </p>
```
- 거의 모든 태그는 style="" 속성 사용 가능

    - 스타일이름 : 스타일값; 형식으로 스타일 지정

    - 여러개를 넣고 싶다면 뒤에 쭉 나열

    - 세미콜론 필수

<br> 

---

<br>

자주 사용하는 글자 스타일들
---
```html
font-size : 20px;       <!-- 글자 크기 -->
font-family : 'gulim';  <!-- 폰트 -->
color : black;      <!-- 글자 색상 -->
letter-spacing : -1px;  <!-- 자간 -->
text-align : center;    <!-- 글자 정렬 -->
font-weight : 600;      <!-- 글자 굵기 -->
```
- 영어 단어를 알고 있다면 무슨 뜻인지 바로바로 파악 가능

<br>

---

<br>

이미지 정렬과 폭 조정
---
```html
display : block;
margin-left : auto;
margin-right : auto;
width : 150px;
```
- 이미지는 width 많이 사용

    - px 혹은 % 이런 단위로 폭 조정 가능

        - % 단위는 부모 사이즈에 비례

        - \<p><a>이동하기</a></p> : <p> 는 부모태그, <a> 는 자식태그

- 이미지를 가운데 정렬하고 싶으면 

    - display : block; margin-left : auto, margin-right : auto

<br>

---

<br>
 
텍스트의 일부만 스타일 변경
---
```html
<p>안녕하세요 저는 <span style="color : red;">뛰어난</span> 개발자입니다.</p>
```
- \<span> 이라는 태그로 감싼 뒤에 스타일 지정 

- \<span> 태그 : 글자 일부를 싸매고 싶을 때 사용하는 큰 의미없는 태그

- \<strong> 태그로 글자 일부를 싸매면 간단히 굵게 표현 가능

<br>

### 💡 참고
- span 태그는 display : inline 이라는 스타일 속성을 내포

    - display : inline 을 가지고 있는 요소는 폭, 높이 등을 단독으로 결정 불가

- 폭, 높이를 주고싶으면 \<p> 태그에 적용

<br>