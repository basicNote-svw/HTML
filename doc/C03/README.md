# Index
|No|Title|Link|
|-|-|-|
|01|Pseudo-element|[바로가기](./01)|
|02|Shadow DOM|[바로가기](./02)|
|03|만든 사이트 발행하기|[바로가기](./03)|
|04|Sass 셋팅|[바로가기](./04)|
|05|Sass 핵심문법|[바로가기](./05)|
|06|Sass : Mixin, use|[바로가기](./06)|
|07|HTML video, audio|[바로가기](./07)|
|08|transform & animation 으로 매끄러운 애니메이션 만들기|[바로가기](./08)|
|09|CSS Grid 레이아웃|[바로가기](./09)|
|10|position : sticky|[바로가기](./10)|
|11|CSS 3D animation|[바로가기](./11)|

<br>

---

<br>

Chart.js 라이브러리
---
- 차트 라이브러리인 Chart.js 사용법

    - 자바스크립트 몰라도 예제코드 복붙 하면 누구나 사용 가능

- chartjs.org

- Get started 버튼 클릭

- 예제코드를 html 파일에 붙여넣기

- chart.js 라이브러리 설치 파일 붙여넣기

    - 예제코드 위에 붙여넣기

<br>

> html
```html
<!-- chart.js 라이브러리 설치 파일 -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<!-- 예제 코드 -->
<canvas id="myChart"></canvas>

<script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: 'rgba(255, 99, 132, 0.2)',
            borderColor: 'rgba(255, 99, 132, 1)',
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    }
});
</script>
```
 
<br>

### 커스터마이징
- type: 'bar'

    - line, pie, doughnut 등으로 바꾸면 각각 라인, 파이, 도넛차트로 바뀜

- labels : 차트 안의 데이터와 라벨 수정가능

> html
```html
labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
    datasets: [{
        label: '# of Votes',
        data: [12, 19, 3, 5, 2, 3],
        fill : true,
```
- fill : true 

    - 라인차트의 경우 하단이 색칠됨

- backgroundColor

    - 색깔 수정가능 


<br> 

 
