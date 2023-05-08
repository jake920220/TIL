# CSS env 함수

아이폰의 노치영역을 대응하기 위해 나온 함수이다.

```css
`env(safe-area-inset-top);`
`env(safe-area-inset-bottom);`
```
등으로 user-agent에 따라 상하단 노치영역에 대한 대응을 해줄 수 있다.

pwa의 경우 데스크탑 애플리케이션일 때 상단의 컨트롤 바 영역까지 화면이 차도록 제어할 수도 있다.

```css
left: env(titlebar-area-x);
top: env(titlebar-area-y);
width: env(titlebar-area-width);
height: env(titlebar-area-height);
```
