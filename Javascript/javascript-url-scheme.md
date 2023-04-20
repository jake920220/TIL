# Javascript url scheme

React native 프로젝트를 하면서 기존 네이티브 앱들의 소스를 분석하다가 다음과 같은 코드를 발견했다.

```
'javascript:${doSomething()};`;
```

네이티브단에서 웹뷰의 내부를 제어하면서 날리는 코드였는데 자바스크립트가 실행되었다.

용어를 정확히 찾아보지는 못했지만 [이 위키](https://wiki.whatwg.org/wiki/URL_schemes#javascript:_URLs) 에서도 명칭을 그냥
javascript: URLs 라고 부른다. 검색을 해보니 대충 Javascript url, Javascript scheme, Javascript url scheme 등으로 부르고 있는 듯 하다.

꼭 앱단이 아니더라도 브라우저 내에서도 동작한다.
