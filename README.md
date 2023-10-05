##  REACT-study 💫

#### ✅part 1

##### return()문 안에 html 코드 작성

##### JSX 문법 1. className 사용 -> class 사용하지 않음.

##### JSX 문법 2. { } 중괄호 사용 -> 자바스크립트 표현식 작성 / 변수 넣을 때 / id, className .. 등등에서 사용 가능 / 데이터 바인딩

##### JSX 문법 3. style= { } -> object형식으로 / js 코드에서 바로 작성

```
style={{ color: 'red', fontSize: '20px' }}
```

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

#### ✅part 2

##### ⭐ Component

##### 길고 복잡한 반복적인 html 한 단어로 정리  / 변경 잦은 UI
##### 기존 function 벗어나 새로운 function 생성 / 대문자로 시작
##### return문 안에 html 작성 / component 생성 후 tag형식으로 함수 사용

```
function Menu() {
  return (
     <div className='menu'>
        <h4>1</h4>
        <p>2</p>
        <p>3</p>
     </div>
  )
}
```



