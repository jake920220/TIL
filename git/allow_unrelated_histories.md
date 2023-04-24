# --allow-unrelated-histories 옵션

Github에서 원래 repository를 만들 때 readme.md도 생성하지 않고 empty repository를 생성하는데,

LICENSE를 적용시켜 repository를 만들었더니 초기에 비어있는 상태의 프로젝트가 아니였다.

로컬에서 yarn init하여 기본 base프로젝트를 해당 remote repository에 push시키려 하니

```
fatal: refusing to merge unrelated histories
```

이런 느낌의 에러가 나며 pull이 되지 않았다.

검색해서 `--allow-unrelated-histories` 를 pull의 옵션으로 사용하여 해결하였는데

Git에서 github에서 생성한 커밋과 내가로컬에서 생성한 커밋은 공통된 조상을 바라보고 있지 않기 때문에, 서로 다른 project로 인식을 하게 된다.

이걸 해결해주는 명령어가 `--allow-unrelated-histories` 이다.
