# CSS Normalize와 Reset의 차이

웹 개발을 하면서 프로젝트를 진행할 때마다 reset.css를 적용한 적이 많다.

normalize css는 써본 적이 없는데 이번에 차이를 알게 되어 정리한다.

## Normalize CSS

normalize css는 브라우저들간의 서로 다른 기본 css들을 맞추어주는 역할을 한다.
IE에서는 a태그에 outline이 존재한다던지, 크롬과 파이어폭스의 h1태그는 크기가 다르다던지 하는 서로 다른 default css를
잡아주는 역할을 하며 기본 HTML element tag들의 css속성은 남겨둔다.

## Reset css

reset css는 브라우저가 html element에 기본적으로 적용시키는 default css를 전부 날려버린다.
h1, h2, h3, h4 ... 등등의 태그들은 전부 같은 폰트사이즈를 갖게 되고 기본적으로 element들에 있는 margin 값들은 사라진다.

사실 normalize css를 언제 쓸지는 잘 모르겠지만 작업을 하다보면 디자이너들이 제공해주는 간격, 속성 등을 지정하기 위해
늘 default css 속성은 날려버리는 것이 편해서 매번 reset css를 사용해왔다.
