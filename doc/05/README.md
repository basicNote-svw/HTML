# 웹레이아웃의 기초 : div를 이용한 네모네모 박스 디자인

네모 박스 디자인에 많이 사용하는 CSS 속성
---
 
```css
.box {
  margin : 20px; 
  padding : 30px;
  border : 1px solid black;
  border-radius : 5px;
}
```
- margin : 바깥 여백

- padding : 안쪽 여백

- border : 테두리 (차례로 두께, 선의 종류, 색상)

- border-radius : 테두리 둥글게 처리 

- display : block; margin-left : auto; margin-right : auto => 가운데 정렬

 <br>


### margin과 padding을 원하는 방향에만 적용
```css
.box {
  margin-top : 20px;
  padding-left : 30px; 
}
```
- top, left, bottom, right 중 원하는 곳에만 여백 주기 가능

- margin은 음수도 가능 (ex) -20px

- margin : 5px 6px 7px 8px; 

    - 띄어쓰기를 이용해 작성시 차례로 상 우 하 좌 마진을 5,6,7,8px 한번에 줄 수 있음 

<br> 

---

<br>

display : block이 내장되어있는 div박스
---
 ```css
.box {
  display : block;
}
```
- 모든 div, p, h1, li 등은 display : block 속성 기본 내장 

    - p태그나 div태그를 그냥 사용하면 한 행을 전부 차지 

- display 속성을 다른 것으로 부여 가능

    - inline, inline-block, flex 등

<br>

### 일부 스타일은 inherit 가능
- 부모 태그에 주어지면 거기 안에 있던 태그들까지 전부 상속(inherit)되는 속성 존재

    - font-size, color, font-family, text-align 등

    - 안에 글자들이나 태그들이 많을 경우 font-size를 부모태그에 한번에 작성가능해 편리 

        - 모든 속성이 inherit 되는건 아니고 글자와 관련된 스타일들이 주로 inherit 됨  

<br>