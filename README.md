# 웹

## 브라우저

브라우저의 기능 - 사용자가 선택한 자원(URI)를 서버에 요청하고 브라우저에 포함하는 것

브라우저 엔진 - 사용자 인터페이스와 렌더링 엔진 사이 동작 제어
렌더링 엔진 - 요청한 콘텐츠를 파싱하여 화면에 표시
통신 - HTTP 요청과 같은 네트워크 호출

_`렌더링 엔진이 문서 파싱 -> DOM 노드로 변환, 스타일 요소 파싱 (렌터 트리 생성) -> 노드를 정확한 위치에 배치 -> 그리기`_

_`한번에 배치, 그리기가 아니라 나머지 내용을 기다리는 동시에 일부를 먼저 화면에 표시`_

<hr >

## DOM - 문서 객체 모델

_`웹 페이지를 자바스크립트로 제어하기 위한 객체 모델`_

BOM(브라우저 객체 모델) : 브라우저와 관련된 객체들의 집합. 최상위 객체는 window. DOM은 BOM의 하나, window의 하위 객체

즉 DOM은 웹 브라우저가 HTML 페이지를 인식하는 방식.
자바스크립트를 이용해서 HTML 문서에 없는 문서 객체를 생성 가능. 동적 문서 객체 생성.

_`원본 HTML -> DOM과 CSSOM 두 모델을 이용해 렌더 트리 생성 -> 렌더링 실행`_

<hr>

## 객체 지향 프로그래밍 (OOP)

_`프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체를 만들고, 객체들 간의 상호작용을 통해 로직을 구성하는 프로그래밍 방법`_

장점

- _`코드 재사용 용이`_ : 다른 사람이 만든 클래스를 이용할 수 있고, 상속을 통해 확장해서 사용 가능.
- _`유지 보수 쉬움`_ : 절차 지향 프로그래밍과 달리 잘못된 부분이 클래스 내부에 있기 때문에 해당 클래스만 수정하면 됨.
- _`대형 프로젝트에 적합`_ : 클래스 단위로 모듈화 시켜서 개발 가능. 업무 분담이 쉬움.

단점

- 처리 속도가 상대적으로 느림
- 객체가 많으면 용량이 커짐
- 설계에 많은 시간과 노력

키워드

- _`클래스` + `인스턴스`_

  클래스 : 데이터를 만들기 위해 추상화를 거쳐 어떤 집단의 `속성과 행위`를 `변수와 메서드`로 정의한 것.
  인스턴스(객체) : 클래스에서 정의한 것을 토대로 실제 메모리에 할당 시킨 것. 실제 프로그래밍에 사용되는 데이터.

- _`추상화`_

  불필요한 정보는 숨기고 중요한 정보만을 표현함으로써 공통의 *속성과 기능*을 묶어 이름 붙이는 것

- _`캡슐화`_

  목적 : 코드를 재수정 없이 재활용하는 것. 캡슐화를 통해 관련된 기능과 특성을 한곳에 모으고 분류하기 때문에 재활용이 원활.

  OOP에서 기능과 특성의 모음을 클래스라는 캡슐에 분류해 넣는 것이 캡슐화

- _`상속`_

  부모 클래스의 속성과 기능을 그대로 이어받아 사용하고 기능의 일부분을 변경해야 할 경우 상속받은 자식 클래스에서 해당 기능만 다시 정의하여 사용할 수 있음.

- _`다형성`_

  하나의 변수명, 함수명 등이 상황에 따라 다른 의미로 해석 가능함.

  오버라이딩 : 부모 클래스의 변수, 메서드를 재정의 하는 것.(JS에서는 매개변수, 리턴값 등의 자유도가 높음)
  오버로딩 : 같은 이름의 함수를 여러개 정의하고 매개 변수와 타입을 다르게 하여 매개 변수에 따라 다르게 호출할 수 있게 하는 것. (JS에서는 없는 개념. 함수 내에서 케이스 처리를 통해 구현)

- _`Getter, Setter`_

  메서드를 통해서 접근하기 때문에, 메서드 안에서 올바르지 않은 입력에 대해 사전 처리가 가능함.

## 함수형 프로그래밍

_`입력과 출력이 통제된 순수 함수 위주로 프로그래밍 하는 것`_

- 입출력이 순수해야 한다.

  반드시 하나 이상의 인자를 받고, 받은 인자를 처리하여 결과물을 돌려줘야 한다. 인자를 제외한 다른 변수는 사용하면 안됨.

- Side Effect가 없어야 한다.

  프로그래머가 바꾸고자 하는 변수 외에는 바뀌어서는 안된다. 원본 데이터는 불변해야한다.

합성 함수

둘 이상의 함수를 조합하여 만들어진 함수. 여러 작은 순수 함수들로 이루어져있기 때문에, 함수들을 연쇄적 또는 병렬적으로 호출하여 더 큰 함수를 만드는 과정

_`함수형 프로그래밍은 순수 함수를 조합하고, 변경가능한 데이터 및 부작용을 피하여 소프트웨어를 만드는 프로세스이다`_

<hr>

# JavaScript

## 자바스크립트 엔진

_`V8엔진`_

메모리힙 : 메모리 할당이 이루어지는 곳

콜스택 : 코드가 실행되면서 스택 프레임이 쌓이는 곳

_`콜스택`_

자바스크립트는 싱글쓰레드 언어, 콜스택이 하나임. 콜스택에 수행할 함수가 있으면, 브라우저는 아무것도 할 수 없음. => 비동기 콜백(asynchronous callbacks)

콜백 : 비동기 함수가 결과를 반환하기를 기다릴수 있는 간단한 방식

콜스택 : 함수의 호출을 기록하는 구조. 후입선출

콜백큐(이벤트큐) : 처리할 이벤트의 목록.

이벤트루프 : 콜스택이 비어있드면 큐에서 이벤트를 콜스택으로 보냄. 틱(tick)

<hr>

## 자바스크립트의 비동기 처리

_`특정 코드의 연산이 끝날 때까지 코드의 실행을 멈추지 않고, 다음 코드를 먼저 실행하는 자바스크립트의 특성`_

### 콜백

_`특정 로직이 끝났을 경우, 원하는 동작을 실행시킬 수 있음.`_

### Promise

_`자바스크립트 비동기 처리에 사용되는 객체`_

프로미스의 3가지 상태

- Pending(대기) : 비동기 처리 로직이 아직 완료되지 않은 상태
- Fulfilled(이행) : 비동기 처리가 완료되어 프로미스가 결과 값을 반환해준 상태
- Rejected(실패) : 비동기 처리가 실패하거나 오류가 발생한 상태

에러 처리 방법

- then()의 두 번째 인자로 에러를 처리하는 방법

```javascript
getData().then(success, error);
```

- catch()를 이용하는 방법

```javascript
getData()
  .then()
  .catch();
```

### async & await

_`자바스크립트의 비동기 처리 패턴 중 하나`_

```javascript
async function 함수명() {
  // 아래의 메서드는 반드시 promise 객체를 반환해야 함.
  await 비동기_처리_메서드_명();
}
```

에러 처리 방법

```javascript
async function 함수명() {
  try {
    await 비동기_처리_메서드_명();
  } catch (error) {
    console.log(error);
  }
}
```

<hr>

## IIFE(즉시 호출 함수 표현식)

함수의 선언 : 자바스크립트의 실행 컨텍스트에 로딩되어 있으므로 언제든 호출 가능.

함수의 표현 : 해당 라인에 도달 했을때만 실행.

```javascript
let a = (function() {
  return 'IIFE!!';
})()(
  // a == 'IIFE!!'

  function() {}
)(); // ()로 둘러싸서

let user = (function() {
  let name = 'gyeol';

  return {
    get: function() {
      return name;
    },
    set: function(newName) {
      name = newName;
    },
  };
})();
```

## 원시타입과 참조타입

### 원시타입

- Boolean
- Number
- String
- Null
- Undefined
- (Symbol)

`모든 원시 타입은 리터럴 형식이 있다.`

```javascript
let name = 'gyeol';
let age = 25;
let happy = true;
let money = null;
let house = undefined;
```

`자바스크립트 변수는 원시타입 값이 그대로 저장된다.` <br>
(메모리 참조가 아닌 값의 복사)

```javascript
let color1 = 'red';
let color2 = color1;
color1 = 'blue';
console.log(color2); // 'red'
```

### 참조타입

- Object
- Array
- function

`참조타입 데이터는 크기가 정해져 있지 않고, 변수에 할당될 때 값이 직접 해당 변수에 저장될 수 없으며, 변수에는 데이터에 대한 참조만 저장된다.`<br>(데이터의 참조 복사)

```javascript
let x = { count: 1 };
let y = x;
x.count = 2;
console.log(y.count); // 2
```

## for ... in & for ... of

### for ... in 반복문

객체의 속성들을 반복하여 작업 수행 가능. <br>
모든 객체에서 사용 가능. <br>
객체의 key 값에 접근 가능하나, value에 접근 불가

### for ... of 반복문

객체가 [Symbol.iterator] 속성을 가지고 있어야만 가능<br>
객체의 value에 접근

```javascript
let iterable = [2, 4, 6];
iterable.a = 'hello';

for (let i in iterable) {
  console.log(i); // 0,1,2,"a"
}

for (let i of iterable) {
  console.log(i); // 2,4,6
}
```

<hr>

## 실행 컨텍스트

`실행 컨텍스트 : 자바스크립트 코드가 실행되고 연산되는 범위를 나타내는 추상적인 개념`

### 실행 컨텍스트

코드가 실행되고 있는 구역, 범위에 대한 개념

- Global Execution Context : 전역 컨텍스트
- Functional Execution Context : 함수가 호출될 때마다, 해당 함수에 대한 실행 컨텍스트가 생성됨. 각각의 함수들은 자신만의 실행 컨텍스트를 가지며, 함수가 호출이 되어야 실행 컨텍스트가 만들어진다.

### 실행 스택

스택 : LIFO(후입선출) 자료 구조.

\_맨 처음 전역 컨텍스트를 만들고 스택에 push. 다른 함수가 호출되면 해당 함수에 대한 실행 컨텍스트를 생성하고, 스택에 push <br> JS 엔진은 실행 컨텍스트가 호출의 맨 위 함수를 실행.

### 실행 컨텍스트 생성 과정

1. Creation Phase

   - 지역 환경 내에 함수와 변수 기록
   - 지역 환경에서 변수를 찾지 못했다면, 외부 환경에서 찾음
   - This binding

2. Execution Phase
   - 전역 컨텍스트에서 코드가 실행되며 각각의 변수에 값 할당
   - 함수가 실행되면 그 함수의 실행 컨텍스트 생성
   - 함수가 값을 리턴하면 스택에서 제거됨. 전역 변수의 값 업테이트

<hr>

## var, let, const

### var

- 재선언 가능
- 함수 스코프
- 호이스팅 발생

### let

- 재선언 불가능
- 재할당 가능
- 블록 스코프

### const

- 재선언, 재할당 불가능
- 블록 스코프

> let과 const 역시 호이스팅이 발생하지만, 초기화가 실행되기 전까지 TDZ(Temporal Dead Zone)에 존재하여 접근 할 수 없음.

<hr>

## Hoisting & Scope

### Hoisting

`변수의 선언문을 유효 범위의 최상단으로 끌어올리는 행위`

### Scope

`유효 범위 : JS에서는 { } 블록 단위가 아닌 funtion{ } 함수 단위 Scope`<br>

> 변수 선언 -> 함수 선언 -> 변수 할당

## Closure

`함수 밖에서 선언된 변수를 함수 내부에서 사용할 때 Closure가 생성됨`

함수가 종료되어도 함수 내부에서 외부에서 생성된 변수를 계속 사용할 수 있도록 클로저가 이러한 _환경을 그대로 기억하는 공간_ 을 형성

<hr>

## This

- 객체가 메서드를 호출할 경우, 메서드를 호출한 객체가 This
- 일반 함수의 경우, 브라우저 상에서 window가 This
- 이벤트가 발생한 경우, 이벤트를 발생한 객체가 This

### call, apply, bind

명시적 this 바인딩

```javascript
let example = function(a, b, c) {
  console.log(Array.prototype.join.call(arguments));
  // arguments는 유사 배열, 따라서 배열의 메소드 사용 X
  // console.log(arguments.join()) // Uncaught TypeError
  // so, join() 함수를 call()을 이용해 this를 변경해 사용 가능
  return a + b + c;
};

example(1, 2, 3);
example.call(this, 1, 2, 3); // this 변경
example.apply(this, [1, 2, 3]); // 인자를 배열 형식으로
example.bind(this); // this만 바꾸고 호출 X
```

<hr>

# React

SPA(Single Page Application)에서 사용자 인터페이스를 구성하는데 사용되는 오픈 소스 프론트엔드 JS 라이브러리

### 특징

- RealDOM 대신 virtualDOM을 사용
- 서버 사이드 렌더링을 지원
- 단방양 데이터 흐름 / 바인딩
- UI 구성 요소 재사용 가능

### 생성

- Functional components
- Class components : state, lifecycle, ref
  - React.Component
  - React.PureComponent

<hr>

## Hook

기존 Class component 중심의 단점

- state와 관련된 로직을 재사용하기 어려움
- lifecycle 관련 메서드들의 복잡성

### useState

```javascript
const example = () => {
  // count 라는 이름의 state와 setState 선언, 초기값 0
  const [count, setCount] = useState(0);
};
```

- destructuring 을 이용해 할당
- 하나의 컴포넌트 내에서 State Hook을 여러 개 사용 가능

### useEffect

```javascript
const example = () => {
  const [count, setCount] = useState(0);

  useEffect(() => {
    // 기본적으로 매 렌더링 후 effect 실행
    document.title = `clicked ${count} times`;

    //Effect 해제. componentWillUnmount와 같은 기능
    return () => {
      document.title = `Reset`;
    };
  }, [count]); // count가 변경되었을 때만 effect 실행
};
```

### useRef

```javascript
const example = () => {
  const divEl = useRef(null);
  console.log(divEl); // 순수 자바스크립트 객체 생성
  console.log(divEl.current); // 자식에게 접근하는 경우 사용
};
```

### useContext

```javascript
const ExampleContext = React.createContext()
...

const Example = () => {
  const { state , action } = useContext(ExampleContext)
}
```
