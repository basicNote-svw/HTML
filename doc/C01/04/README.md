# CSS 파일 만들고 첨부
- style 속성 안에 들어갈 코드가 매우 길어지면 HTML 더러워짐
    - 이걸 CSS 파일로 빼서 작성 가능

    - Cascading Style Sheet : 스타일 보관 파일

        - cascading : 폭포처럼 떨어진다는 뜻

<br>

---

<br>

CSS 파일 작성
---

### 00. CSS파일을 만든 후 HTML에 첨부
- 작업폴더에 .css 로 끝나는 파일 생성

- HTML 파일로 돌아와서 아래 코드 적용

```html
 <link href="css파일경로" rel="stylesheet">
```
- \<head>태그 안에 \<link>태그 넣기

    - href 속성에 .css 파일 경로 지정 

- ex) css 폴더 안에 main.css 파일 생성 

    - 경로 : css/main.css

    - 현재 html 파일과 같은 경로에 있는 css  폴더 내부의 main.css 파일을 첨부하라는 뜻

<br>

### 01. CSS파일에 스타일 작성 및 작명
```css
.profile { 
  width : 200px;
  display : block;
  margin : auto;
}
```
- 스타일을 적고 .클래스작명 후 { } 중괄호로 묶기

- 위의 코드는 3줄의 스타일을 .profile 클래스로 묶은 것

<br> 

### 02. HTML에 클래스 명을 첨부해서 스타일 지정
```html
<img src="lion.png" class="profile">
```
- class 속성을 열고 클래스명을 집어넣으면 

    - css 파일에서 묶어놨던 스타일들이 다 적용 

<br>

### 03. Brackets 에디터에선 클래스 만드는 작업을 빠르게 가능

- class 하나 미리 작명 후 커서 찍고 ctrl + e / command + e

    - \<link>로 연결해둔 css 파일이 열림
    
        - css 파일 쉽게 수정 가능

<br> 

#### 💡 CSS selector 
- class 말고 다른 식으로 스타일 묶기 
```css
.profile { font-size : 20px }  /*클래스*/
#special { font-size : 30px } /*아이디*/
p { font-size : 16px } /*태그*/
```
- 클래스 selector => .클래스명{ } 

    - 모든 class="클래스명"을 가진 요소에 스타일 적용 가능

- 아이디 selector => #아이디명 { } 

    - 모든 id="아이디명" 속성을 가진 요소에 스타일 적용 가능

- 태그 selector => p { 스타일~~ } 

    - 모든 <p> 태그에 스타일 적용 가능

<br>

---

<br>

셀렉터의 우선순위
---
- class, id를 동시에 가지는 html 요소라면 스타일이 겹칠 수 있음

    - 그럴 경우 우선순위 존재

```css
style="" (1000점)
#id (100점)
.class (10점) 
p (1점) 
```
- 정확한 카운트법은 아님

- 점수가 높을 수록 더 우선적으로 적용

<br>
 
