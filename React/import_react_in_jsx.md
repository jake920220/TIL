# import React from "react"를 해줘야 했었던 이유와 지금은 안해도 되는 이유

리액트를 이전부터 사용해왔던 개발자라면 습관적으로 함수형 component를 만들 때
`import React from "react";` 구문을 최상단에 작성하는 것이 익숙할 것이다.

실제로 17버전 밑의 react에서는 React를 사용하지 않더라도 import구문을 넣어주지 않으면
에러가 나곤 했었는데, 그 이유는 js / jsx에서 우리가 사용하는 jsx문법이 babel을 통해
transform 되는 과정에서 React.createElement를 사용해서 dom을 생성하고 있었기 때문이다.


그러나 react 17버전 이후부터는 내부적으로 jsx를 처리하는 방식이 달라졌기에 더 이상 import React from "react"를 상단에
추가해주지 않아도 에러가 나지 않는다.


참고한 공식문서
https://legacy.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html
