# Syntactic Sugar

Syntactic Sugar는 문법적 설탕이라고 직역할 수 있는데 말 그대로 코드를 사람이 읽기 쉽게 (달달하다) 간결하게 표현된 것을 말한다.

간단한 예시는 다음과 같다.

```javascript
const Person = function(name, age) {
    this.name = name;
    this.age = age;
    this.greeting = () => {
        return `안녕하세요. 저는 ${name}이고 ${age}세 입니다.`
    }
}

const me = new Person("김준현", 32);
me.greeting();
```
> 생성자 함수를 사용해 객체를 만드는 문법

```javascript
const me = {
    name: "김준현",
    age: 32,
    greeting: () => {
        return `안녕하세요. 저는 김준현이고 32세입니다.`
    }
}
```
> 객체 리터럴로 바로 생성하는 방식

생성자 함수로 객체를 만드는 방법보다 훨씬 쉽고 간결하다. 코드량도 적고 한눈에 들어온다.

```javascript
let a = 0;
a = a + 1;
console.log(a);
// 1
```

```javascript
let a = 0;
a++;
console.log(a);
// 1
```

위와 같이 우리가 자주 쓰던 ++; 도 syntactic sugar에 속한다고 볼 수 있다.
