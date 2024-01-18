# HTML 요소 조작하기

우리가 HTML에 스타일을 적용할 때 HTML 요소를 선택한 후에 적절한 요소를 선택한 후에 적절한 CSS 속성을 사용하여 스타일 했듯이 HTML 조작도 마찬가지입니다. HTML 문서를 조작하기 위해서는 HTML 요소를 선택한 후에 함수나 속성을 사용하여 HTML 요소를 제어! 즉 조작할 수 있습니다.

## HTML 요소 선택하기

### get 메서드

- `document.getElementById` - 모든 HTML 요소에는 고유한 ID를 할당받을 수 있습니다. `getElementById`를 이용해 요소를 찾을 수 있습니다.
- `document.getElementsByClassName` - HTML 클래스 명으로 요소를 찾을 수 있습니다.
- `document.getElementsByTagName` - HTML 태그명으로 요소를 찾을 수 있습니다.
  > 예시 HTML
  >
  > ```HTML
  > <ul id="list">
  > 	<li class="item">
  > 	<li class="item">
  > 	<li class="item">
  > </ul>
  > ```
  >
  > 예시 get 메서드
  >
  > ```javascript
  > document.getElementById('list') <!-- ul 선택 -->
  > document.getElementsByClassName('item') <!-- li태그 3개 선택 -->
  > document.getElementsByTagName('li') <!-- li태그 3개 선택 -->
  > ```
  >
  > DOM 메서드가 반환하는 커렉션은 자바스크립트 배열이 아니라 HTMLCollection의 인스턴스로, 배열 비슷한 객체입니다.
  >
  > ***

### DOM 요소 쿼리

get 메서드와 같은 방법도 유용하지만, ID나 클래스, 태그 이름 같은 한 가지 조건이 아니라 다른 요소와의 관계를 사용해 원하는 요소를 찾는 훨씬 더 강력하고 범용적인 메서드도 있습니다.

`querySelector`와 `querySelectorAll`은 CSS 선택자를 사용해 요소를 찾는 메서드입니다.

- `document.querySelector(CSS Selector`) - 지정된 선택자에 일치하는 문서 내 첫 번째 요소를 반환합니다. 일치하는 요소가 없으면 null을 반환합니다.
- `document.querySelectorAll` - 지정된 선택자에 일치하는 요소 목록을 반환합니다.

## HTML 요소 조작하기

### 콘텐츠 수정하기

요소를 찾는 방법은 이제 알았습니다. 그러면 찾은 요소로 무엇을 할 수 있을까요? 우선! 콘텐츠 수정부터 시작해보도록 하겠습니다. 모든 요소에는 `textContent`와 `innerHTML` 프로퍼티가 있습니다. 이 프로퍼티를 통해 요소의 콘텐츠를 가져오거나 수정할 수 있습니다.

- `textContent` - HTML 태그를 모두 제거하고 순수한 텍스트 데이터만 제공합니다.
- `innerHTML` - HTML 태그를 그대로 제공합니다.

### 속성 제어하기

- `setAttribute` - 요소에서 주어진 이름의 속성값을 입력합니다.
- `getAttribute` - 요소에서 주어진 속성의 값을 가져옵니다.
- `removeAttribute` - 요소에서 주어진 이름의 속성을 제거합니다.

## HTML 요소 스타일링

### 요소 프로퍼티 직접 수정

- `style` - style 프로퍼티를 사용하여 직접 수정

```javascript
const btn = document.getElementById('button');
btn.style.color = 'white';
btn.style.backgroundColor = 'black';
```

### CSS 클래스 이용

- `classList` - classList 객체를 사용하여 class 를 수정

```JavaScript
const btn = document.getElementById('button');
btn.classList.add('dark')
btn.classList.remove('dark')
```
