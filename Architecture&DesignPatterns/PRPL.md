# PRPL 패턴



## What is PRPL?

PRPL은 구글에서 고안한 아키텍처로 휴대기기 등에서 웹사이트 로드의 성능 향상을 목적으로 만들어졌다.



구글에서는 자바스크립트의 네트워크 전송 비용 감소를 위해 다음의 방법들을 이야기한다.

- 사용자에게 필요한 코드만 전송 (Code Splitting)

- 최소화 (Uglify)
- 압축 (gzip)
- 사용되지 않는 코드 제거
- 네트워크 트립 최소화를 위한 코드 캐싱



그리고 PRPL 은 다음 4가지의 약어이다.

- **Push**
- **Render**
- **Pre-cache**
- **Lazy-load**



각각의 항목들이 어떠한 뜻인지 정리했다.



### Push (preload)

**Push** 는 중요한 리소스들을 미리 로드하라는 것을 말한다. 다른 의미로는 Preload가 되겠다.

CSS의 경우 rel="preload" 를 붙여줌으로서 리소스를 최대한 빨리 요청하게 끔 처리할 수 있다.



### Render

Chrome 의 Lighthouse 로 웹사이트를 검사할 경우 First initial paint 등에 큰 의미를 부여한다.

웹사이트에서 js, css는 render blocking 요소로서 js와 css를 요청한 뒤, 파싱을 하는 과정을 거쳐 화면이 로드가 되기 시작한다.

사용자가 메인페이지에 진입했을 때 메인이 아닌 다른 라우트에서 동작하는 스크립트와 CSS 마저 로드해온다면 이는 불필요한 리소스이고 그 만큼의 시간이 더 들 것이다.

그렇기에 Code splitting 을 통한 chunk loading이 중요하다고 볼 수 있다.



### Pre-cache

클라이언트가 서버에 요청하고 서버에서 해당 리소스를 다시 응답하고 하는 과정들을 Service worker를 둠으로써 Cache storaging 할 수 있다.

자세한 사항은 https://web.dev/service-workers-cache-storage/ 에서 확인이 가능하다.



### Lazy-load

모든 이미지들도 서버에 대한 리소스 요청이다.

사용자가 아직 확인하지 못하는 스크롤 하단 영역의 리소스 등을 처음부터 한꺼번에 요청할 경우 렌더 속도가 더뎌지고 이는 퍼포먼스와도 직결된다.

Lazy-load를 통해 사용자가 확인을 하기 직전에 Asset을 서버로 요청하게끔 하여 로드 속도 개선과 부하를 줄일 수 있다.





## 자료조사

[구글 웹 개발자 문서](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/javascript-startup-optimization?hl=ko)

https://web.dev/apply-instant-loading-with-prpl/

https://web.dev/preload-critical-assets/