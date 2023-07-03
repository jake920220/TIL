# unstable_usePrompt, unstable_useBlocker

특정 페이지에서 저장하지 않은 사항이 있을 때 라우트 이동을 막기 위한 기능이 필요했고, usePrompt를 사용하여 처리하려했으나

react-router가 v6로 올라오며 해당 기능을 제공하지 않는다는 글을 보게 되었다.

찾아보니 브라우저별로 다른 동작을 하고 있고 그에 따른 결과를 보장해주지 못하기 때문에 지원이 종료된 기능이라고 했다.

그러나 여전히 해당 기능은 많은 사랑을 받고 있기 때문에 unstable_ 이라는 prefix가 붙은 채로

unstable_usePrompt와 unstable_useBlocker 가 react-router 내에 존재하고 있다.

unstable_usePrompt의 경우 when과 message를 객체로 하나의 아규먼트를 받고 있다.

```javascript
declare function usePrompt({ when, message }: {
    when: boolean;
    message: string;
}): void;
export { usePrompt as unstable_usePrompt };
```


```javascript
export declare function useBlocker(shouldBlock: boolean | BlockerFunction): Blocker;
```




출처

[react-router-github](https://github.com/remix-run/react-router/issues/8139)
[stackoverflow](https://stackoverflow.com/questions/70617041/react-router-v6-doesnt-support-prompt-or-useprompt)
