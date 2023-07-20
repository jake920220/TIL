# Aspect Ratio (Padding hack)

Aspect Ratio는 Padding hack이라고도 불리며 width가 가변적일때 height를 width가 변하더라도 늘 비율에 맞게
제공해주고 싶을 때 사용하는 기법이다.

height 대신 padding-top 으로 % 비율에 맞게 설정함으로써 늘 같은 비율을 유지한다.

예를 들어 width 320px 기준 height가 240px이 나오는 박스가 있는데 width가 100%여서 화면 너비가 커지면 계속 커질 수 있는 element가 있다고 하자.

240 / 320은 0.75 이니까 75%의 비율로 padding-top을 주면 width가 늘어나더라도 늘 동일한 비율의 형태를 유지할 수 있다.
