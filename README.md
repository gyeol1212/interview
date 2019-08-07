# 웹

## 브라우저

브라우저의 기능 - 사용자가 선택한 자원(URI)를 서버에 요청하고 브라우저에 포함하는 것

브라우저 엔진 - 사용자 인터페이스와 렌더링 엔진 사이 동작 제어
렌더링 엔진 - 요청한 콘텐츠를 파싱하여 화면에 표시
통신 - HTTP 요청과 같은 네트워크 호출

_`렌더링 엔진이 문서 파싱 -> DOM 노드로 변환, 스타일 요소 파싱 (렌터 트리 생성) -> 노드를 정확한 위치에 배치 -> 그리기`_

_`한번에 배치, 그리기가 아니라 나머지 내용을 기다리는 동시에 일부를 먼저 화면에 표시`_

<hr >

## RESTful & GraphQL

### RESTful

Resource 들을 하나의 Endpoint에 연결해두고, 각 Endpoint는 그 Resource와 관련된 내용만 관리하는 방법론

- POST
- GET
- PATCH
- DELETE

### GraphQL

Graph Query Language<br>
server API를 통해 정보를 주고받기 위해 사용하는 Query Language

- 하나의 EndPoint를 사용
- 요청할 때 사용한 Query 문에 따라 응답의 구조가 달라짐
- 사용자가 응답의 구조를 자신이 원하는 방식으로 바꿀 수 있음

장점

- HTTP 요청의 횟수를 줄일 수 있음 : 원하는 정보를 하나의 Query 에 담아서 요청할 수 있음
- 응답의 Size를 줄일 수 있음 : 필요한 부분적으로 요청 가능

단점

- 요청의 크기가 커질 수 있음

### RESTful vs GraphQL

1. RESTful

- HTTP와 HTTPs에 의한 caching을 사용하고 싶을 때
- 파일 전송 등 단순한 Text로 처리되지 않는 요청이 있을 때
- 요청의 구조가 단순하고 정해져 있을 떄

2. GraphQL

- 서로 다른 모양의 다양한 요청에 대해 응답할 수 있어야 할 때
- 대부분의 요청이 CRUD에 해당할 때

<hr>

## CORS

전송되는 리소스의 도메인과 다른 도메인으로부터 리소스가 요청될 때, cross-origin HTTP 요청에 의해 요청됨. <br>
보안 상의 이유로, 브라우저들은 스크립트 내에서 초기화되는 cross-origin HTTP 요청을 제한함.<br>
이러한 요청을 허용하기 위해 도입된 것이 CORS(Cross-Origin Resource Sharing)<br>
일반적으로 서버사이드에서 핸들링.

<hr>

## PWA(Progressive Web App)

웹과 앱의 장점을 결합한 웹앱.<br>
지원하는 웹 브라우저를 통해 설치 없이 접속할 수 있고, 바탕화면에 앱 아이콘을 추가할 수 있고, 푸시 알림 또한 가능함.

<hr>

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


### MVVM

- MVC : Model + View + Controller
    - 사용자의 Action이 Controller에 들어오고, Controller는 사용자의 Action을 확인하고 Model을 업데이트, Model을 나타낼 View를 선택. View는 모델을 이용하여 화면을 나타냄
    - View와 Model 사이의 의존성이 높아, 어플리케이션이 커질수록 복잡해지고 유지보수가 어려워 짐.
- MVP : Model + View + Presenter
    - 사용자의 Acion이 뷰를 통해, View는 데이터를 Presenter에 요청. Presenter는 Model에 요청. 역순 응답.
    - Presenter가 View와 Model을 연결하는 역할. Presenter와 View는 1:1 관계. View와 Presenter의 의존성이 강해짐.
- MVVM : Model + View + ViewModel 
    - 사용자의 Action들이 View를 통해 들어옴. Command 패턴으로 View Model에 Action 전달. VM이 Model에 데이터 요청, 응답. VM이 데이터 가공 저장. 데이터 바인딩을 통해 View가 표시.
    - Command 패턴과 Data Binding 패턴을 사용하여 View와 VM 사이의 의존성을 없앰.
    - View는 Model, VM 모두와 의존성이 없기 때문에 모듈화하여 개발 가능.

### Flux
단방향 데이터 흐름을 만들기 위한 패턴
- Dispatcher : Flux의 데이터 흐름을 관리하는 허브. Action이 발생하면 Dispathcer로 전달되고, 전달받은 Action을 보고 콜백 함수를 실행하여 Store에 데이터 전달
- Store : 상태 변경을 담당하는 곳. Dispatcher에 콜백 함수를 등록하면 Dispathcer로부터 수신 받음. Store가 변경되면 View에 변경되었다는 사실을 알려줌
- View : 화면에 나타나는 것 뿐만 아니라, 자식 View로 데이터를 보내는 뷰 컨트롤러의 역할도 함께 함.

### 생성

- Functional components
- Class components : state, lifecycle, ref
  - React.Component
  - React.PureComponent : shouldComponentUpdate 가 이미 적용

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

## LifeCycle

### `constructor`

컴포넌트 생성자 함수. 컴포넌트가 새로 만들어질 때마다 함수가 호출됨.

```javascript
constructor(props) {
  super(props)
}
```

### `componentDidMount`

컴포넌트가 화면에 나타났을 때 호출됨.<br> 주로 외부 라이브러리 연동, ajax 요청, DOM 속성 변경 작업 진행

```javascript
componentDidMount() {
  // 외부 라이브러리, 컴포넌트에 필요한 요청, DOM 작업
}
```

### `getDerivedStateFromProps`

props로 받아온 값을 state로 동기화 하는 작업을 하는 경우 사용

```javascript
static getDerivedStateFromProps(nextProps, prevState) {
  if(nextProps.value !== prevState.value){
    return { value: nextProps.value}
  }
  return null
}
```

### `shouldComponentUpdate`

변화가 발생한 경우에만 render 함수를 호출하도록 할 수 있음

```javascript
shouldComponentUpdate(nextProps, nextState) {
  // true일 경우에만 업데이트
  return nextProps.value !== this.props.value
}
```

### `getSnapshotBeforeUpdate`

DOM의 변화가 일어나기 직전의 DOM 상태를 가져오고, 리턴하는 값은 componentDidUpdate에서 3번째 파라미터로 사용할 수 있음

> render() => getSnapshotBeforeUpdate() => DOM 변화 발생 => componentDidUpdate()

```javascript
getSnapshotBeforeUpdate(prevProps, prevState) {
  // 변화 발생 전, 스크롤 유지 등
  ...
  // 반환값은 CDU 에서 snapshot 값으로 받아올 수 있음
  return { scrollTop, scrollHeight }
}
```

### `componentDidUpdate`

DOM의 변화가 일어난 후 실행

```javascript
componentDidUpdate(prevProps, prevState, snapshot) {
  // 세번째 인자로 getSnapshotBeforeUpdate의 return 값
}
```

### `componentWillUnmount`

컴포넌트가 더 이상 필요하지 않게 되면 호출 <br>
주로 등록했던 이벤트 제거, clearTimeout, 외부 라이브러리 종료

```javascript
componentWillUnmount() {

}
```

## Redux

`상태관리 라이브러리`

### Ducks 패턴

한 파일 내에 Actions, Reducer, Action 생성 함수 모두 작성.

### 액션(Action)

상태에 어떠한 변화가 필요할 때 '액션'을 발생시킴

```javascript
{
  type: 'ADD_TODO',
  data : {
    id : 0,
    text: 'adsf'
  }
}
```

### 액션 생성 함수

액션을 생성하는 함수. 파라미터를 받아와 액션 객체로 만듦.

```javascript
function addTodo(data) {
  return {
    type: 'ADD_TODO',
    payload: data,
  };
}
```

### 리듀서(Reducer)

변화를 일으키는 함수. state와 action 두가지 파라미터를 받아옴.

```javascript
function reducer(state, action) {
  // 상태 업데이트 로직
  return changedState;
}
```

여러개의 리듀서를 합치기 위해서는 `combineReducers`를 사용

> RootReducer = SubReducer + SubReducer + ...

### 스토어(Store)

스토어 내부에는 현재의 앱 상태와 리듀서가 들어있고, 내장 함수가 있음

### 디스패치(dispatch)

스토어 내장 함수 중 하나. 액션을 발생시킴. dispatch라는 함수에 action을 파라미터로 전달하면 스토어는 리듀서 함수를 실행시켜 해당 액션을 처리하여 새로운 상태를 만들어 줌.

### 구독(subscribe)

스토어 내장 함수 중 하나. 함수 형태의 값을 파라미터로 받아, 액션이 디스패치 될 때마다 전달해준 함수가 호출된다.

### mapStateToProps & mapDispatchToProps

`mapStateToProps` : props로 넣어줄 스토어의 상태값

```javascript
const mapStateToProps = state => {
  return {
    color: state.count.color,
  };
};
```

`mapDispatchToProps` : props로 넣어줄 액션 생성 함수

```javascript
const mapDispatchToProps = dispatch => {
  return {
    changeColor: color => dispatch(changeColor(color)),
  };
};
```

`connect` : 컴포넌트에 리덕스 스토어 연동

```javascript
export default connect(
  mapStateToProps,
  mapDispatchToProps
)(App);
```

### `정리`

1. `Ducks 패턴으로 한 파일 내에 Actions / Reducer / Action 생성 함수 정의`
2. `CombineReducers로 RootReducer 만들기`
3. `Store 만들어서 전체 App에 적용하기`
4. `Connect 함수를 사용하여 컴포넌트에 스토어 연동하기`

## MobX

상태 관리 라이브러리<br>
setState조차 필요없게 됨.

```javascript
decorate(App, {
  number: observable, // number라는 변수를 관찰
  increase: action, // increase라는 함수를 action으로
  decrease: action,
});

export default observer(App);
```

## Redux와 Context API

context API가 `전역 상태 관리`를 Redux에 비해 조금 더 쉽고 간단하게 가능하도록 제공하는 것은 맞으나, Redux의 장점은 그 이상임. `다양한 미들웨어, 협업 환경에서의 훌륭함, 강력한 개발자 도구` 등.


## TypeScript
JS + type 선언. 정적 타입 체크 <br>

### 선택적 매개변수
함수 생성시 선택적 매개변수를 만들고 싶다면 `'?'` 사용
```typescript
const example = (name: string, age? : number) : string {
  return 'Hello'
}
```

### 인터페이스
TS에서 구조를 만들 때 사용하는 방법. interface를 통해 객체 내부 변수의 type을 지정.
```typescript
interface User {
  name : string;
  age : number;
}

const info = {
  name : 'gyeol',
  age : 25
}

const example = (info : User) : string => {
  return `${info.name}님, 안녕하세요. ${info.age}이시네요.`
}
```

<hr>

# 자료구조

## `스택`

`한쪽 끝에서만 자료를 넣고 뺄 수 있는 LIFO 형식의 자료 구조`

```javascript
class Stack {
  constructor() {
    this._arr = [];
  }
  push(item) {
    this._arr.push(item);
  }
  pop() {
    return this._arr.pop();
  }
  peek() {
    return this._arr[this._arr.length - 1];
  }
}
```

## `큐`

먼저 집어 넣은 데이터가 먼저 나오는 FIFO구조

```javascript
class Queue {
  constructor() {
    this._arr = [];
  }
  enqueue(item) {
    this._arr.push(item);
  }
  dequeue() {
    return this._arr.shift();
  }
}
```

## `힙`

완전 이진 트리의 일종으로, 우선순위 큐를 위해 만들어진 자료 구조<br>
`우선순위 큐` : 데이터들이 우선순위를 가지고 있고, 우선순위가 높은 데이터가 먼저 나감.<br>
`완전 이전 트리` : 트리의 모든 높이에서 노드가 꽉 찬 형태, 왼쪽에서 오른쪽으로 꽉차야 함.

### 삽입

1. 힙의 마지막 노드에 삽입
2. 새로운 노드를 부모의 노드와 비교, 교환하여 힙의 성질 만족

### 삭제

1. 최대 힙에서 최댓값은 루트 노드이므로 루트 노드 삭제
2. 힙의 마지막 노드를 루트 노드로 가져옴
3. 루트 노드와 자식 노드를 비교하여 힙의 성질 만족

## `트리`

여러 데이터가 계층 구조 안에서 서로 연결된 형태. 그래프의 한 종류. '최소 연결 트리'

- 노드 : 트리 안에 들어있는 각 항목
- 자식 노드
- 부모 노드
- 뿌리 노드 : 가장 상층부의 노드
- 잎 노드 : 자식 노드가 없는 노드

```javascript
class Node {
  constructor(content, children = []) {
    this.content = content;
    this.children = children;
  }
}

const tree = new Node('hello', [
  new Node('world'),
  new Node('and'),
  new Node('fun', [new Node('javascript!')]),
]);
```

## 그래프

단순히 노드와 그 노드를 연결하는 간선을 하나로 모아 놓은 자료 구조 <br>

트리와의 차이

- 무방향 그래프 존재
- 사이클, 자체 순환 가능
- 루트 노드, 부모-자식 개념 X

<hr >

## 그래프 탐색

하나의 정점으로부터 시작하여 차례대로 모든 정점들을 한 번씩 방문하는 것

### 깊이 우선 탐색(DFS)

루트 노드에서 시작해서 다음 분기로 넘어가기 전까지 해당 분기를 완벽하게 탐색하는 방법<br>
모든 노드를 방문하고자 하는 경우에 선택. 검색 속도는 BFS에 비해 느림
<br>
`스택을 이용하여 방문한 정점들을 스택에 저장하였다가 다시 꺼내어 작업`

### 너비 우선 탐색(BFS)

루트 노드에서 시작해서 인접한 노드를 먼저 탐색하는 방법<br>
두 노드 사이의 최단 경로 혹은 임의의 경로를 찾고 싶을 때 선택.<br>
`깊이가 1인 노드들을 전부 방문하고, 방문한 노드를 큐에 삽입. -> 큐에서 꺼낸 노드를 방문 -> 인접한 노드들을 모두 방문하고 큐에 삽입`

# 알고리즘

## 선택정렬

첫 번째 자료를 두 번째 자료부터 마지막 자료까지 차례대로 비교하여 가장 작은 값을 찾아 처음에 놓는 작업을 반복하여 정렬하는 방법<br>
시간복잡도 O(n^2)

```javascript
const selectionSort = array => {
  let result = [...array];

  for (let i = 0; i < result.length - 1; i++) {
    let minIndex = i;

    for (let j = i + 1; j < result.length; j++) {
      if (result[minIndex] > result[j]) {
        minIndex = j;
      }
    }

    if (minIndex !== i) {
      let temp = result[minIndex];
      result[minIndex] = result[i];
      result[i] = temp;
    }
  }
  return result;
};
```

## 삽입정렬

두번째 자료부터 시작하여 앞의 자료들과 비교하여 삽입할 위치를 지정한 뒤 자료를 뒤로 옮기고 지정한 자리에 삽입하여 정렬

```javascript
const insertionSort = arr => {
  let result = [...arr];

  for (let i = 1; i < result.length; i++) {
    let temp = result[i]; // 현재값 저장
    let target = i - 1; // 정렬된 부분의 현재 인덱스

    // 좌측 값이 현재 값보다 클 때 swap
    while (target >= 0 && result[target] > temp) {
      result[target + 1] = result[target];
      target--;
    }

    // 임시로 저장한 현재값을 정렬된 부분의 인덱스에 부여
    result[target + 1] = temp;
  }

  return result;
};
```

## 버블정렬

서로 인접한 두 원소를 검사하여 정렬하는 알고리즘

```javascript
const bubbleSort = array => {
  let result = [...array];

  for (i = 0; i < result.length - 1; i++) {
    for (j = 0; j < result.length - 1 - i; j++) {
      if (result[j] > result[j + 1]) {
        let temp = result[j];
        result[j] = result[j + 1];
        result[j + 1] = temp;
      }
    }
  }
  return result;
};
```

## 합병정렬(Merge Sort)

리스트를 두 개의 균등한 크기로 분할하고 분할된 부분 리스트를 정렬한 다음, 정렬된 부분 리스트를 합하여 전체가 정렬된 리스트가 되도록 하는 방법

```javascript
const mergeSort = array => {
  if (array.length <= 1) {
    return array;
  }

  const middle = Math.floor(array.length / 2);
  const left = array.slice(0, middle);
  const right = array.slice(middle);

  return merge(mergeSort(left), mergeSort(right));
};

const merge = (left, right) => {
  let result = [];
  while (left.length && right.length) {
    left[0] > right[0] ? result.push(right.shift()) : result.push(left.shift());
  }
  while (left.length) {
    result.push(left.shift());
  }
  while (right.length) {
    result.push(right.shift());
  }

  return result;
};
```

## 퀵정렬

```javascript
const quickSort = array => {
  if (!array.length) {
    return [];
  }

  let pivot = array[0];
  let left = [],
    right = [];

  for (let i = 1; i < array.length; i++) {
    array[i] < pivot ? left.push(array[i]) : right.push(array[i]);
  }
  return [...quickSort(left), pivot, ...quickSort(right)];
};
```

## 힙정렬

```javascript
const swap = (array, index_A, index_B) => {
  let temp = array[index_A];

  array[index_A] = array[index_B];
  array[index_B] = temp;
};

const heapify = (array, index, len) => {
  let left = 2 * index + 1;
  let right = 2 * index + 2;
  let max = index;
  // let len = array.length;

  if (left < len && array[left] > array[max]) {
    max = left;
  }
  if (right < len && array[right] > array[max]) {
    max = right;
  }

  if (max !== index) {
    swap(array, index, max);
    heapify(array, max, len);
  }
};

const heapSort = array => {
  let len = array.length;

  for (let i = Math.floor(len / 2); i >= 0; i--) {
    heapify(array, i, len);
  }

  for (let i = len - 1; i > 0; i--) {
    swap(array, 0, i);
    len--;

    heapify(array, 0, len);
  }

  return array;
};
```
