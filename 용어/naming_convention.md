# 변수/파일명 네이밍 컨벤션

## camelCase (카멜 케이스)

카멜 케이스의 경우 변수명을 지을 때 첫 글자를 소문자로 하고, 단어와 단어 사이의 구분을 대문자로 지어준다.

```javascript
//example : user login state
let userLoginState;
```

## PascalCase (파스칼 케이스)

파스칼 케이스의 경우 camelCase와 유사하지만, 첫 글자도 대문자로 시작한다는 점이 차이점이다.
upper camel case 라고도 불린다.
React에서는 component 네이밍을 지을 때 PascalCase를 사용하는 것을 컨벤션으로 두고 있다.

```javascript
//example: user login state
let UserLoginState;
```

## snake_case (스네이크 케이스)

스네이크 케이스의 경우 변수명을 지을 때 단어와 단어 사이의 구분을 underscore `_` 로 나눈다.
소문자로 구성되는 것이 일반적이지만 enumal 한 상수값을 선언할 때에는 보통 대문자 snake_case를 사용한다.

```javascript
//example: user login state
let user_login_state;
const USER_LOGIN_STATE;
```

## kebab-case (케밥 케이스)

케밥 케이스의 경우 변수명을 지을 때 단어와 단어 사이의 구분을 하이픈 `-` 으로 나눈다.
snake_case와의 차이점은 underscore이냐 hypen이냐의 차이점 뿐이지만 대체로 잘 사용하지 않는다.
css에서 class나 id의 네임으로 사용할 때에 사용하는 경우가 많다.

```css
.kebab-case {
    
}
```
