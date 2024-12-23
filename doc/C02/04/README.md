# head 태그에 들어갈 내용 정리
 
> html
```html
<!DOCTYPE HTML>
<head>
  어쩌구
</head>
<body>
  저쩌구
</body>
```
- HTML 문서의 기본 템플릿 : head와 body 태그 포함

    - head태그 : 사이트 내에서 눈에는 보이지 않는 중요한 정보들

<br>

---

<br>

head태그 내에서 쓸 수 있는 중요한 태그들
---
### 1. 각종 CSS 파일들 
> html
```html
<head>
  <link href="css/main.css" rel="stylesheet">
</head>
```
- CSS 파일들을 첨부할 때 링크태그를 집어넣을 수 있음

    - 현 HTML 파일과 같은 위치에 있는 css폴더 안에 있는 main.css 파일을 첨부하라는 뜻

- 경로

    - css/main.css

        - 상대경로

        - 현재 HTML파일과 같은 경로에 있는 css라는 폴더 내의 main.css 파일

    - /css/main.css

        - 절대경로

        - 현재 사이트의 메인경로 (index.com)부터 시작해서 index.com/css/main.css 파일

    - 슬래쉬 기호가 처음부터 붙어있으면 사이트 메인경로부터 시작해라는 의미


<br>

### 2. 스타일 태그
> html
```html
<head>
  <style>
    .button {
      color : red;
    }
  </style>
</head>
```
- CSS 파일 생성 대신 \<style> 태그를 열어서 CSS를 작성하기도 함

- CSS 파일과 유사하게 동작

- \<body> 안에 넣어도 동작하긴 하지만 보통 \<head>에 넣음

    - html 파일안의 코드는 위에 있을 수록 먼저 읽음

    - \<body>태그 맨 밑에 두면 사이트 로딩시 스타일이 잠깐 깨질 수 있음

<br>

### 3. 사이트 제목
> html
```html
<head>
  <title>네이버입니다</title>
</head>
```
- 사이트 제목 (브라우저 탭에 뜨는 이름)


<br>

### 4. 여러가지 meta 태그
> html
```html
<head>
  <meta charset="UTF-8">
  <meta name="description" content="html 잘하는 방법">
  <meta name="keywords" content="HTML,CSS,JavaScript,자바스크립트,코딩">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```
- charset="UTF-8"

    - 사이트의 인코딩 형식 지정

- name="description" content="html 잘하는 방법"

    - 사이트의 검색 결과 화면에 뜨는 글귀를 수정하고 싶을 때 추가하는 속성

        - description : 구글 검색시 파란 제목으로 뜨는 글귀

        - keywords : 검색에 도움을 주는 키워드

- name="viewport"

    - 사이트 초기 zoom 레벨이나 폭 지정

        - width=device-width : 모바일 기기의 실제 폭으로 렌더링 해달라는 뜻

            - 실제 접속시 스마트폰 기기의 실제 가로폭을 보고 렌더링하라고 명령하는 부분

        - initial-scale=1 : 접속시의 화면 줌레벨 설정

- 반응형 웹을 만들 때 위 meta 태그를 복붙하고 시작    

<br>

### 5. open graph

|-|
|-|
|![이미지](./img/01.png)|

> html
```html
<head>
  <meta property="og:image" content="/이미지경로.jpg">
  <meta property="og:description" content="사이트설명">
  <meta property="og:title" content="사이트제목">
</head>
```
- facebook이 만든 og 라는 메타태그

    - 카톡 페북 이런 곳에 링크를 공유하면 박스가 뜨고 사이트 설명, 제목, 이미지 같이 뜸

    -  커스터마이징하고 싶으면 위 meta 태그를 따로 집어넣으면 됨

<br>

### 6. Favicon

> html
```html
<head>
  <link rel="icon" href="아이콘경로.ico" type="image/x-icon">
</head>
``` 
- 웹사이트 제목 옆에 뜨는 아이콘 커스터마이징

    - link 태그로 첨부

- ico 대신 png 파일 OK

    - ico가 호환성은 가장 좋음

- 32 x 32 사이즈로 제작

- 웹사이트를 바탕화면에 바로가기추가했을 경우 뜨는 아이콘도 커스터마이징 가능

    - rel="apple-touch-icon-precomposed" 

        - rel 속성 조정
        
            - OS마다 요구하는 rel 속성이 달라서 필요해지면 찾아서 적용

        - favicon generator : OS별로 알아서 만들어줌

 
<br>
 