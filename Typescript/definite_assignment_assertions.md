# 확정적 할당 어설션 ( Definite Assignment Assertions )

다른 언어들에서는 `!`를 `falsy`한 state로 사용하지만 `Typescript`에서는 `!`를 변수나 return값이 있는 함수 뒤에
넣을 때 컴파일러에게 "이 변수는 값이 없을 리가 없어~" 라고 선언해주는 효과를 낸다.

이걸 확정적 할당 어선셜이라고 하는데

```typescript
let x: number;

doSomethingWithX();

console.log(x+10);
// error
```
이렇게 x가 명확히 할당되지 않은 상태에서 사용하려고 하면 컴파일 단계에서 에러를 내지만

```typescript
let x!: number; // x는 값이 무조건 할당될거란다~~ 라는 얘기

doSomethingWithX();

console.log(x+10);
// No Error
```

이렇게 `!`를 변수 뒤에 붙여 선언하면 확정 할당 어선셜이라고 하여 변수에 무조건 값이 들어가있다고 판단, 에러가 나지 않는다. 
