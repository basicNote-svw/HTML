# HTML 기초와 개발환경 셋팅
에디터 설치
---
[Brackets 에디터](https://brackets.io/) (윈도우는 .msi 맥은 .dmg)

[Visual Studio code 에디터](https://code.visualstudio.com/)

<br>

(참고1) 에디터 상단 메뉴에서 '폴더열기'로 먼저 작업폴더 오픈 후 파일 생성 및 코딩 진행

(참고2) 에디터의 번개 버튼을 누르시면 실시간 미리보기가 가능

(참고3) ctrl + s 단축키로 파일 저장 (맥북은 ctrl 대신 command)

<br>

#### 💡 Brackets 에디터 실시간 미리보기가 잘 안되는 경우

- 번개버튼 다시 껐다 켜보거나 파일 저장 하기

<br>

---

<br>

HTML?
---
- 웹페이지를 만들고 디자인하고 싶을 때 사용

  - 세상에 존재하는 모든 웹페이지는 html 언어로 작성

- HTML은 Hypertext Markup Language의 약자

   - Markup Language (마크업 언어) : 자료의 구조를 표현하기 위한 언어

> 요약
```
  웹페이지에 우리가 글넣고 그림넣고 박스넣고 버튼넣고 .. 자료를 입력
  
  그 자료들이 어디에 배치되는지 그런 것들을 기록하기 위해 존재하는 언어가 바로 HTML
  
  HTML 언어로 글넣고 그림넣고 하면 웹페이지가 되는 것
```
 
<br>
 
HTML 파일 기본 템플릿
---
> index.html
```html
  <!DOCTYPE html>
  <html>
      <head>
          <meta charset="UTF-8">
          <title>Documents</title>
      </head>
      <body>
          안녕하세요
      </body>
  </html>
```
- HTML 문서는 .html로 끝나도록 저장

- 모든 HTML 문서는 위의 코드를 가지고 있어야 HTML 파일로 인식

- <head> 내부엔 사이트 생성에 필요한 인코딩형식, 사이트제목, 필요한 CSS나 JS파일 등 작성

- <body> 내부엔 실제 웹사이트에서 보여줄 글, 그림 등 작성

<br>


