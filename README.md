##  REACT-study 💫

#### ✅part 1

##### return()문 안에 html 코드 작성

##### JSX 문법 1. className 사용 -> class 사용하지 않음.

##### JSX 문법 2. { } 중괄호 사용 -> 자바스크립트 표현식 작성 / 변수 넣을 때 / id, className .. 등등에서 사용 가능 / 데이터 바인딩

##### JSX 문법 3. style= { } -> object형식으로 / js 코드에서 바로 작성

```
style={{ color: 'red', fontSize: '20px' }}
```

##### React.js를 사용할 때는 화면에 무엇이 표현되어야 하는가, 즉 목표를 정의하고 React가 거기까지 도달하는 방법을 알아내도록 만들어야 한다.
##### React.js에서는 선언형(Declarative) JS 코드로 작성.
##### JSX 구문은 React 프로젝트에서 활성화되는 특수한 비표준 구문이며, 백그라운드에서 표준 JS 코드로 컴파일된다.

-----

##### ⭐ Component ⭐

##### 일반적으로 해당 컴포넌트가 사용될 때 화면에 표시되는 HTML(=JSX) 코드를 반환하는 JS 함수
##### 길고 복잡한 반복적인 html 한 단어로 정리  / 변경 잦은 UI
##### 기존 function 벗어나 새로운 function 생성 / !대문자로 시작!
##### return문 안에 html 작성 / component 생성 후 tag형식으로 함수 사용

##### 컴포넌트 트리 : 루트 노드 아래에 여러 컴포넌트가 중첩되어 있는 것. 

```
function ExpenseItem() {
  return <h2>Expense item!</h2>;
}

export default ExpenseItem;

---------------------------------------------------

import ExpenseItem from './components/ExpenseItem';

function App() {
  return (
    <div>
      <h2>Let's get started!</h2>
      <ExpenseItem></ExpenseItem>
    </div>
  );
}

export default App;
```

##### 1. 함수명은 파일 이름에서 확장자를 빼고 다시 넣는 게 규약.
##### 2. export - import
##### 3. JSX 코드 스니펫 안에는 하나의 루트요소만 허용.
##### 4. css -> import css file , className
##### 5. function안에 선언된 js 상수는 return 중괄호 안에 입력하여 출력


-----
##### 🧸 Composition 🧸
##### 컴포넌트를 조합할 때는 항상 컴포지션을 사용
##### ❄ 컴포넌트 안에 로직과 JSX 코드가 많아지면서 컴포넌트가 점점 커지게 된다.
##### 1 👉🏻 하나의 핵심 작업에 집중하기 위해 앱을 작은 요소들로 나누고, 그 구성들을 조합해서 전체적인 사용자 인터페이스를 구축.
##### 2 👉🏻 모든 컴포넌트들이 비교적 작고 관리하기 쉬운 상태로 유지되고, 코드 베이스를작고 관리하기 쉽게 유지.
##### 3 👉🏻 언제 새 컴포넌트를 만들어야 하는지, 기존 컴포넌트에 내용을 추가해야 하는지 등에 대한 정해진 규칙은 없음.


##### 💲 props 💲
##### 컴포넌트의 외부에서 데이터를 받음 / 리액트 컴포넌트 간에 데이터 공유, 전달
##### 컴포넌트를 재사용 가능하게 함. <--- 핵심 개념!!!

-----

##### 🌞 useState( ) 
##### useState는 현재의 state 값과 이 값을 업데이트하는 함수를 쌍으로 제공 / 자동 재렌더링
```
const [count, setCount] = useState(0);
```

##### 재렌더링 / state 변경 -> state함수명(새로운 state)
##### 클릭하면 useState 값이 1로 변경
```
<span onClick={() => {setCount(1)}}>👍🏻</span> {count}
```
##### 클릭하면 useState 값이 +1씩 증가
```
<span onClick={() => {setCount(count+1)}}>👍🏻</span> {count}
```

##### state - array / object 변경 -> 새로운 공간에 값을 복사하여 할당/ [...배열] {...객체} / state 값 같을 경우 변경 X 
