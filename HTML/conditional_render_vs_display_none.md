# display:none; vs 조건부 렌더링

css의 `display: none;` 속성을 주면 엘리먼트는 DOM tree에는 포함되지만
CSSOM의 display: none;을 인식하여 render tree로 구성될 때에는 제외되게 된다.

반면 react나 vue, angular 등 모던 javascript 프레임웍을 사용할 때 조건부에 따라서
element를 그리는 `조건부 렌더링`을 이용할 경우 DOM tree에도 포함되지 않게 된다.

보편적으로는 DOM Tree에 포함이 될 경우 re-rendering이 일어날 때 영향을 받게 되어
display: none; 이 조건부 렌더링보다 퍼포먼스가 좋지 않은 편이나, 이 차이는 굉장히 경미하고
조건부 렌더링의 조건식이 복잡해지는 경우에는 script가 가져가는 퍼포먼스적 이슈가 있기에
절대적으로 'display:none;이 성능이 더 좋지 않다. 사용을 피해야 한다.' 라고 생각할 필요는 없다.

보통 간편하게 css적인 접근으로 계산이 가능한 경우 display: none;을 혼용하여 사용하고
그렇지 않을 때에는 조건부 렌더링을 사용했으나, emotion이나 styled-component와 같이 `css-in-js` 형태의
css 라이브러리들이 인기를 얻고 난 뒤로는 조건에 따른 제어가 display: none;도 어렵지 않아졌기에
편한대로 사용하면 된다.
