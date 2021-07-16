![](https://images.velog.io/images/sh981013s/post/3db176f7-9b75-4bae-9f07-346647ae6dc6/image.png)

# DOM API

### DOM API
#### Document Object Model, Application Programming Interface
- Document = HTML
- Object Model = DIV, SPAN, INPUT ... etc
- API = 웹사이트가 동작하기위한 프로그래밍 명령

```javascript
// HTML 요소(Element) 1개 검색/찾기
const boxEl = document.querySelector('.box');

// HTML 요소에 적용할 수 있는 메소드!
boxEl.addEventListener();

// 인수를 추가 가능!
boxEl.addEventListener(1, 2);

// 1 - 이벤트 (상황)
boxEl.addEventListener('click', 2);

// 2 - 핸들러 (실행할 함수)
boxEl.addEventListener('click', function () {
  console.log('Click!');
});

// 요소의 클래스 정보 객체 활용!
boxEl.classList.add('active');
let isContains = boxEl.classList.contains('active');
console.log(isContains); // true

box.classList.remove('active');
isContains = boxEl.classList.contains('active');
console.log(isContains); // false
```

---

```javascript
// HTML 요소 모두 검색/찾기
const boxEls = document.querySelectorAll('.box');
console.log(boxEls);

// 찾은 요소들 반복해서 함수 실행!
// 익명 함수를 인수로 추가!
boxEls.forEach(function () {});

// 첫 번째 매개변수 (boxEl) : 반복 중인 요소.
// 두 번째 매개변수 (index) : 반복 중인 번호.
boxEls.forEach(function (boxEl, index) {});

// 출력!
boxEls.forEach(function (boxEl, index) {
  boxEl.classList.add(`order-${index + 1}`);
  console.log(index, boxEl);
});
```