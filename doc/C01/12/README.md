# form & input
form 은 form 태그로 생성
---
 > html
```html
<form action="" method="get">
  <input>
</form>
```
- \<form action=""> : 작성한 내용이 어떤 서버 경로로 전달될지 기재

- \<form method=""> : 작성한 내용이 어떤 방식으로 서버에 전달될지 기재
- input태그는 닫지 않음

<br>

---

<br>

input의 type
---
> html
```html
<input type="text">         <!-- 일반 글자 입력 -->
<input type="email">        <!-- 이메일 입력 -->
<input type="password">     <!-- 패스워드 입력 -->
<input type="radio">        <!-- 라디오 버튼 소환 -->
<input type="date">         <!-- 날짜 입력 -->
<input type="file">         <!-- 파일 첨부 -->
<input type="checkbox">     <!-- 체크박스 소환 -->
<input type="submit">       <!-- 전송 버튼1 -->
<button type="submit">전송</button>     <!-- 전송 버튼2 -->
<select>                    <!-- 셀렉트박스 소환 -->
  <option>옵션1</option>    <!-- 셀렉트박스 옵션 -->
</select>
<textarea></textarea>       <!-- 큰 인풋박스, 드래그하여 원하는 크기로 조절 가능, row="10" 속성으로 최초 크기 지정 가능 -->
```
- 가장 자주 쓰는 것만 알아두고 더 필요한건 찾아서 쓰기

<br>

---

<br>

input에 넣는 속성들
---
> html
```html
<input placeholder="어쩌구" value="어쩌구" name="age">
```
- placeholder : 배경 글자

- value : 미리 입력된 값

- name : 서버 기능개발에 필요한 인풋의 이름 설정 가능

<br>
 
---

<br>
 
HTML 속성으로 CSS 셀렉터 사용 가능
---
> css
```css
input[type=email] {
  color : grey
}
```
- input[속성명=속성값]

    - input 의 type 속성이 email 인 요소만 찾아서 스타일 지정 

        - 폼에서 특히 유용하게 사용

 
<br>
 
---
 
<br>
 
전송버튼
---
> html
```html
<button type="submit">전송</button>
<input type="submit">
```
- 둘 중 하나 사용

- \<form> 태그 안에 있어야 잘 작동

<br> 

---

<br>


form 레이아웃 제작
---
- 예시 디자인 위에 박스부터 그려놓고 그대로 div 로 구현

> html 
```html
<form>
  <div class="w-100">
    <input>
  </div>
  <div class="w-50">
    <input>
  </div>
  <div class="w-50">
    <input>
  </div>
  <div class="w-100">
    <textarea></textarea>
  </div>
</form>
```
- 가로로 꽉찬 input들 = w-100 이라는 div

    - w-100 = width : 100%

- 가로로 반반 차지할 input들 = w-50 이라는 div

    - w-50 = width : 50%; float : left 

- 만약 float 사용시 clear : both 필수
 
<br>
 
---
 
<br>
 

input 태그 디자인
---
- 가로로 100% 폭, padding 조금, box-sizing : border-box 적용

    - border-box 안해놓으면 폭이 padding 을 포함해서 조금 커질 수 있기 때문

<br>

---

<br>

전송버튼
---
> html
```html
<form>
  <button type="submit">전송</button>
  <input type="submit">
</form>
```
- 두개 중 하나 사용

<br>

---

<br>
 

label 태그와 for 속성
---
> html
```html
<input type="checkbox" id="subscribe">
<label for="subscribe">누르기</label>
```
- label 과 for 속성을 적절히 활용하면 input 대신 label 눌러도 input 선택 가능

    - input 의 id, label 의 for 속성을 똑같이 맞줘주기

- \<input> 에 제목이 필요할 때도 h, p 태그 대신 \<label> 태그를 가끔 이용


 

<br>
