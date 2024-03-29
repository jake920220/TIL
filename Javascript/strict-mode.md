# 엄격 모드 (Strict Mode)

Javascript가 많은 버전 업데이트를 거쳐오면서 '사양으로는 존재하지만 현재는 안정성 및 효율성 면에서 사용하지 말아야하는 구문' 이 존재한다.

기존의 자바스크립트 개발자들은 이러한 이슈들을 파악해서 문제가 생기지 않게 코딩해야 했는데 이러면 개발자들에게 불필요한 러닝커브가 생기는것과 다름없음.  그리고 개발자들의 수준에 차이가 크므로 한 사람이 이슈를 파악하고 있다고해서 프로젝트를 진행하는 다른 개발자가 문제가 생기는 코드를 넣지 말라는 법이 없음.

<b>Strict mode는 이러한 자바스크립트의 함정을 파악하여 Error로 스크립트의 실행을 막아버리는 역할을  함</b>

<b>Strict mode에 의한 주요 제한 요소</b>는 다음과 같음



- 변수
  - 변수 선언시 var 생략을 금지함
  - 인수/프로퍼티 명 중복 금지 (ES6에서는 가능함)
  - undefined, null에 값 대입 금지
- 명령
  - with 명령문 이용금지
  - arguments.callee 프로퍼티로 액세스 금지
  - eval 명령으로 선언된 변수를 주위 스코프로 확산 금지
- 그외
  - 함수 내부의 this는 글로벌 객체를  참조하지 않는다. (undefined가 됨)
  - '0~' 의 8진수 표기법 금지



Strict Mode를 사용하면 Javascript의 deprecated된 문법과 그로 인해 생길 문제점을 미연에 방지할 수 있을 뿐  아니라 다음과 같은 장점도 얻을 수 있다.

- 비 Strict 모드보다 코드가 빠르게 동작하는 경우가 있음
- 미래의 자바스크립트에서 변경되는 점을 금지함
- 뭘 하지 말아야되는지 에러를 보고 배울 수 있음



사용은 다음과 같다.

```
"use strict";
```

저 명령문 하나로 Strict 모드가 적용되며, 해당 명령문은 스코프단위 선언이기때문에 함수내에서만 선언해줄 수도 있다.





### Strict mode는 IE 10+부터 동작함. 그러나 단순히 문자열 선언이기에 9이하 버전에서 동작은 하지 않더라도 에러는 나지 않음

###  Angular에서는 기본적으로 내장되어 있으며, 사실상 코딩 컨벤션 수준이라 하기에도 미흡한 수준의 실수 혹은 오래전 deprecated되어 잘 사용되지 않는 문법들이기에 최근 개발에서는 잘 사용하지 않는 추세임. Lint나 Prettier 처럼 코딩 컨벤션을 지켜주는 라이브러리를 사용하는게 차라리 낫다!

