# 500번대 http 통신 에러코드

500번대 에러는 서버오류인데 개발자가 예기치 못한 경우의 에러가 대부분인것으로 원래 알고있었는데
공부의 목적으로 정리한다.


## 500 (내부 서버 오류)

서버에 오류가 발생하여 요청이 수행불가일 때 나온다. 대부분의 status code return에서 500을 쉽게 볼 수 있다.

## 501 (구현되지 않음)

서버에 요청을 수행할 수 있는 기능이 없음을 말함. 서버가 요청한 메서드를 인식하지 못한다거나 할때 501을 return 한다.

## 502 (Bad gateway)

한 번 쯤 쉽게 접할 수 있는 에러코드이다. 서버가 게이트웨이 혹은 프록시의 역할을 하고있어서 보통의 요청서버가 아니거나 
업스트림 서버에서 잘못된 요청을 받았을 때 반환한다.

## 503 (서비스를 사용할 수 없음)

서버가 오버로드되었거나 다운된 상태여서 현재 이용이 불가할 때 나타남. 대개 일시적인 에러 상태이다.

## 504 (게이트웨이 시간초과)

502와 비슷하나 업스트림 서버에서 제때 요청을 받지못했을 때의 차이가있다.


그 외 다른 500번대 에러가 많이 있지만 이정도만 알아두어도 무방하다.
