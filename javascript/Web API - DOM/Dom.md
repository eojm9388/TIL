# Dom 이란?

Document Object Model의 약어로 웹 문서를 제어하기 위해서 웹 문서를 객체화한 것을 말한다.

객체는 값을 나타내는 `프로퍼티`와 어떠한 수행을 하는 `메서드`를 갖고 있다.

### 웹 문서 body에 `"Hello World1` 텍스트 삽입

```javascript
document.querySelector('body').innerHTML = 'Hello World!';
document.body.innerHTML = 'Hello World!';
```

### 웹 문서에서 H1 태크 가져와서 삭제하기

```javascript
const $h1 = document.querySelector('h1');
$h1.remove();
```

## DOM 요소 조작하기

- DOM 요소 조회

  - `getElemntById()`
  - `getElementsByTagName()`
  - `querySelector()`
  - `querySelectorAll()`

- DOM 요소 조작
  - `dom.textContent` = 'Hello World!';
  - `dom.innerHTML` = 'Hello World!';
