# Void

자바스크립트에서 `Void` 연산자에 대해서 알게 되었다.

예전에 Java를 공부하며, 그리고 더 가물가물하지만 C등의 언어를 공부했을 때에는 void는 리턴값이 없는 함수에 대한
선언이라고 이해했었다.

다만 자바스크립트에서는 함수선언 단계에서 함수의 리턴값을 명시할 필요도 없고, 함수의 인자를 명시할 필요도 없다고 배웠었다. (그래서 자바스크립트에서는 함수오버로딩이 없는것)

그런데 얼마 전 `void`를 붙인 함수가 있는 것을 스택오버플로우에서 보고 매우 신기해 했었던 기억이 난다.

javascript 에서 `void` 연산자를 붙이면 리턴값이 무엇이던 `undefined`로 고정한다.

```
function returnPromise() {
    return new Promise((res, rej) => {
        // ...
    });
}

void returnPromise();
// undefined
```

위와 같이 프로미스를 리턴하는 함수여도 `void`를 연산자로 붙이면 리턴값이 undefined가 된다.

사실 JS를 5년 이상 사용하면서 한 번도 마주한 적이 없었던 문법인 만큼, 실 사용할 일이 있겠느냐 싶겠냐만은
개념에 대해 알게 되어 정리했다.