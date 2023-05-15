# Guard Clause

번역하면 가드 절? 같은 느낌이다.

if/else 문은 어떤 언어를 배우던 초반에 배우는 기초 문법이다.

if/else를 사용할 때 조건문이 중첩될 필요가 있을 때가 있는데 3중첩을 넘어가기 시작하면 코드가 굉장히
지저분해보이고 유지보수가 어렵다.

다음과 같은 코드가 있다고 가정해보자.

## guard clause 적용 전
```javascript
if(userCount >= 20) {
    if(region === "ko") {
        for(let user in users) {
            return user.gender === "male" ? "남성" : "여성"
        }
    }
}
```

사용자가 20명 이상이고 지역이 한국일 때 라는 조건이 있는 코드이다.
3중첩된 nested scope 들이 마음에 들지 않는다.

## guard clause 적용 후
```javascript
if(userCount < 20 || region !== "ko") return;

for(let user in users) {
    return user.gender === "male" ? "남성" : "여성"
}
```

코드가 더 눈에 명확하게 들어오게 된다.

우리는 용어만 몰랐을 뿐 일상에서 이미 이와 같은 코딩을 하고 있었다.
