# Error boundary

에러 바운더리란 JS에서 일어나는 일부 에러가 에플리케이션 전체를 중단시키지 않게 하기 위해
React 16버전에서 도입된 새로운 개념이다.

에러 바운더리는 하위 컴포넌트 트리의 어디에서든 자바스크립트 에러를 기록하며, 깨진 컴포넌트 트리 대신 폴백 UI를 제공하는
React component 이다.

- 이벤트 핸들러
- 비동기적 코드 (예: setTimeout 혹은 requestAnimationFrame 콜백)
- 서버 사이드 렌더링
- 자식에서가 아닌 에러 경계 자체에서 발생하는 에러

위의 에러들은 Error boundary 에 포착되지 않는다.
