# React.forwardRef

React 에서 `ref`는 엘리먼트에 접근하기 위해서 사용된다.
input 등의 컴포넌트를 만들고 ref를 제어해야하는 상황이 필요할 때, 상위 컴포넌트에서 input 컴포넌트로
ref를 props처럼 넘겨주면 ref는 prop요소가 아니라는 React 에러가 난다.

이것을 이전에는 key값등을 넘겨줘 useRef를 input컴포넌트 내에서 생성하고, key값을 붙여서 다른 input들과 겹치지 않도록 제어했는데
부모컴포넌트에서 생성한 ref를 넣어주고, input컴포넌트 내에서 React.forwardRef()로 mapping해주면 에러없이 동작함을 확인할 수 있다.
