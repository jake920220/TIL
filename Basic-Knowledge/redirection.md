# http status 300번대 redirection 차이점

300번대 http status는 redirection 에 대한 내용을 포함하고 있다.

평소에 많이 알아둘 필요가 없었는데, vercel domain redirection 설정을 하다가 301, 302, 307, 308을 직접 설정하는 부분이 있어
찾아보게 되었다.

## 301
- 사용자에게 새로은 location으로 redirection을 시키고 싶음
- 새 location과 resource가 동일함
- 새 location이 일시적인 location이 아님.
- http method가 GET으로 요청 변경될 수 있음

## 302
- 사용자에게 새로은 location으로 redirection을 시키고 싶음
- 새 location과 resource가 동일함
- 새 location이 일시적 location임.
- http method가 GET으로 요청 변경될 수 있음


## 307
- 사용자에게 새로은 location으로 redirection을 시키고 싶음
- 새 location과 resource가 동일함
- 새 location이 일시적 location임.
- http method가 이전 요청과 반드시 같아야함. 변경될 수 없음.

## 308
- 사용자에게 새로은 location으로 redirection을 시키고 싶음
- 새 location과 resource가 동일함
- 새 location이 일시적인 location이 아님.
- http method가 이전 요청과 반드시 같아야함. 변경될 수 없음.


이렇게 보면 결국 

그 외

## 304
특수 리다이렉션으로 보통 캐시를 목적으로 사용한다.
리소스가 수정되지 않았음을 알려주고 클라이언트는 로컬에 저장된 캐시를 재사용한다.
따라서 304응답에 바디 등의 페이로드가 포함됟어선 안된다.
