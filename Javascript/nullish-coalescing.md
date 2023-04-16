# NULL 병합 연산자, NULL 병합 할당자 (Nullish-coalescing, Nullish-coalescing Assignment)

<br>

## NULL 병합 연산자 (Nullish coalescing)

널 병합 연산자에 대해서 사용하는 것을 최근에 발견해 [문서](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)를 정독했다.

문법은 `??` 이렇게 사용한다.

쉽게 설명해 왼쪽의 값이 `undefined` 이거나 `null`일 경우 오른쪽의 값을 반환하는 연산자이다.

처음 이 문법을 봤을 때 삼항연산자와 굉장히 흡사하게 생겼다는 느낌을 받았는데, 삼항연산자의 축약 같은 느낌으로 다가왔다.

```
let a = condition ? b : c;
```

```
let a = b ?? c;
```

다만 삼항연산자에서는 condition이 Falsy 한 값일 경우 (ex: `0`, `false`)에도 조건이 바뀌지만, 널병합 연산자에서는 조건이 `undefined`나 `null`이 아니라면 값이 falsy 하더라도 값을 반환한다는 차이가 있다.

<br>

## NULL 병합 할당자 (Nullish coalescing assignment)

널 병합 할당자는 `??=` 형태의 문법을 사용한다.

널 병합 연산자와 비슷하게 생각하면 된다. 할당할 변수가 Nullish 하다면 값을 대입하겠다는 뜻이다.

```
const a = { duration: 50 };

a.duration ??= 10;
console.log(a.duration);
// Expected output: 50

a.speed ??= 25;
console.log(a.speed);
// Expected output: 25
```

위 문법을 보면 a.duration은 이미 50이 할당되어 있어 `a.duration ??= 10;` 을 선언해도 그대로 50인 상태이다.
반대로 a.speed는 존재하지 않던 개체로 25의 값이 할당됨을 확인할 수 있다.
