# pseudo-class로 인터랙티브 버튼 만들기

상태에 따라서 스타일을 줄 수 있는 Pseudo-class 셀렉터
---
> css
```css
.btn:hover {
  background : chocolate; /*마우스를 올려놓을 때*/
}
.btn:focus {
  background : red; /*클릭 후 계속 포커스 상태일 때*/
}
.btn:active {
  background : brown; /*클릭 중일 때*/
}
```
- pseudo-class 셀렉터를 붙이면 여러 상태에 따른 스타일 지정 가능

- hover, focus, active 스타일 넣을 때 순서는 꼭 이렇게 선언해야 잘 동작함

    - 1. hover

    - 2. focus

    - 3. active

    - hofa 로 외우기
    
- 이 외에도 수많은 pseudo-class가 있기 때문에 필요하면 찾아쓰기

<br>

```css
:any-link /*방문 전, 방문 후 링크 한번에 선택할 때*/
:playing /*동영상, 음성이 재생중일 때*/
:paused /*동영상, 음성이 정지시*/
:autofill /*input의 자동채우기 스타일*/
:disabled /*disabled된 요소 스타일*/
:checked /*체크박스나 라디오버튼 체크되었을 때*/
:blank /*input이 비었을 때*/
:valid /*이메일 input 등에 이메일 형식이 맞을 경우*/
:invalid /*이메일 input 등에 이메일 형식이 맞지 않을 경우*/
:required /*필수로 입력해야할 input의 스타일*/
:nth-child(n) /*n번째 자식 선택*/
:first-child /*첫째 자식 선택*/
:last-child /*마지막 자식 선택*/
```
- [참고](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

 
<br>
 
---

<br>
 
input 등에도 자주 사용
---
> css
```css
input:focus {
  border : 2px solid red;
}
```
- 인풋에 커서가 찍혀있을 때 인풋에 스타일을 주고 싶으면 :focus 사용

 
<br>
 
---
 
<br>
 

a 태그에도 자주 사용
---
> css
```css
a:link { 
  color : red; /*방문 전 링크*/ 
} 
a:visited { 
  color : black; /*방문 후 링크*/ 
} 
```
- :link를 붙이면 방문 전 링크

- :visited를 붙이면 방문 후 링크에 스타일을 넣을 수 있음

- 모든 링크의 밑줄제거는 그냥 a태그에 text-decoration : none

<br>

 

 