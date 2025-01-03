# CSS 3D animation
transform 3D 스타일 회전 
---
> css
```css
transform : rotateX(180deg);
transform : rotateY(180deg);
transform : rotateZ(180deg);
```
- 각각 X,Y,Z축 회전 가능 

- X축 : 가로줄

    - rotateX() : 가로줄을 축으로 회전

- Y축 : 세로줄 

    - rotateY() : 세로줄을 축으로 회전

- Z축 : 얼굴과 모니터 간의 가상의 선 가정

    - rotateZ() : 가상의 선을 축으로 회전

 
<br>

---

<br>

종이처럼 뒤집히는 프로필사진 만들기
---
### step 1. 앞면과 뒷면 레이아웃을 각각 만들어줌
> html
```html
<div class="flip-outer">
    <div class="flip-inner">
      <img src="profile.png" class="front">
      <div class="back">
        <h4>개발자 김철용</h4>
        <p>Frontend Developer</p>
      </div>
    </div>
 </div> 
```
- 앞면엔 사진, 뒷면엔 글씨

- flip-inner라고 작명한 앞뒷면 둘다 감싸는 박스 생성

    - 마우스를 올리면 앞면과 뒷면을 각각 회전시키기 보다는 저 박스 전체를 회전시키면 편리

    - 앞면과 뒷면은 position : absolute로 띄워야 앞뒤로 배치 가능
    
        - position : relative 주는 용도

<br>

### step2. 앞면과 뒷면에 position : absolute

> css
```css
.flip-outer {
  width: 300px;
  height: 300px;
}

.flip-inner {
  width: 100%;
  height: 100%;
  position: relative;
}

.front {
  width: 100%;
  position: absolute;
  z-index : 1;   //안나오면 이것도 추가
}

.back {
  width: 100%;
  position: absolute;
  transform: rotateY(180deg);
} 
```
- absolute를 이용해 앞뒷면으로 배치

- 앞면이 안보이면 앞면사진에 z-index : 1; 추가

- 뒷면은 rotateY(180deg) 먼저 적용

    - 최종완성본에서 마우스를 올려 회전시켰을 때 제대로 글씨가 보임


<br>

---

<br>

### step3. 마우스를 올렸을 때 Y축으로 180도 회전시키도록 애니메이션 작성

> css
```css
.flip-inner {
  width: 100%;
  height: 100%;
  position: relative;
  transition: all 1s;
  transform-style: preserve-3d;
}

.flip-inner:hover {
  transform: rotateY(180deg);
} 
```
- hover시 Y축 180도 회전

- 애니메이션처럼 동작하도록 transition도 포함

- transform-style: preserve-3d; 

    - 어떤 요소를 회전시킬 때 3d 사물처럼 동작

<br>

---

<br>

step4. 뒷면에 비치는 그림자를 안보이게 처리
---
> css
```css
.front {
  backface-visibility: hidden;
} 
```
- 원래 어떤 HTML 요소를 뒤집으면 뒷면의 그림자가 보임

    - 그림자 안보이게 처리해주는 명령어

<br>
 