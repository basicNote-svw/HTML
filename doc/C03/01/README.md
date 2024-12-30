# Pseudo-element
- 특정 HTML 요소의 안쪽 일부만 스타일을 주고 싶을 때 Pseudo-element 셀렉터 이용해 스타일 가능


```
:pseudo-class(다른 상태일 때)
::pseudo-element(내부의 일부분만 스타일줄 때)
```

<br>
 

Pseudo-element로 HTML 특정부분에 스타일링하기/글씨넣기
---

> css
```css
.text::first-letter {
  color : red;
}

.text::first-line {
  color : red;
}

.text::after {
  content : '뒤에추가';
  color : red;
}

.text::before {
  content : '앞에추가';
  color : red;
}
```
- pseudo-element를 선택하려면 콜론 2개 :: 사용

- ::first-letter ⇒ 안에 있는 글자 중 첫 글자만 스타일 적용

- ::first-line ⇒ 안에 있는 글자 중 첫 줄만 스타일 적용

- ::after ⇒ 내부의 맨 마지막 부분에 특정 글자 추가 가능

- ::before ⇒ 내부의 맨 앞 부분에 특정 글자 추가 가능

<br>

### 💡 first-letter vs \<span>첫글자\<span>뒷글자
- 서버와 데이터베이스로 인해 글자가 항상 다이나믹하게 변하는 경우 

    - 자바스크립트 작성하지 않는 이상 항상 span태그 넣기 불가능

<br>

---

<br>

Pseudo-element로 clear : both 박스 편하게 만들기
---

> css
```css
.box::after {
  content : '';
  display : block;
  clear : both;
}
```
- 갑자기 어떤 요소 뒤에 clear : both 속성을 가진 div박스 필요해질 경우

    - 예제처럼 div를 흉내내서 사용 가능

    - div를 하나 만들 필요 없음

        - content 안에 아무것도 안적은 후 display : block을 주면 div 비슷한게 생성됨

<br>

---

<br>

Pseudo-element 활용
---
- [CSS 만으로 버튼에 마우스 올리면 배경 어둡게하기](https://codepen.io/css-tricks/pen/dxyfA)

- [CSS만으로 3D 느낌 리본모양만들기](https://codepen.io/team/css-tricks/pen/mVZGKa)

- [ol 태그의 숫자 스타일링하기](https://www.456bereastreet.com/archive/201105/styling_ordered_list_numbers/)

- [table 반응형으로 만드는 여러가지 방법](https://css-tricks.com/responsive-data-tables/)


<br>