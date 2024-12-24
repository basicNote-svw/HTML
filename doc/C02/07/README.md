# Font Awesome 아이콘 넣기


[Font Awesome 5버전](https://fontawesome.com/v5.15/how-to-use/on-the-web/setup/hosting-font-awesome-yourself) 다운받아 첨부하기 
---
- Font Awesome 홈페이지의 다운로드 메뉴에서 다운받아 압축을 풀면 여러개의 폴더가 나옴

- 이 중에 CSS, Webfonts 두개의 폴더를 작업폴더에 복붙

- CSS 폴더 내의 all.css 파일을 하나만 head 태그 안에 첨부

> html
```html
<link href="님 작업폴더에 있는 all.min.css 파일 경로" rel="stylesheet">
```

<br>

---

<br>
 

Font Awesome CDN으로 첨부하기 
---
- CSS파일을 호스팅해주는 사이트가 제공하는 all.min.css 파일을 link태그로 첨부

    - 직접 다운받지 않고도 동일한 CSS파일 이용가능

- 구글에 font awesome 5 cdnjs 검색 

> html
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" />
```
- 장점 : 간편하고 빠름

    - 사이트가 다운이 되면 CSS 파일도 이용 불가능 → 불안정

<br>

---

<br>

Font Awesome 아이콘 넣기
---
- Font Awesome 5버전 홈페이지의 icons 메뉴

- 마음에 드는 아이콘 선택

- 예제 코드를 HTML에 복붙

> html
```html
<i class="fas fa-book"></i>
```
- 책 아이콘 넣기

    - 사이즈나 색 수정은 글자 수정하는 것과 똑같이 작업 

<br> 