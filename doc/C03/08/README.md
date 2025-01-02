# transform & animation
transform 관련 CSS 속성들 
---
> css 
```css
.box {
  transform : rotate(10deg); 
  transform : translate(10px, 20px);
  transform : scale(2);
  transform : skew(30deg);
  
  /*transform 두개 이상을 한꺼번에 쓰려면*/
  transform : rotate(10deg) translateX(30px);
}
```
- transform 은 어떤 요소를 독립적으로 움직이게 만들고 싶을 때 사용

- 본인 원래 위치에서 자유롭게 (다른 요소에 영향 없이) 이동

- rotate는 회전, translate는 좌표이동, scale은 확대축소, skew는 비틀기 

- 애니메이션을 동작시킬 때 transform 속성을 쓰면 효과적
 

<br>

---   

<br>

복잡한 애니메이션 구현법
---
- 간단한 a -> b 애니메이션 : 시작스타일, 최종스타일, 트리거, transition 

    - a -> b -> a,  a -> 1초정지 -> b 같은 복잡한건 불가능

    - @keyframes를 쓰면 가능

<br>

### 1. @keyframes 정의

> css
```css 
@keyframes 애니메이션{
  0% {
    transform : translateX(0px); /* 애니메이션이 0%만큼 동작시 */
  }
  50% {
    transform : translateX(-20px); /* 애니메이션이 50%만큼 동작시 */
  }
  100% {
    transform : translateX(20px); /* 애니메이션이 100%만큼 동작시 */
  }
}
```
- @keyframes : 커스텀 애니메이션을 정의하기 위한 공간

- 애니메이션을 0%, 50%, 100% 진행했을 때의 CSS 각각 작성

    - % 수치는 맘대로 변경, 추가 가능

<br>
 

### 2. keyframes를 원하는 곳에 첨부합

> css
```css
.box:hover {
  animation-name : 애니메이션;
  animation-duration : 1s;
}
```
- animation 속성 이용시 애니메이션 동작 가능

    - 꼭 필요한 속성 : name(애니메이션 이름), duration(애니메이션 동작시간)

- 마우스 올렸을 때 애니메이션 동작

 
<br>
 
### 3. 애니메이션 세부조정

> css
```css
.box:hover {
  animation-name : 애니메이션;
  animation-duration : 1s;
  animation-timing-function : linear; /*베지어 주기*/
  animation-delay : 1s; /*시작 전 딜레이*/
  animation-iteration-count : 3; /*몇회 반복할것인가*/
  animation-play-state : paused;  /*애니메이션을 멈추고 싶은 경우 자바스크립트로 이거 조정*/
  animation-fill-mode: forwards;  /*애니메이션 끝난 후에 원상복구 하지말고 정지*/
}
```
 

<br> 

---

<br>
 

margin, width, left 대신 transform 사용 이유 
---
 - 크롬같은 웹브라우저들은 님들이 짠 html css 코드를 2D 그래픽으로 바꿔주는 프로그램

    - html css 코드를 그래픽으로 바꿀 때 layout 잡기 -> 색칠하기 -> transform 적용하기 순서로 동작  

    - layout이 바뀌면 layout 부터 transform 까지 쭉 다시 렌더링

    - transform이 바뀌면 transform 부분만 다시 렌더링 가능

- 이동시키고 싶으면 margin 보다 transform 쓰는게 빠르게 동작


<br>

---

<br>

성능 개선
---
### 1. will-change 
> css
```css
.box {
  will-change: transform;
} 
```
- 애니메이션을 주는 .box가 약간 느리게 동작한다면 will-change : 애니메이션줄속성;

    - 바뀔 내용을 미리 렌더링해주는 속성.

- 많이 쓰면 브라우저 자체가 더 느려질 수 있음

https://dev.opera.com/articles/ko/css-will-change-property/

 
<div>

 

### 2. 하드웨어 가속
- 애니메이션이 너무 많아 CPU만으로 전부 연산이 불가능하다면 GPU 사용

> css
```css
.box {
  transform: translate3d(0, 0, 0);
}
```
- transform : translate3d 사용시 3D 이동도 가능

    - 이 속성의 경우 GPU를 사용해서 연산

- GPU를 이용해서 .box가 가진 transform 속성들 연산 방법

    - translate3d(0, 0, 0) 로 아무데도 움직이지 않는 3D 이동명령

        - 뒤에 필요한 transform을 더 적용

- 꼭 써야하는건 아니고 느리게 동작한다면 써볼 수 있는 것들

<br>
 

 