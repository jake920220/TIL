# React Router v6

이전의 router와 설정이나 몇 가지가 달라져서 공식문서를 읽으며 공부했다.

V6는 React 16.8 이상에서 사용이 가능하다.

가장 큰 차이점은 data api를 지원한다는 것이다.

Nextjs 프로젝트를 다루거나 graphQL을 사용할 일이 있었던 경우처럼 react도 router 단계에서

data fetching을 할 수 있게 data api를 지원한다.

data api는 route component의 props에 포함된다.

6.4의 새 라우터들은 `createBrowserRouter`, `createMemoryRouter`, `createHashRouter`, `createStaticRouter` 등이 있는데
이것들을 사용하면 data api를 쓸 수 있다.

`<BrowserRouter>`,
`<MemoryRouter>`,
`<HashRouter>`,
`<NativeRouter>`,
`<StaticRouter>` 얘네들은 data api를 쓸 수 없음.

공식문서에서는 BrowserRouter 대신 createBrowserRouter를 사용하는 것을 강력하게 추천하고 있다.

V5와의 차이점은 다음과 같다.

이전의 <switch>가 <Routes>로 대체됨.

이제 exact를 사용하지 않아도 매칭되는 url path에 맞게 매칭됨 (이전에는 /product, /product/:productId 라우트는 exact를 쓰지 않으면
productId의 path에 접근했을 때 product도 동작했다.)

useHistory가 useNavigate로 변경됨

Redirect 가 Navigate로 대체됨
