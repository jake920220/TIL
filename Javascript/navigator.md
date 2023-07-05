# Navigator

Navigator read-only 인터페이스는 UserAgent에 따른 상태값들을 나타내는 객체이다.

window.navigator로 브라우저에서 접근할 수 있다.

보통 사용할 때는 navigator.userAgent 를 보기 위한 용도로 많이 사용했으나
객체 내에 정보는 gpu, memory, 쿠키유무, 블루투스, 클립보드내용, 앱버전, language, 플랫폼, usb연결여부 등등을 알 수 있다.

이번에 프로젝트에 국제화를 위한 언어팩 설정을 개발하려다가 navigator.language를 사용하여 현재 언어를 가져올 수 있다는 것을 알게 되었다.

navigator.languages 는 배열이고, 사용자가 선호하는 언어들이 담겨있다.

navigator.language는 navigator.languages[0] 을 담고 있다.
