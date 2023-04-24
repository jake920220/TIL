# UX 에 관하여

> 이번 TIL은 [우아한테크 테코톡 워니님의 프론트엔드 개발자에게 UX란](https://youtu.be/0fzA1cRxFiU)을 보며 학습한 내용을 정리했다.

<br>

테코톡에서 디자이너 뿐만 아니라 프론트엔드 개발자에게도 UX는 매우 중요한 요소임을 강조한다.

발표자 분께서는 6개의 법칙을 정리하여 발표해주셨는데 하나하나 보며 내가 오늘 학습한 점을 정리한다.

<br>

## 1. 제이콥의 법칙

<br>

> 사용자가 새로운 경험을 이해하기 위해서 기존 경험을 활용한다.

앱을 예로 들었는데 장바구니나 마이페이지 같은 아이콘은 보편적으로 우측 상단에 존재하며 우리는 새로운 서비스를 이용하더라도 경험적으로 그것을 알고 있는 것을 말한다.

이는 결국 어느 정도 보편적인 UI를 채용하여야 사용자에게 불편한 경험을 주지 않을 수 있음을 말한다.


<br>

## 2. 피츠의 법칙

<br>

> 터치 대상의 크기는 정확하게 선택할 수 있는 영역보다 여유 있어야 한다. 터치 영역끼리의 간격도 중요하다.

이전부터 모바일의 개발을 할때 항상 버튼에 적절한 패딩값을 주어 모바일에서의 click 영역을 넓게 잡고, hover 나 focus에 대한 시각적 효과도 확실하게 구현하게끔 배워왔던 나로서는 당연한 얘기여서 공감이 됐다.

<br>

## 3. 힉의 법칙

<br>

> 의사결정에 걸리는 시간은 선택지의 개수와 복잡성에 비례해서 늘어난다.

발표자는 노인들을 위한 리모컨이라며 채널과 볼륨, 숫자를 제외한 모든 부분을 테이프로 칭칭감은 리모콘 짤방을 프레젠테이션에 담아서 예시를 들었다.

선택지가 많고 무엇을 해야할 지 모른다면 당연히 의사결정에 시간이 오래걸리며, 최악의 경우 해당 페이지로의 방문을 더 이상 하지 않을 수도 있다.

나는 동네에서 간혹 나이 많으신 분들이 키오스크를 사용하지 못해 쩔쩔메는 모습을 보며 미래에 우리도 기초적인 생활에
불편함이 생기지 않을까 하는 걱정을 하곤 했다.

키오스크 등은 추가주문을 유도하고 매출을 올리기 위해 중간 중간에 추가메뉴를 제시한다거나, 버튼의 배치도 꼬아놓았는데, UX를 사용자 친화적으로 만들어 그러한 불편을 없애는 것이 중요할 것 같다.

<br>

## 4. 피크엔드 법칙

<br>

> 인간은 경험 전체의 평균이나 합계가 아니라, 절정의 순간과 마지막 순간에 느낀 감정을 바탕으로 경험을 판단한다.

발표자는 서비스를 만들 때에도 해당 순간들에 더 집중해야 함을 강조했다.
그리고 긍정적인 모먼트보다 부정적인 모먼트가 훨씬 기억에 깊이 남는다는 것을 말했다.

해결방법으로는 404 페이지를 귀엽거나 유쾌하게 꾸며서 부정적인 경험을 좀 덜 느끼게 한다는 것을 예시로 들었는데 몇 년 전에 내가 Github를 접속하는데 redirect URL이 무언가 잘못되었는지 계속 404페이지가 떴지만 Github 캐릭터가 귀엽게 애니메이션 되는 효과가 있어서 크게 불쾌하지 않았던게 기억으로 남는다.

또 내가 들었던 생각은 쇼핑몰 페이지를 예로 들면 단순한 배너클릭 시 404보다, 모든 배송지 정보를 다 입력하고 결제정보를 다 입력한 상태에서 결제하기를 눌렀을 때 404가 뜨는 것이 훨씬 불쾌한 경험일 것이라는 생각이 들었다. 그것이 아마 절정의 순간에 느끼는 감정에 주의해야 한다는 포인트로 이해가 됐다.

<br>

## 5. 폰 레스토프 효과

<br>

> 비슷한 사물이 여러개 있으면 그 중 가장 차이가 나는 한가지만 기억한다.

예 아니오의 선택지가 뜨는 Dialog에서 예의 버튼에 포인트 컬러를 입히고 아니오를 회색으로 맞춘다던지, 서비스의 유료 플랜에 대해 설명하는 표에서 그 기업이 가장 추천하는 요금제 플랜에 색상을 입혀놓아서 고객이 자연스럽게 해당 플랜으로 결제를 할 수 있도록 유도한다던지 하는 내용이 담겨 있었다.


<br>

## 6. 도허티 임계

<br>

> 시스템의 반응 속도는 전체 사용자 경험을 좌우하는 중요한 요소

도허티 임계에서는 0.4초를 규정했는데, 이것보다 더 시간이 걸릴 경우는 사용자에게 시각적으로 프로세싱에 대한 피드백을 줄 수 있어야 함을 강조했다. (ex> 로딩, 스켈레톤 등)


<br>

## 느낀 점

결국 프론트엔드 개발자가 UX에 대해 신경쓰는 것은 어느정도 퍼포먼스 적인 부분에서 오는 게 크다는 것을 느꼈다.
색상이라던지 위치에 대한 배치는 보통 디자이너가 지정을 하기 때문이다.

다만 프론트엔드 개발자도 해당 부분을 함께 신경써주고, 성능 최적화를 통해 사용자 경험에 불편함이 없도록 해야 좋은 UX를
지킬 수 있다고 할 수 있을 것이다.