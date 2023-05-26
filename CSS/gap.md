# gap

CSS의 `gap` 속성에 대해 알게 되었다.

이전에는 IE나 그 외 브라우저들이 gap을 지원하지 않았고, gap을 사용하려면 `display: grid;`에서만 가능했으나,
이제 대다수의 브라우저들이 `gap`을 지원하며 `display: flex;` 에서도 사용할 수 있다.

margin과의 차이는 margin은 다른 요소들이 없어도 단일 개체가 margin 값을 가진다는 것에 비해
gap은 다른 요소와의 공간만을 벌려줄 뿐이기에 예상 외의 레이아웃이 발생할 일이 없다.

gap은 margin이나 padding과 같이 gap: 10px; 로 사용했을때는 top bottom right left 를 다 10px로 설정하겠다는 함축어이며,
gap: 16px 12px; 처럼 2개를 넣어주면 top bottom 16px, right left 12px로 사용하겠다는 선언이다.

하나의 p태그를 column-count: 3; column-gap: 10px; 이렇게 주면 3칸으로 나누어서 10px씩 띄워 화면에 표시할 수도 있다.
