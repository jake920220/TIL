# Redux toolkit의 Immer와 불변 변수 수정

Redux toolkit의 createReducer와 createSlice는 내부적으로 [Immer](https://immerjs.github.io/immer/) 를 사용하고 있다.
Immer는 불변 변수를 쉽게 수정할 수 있도록 도와주는 라이브러리이다.

보통 javascript 에서는 Immutable 한 데이터를 수정하려면 값은 같지만 참조하는 주소값이 다른 데이터를 만들어야 한다.
JSON.parse(JSON.stringify(data)) 같은 형태로 혹은 Object.assign 같은 형태로 많이들 코드를 작성한 적이 있을 것이다.

reducer에서는 state는 불변변수이므로 state의 값을 직접 assign 해서 수정하는 것은 금지되어 있었다.

```javascript
// x
state.value = 123;
```

그러나 RTK 에서는 Immer를 내부적으로 사용하고 있으므로 state에 직접적인 할당을 통해 불변 변수를 수정할 수 있다.

RTK 측에서 Immer를 왜 내부적으로 쓰냐는 문의를 많이 받았다고 하며
Immer는 RTK의 필수적인 요소이며 향후 업데이트에서도 바꿀 일이 없다. 라고 단언 했다.

Immer의 장점 두가지를 언급하였는데, 하나는 복잡한 불변 변수 수정 로직을 간단하게 만들어준다는 것,
또 하나는 불변 변수 수정을 위한 코드 작성은 어렵고 실수가 흔히 생길 수 있는 영역인데 이를 없애준다는 것 이라고 했다.

[Writing Reducers with Immer 공식문서](https://redux-toolkit.js.org/usage/immer-reducers)
