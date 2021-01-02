# Trailing slash



주소창에 있는 URL을 복사해서 붙여넣다보면 맨 끝에 / 가 붙는 것을 확인할 수 있다.

이것을 Trailing slash 라고 부른다.



![1609582321666](C:\Users\김준현\AppData\Roaming\Typora\typora-user-images\1609582321666.png)

<center>주소 복사 전</center>

![1609582477210](C:\Users\김준현\AppData\Roaming\Typora\typora-user-images\1609582477210.png)

<center>주소 복사 후</center>



## 그렇다면 이러한 현상은 왜 생기는 걸까?

Trailing slash (이하 트레일링 슬래시)가 있고 없음의 차이는 서버에서 요청 URL에 대한 처리를 어떻게 하느냐에 따라 다르다.

트레일링 슬래시가 있는 경우 서버는 요청 리소스를 디렉토리로 간주한다.

트레일링 슬래시가 없는 경우는 **우선적으로 파일**로 간주한다.



### 트래일링 슬래시가 있는 경우

1. 서버에서는 리소스에 해당하는 디렉토리 명이 있는지를 확인
2. 디렉토리가 있다면 그 안의 디폴트파일을 확인 (디폴트는 index.html)



### 트래일링 슬래시가 없는 경우

1. 서버에서는 리소스에 해당하는 파일명이 있는지를 확인
2. 파일명이 없다면 디렉토리가 있는지를 확인
3. 디렉토리가 있다면 그 안의 디폴트파일을 확인 (디폴트는 index.html)



이도 저도 없다면 404가 뜰 것이다.



## 결론은?

자료조사를 참고한 곳에 따르면 트레일링 슬래시는 개발자라면 붙여주는 것이 원칙에 어긋나지 않는다.

URL을 떼어내 볼때

https://www.naver.com/blog 라고 한다면 https:// 는 프로토콜, www.naver.com 은 Host, /blog 는 path가 된다.

blog가 있다면 저게 path겠지만 blog가 없이 https://www.naver.com 만 놓고 본다면 프로토콜과 Host만 있고 path가 명시되어 있지 않기 때문에 원칙에 어긋난다는 것이다.

https://www.naver.com/ 처럼 트레일링 슬래시가 붙어야 해당 Host의 Root 디렉토리임을 올바르게 명시하는 것이 된다.



당연히 위에 명시한대로 트레일링 슬래시가 있는 경우와 없는 경우의 서버에서의 처리마저 한 스텝 더 추가되므로 트레일링 슬래시를 잘 붙여주는 것이 퍼포먼스 상으로도 더 낫다고 한다.



따라서 개발자라면 트레일링 슬래시를 붙여주는 습관을 쌓도록 하자.





## 자료조사

[Uno's blog](https://djkeh.github.io/articles/Why-do-we-put-slash-at-the-end-of-URL-kor/)

[Ryte Wiki](https://en.ryte.com/wiki/Trailing_Slashes)

