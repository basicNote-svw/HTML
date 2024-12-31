# Sass : Mixin, use 등

Sass 문법 4. 코드를 한단어로 축약하는 @mixin
---
- 변수랑 매우 유사

    - 변수 : 짧은 값 하나만 저장해서 쓸 수 있는 문법

    - @mixin : 스타일 여러줄을 한 단어로 치환해서 사용가능

<br>

> scss
```scss
@mixin 버튼기본디자인() {
  font-size : 16px;
  padding : 10px;
}

.btn-green {
  @include 버튼기본디자인();
  background : green;
}
```
- @mixin 기재

- 작명 ( ){ }

- 한 단어로 치환할 값들을 중괄호 안에 나열

- @include mixin이름 으로 사용

    - mixin 안에 있던 코드가 그 자리에 복붙됨

- 여러줄을 한 단어로 치환해서 쓰고싶을 때 쓰는 문법

    - extend 문법과 유사

<br>

- mixin만의 장점

    - 긴 코드를 한 단어로 축약 가능

    - 내부에 묶어둔 속성들에 구멍을 하나 뚫어줄 수 있음

        - 사용할 때마다 각각 다른 내용 넣을 수 있음

> scss
```scss
@mixin 버튼기본디자인($구멍) {
  font-size : 16px;
  padding : 10px;
  background : $구멍;
}
```
- 소괄호의 역할 : 구멍

    - 버튼기본디자인() 사용시 소괄호구멍 안에 아무거나 값을 넣을 수 있음

- background : 옆에있는 또 하나의 구멍으로 들어감

- 버튼기본디자인(테스트)

    - 테스트라는 글자 들어감
    
        - background : 테스트

<br>

> scss
```scss
@mixin 버튼기본디자인($구멍) {
  font-size : 16px;
  padding : 10px;
  background : $구멍;
}

.btn-green {
  @include 버튼기본디자인(#229f72);
}
```

> .btn-green 클래스에 채워질 내용
```scss
.btn-green {
  font-size : 16px;
  padding : 10px;
  background : #229f72;
}
```

<br> 

---

<br>

Sass 문법 5. @use와 언더바 파일
---
- CSS파일마다 맨위에 첨부하는 reset 같은걸 자주 복붙한다면 import문법 사용

> scss 
```scss
@use 'reset.scss';
```
- reset.scss 파일을 해당 SCSS파일에 전부 복붙

    - 파일이 다른 폴더 안에 있다면 '폴더명/reset.scss' 이런 식으로 경로 기재  

<br>

> scss
```scss
@use '_reset.scss';
```
- scss 파일명 작명시 언더바를 파일명 맨 앞에 붙이는 경우

    - 이 파일은 CSS파일로 따로 컴파일하지 말아달라는 의미

    - 첨부용 파일이라는 뜻

<br>
 
> scss
```scss
@use '_reset.scss';

reset.$변수명;  /* 다른 파일의 변수쓰는법 */
@include reset.mixin이름();  /* 다른 파일의 mixin쓰는법 */
```
- @use 해온 다른 파일에 있던 $변수와 @mixin 가져와 사용 가능

    - 이 경우엔 꼭 파일명을 앞에 붙여야함

- 다른 파일에서 자주 사용할법한 _button.scss _navbar.scss 파일 등 미리 작성

    - 첨부식으로 CSS 개발 가능

- @use 사용할 땐 파일 경로만 조심

 

 

 

 

 
<br>