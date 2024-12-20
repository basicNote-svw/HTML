# 배경 css 속성 & margin collapse
배경관련 CSS 속성들
---
> css
```css
.main-background {
  background-image : url(../img/shoes.jpg);
  background-size : cover;
  background-repeat : no-repeat;
  background-position : center;
  background-attachment : fixed;
}
```
- background-size : px, % 단위 가능

- cover : 여백없이 배경으로 꽉 채우기

- contain : 배경이 잘리지 않게 꽉 채우기

- background-attachment : 웹사이트가 스크롤될 때 배경 동작

<br> 

### 배경 두개 겹치기
> css
```css
.main-background {
  background-image : url(../img/shoes.jpg), url(person.jpg);
}
```
- 콤마로 이미지 두개를 첨부

    - 투명도를 지원하는 png 이미지를 사용하면 더 재밌는 디자인 가능

<br>
 
### 배경에 검은색 틴트 주기 
> css
```css
.main-background {
  background-image: linear-gradient( rgba(0,0,0,0.5), rgba(0,0,0,0.5) ), url(이미지경로~~) ;
 
}
```
- linear-gradient : 색이 점진적으로 변하는 gradient 를 줄 수 있는 키워드

    - 투명도 0.5의 검은색을 입힌 후에 배경겹치기 사용

 
<br>

---

<br>
 

주의해야할 margin 버그 
---
> html
```html
<div class="배경">
  <p>안에 글씨</p>
</div>
```
- div 박스 안에 p 태그를 사용

    - p 태그에 상단 margin을 주기 위해 margin-top을 주게 되면

        - div와 p가 동시에 margin-top 생김
 
- 이 현상은 margin collapse effect 라고 부르는 일종의 버그

    - 박스들의 테두리가 만나면 margin이 합쳐짐
    
        - 박스가 내부에서 만나든 외부에서 만나든 상관 X

    - 둘 다 마진이 있으면 둘 중에 더 큰 마진 하나만 적용

- 두 박스의 테두리가 겹치지 않도록 한다면 더 정확한 마진 작업 가능 

    - ex) 부모 박스에 padding : 1px

<br> 
