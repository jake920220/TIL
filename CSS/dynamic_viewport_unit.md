# Dynamic Viewport Unit

개발자는 화면의 높이 100%를 채우는 기대값을 가지고 viewport height를 100을 준다.

100vh는 그러나 모바일 os 네비게이션바나 브라우저의 주소창등의 차이로 인해 원하는대로 동작하지 않고 스크롤바가 생길 여지가 있다.

그걸 방지하기위해 새로 css에 추가되는 것이 다이나믹 뷰포트이다.

https://developer.chrome.com/blog/whats-new-css-ui-2023/#dynamic-viewport-units

d를 붙여서 100dvh 이런식으로사용하면 다이나믹 뷰포트가 알아서 100을 잡아준다.
