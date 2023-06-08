# Suspense

React의 suspense는 16버전 까지는 실험적인 기능으로 존재하다가 18버전 이후부터 정식으로 react의 기능으로 포함되었다.

기존에 비동기 처리 시 loading 컴포넌트를 보여주고 싶은 경우 isLoading 이라는 변수를 새로 만들고 true와 false일때의 분기처리를

따로 해주어 loading 컴포넌트를 return하거나 원하는 컴포넌트를 return시키는 처리를 해주곤 했다.

```jsx
// 기존 처리
{
    isLoading ? 
        <LoadingComponent/> : <UserInfo>...</UserInfo>
}
```

그러나 suspense는 wrapping 한 자식의 비동기처리 결과에 따라 fallback으로 넣어준 component를 return 한다.

```jsx
import React, {suspense} from "react";

<suspense fallback={<LoadingComponent/>} >
    <UserInfo>...</UserInfo>
</suspense>
```

suspense는 react lazy와 함께 route처리에서 또한 사용이 가능하다.
