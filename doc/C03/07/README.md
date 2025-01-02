# HTML video, audio
비디오 삽입
---
- 비디오 파일을 작업폴더안에 준비 후 코드 작성

> html
```html
<video>
  <source src="비디오파일경로" type="video/타입">
</video>
```


<br>

---

<br>

비디오 태그에 넣을 수 있는 속성
--

> html 
```html
<video autoplay muted loop poster="썸네일경로" preload="metadata">
  <source src="비디오파일경로">
</video>
```
- muted : 음소거상태

- autoplay : 자동재생 (muted와 함께 넣어야 동작)

- poster="경로" : 썸네일이미지

- preload : 영상 선다운로드 여부 선택 (auto:미리 다운O, metadata:미리 다운 적당히, none:미리 다운X 사용가능)

- loop : 무한반복재생


<br>

비디오를 '배경'으로 쓰고싶다면 
---
- Youtube 비디오 넣는 방법처럼 \<iframe> 코드 복붙 X

- 비디오 파일을 직접 다운받아서 같은 폴더에 준비 후 레이아웃 작성

> html
```html
<div class="video-box">
  <video class="video-container" autoplay muted loop>
    <source src="img/bridge.mp4" type="video/mp4">
    <source src="img/bridge-m.webm" type="video/mp4">
  </video>
  <h3 class="video-title">Buy Our Shoes!</h3>
</div>
``` 
- source 파일형식 여러개 준비할 경우 

    - 여러가지 확장자의 비디오 파일이 있으면 \<source>에 모두 넣기

        - 브라우저에 최적화된 비디오 파일 자동 선택됨

<br>

> css
```css
.video-box {
  height: 500px;
  width: 100%;
  overflow: hidden;
  position: relative;
}

.video-container {
  position: absolute;
  width : 100%;
  top: 50%;
  left: 50%;
  transform : translate(-50%,-50%);
  z-index: -1;
}
```
- 비디오가 배경처럼 크게 보이게 하는 작업

- 어떤 요소를 가운데정렬을 하고 싶을 때

    - position absolute
    
    - top, left, transform 속성을 차례로 작성

        - position relative를 가진 부모에 대해 정가운데 위치시킬 수 있음

    - max-width, width 등으로 크기 조정

- 원하는 html을 \<video> 하단에 적으면 비디오 위에 글 작성 가능

 
<br>

---

<br>
 
audio 삽입
---
> html
```html
    <audio src="경로" controls></audio>
```
- autoplay 작동 X

  - 자동 재생하려면 javascript 작성

- preload="" : 설정 가능

- \<source> 사용 가능

<br>