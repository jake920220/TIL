# DNS와 A레코드, CNAME

기존 블로그 URL을 변경하며 새롭게 알게 된 사실들에 대하여 정리한다.

DNS는 원래 알고있었지만 Domain Name System, 즉 인터넷 상에 존재하는 도메인들은 ip로 구성이 되어있는데, `ooo.com` 등으로 이름으로 사용할 수 있게 해주는 것을 말한다.

정확히는 `ooo.com`같은 형태의 문자열 주소를 IPv4 등의 ip 주소로 변환시켜 주는 시스템을 뜻한다.

A레코드와 CNAME에 대해서인데

`A레코드`는 위의 ip를 직접적으로 문자열 주소에 맵핑하는 형태를 말한다.

`linokim.dev`라는 문자열 주소를 직접적으로 ip에 연결해버리는 경우이다.

`CNAME`의 경우 Canonical Name의 약자로 도메인 주소를 다른 도메인 주소에 맵핑시키는 형태를 말한다.

`blog`라는 CNAME을 설정하면 `blog.linokim.dev`는 `linokim.dev`로 연결시킬 수 있는것이다.

`linokim.dev`가 ip형태의 도메인과 맵핑되어 있는 것과는 다르게 `blog.linokim.dev`가 `linokim.dev`와 맵핑되는, 문자열 주소와 문자열 주소끼리의 맵핑으로 생각하면 쉽다.