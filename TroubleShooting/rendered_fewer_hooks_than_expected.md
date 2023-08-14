# Error: Rendered fewer hooks than expected

React에서 Hook을 사용하다가 발생할 수 있는 에러이다.

Hook의 사용조건을 위배했을 때 나오는데 login 이 되어있지 않으면 다른곳으로 return navigate시키는 함수가 상위에 작성되어있었고,
그 아래에 hook을 사용하고 있어서 겪었다.

훅은 최상위 계층에만 작성되어야하고, react 함수내에만 존재해야한다는 Hook의 rule에 위배될 때 볼 수 있는 에러이다.
