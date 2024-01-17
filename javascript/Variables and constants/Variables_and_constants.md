# 변수와 상수
대다수의 자바스크립트 애플리케이션은 사용자나 서버로부터 입력받은 정보를 처리하는 방식으로 동작한다.

변수는 정보를 저장하는 용도로 사용된다.

## 변수
변수는 데이터를 저장할 때 쓰이는 `이름이 붙은 저장소`이다. 

자바스크립트에선 `let` 키워드를 사용해 변수를 생성한다.
``` javascript
let message;
```
데이터를 저장하면, 변수에 연결된 메모리 영역에 저장되었기 때문에, 변수명을 이용해 문자열에 접근할 수 있다.
``` javascript
let message;
message = 'Hello!';

alert(message); // 변수에 저장된 값을 보여줍니다.
```

아래와 같이 변수 선언과 값 할당을 한줄에 작성할 수도 있다.
``` javascript
let message = 'Hello!'; // 변수를 정의하고 값을 할당합니다.

alert(message); // Hello!
```

한줄에 여러 변수를 선언하는 것도 가능하다.
``` javascript
let user = 'John', age = 25, message = 'Hello';
```

이 방법은 코드가 짧아보이기는 하지만, 가독성을 위해 한 줄에는 하나의 변수를 작성하는 것이 좋다.

변수는 원하는 만큼 값을 변경할 수도 있다.
``` javascript
let message;

message = 'Hello!';

message = 'World!'; // 값이 변경되었습니다.

alert(message);
```
값이 변경되면, 이전 데이터는 변수에서 제거된다.

변수 두 개를 선언하고, 한 변수의 데이터를 다른 변수에 복사할 수도 있다.

``` javascript
let Hello = 'Hello world!';

let message;

// Hello의 'Hello world' 값을 message에 복사합니다.
message = Hello;

// 이제 두 변수는 같은 데이터를 가집니다.
alert(Hello); // Hello world!
alert(message); // Hello world!
```

> 변수를 두 번 선언하면 에러가 발생한다.
>
> 변수는 한 번만 선언해야 한다.
>
> 같은 변수를 여러 번 선언하면 에러가 발생한다.
>``` javascript
>let message = "This";
>// 'let'을 반복하면 에러가 발생합니다.
>let message = "That"; // SyntaxError: 'message' has already been declared
>```
>
> 따라서 변수는 딱 한 번만 선언하고, 선언한 변수를 참조할 때는 `let` 없이 변수명만 사용해 참조해야 한다.

### 변수 명명 규칙
1. 변수명에는 오직 문자와 숫자, 그리고 기호 `$`와 `_`만 들어갈 수 있다.
2. 첫 글자는 숫자가 될 수 없다.
3. 대/소문자 구별
4. 예약어는 변수명으로 사용할 수 없다.

``` javascript
let userName;
let test123;
```

여러 단어를 조합하여 변수명을 만들 땐 `카멜 표기법`이 흔히 사용된다. 카멜 표기법은 단어를 차례대로 나열하면서 첫 단어를 제외한 각 단어의 첫 글자를 대문자로 작성한다. `myVeryLongName`처럼

## 상수
변화하지 않는 변수를 선언할 땐, `let` 대신 `const`를 사용한다.

`const`로 선언한 변수를 '상수'라고 부른다. 상수는 재할당할 수 없으므로 상수를 변경하려고 하면 에러가 발생한다.

```javascript
const myBirthday = '18.04.1982';

myBirthday = '01.01.2001'; // error, can't reassign the constant!
```

### 대문자 상수
기억하기 힘든 값을 변수에 할당해 별칭으로 사용하는 것은 널리 사용되는 관습이다.


## 요약
`var`, `let`, `const`를 사용해 변수를 선언할 수 있다. 선언된 변수엔 데이터를 저장할 수 있다.

- let – 모던한 변수 선언 키워드이다.
- var – 오래된 변수 선언 키워드이다. 잘 사용하지 않는다.
- const – let과 비슷하지만, 변수의 값을 변경할 수 없다.
- 변수명은 변수가 담고 있는 것이 무엇인지 쉽게 알 수 있도록 지어져야 한다.


  



