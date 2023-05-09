# Viewport

스마트폰 이전의 브라우저는 데스크탑만을 고려했기 때문에 스마트폰으로 웹페이지를 접속했을 때 가로 세로 스크롤을 해가며
페이지를 봐야만 했다.

디바이스들은 크기가 다양하고 환경도 다 다른데 이를 균일하게 페이지를 볼 수 있게 해주는 것이 viewport 라는 가상의 화면이다.

```html
<meta name="viewport" content="">
```
이런식으로 메타태그의 name을 viewport로 잡고 content안에 내용물을 넣어주면 된다.

content 안에 들어갈 내용들로는

`initial-scale` : 보통 1.0으로 해준다.
`width`: 보통 "device-width"로 잡아 기기별로 동일하게 보이도록 설정한다.
`user-scalable`: 손가락으로 swipe하여 scale을 조절할 수 있는지 없는지 설정하는 값.
`viewport-fit`: 보통 auto가 default이고, iPhone의 노치로 인해 생겨난 항목이다. cover로 설정하면 노치영역까지 포함할 수 있다.
`minimal-ui`: 아이폰 사파리의 주소창이 축소되어서 보여진다.
