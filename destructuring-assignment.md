# 분할 대입 (Destructuring assignment)

분할 대입이란 배열 및 객체를 분해하여 내부의 요소를 개별 변수로 지정해주는 구문이다.

배열의 경우 다음과 같이 사용할 수 있다.

```
let data = [1,2,3,4,5,6,7,8];
let [x1, x2, x3, x4, x5] = data;
```

다음과 같이 사용할 경우 x1 ~ x5에는 각각 배열의 인덱스와 동일한 값이 들어가게 된다.

x6은 not defined가 나오게 된다.

data객체가 위와 같은 상태라고 가정했을 때

```
let [x1, x2, x3, ...xOthers] = data;
```

다음 코드에서 x1, x2, x3은 순서대로 1,2,3이 담기게 되며 배열의  나머지가 xOthers에 들어가서

xOther는 [4,5,6,7,8]의 배열이 된다.



ES6 이전에는 변수 x와 변수 y의 값을 서로 바꾸기 위해서는 temp변수를 만들어 값을 바꿔줘야 하는 불편함이 있었으나

분할대입이 생긴 이후로는 다음과 같이 변수끼리 값을 변경할 수 있다.

```
let x = 1;
let y = 2;
[x, y] = [y, x];
```



다음과 같이 응용할 수 있다.

````
function getMinMax(...nums) {
    return [Math.min(...nums), Math.max(...nums)];
}

console.log(getMinMax([1,5,9,30,99]));
````

콘솔을 찍으면 [1, 99]의 배열이 나올것이다. 그러나 분할대입을 한번 더 사용해서 다음처럼 값을 가져올 수 있다.

```
let [min, max] = getMinMax([1,5,9,30,99]);
```

이러면 min에는 1, max에는 99가 대입된 변수를 가져올 수 있다.







객체의 경우는 다음과 같다.

```
let obj = {item: "item", child: "child", prop: "prop"};
let {item, child, value = 'value'} = obj;
```

item과 child는 obj내의 키 기준으로 값이 바인딩되지만 obj객체 내에 value라는 키값은 없으므로 default로 'value'라는 값을

가진 value 객체가 같이 선언됨. 객체는 키값을 기준으로 값을 가져오므로 배열과 달리 순서가 중요하지 않음.



객체 안의 객체의 경우 다음과 같이 표현이 가능

```
let obj = {
    childObj: {
        childObjKey: 'value'
    }
};

let {childObj, childObj: {childObjKey}} = obj;
```

이런 경우 childObj는 obj객체 내의 childObj객체가 그대로 담기며 childObjKey라는 변수가 하나 더 만들어지게 된다.



객체는 변수명을 재지정 할 수 있다. 예를 들면

```
let book = {title: "자바스크립트", author: "김준현};
let {title: bookName, author: name};
```

의 경우 bookName변수에 title값인 자바스크립트가, name변수에는 author값인 김준현이 들어감.

