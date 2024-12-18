# Table 레이아웃과 vertical-align 속성
vertical-align 속성을 실험해볼 이미지와 글자
---
> html
```html
<div> <img src="https://mdn.mozillademos.org/files/12245/frame_image.svg" width="32" height="32"> image with a default alignment.</div> 
```
<br>
 
---

<br>

기본적인 table HTML 구성 
---
> html
```html
<table>
  <thead></thead>
  <tbody>
    <tr>
      <td>내용</td>
      <td>내용</td>
    </tr>
  </tbody>
</table>
```
- table 태그 내에 tr 은 row, td 는 column 의미

    - 원하는 만큼 row, column 넣어주면 표 완성

- tbody, thead : 헤드부분 영역구분을 위해 사용

    - td 대신 th 태그를 사용하면 기본적으로 제목처럼 굵게 처리 

<br>

---

<br>
 

테이블 셀 내에서 상하정렬할 땐 vertical-align 
---
> css
```css
td, th {
  vertical-align : middle;
}
```
- vertical-align 속성을 이용해 테이블 내에서의 상하정렬 가능

    - top, bottom, middle 사용가능


<br>

---

<br>
 

inline 요소 간 상하정렬할 땐 vertical-align 
---
> html
```html
<p>
  <span style="font-size : 50px">Greetings</span>   <span style="font-size : 20px">안녕</span>
</p>
```
- display : inline 혹은 inline-block 요소들을 나란히 배치하면 상하정렬이 이상한 경우 발생

    - 큰 이미지와 글 또는 큰 글씨옆에 있는 작은 글씨 등을 나란히 배치했을 때 서로 높이가 맞지 않는 경우가 많음

        - margin-top 대신 사용하는 속성

- top, middle, bottom 말고도 super, sub, px 단위로 사용가능

- 용도 정리

    - 용도1 : inline/inline-block 요소 간의 세로정렬할 때 사용

        - inline : 항상 옆으로 채워지는 폭과 너비가 없는 요소

    - 용도2 : table 안에서 세로정렬할 때 사용

        - table 안에선 top, middle, bottom 만 사용가능


- 비교
> html
```html
<p>
  <span style="font-size : 50px">Greetings</span>   <span style="font-size : 20px; vertical-align : top;">안녕</span>
</p>
```

<br>

---

<br>

 

display : table 
---
> html
```html
<div style="display: table">
    <div style="display: table-row">
        <div style="display: table-cell">21</div>
        <div style="display: table-cell">23</div>
    </div>
</div>
```

> css
```css
.box {
  display : table;
  display : table-row;
  display : table-cell;
}
```
- div로 이루어진 요소들을 테이블화 시키고 싶을 때

    - table 태그로 변하길 원하는 요소에 display : table 기재

    - tr로 변하길 원하는 요소엔 display : table-row 기재

    - td로 변하길 원하는 요소엔 display : table-cell 기재

- 이럴 일은 거의 없기 때문에 참고로만 알아두기

<br>
 




