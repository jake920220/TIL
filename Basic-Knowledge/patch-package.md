# node_module 커스터마이징한 것 프로젝트에 유지시키는 법

해당 모듈을 fork떠서 수정사항을 적용하고, fork github repo를 dependency에 추가해주는 방법 외에,

```
npm install
```

```json
{
  "scripts": {
    "postinstall": "patch-package"
  }
}
```
추가 해주고

node module에서 원하는 모듈의 파일 들어가서 수정해준 뒤

npx patch-package ${모듈명}

하면 patches 라는 디렉토리 `root`에 생성됨.
patches 내에 .patch 파일이 있으면 다시 node_modules 폴더 지우고 npm install 하더라도 수정사항을 반영해서 설치됨.
